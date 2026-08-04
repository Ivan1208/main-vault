---
estado: activo
fecha_inicio: 2026-07-27
fecha_objetivo: 
tags:
  - proyecto
  - estado/activo
  - tema/finanzas-cuantitativas
---

# Sistema de Trading Cuantitativo (Research → Backtesting → MT5 → Darwinex Zero)

## 📝 Descripción
Proyecto personal, en paralelo a mis estudios de Ciencia de Datos Aplicada en la UCM, para construir un flujo completo de trading cuantitativo: desde la investigación de estrategias hasta operarlas en real con capital de terceros a través de Darwinex Zero.

## 🎯 Objetivos
1. Investigar papers académicos y leer artículos de Medium para captar ideas de estrategias.
2. Desarrollar la estructura de un motor de backtesting con VectorBT, programando cada proceso por separado (datos, señales, ejecución, métricas, etc.) y organizando una estructura de proyecto ordenada para todos ellos.
3. Una vez terminado el motor, empezar a testear estrategias dentro de él.
4. Integrar Python con MT5 para poder operar en la plataforma los sistemas ya validados.
5. Poner a operar en real, en una cuenta de Darwinex Zero, todos los sistemas que superen el backtesting.

## 📌 Decisiones clave
- 2026-07-27: VectorBT elegido como motor base de backtesting.
- 2026-07-27: MT5 elegido como plataforma de ejecución y Darwinex Zero como cuenta para llevar a real los sistemas validados.
- 2026-07-28: Definidas las pruebas de validación que debe superar cada estrategia antes de pasar a real (lista abierta, ver sección "🧪 Pruebas de validación").
- 2026-07-29: Se usará Claude Code para desarrollar el entorno de testeo de estrategias (las pruebas de validación) y el generador de informes que recoge sus resultados.
- 2026-08-03: Se abandona el proyecto paralelo [[generacion-videos-agentes-inmobiliarios-airbnb]] (idea de negocio no convincente tras investigar) para mantener el foco en finanzas cuantitativas.

## ✅ Próximos pasos

### Fase 1 — Investigación de estrategias
- [ ] Buscar papers académicos sobre estrategias cuantitativas (arXiv q-fin, SSRN, Google Scholar)
- [ ] Leer y resumir cada paper encontrado (una nota en research/ por paper)
- [ ] Leer artículos de Medium sobre backtesting y estrategias
- [ ] Leer artículos del blog de QuantInsti (https://blog.quantinsti.com/)
- [ ] Mantener un listado de ideas de estrategias candidatas a testear

### Fase 2 — Motor de backtesting (VectorBT)
- [ ] Definir la estructura de carpetas del proyecto Python (src/, tests/, notebooks/, data/)
- [ ] Configurar el entorno (dependencias, instalación de VectorBT)
- [ ] Programar el módulo de datos (carga/descarga de históricos, ajuste por dividendos/splits)
- [ ] Programar el módulo de señales (lógica de entrada/salida por estrategia)
- [ ] Programar el módulo de ejecución (simulación de órdenes, comisiones, slippage)
- [ ] Programar el módulo de métricas (Sharpe, drawdown, etc.)
- [ ] Programar el módulo de reporting/visualización de resultados

### Fase 3 — Testeo de estrategias
- [ ] Implementar una primera estrategia de prueba en el motor
- [ ] Validar el motor contra un caso conocido/benchmark
- [ ] Testear cada estrategia candidata de la Fase 1 pasándola por las pruebas de validación (ver abajo)
- [ ] Documentar los resultados de cada estrategia testeada

## 🧪 Pruebas de validación (por estrategia)
Lista abierta — se irán añadiendo más pruebas a medida que surjan. Todas se implementan con VectorBT.

- [x] Walk-forward test — implementado
- [ ] In-sample Monte Carlo permutation test — implementado, pendiente de refinar (ver [[retrospective-simulation-trading]] para el framework de refinamiento: bootstrap no paramétrico, anclaje a precios reales, optimización por consenso multi-camino, métricas VaR/CVaR/skew/kurtosis)
- [ ] System param permutation test
- [ ] Benchmark comparison
- [ ] Slippage and commission variation test
- [ ] Skill vs. trend test

**Entorno de testeo + informes:** se va a desarrollar con Claude Code un entorno que ejecute estas pruebas de validación sobre cada estrategia y genere un informe con los resultados.
- [ ] Diseñar con Claude Code el entorno de testeo que ejecute todas las pruebas de validación de esta lista sobre una estrategia dada
- [ ] Diseñar con Claude Code el generador de informes (recoge los resultados de cada prueba por estrategia)
- [ ] Explorar [[claude-code-para-informes-de-backtesting]]: usar Claude Code para almacenar y organizar los gráficos/informes de cada backtest

### Fase 4 — Integración Python + MT5
- [ ] Investigar la librería/API de conexión Python-MT5 (paquete `MetaTrader5`)
- [ ] Probar una conexión básica (leer datos, enviar una orden de prueba en cuenta demo)
- [ ] Adaptar las señales del motor para generar órdenes reales en MT5

### Fase 5 — Operativa real (Darwinex Zero)
- [ ] Abrir/configurar la cuenta en Darwinex Zero
- [ ] Desplegar en real los sistemas validados conectando MT5 a Darwinex Zero
- [ ] Monitorizar y llevar registro de la operativa en real

## 🔗 Relacionado
- [[curso-finanzas-yale]]
- [[curso-microestructura-coursera]]
- [[topics-in-mathematics-finance-mit]]
- [[redes-sociales-divulgacion-trading-cuantitativo]]
- [[retrospective-simulation-trading]]
- [[pairs-trading-cointegracion-nse-epat]]
- [[claude-code-para-informes-de-backtesting]]
- [[chd-volatility-expansion-breakout-strategy]]
- [[sistema-trading-parametros-adaptativos-walk-forward]]
