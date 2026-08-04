---
fuente: "https://medium.com/@kridtapon/beyond-backtesting-building-a-robust-trading-system-with-adaptive-parameters-fd8d3c3817c5"
fecha: 2026-08-04
relevancia: alta
estado: pendiente
tags:
  - research
  - tema/backtesting
  - tema/estrategias
---

# Beyond Backtesting: sistema de trading con parámetros adaptativos

## 📝 Resumen
Tesis central: los backtests tradicionales (parámetros fijos, un único pase) son insuficientes para validar robustez. El autor propone usar **optimización walk-forward** para que los parámetros de la estrategia se reajusten periódicamente según ventanas de entrenamiento/prueba secuenciales, en vez de fijarse una sola vez sobre todo el histórico — reduciendo así el riesgo de overfitting frente a un sistema estático.

**Indicadores usados como ejemplo**
- Vortex Indicator (VI)
- Chande Kroll Stop (CKS)

**Activo de prueba:** TPL (mismo activo usado en un artículo anterior del mismo autor).

## ⚠️ Nota sobre acceso
Contenido parcialmente oculto tras el muro de membresía de Medium. No se pudieron extraer las reglas exactas de entrada/salida con VI+CKS, el tamaño/paso de las ventanas walk-forward, ni métricas de backtest (solo se menciona que compara el sistema adaptativo contra buy-and-hold, sin cifras visibles). El autor advierte que los resultados mostrados son solo históricos y no garantizan rendimiento futuro.

## 🛠 Aplicación práctica
Muy relevante justo ahora para [[sistema-trading-cuantitativo]], porque el walk-forward es exactamente lo que se está programando hoy para testear [[chd-volatility-expansion-breakout-strategy]]:
1. Conseguir acceso completo para ver el esquema exacto de ventanas walk-forward (tamaño de entrenamiento, paso de test) que usa el autor, y compararlo con el propio walk-forward test ya implementado en el proyecto.
2. Considerar Vortex Indicator + Chande Kroll Stop como señales/gestión de salida candidatas adicionales a probar en el motor de VectorBT, independientemente de la estrategia CHD.
3. Confirmar el punto central del artículo (reparametrización periódica walk-forward reduce overfitting frente a estrategia estática) contra la propia experiencia al testear CHD — es una hipótesis a contrastar, no un hecho probado por el artículo dado el acceso limitado.

## 🔗 Relacionado
- [[sistema-trading-cuantitativo]]
- [[chd-volatility-expansion-breakout-strategy]]
- [[retrospective-simulation-trading]]
