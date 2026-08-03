---
fuente: "https://blog.quantinsti.com/retrospective-simulation-trading/"
fecha: 2026-07-30
relevancia: alta
tags:
  - research
  - tema/backtesting
---

# Retrospective Simulation en trading (QuantInsti)

## 📝 Resumen
Artículo de QuantInsti sobre "retrospective simulation": un método para generar caminos de precio alternativos y plausibles ("que podrían haber pasado") a partir del histórico real, mediante bootstrap no paramétrico (remuestreo con reemplazo de los retornos históricos reales), en vez de optimizar y validar una estrategia sobre el único camino de precios que realmente ocurrió. Idea central: el precio realizado fue solo uno de infinitos caminos posibles, así que validar una estrategia contra ese único camino es estadísticamente frágil.

## 💡 Insights principales
- **Simulación no paramétrica:** en vez de asumir una distribución normal de retornos, se remuestrean los retornos históricos reales (con reemplazo) para generar 1000+ caminos alternativos — preserva colas gruesas y comportamiento empírico real sin asumir una forma paramétrica.
- **Puntos de anclaje (anchor points):** los precios de inicio y fin del periodo se mantienen fijos a los valores reales; los precios intermedios se suavizan geométricamente para garantizar convergencia.
- **Optimización multi-camino:** en vez de optimizar los parámetros de una estrategia sobre un único camino histórico, se testea sobre TODOS los caminos simulados y se identifica qué combinación de parámetros funciona mejor de forma más consistente (consenso estadístico), no la que da el pico de rendimiento en un solo camino.
- **Ejemplo de overfitting mostrado en el artículo:** unos parámetros optimizados in-sample (SEMA=5, LEMA=40) lograron un 873% de retorno... pero solo un 15.5% out-of-sample. La optimización multi-camino busca evitar precisamente este tipo de sobreajuste a un único histórico.
- **Métricas de riesgo calculadas sobre TODOS los caminos simulados:** VaR (95%: -2.21% de pérdida diaria), CVaR/expected shortfall (95%: -3.53%), skewness (-0.116) y kurtosis (9.6, frente al 3.0 de una normal) — hay que verificar que la simulación preserva colas pesadas y no comprime artificialmente la volatilidad.
- **Cuándo la estrategia "falla":** si tras optimizar por consenso sobre múltiples caminos la estrategia sigue sin funcionar out-of-sample, es señal de que no tiene una ventaja predictiva real — no un fallo de la metodología. Esto separa señal genuina de suerte antes de arriesgar capital real.

## 🛠 Aplicación práctica
Checklist para aplicar esto al motor de backtesting de [[sistema-trading-cuantitativo]]:
1. Separar limpiamente los datos in-sample / out-of-sample, documentando fechas de corte y considerando un periodo de "embargo" para minimizar fugas por autocorrelación.
2. Generar 1000+ caminos simulados con bootstrap no paramétrico de los retornos históricos reales (no asumir una distribución).
3. Anclar las simulaciones a los precios de inicio/fin reales.
4. Optimizar los parámetros de cada estrategia contra TODOS los caminos simulados, y quedarse con la combinación más consistente (consenso), no la de mejor pico aislado.
5. Validar en out-of-sample real con los parámetros de consenso, comparando contra buy-and-hold, y calculando Sharpe, máximo drawdown y hit ratio.
6. Calcular VaR/CVaR a varios niveles de confianza (90/95/99%) sobre el conjunto de caminos simulados, y comparar los extremos simulados contra los extremos históricos reales.
7. Verificar que la distribución simulada conserva colas pesadas (kurtosis alta) y no comprime artificialmente la volatilidad — comparar histograma simulado vs. normal.
8. Documentar explícitamente las asunciones y limitaciones: la simulación preserva relaciones estadísticas, no causales, y las condiciones macro simuladas no son las reales.

**Conexión directa con una prueba que ya tienes:** esto es, en esencia, la metodología detrás de tu prueba de validación **"In-sample Monte Carlo permutation test"**, la que ya tienes implementada pero pendiente de refinar (ver [[sistema-trading-cuantitativo]]). Este artículo da un framework concreto para ese refinamiento: bootstrap no paramétrico con reemplazo (en vez de permutación simple), anclaje a precios reales, optimización por consenso entre caminos, y un set de métricas de riesgo (VaR/CVaR/skew/kurtosis) para validar que la simulación es realista.

## 🔗 Relacionado
- [[sistema-trading-cuantitativo]]
- [[blog-quantinsti]]
