---
fuente: "https://blog.quantinsti.com/cointegrated-pairs-trading-indian-equity-market-epat-project/"
fecha: 2026-07-31
relevancia: alta
tags:
  - research
  - tema/backtesting
  - tema/pairs-trading
---

# Pairs trading con cointegración (proyecto EPAT, mercado indio) — QuantInsti

## 📝 Resumen
Artículo de QuantInsti que documenta un proyecto EPAT de *pairs trading* basado en cointegración sobre 25 acciones large-cap del NSE (India), entre 2015 y mediados de 2025. Sirve como plantilla metodológica completa — selección de pares, señales de entrada/salida, dimensionamiento de posición, backtesting walk-forward y métricas de resultado — aunque el rendimiento ajustado por riesgo obtenido fue modesto.

## 💡 Insights principales

**Metodología de selección de pares**
- Estima el *hedge ratio* entre cada par de acciones mediante regresión OLS.
- Testea la estacionariedad de los residuos (el spread) con el test de Dickey-Fuller aumentado (ADF), a lag 0, para obtener p-valores.
- Controla el problema de comparaciones múltiples (*false discovery*) aplicando el procedimiento de Benjamini-Hochberg (FDR) al 5% de significancia — es decir, no se queda con "el par que salió significativo por azar" al testear muchos pares a la vez.

**Señales de entrada/salida**
- Se opera sobre el z-score del spread entre las dos acciones del par.
- Entrada cuando |z-score| > 1.5; salida cuando el z-score cruza cero.
- Importante: la media y desviación estándar móviles usadas para calcular el z-score se desplazan estrictamente 1 día (*shift*), precisamente para evitar *look-ahead bias*.

**Dimensionamiento y costes**
- Capital fijo asignado por par activo (₹5,00,000 por par).
- Costes de transacción modelados en 5 puntos básicos por pata (*leg*) y lado.
- Las posiciones abiertas al final del periodo de backtest se cierran forzosamente, para que el P&L quede completo.

**Backtesting walk-forward**
- Ventana de entrenamiento de 252 días de negociación (~1 año) y paso de test de 21 días (~1 mes) — es decir, reentrena/reselecciona pares cada mes usando el año anterior, evitando *look-ahead bias*.

## 📊 Resultados obtenidos (a título informativo, no para copiar directamente)
- Universo: 25 large-caps del NSE (banca, IT, farma, cemento, auto), 2015-01-01 a 2025-06-30.
- 3 pares finalmente seleccionados por alta cointegración: HDFCBANK-KOTAKBANK, HEROMOTOCO-ULTRACEMCO, HCLTECH-ICICIBANK.
- 271 operaciones totales, ratio de acierto 63.47%.
- Retorno total 11.04% sobre capital, retorno anualizado 0.30% (muy bajo).
- Sharpe ratio: 0.089 (muy débil).
- Máximo drawdown: -34.31% (muy alto para ese nivel de retorno).

> ⚠️ El resultado numérico en sí es mediocre (Sharpe casi nulo, drawdown severo) — el valor de este artículo está en la **metodología**, no en la estrategia final tal cual. El propio artículo lo reconoce y propone mejoras (ver abajo).

## 🛠 Aplicación práctica
Como plantilla para investigar *pairs trading* dentro de [[sistema-trading-cuantitativo]] (Fase 1, y luego Fase 2/3 al implementarlo en VectorBT):

1. **Selección de pares:** hedge ratio vía OLS + test ADF sobre los residuos + corrección Benjamini-Hochberg (FDR) para evitar falsos positivos al testear muchos pares a la vez. El propio artículo recomienda mejorar esto con un selector de lag basado en criterios de información (AIC/BIC) en vez de ADF a lag 0 fijo.
2. **Universo amplio y diverso:** no limitarse a pocas acciones large-cap; incluir mid-caps y más sectores para tener más candidatos a pares y reducir concentración.
3. **Señales:** z-score del spread con *shift* de 1 día obligatorio (anti-look-ahead); los umbrales de entrada/salida (aquí 1.5 / 0) sirven como punto de partida, pero el artículo recomienda calibrarlos dinámicamente según volatilidad/régimen de mercado en vez de dejarlos fijos.
4. **Dimensionamiento:** sustituir el capital fijo por par por *sizing* ajustado a volatilidad, o un enfoque tipo Kelly.
5. **Gestión de riesgo:** añadir stops a nivel de par (p. ej. cerrar si |z-score| > 3.0) para limitar el drawdown cuando la relación de cointegración se rompe (*regime break*) — esto probablemente explica el -34% de drawdown del artículo: sin ese stop, un par que deja de cointegrar puede divergir sin límite.
6. **Sesgo de supervivencia:** usar listas de componentes del índice válidas en cada momento histórico (*point-in-time*), no una lista fija actual aplicada retroactivamente.
7. **Backtesting:** walk-forward con ventana de entrenamiento (aquí 252 días) y paso de test (aquí 21 días) — reentrenar/reseleccionar pares periódicamente en vez de fijar los pares una sola vez al principio.

Esto encaja directamente con el **walk-forward test** que ya tienes en la lista de pruebas de validación de [[sistema-trading-cuantitativo]] — este artículo es un ejemplo concreto de walk-forward aplicado a selección de pares, no solo a los parámetros de una única estrategia.

## 🔗 Relacionado
- [[sistema-trading-cuantitativo]]
- [[blog-quantinsti]]
- [[retrospective-simulation-trading]]
