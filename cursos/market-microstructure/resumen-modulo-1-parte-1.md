---
curso: "[[curso-microestructura-coursera]]"
tags:
  - apunte
---

# Resumen — Módulo 1, Parte 1: mercados perfectos vs. reales, liquidez y descubrimiento de precios

## 📝 Resumen
Resumen oficial de la primera parte del Módulo 1, que conecta y cierra los conceptos ya vistos en los apuntes anteriores: [[precios-mercados-perfectos-vs-reales]], [[liquidez-de-mercado-y-bid-ask-spread]], [[descubrimiento-de-precios]], [[importancia-de-la-liquidez-de-mercado]], [[conceptos-centrales-microestructura-y-puzzles-empiricos]] y [[microestructura-diseno-de-mercado-y-regulacion]]. Esta nota funciona como mapa/índice de esa parte del módulo, con las citas académicas exactas que la clase confirma.

### Mercados perfectos vs. reales
En un mercado perfecto, el precio refleja la "visión de consenso" de todos los inversores sobre los fundamentales (flujos de caja futuros, etc.), bajo estos supuestos:
- Todos los compradores y vendedores potenciales están presentes en el mercado y actúan como tomadores de precio (*price takers*).
- Todos negocian a un único precio de equilibrio (*market-clearing price*).
- No hay "fricciones": ni comisiones de bróker ni impuestos sobre transacciones, ni bid-ask spread, ni coste de obtener información.
- El flujo de órdenes en sí mismo no afecta a los precios.

En el mundo real, no todos participan todo el tiempo: en cada momento los precios los determinan unos pocos participantes que absorben las órdenes (los *market makers*). Las fricciones son la norma, y el flujo de órdenes sí afecta a los precios de transacción, que pueden desviarse del "precio de consenso" de un mercado perfecto:
- **Cuánto se desvían ⇒ iliquidez.**
- **Con qué rapidez convergen ⇒ velocidad del descubrimiento de precios.**

### Liquidez
Grado en que los precios de transacción se desvían del valor de consenso del activo. Las órdenes de compra suben el precio, las de venta lo bajan: ask > bid ⇒ bid-ask spread = iliquidez. El spread difiere mucho según la capitalización de mercado, como muestra el ejemplo de la clase:

| Acción | Amazon | Boeing | Campbell Soup | Borr Drilling |
|---|---|---|---|---|
| Capitalización de mercado (bn $) | 1566.88 | 117.65 | 13.78 | 0.23 |
| Mejor precio bid | 3124.00 | 207.71 | 45.48 | 0.99 |
| Mejor precio ask | 3124.75 | 207.79 | 45.36 | 1.03 |
| Spread en $ | 0.75 | 0.08 | 0.38 | 0.04 |
| Spread en % | 0.02% | 0.04% | 0.83% | 3.96% |

> Nota: en la fila de Campbell Soup el ask (45.36) aparece por debajo del bid (45.48), lo cual es inconsistente (el ask siempre debe ser ≥ bid). Puede ser una errata de la imagen original o un error de lectura por mi parte al transcribirla — si te importa la precisión de este dato concreto, conviene verificarlo contra la diapositiva original del curso.

La relación general sí es clara: a mayor capitalización de mercado, menor spread relativo (Amazon: 0.02% frente a Borr Drilling: 3.96%) — la evidencia numérica de lo ya visto en [[liquidez-de-mercado-y-bid-ask-spread]].

### Descubrimiento de precios
Velocidad y precisión con la que los precios de transacción incorporan la información disponible. Ejemplo de la clase: la explosión del transbordador Challenger (28 de enero de 1986) — en 15 minutos el mercado ya "sabía" cuál de los 4 fabricantes posibles era responsable del accidente (parón de negociación de sus acciones por venta masiva), mientras que los científicos tardaron 15 días en llegar a la misma conclusión. Ver [[descubrimiento-de-precios]].

