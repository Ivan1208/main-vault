---
fuente: "https://medium.com/@Kryptera/chd-volatility-expansion-breakout-strategy-b5dc71093bf4"
fecha: 2026-08-03
relevancia: media
estado: en-curso
tags:
  - research
  - tema/backtesting
  - tema/estrategias
---

# CHD Volatility Expansion Breakout Strategy

## 📝 Resumen
Estrategia que combina **Mass Index** (detecta expansión de rangos de precio/volatilidad) con **Bandas de Bollinger** (define tomas de ganancias en extensiones de precio extremas). Premisa central: convertir la propia volatilidad en señal de entrada, en vez de usarla solo como filtro. Aplicada sobre el símbolo **CHD (Church & Dwight)**, con datos diarios de enero de 2000 a diciembre de 2025.

## ⚠️ Nota sobre acceso
El artículo está parcialmente oculto tras el muro de membresía de Medium. No se pudieron extraer: reglas exactas de entrada/salida, gestión de riesgo (stop loss, take profit, sizing) ni métricas de backtest (retorno, Sharpe, drawdown). El propio autor aclara que los resultados mostrados son históricos y no garantizan rendimiento futuro.

## 🛠 Aplicación práctica
Decidido (2026-08-04): entra en la lista de estrategias a testear de [[sistema-trading-cuantitativo]] (Fase 1 → Fase 3). En marcha:
1. Conseguir acceso completo al artículo (membresía Medium) para extraer las reglas exactas de entrada/salida y gestión de riesgo antes de intentar replicarla.
2. ~~Implementar Mass Index + Bandas de Bollinger como señales en el motor de backtesting (VectorBT)~~ — hecho el 2026-08-05.
3. Pasarla por las pruebas de validación ya definidas del proyecto (walk-forward, Monte Carlo permutation test, etc.) antes de considerarla viable — el propio artículo no aporta métricas de robustez, así que esa validación recae enteramente en el proceso propio.

## 📊 Resultados / Observaciones (2026-08-05)
- Primera implementación en VectorBT lista, pero los retornos salen muy parecidos a los del activo subyacente (buy-and-hold) — señal de que la estrategia no está aportando alpha real todavía.
- Siguientes pasos: añadir un filtro de tendencia a las señales para intentar diferenciar el comportamiento del de comprar y mantener, y luego pasarla por el walk-forward.

## 🔗 Relacionado
- [[sistema-trading-cuantitativo]]
