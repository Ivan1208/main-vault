---
curso: "[[curso-microestructura-coursera]]"
tags:
  - apunte
---

# Conceptos centrales de la microestructura y puzzles empíricos

## 📝 Resumen
Este contenido introduce los conceptos centrales de liquidez y descubrimiento de precios en microestructura de mercados, explicando cómo funcionan los mercados de valores y por qué se producen ciertos comportamientos de mercado.

**Conceptos centrales de la microestructura de mercado**
- La liquidez y el descubrimiento de precios son fundamentales para entender cómo operan los mercados de valores y cómo se determinan los costes de negociación y la profundidad de mercado.
- El curso aporta herramientas analíticas para explicar "puzzles" empíricos del comportamiento de mercado que, de otro modo, podrían parecer confusos.

**Puzzles empíricos sobre la liquidez de mercado**
- Durante las crisis financieras (2008, la Gran Depresión), la liquidez se seca: los *bid-ask spreads* se amplían de forma significativa y los mercados llegan a "congelarse".
- A largo plazo, la liquidez de mercado ha mejorado: los *bid-ask spreads* en el mercado bursátil estadounidense han ido disminuyendo de forma sostenida desde la Segunda Guerra Mundial, junto con la reducción de las comisiones de intermediación (*brokerage*).

**Impacto en precio de las operaciones grandes (block trades)**
- Las operaciones grandes (*block trades*) tienden a mover el precio temporalmente: las compras grandes empujan el precio al alza y las ventas grandes lo empujan a la baja.
- Estos movimientos de precio suelen revertirse parcialmente poco después, lo que refleja presión de precio temporal (*price pressure*) más que un cambio permanente en el valor.

## 🔑 Conceptos clave
- **Profundidad de mercado (market depth):** cantidad que se puede negociar a un precio dado sin moverlo significativamente; junto con el spread, es una de las dimensiones de la liquidez.
- **Congelamiento de mercado (market freeze):** situación extrema de iliquidez en crisis, donde casi no hay contrapartidas dispuestas a negociar a ningún precio razonable.
- **Tendencia secular de liquidez:** mejora estructural a largo plazo (más liquidez, spreads más bajos) frente a los shocks puntuales de iliquidez en crisis — dos fenómenos con causas distintas (uno estructural/tecnológico-regulatorio, otro cíclico).
- **Price pressure (presión de precio) temporal:** movimiento de precio causado por el desequilibrio momentáneo de una orden grande, que se revierte parcialmente cuando esa orden deja de presionar el libro — distinto del impacto permanente que sí refleja información nueva.

## 💬 Nota complementaria
Esta clase funciona como una recapitulación de lo visto en [[liquidez-de-mercado-y-bid-ask-spread]] y [[descubrimiento-de-precios]], y añade una distinción importante: no todo movimiento de precio tras una operación grande es descubrimiento de precios (información nueva permanente); parte es solo *price pressure* — un desequilibrio temporal de oferta/demanda que el mercado corrige poco después. En la práctica, los estudios de microestructura descomponen el impacto de una operación grande en un componente permanente (información) y uno transitorio (liquidez/presión), y esta distinción es clave para cualquier estrategia de ejecución: intentar aprovechar la parte transitoria (reversión) es la lógica detrás de estrategias de *mean reversion* de muy corto plazo basadas en el flujo de órdenes.

Para [[sistema-trading-cuantitativo]]: si en el futuro implementas una estrategia que opera con tamaños grandes en relación al volumen del activo, este es el fenómeno que hace que el precio de ejecución real sea peor que el precio "de pantalla" — justo lo que tu módulo de ejecución del motor de backtesting (comisiones y slippage) debería modelar.

**Fuentes exactas de los 3 puzzles** (confirmadas en [[resumen-modulo-1-parte-1]]):
- Iliquidez en la crisis subprime: A. Beber y M. Pagano, "Short-Selling Bans around the World: Evidence from the 2007-09 Crisis," Journal of Finance, 2012.
- Tendencia secular de los costes de transacción: C. Jones, "A Century of Stock Market Liquidity and Trading Costs," Working Paper, 2002.
- Impacto y reversión de block trades: A. Kraus y H. Stoll, "Price Impacts of Block Trading on the New York Stock Exchange," Journal of Finance, 1972.

## 🔗 Relacionado
- [[curso-microestructura-coursera]]
- [[liquidez-de-mercado-y-bid-ask-spread]]
- [[descubrimiento-de-precios]]
- [[resumen-modulo-1-parte-1]]
- [[sistema-trading-cuantitativo]]