### ¿Por qué nos debe importar?
- **Liquidez:** en mercados ilíquidos los inversores enfrentan mayores costes de negociación ⇒ menor rentabilidad de las acciones ⇒ exigen un descuento de liquidez compensatorio ⇒ las empresas afrontan un mayor coste de capital en el mercado primario.
- **Descubrimiento de precios:** un descubrimiento lento genera errores en las decisiones de cartera de los inversores, y hace que el precio de la acción sea poco fiable como referencia tanto para las decisiones reales de inversión de los directivos como para evaluar su desempeño (esquemas de compensación con acciones/opciones).

### Los 3 puzzles empíricos del módulo (con cita exacta)
1. **Iliquidez y la crisis subprime:** durante la crisis, los bid-ask spreads de las acciones (especialmente financieras) subieron con fuerza; varios mercados de renta fija llegaron a "congelarse" por completo. El gráfico de la clase muestra el spread medio en % disparándose tras el colapso de Lehman Brothers (línea vertical) y bajando después. *Fuente: A. Beber y M. Pagano, "Short-Selling Bans around the World: Evidence from the 2007-09 Crisis," Journal of Finance, 2012.*
2. **Tendencia secular en los costes de transacción:** los bid-ask spreads han bajado desde los años 30, sobre todo desde finales de los 80; las comisiones también bajaron desde mediados de los 70 (de 0.9% a 0.1%). *Fuente: C. Jones, "A Century of Stock Market Liquidity and Trading Costs," Working Paper, 2002.*
3. **Efectos en precio de las operaciones en bloque (block trades) y su reversión:** conocido desde Kraus & Stoll (1972) — una venta en bloque deprime el precio de transacción, pero el efecto se revierte en gran parte al cierre del mercado; simétrico para una compra en bloque. *Fuente: A. Kraus y H. Stoll, "Price Impacts of Block Trading on the New York Stock Exchange," Journal of Finance, 1972.*

Ver también [[conceptos-centrales-microestructura-y-puzzles-empiricos]], que ya recogía estos tres puzzles — ahora con la cita exacta de cada uno.

### Cuestiones de política y regulación (diseño de mercado)
- **Transparencia:** el sistema TRACE en el mercado de bonos corporativos de EE.UU. aumentó la liquidez, especialmente en operaciones pequeñas. *Fuente: Goldstein, M. A., Hotchkiss, E. S., y Sirri, E. R., "Transparency and Liquidity: A Controlled Experiment on Corporate Bonds," The Review of Financial Studies, vol. 20, nº 2, marzo 2007, pp. 235–273.*
- **Subasta periódica vs. negociación continua:** los inversores prefirieron la negociación continua frente a la subasta periódica cuando la Bolsa de Tel Aviv hizo la transición en 1997-98. *Fuente: Kalay, Avner, et al., "Continuous Trading or Call Auctions: Revealed Preferences of Investors at the Tel Aviv Stock Exchange," The Journal of Finance, vol. 57, nº 1, 2002, pp. 523–542.*
- **Prohibiciones de venta en corto:** las introducidas en 2007-08 perjudicaron la liquidez y el descubrimiento de precios, especialmente en mercados bajistas. *Fuente: Beber, A. y Pagano, M., "Short-Selling Bans Around the World: Evidence from the 2007–09 Crisis," The Journal of Finance, vol. 68, nº 1, febrero 2013.*

Ver también [[microestructura-diseno-de-mercado-y-regulacion]] (mismo contenido, ahora con las citas completas confirmadas).

## 🔗 Relacionado
- [[curso-microestructura-coursera]]
- [[precios-mercados-perfectos-vs-reales]]
- [[liquidez-de-mercado-y-bid-ask-spread]]
- [[descubrimiento-de-precios]]
- [[importancia-de-la-liquidez-de-mercado]]
- [[conceptos-centrales-microestructura-y-puzzles-empiricos]]
- [[microestructura-diseno-de-mercado-y-regulacion]]
