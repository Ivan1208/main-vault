---
curso: "[[curso-microestructura-coursera]]"
tags:
  - apunte
---

# Liquidez de mercado y el bid-ask spread

## 📝 Resumen
Esta clase explica el concepto de liquidez de mercado y cómo afecta a los precios de negociación de los activos.

**Definición y dimensiones de la liquidez de mercado**
- Un mercado es líquido si un activo puede negociarse cerca de su valor fundamental y con rapidez.
- La iliquidez tiene dos caras: desviaciones de precio respecto al valor de consenso, y retrasos en la ejecución de las operaciones.

**Formación de precios y el bid-ask spread**
- Las órdenes de compra tienden a subir los precios y las órdenes de venta a bajarlos, lo que da lugar al *bid-ask spread* (diferencial de compra-venta).
- El bid-ask spread es una medida de iliquidez: en todo momento, el precio de venta (*ask*) es superior al precio de compra (*bid*).

**Observaciones empíricas y variaciones de mercado**
- Las operaciones ejecutadas al precio *ask* suelen ser órdenes de compra; las ejecutadas al precio *bid* suelen ser órdenes de venta.
- Las empresas grandes tienen *bid-ask spreads* más estrechos (más liquidez) que las empresas pequeñas.
- Los *bid-ask spreads* varían a lo largo del tiempo y entre plataformas de negociación, y se amplían durante crisis, como en 2008.

## 🔑 Conceptos clave
- **Liquidez de mercado:** capacidad de negociar un activo cerca de su valor fundamental y con rapidez, sin mover mucho el precio.
- **Bid price (precio de compra):** precio más alto al que alguien está dispuesto a comprar en ese momento.
- **Ask price (precio de venta):** precio más bajo al que alguien está dispuesto a vender en ese momento; siempre ≥ bid price.
- **Bid-ask spread:** diferencia entre ask y bid; cuanto mayor es, menos líquido es el mercado (y mayor el coste implícito de negociar).
- **Tamaño de la empresa y liquidez:** relación inversa entre capitalización/volumen negociado y el spread — empresas grandes = más liquidez = spreads más estrechos.

## 💬 Nota complementaria
Este bloque conecta directamente con [[precios-mercados-perfectos-vs-reales]]: el bid-ask spread es, en la práctica, la manifestación concreta de esas "imperfecciones del mundo real" (costes de negociación e información) que separan el precio de consenso del precio de transacción. Es también la variable que probablemente veas modelizada formalmente más adelante — el spread se suele descomponer en tres componentes: costes de procesamiento de órdenes, costes de inventario (el market maker asumiendo riesgo) y costes de selección adversa (asimetría de información, modelo de Glosten-Milgrom). El ensanchamiento de spreads en crisis como 2008 es el ejemplo clásico de un shock de liquidez: sube el riesgo de inventario y la incertidumbre sobre información, así que los market makers se protegen ampliando el spread.

## 🔗 Relacionado
- [[curso-microestructura-coursera]]
- [[precios-mercados-perfectos-vs-reales]]
