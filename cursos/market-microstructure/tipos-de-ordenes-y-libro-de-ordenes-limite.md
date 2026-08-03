---
curso: "[[curso-microestructura-coursera]]"
tags:
  - apunte
---

# Tipos de órdenes y el libro de órdenes límite

## 📝 Resumen
Este contenido explica el funcionamiento de los mercados de orden límite: los tipos de órdenes, el libro de órdenes límite (LOB) y cómo las órdenes afectan a la liquidez y los precios.

**Tipos de órdenes**
- Las órdenes de mercado (*market orders*) se ejecutan de inmediato al mejor precio disponible: ofrecen inmediatez, pero a menudo a peor precio, porque pagan el bid-ask spread.
- Las órdenes límite (*limit orders*) especifican un precio límite: pueden conseguir mejor precio, pero cargan con riesgo de ejecución si el precio de mercado nunca llega a ese límite.

**El libro de órdenes límite (LOB) y el mecanismo de mercado**
- Todas las órdenes entran en el libro de órdenes límite (LOB), que las prioriza por precio y luego por tiempo (prioridad precio-tiempo).
- En los mercados por lotes o de subasta (*batch/call markets*), las órdenes se acumulan y se casan en intervalos discretos, buscando el precio de equilibrio donde la demanda iguala a la oferta.
- Las órdenes no negociables al instante (*non-marketable orders*) forman el LOB inicial en la negociación continua, definiendo los calendarios de oferta y demanda y el bid-ask spread.

**Impacto de las órdenes en liquidez y precios**
- Las órdenes grandes tienen un coste mayor: los compradores "suben" (*walk up*) por el calendario de venta y los vendedores "bajan" (*walk down*) por el calendario de compra, ampliando el bid-ask spread efectivo.
- Las órdenes de mercado consumen liquidez: retiran órdenes límite del LOB, ampliando el spread.
- Las órdenes límite, en cambio, generalmente añaden liquidez si no se ejecutan por completo, reponiendo el LOB.

## 🔑 Conceptos clave
- **Market order:** orden que se ejecuta inmediatamente al mejor precio disponible del LOB; prioriza inmediatez sobre precio.
- **Limit order:** orden con un precio límite especificado; prioriza precio sobre inmediatez, con riesgo de no ejecutarse.
- **Limit Order Book (LOB):** registro de todas las órdenes límite pendientes, organizadas por prioridad precio-tiempo.
- **Batch/call market:** mecanismo donde las órdenes se acumulan y se casan en momentos discretos a un precio de equilibrio único, en vez de negociación continua.
- **Walk up / walk down:** efecto por el cual una orden grande "consume" varios niveles de precio del LOB, empeorando el precio medio de ejecución cuanto mayor es el tamaño de la orden.
- **Consumo vs. aporte de liquidez:** las órdenes de mercado consumen liquidez (retiran del LOB); las órdenes límite no ejecutadas la aportan (añaden al LOB).

## 💬 Nota complementaria
Esta clase conecta el "cómo" con el "por qué" de [[liquidez-de-mercado-y-bid-ask-spread]]: ahí se explicaba el bid-ask spread como síntoma de iliquidez; aquí se ve el mecanismo concreto que lo genera y lo ensancha — el LOB y el efecto walk-up/walk-down. También formaliza lo visto de forma más general en [[mercados-de-orden-limite-vs-mercados-de-dealers]]: el LOB es, literalmente, la estructura de datos que define a un "mercado de orden límite" (order-driven market).

Para [[sistema-trading-cuantitativo]]: esto es directamente relevante para el módulo de ejecución del motor de backtesting (VectorBT) — simular órdenes de mercado como si se ejecutasen siempre al precio de cierre/mid, sin modelar el walk-up/walk-down del LOB, sobreestima sistemáticamente el rendimiento de cualquier estrategia que opere con tamaños de orden significativos respecto a la liquidez disponible. Es otro motivo (junto con lo visto en [[ciclo-de-vida-de-una-orden]] y en [[mercados-de-orden-limite-vs-mercados-de-dealers]]) para no asumir que la ejecución simulada se parece a la ejecución real.

## 🔗 Relacionado
- [[curso-microestructura-coursera]]
- [[liquidez-de-mercado-y-bid-ask-spread]]
- [[mercados-de-orden-limite-vs-mercados-de-dealers]]
- [[ciclo-de-vida-de-una-orden]]
- [[sistema-trading-cuantitativo]]
