---
curso: "[[curso-microestructura-coursera]]"
tags:
  - apunte
---

# La importancia de la liquidez de mercado

## 📝 Resumen
Este contenido explica por qué la liquidez de mercado importa y cómo afecta a los inversores, a los precios de los activos y a las decisiones económicas.

**Importancia de la liquidez de mercado**
- La liquidez afecta a la rentabilidad de la inversión: los activos ilíquidos son costosos de negociar, lo que reduce la rentabilidad neta.
- Las variaciones en la liquidez añaden riesgo: los inversores deben ser compensados tanto por los costes de negociación como por el riesgo de liquidez (el riesgo de que la liquidez empeore justo cuando necesitas negociar).

**Efectos sobre los precios y la inversión**
- La iliquidez reduce el precio de los activos, ya que el mercado incorpora de antemano los costes y riesgos de negociación esperados — esto es lo que conecta la microestructura de mercado con la valoración de activos (*asset pricing*).
- La reducción de liquidez durante las crisis puede provocar caídas bruscas de precios y una menor inversión por parte de las empresas, amplificando los cambios en los fundamentales.

**El papel de los reguladores y la eficiencia del mercado**
- A los reguladores/*policymakers* les preocupa la liquidez porque influye en la estabilidad del mercado y en la actividad económica.
- La velocidad del descubrimiento de precios importa, porque refleja cuánta información incorporan los precios, lo cual ayuda tanto a tomar decisiones de inversión como a evaluar el rendimiento (*performance evaluation*).

## 🔑 Conceptos clave
- **Riesgo de liquidez:** riesgo de que la liquidez de un activo empeore justo en el momento en que necesitas negociarlo, distinto del riesgo de precio "normal".
- **Prima de liquidez:** compensación adicional exigida por los inversores para mantener activos menos líquidos, que reduce su precio de equilibrio (los activos más ilíquidos cotizan "más baratos" precisamente por serlo).
- **Vínculo microestructura ↔ asset pricing:** los costes/riesgos de negociación de un activo no son solo "fricción" técnica, terminan incorporados en su precio de equilibrio.
- **Amplificación en crisis:** menor liquidez → precios caen más de lo que justifican los fundamentales → las empresas invierten menos → el shock inicial se amplifica (canal de transmisión hacia la economía real).

## 💬 Nota complementaria
Esta clase cierra el círculo con los dos apuntes anteriores: primero viste el mecanismo (bid-ask spread, [[liquidez-de-mercado-y-bid-ask-spread]]) y el proceso ([[descubrimiento-de-precios]]); ahora ves por qué importa a nivel macro. La idea de que la liquidez tiene un precio (los activos ilíquidos ofrecen mayor rentabilidad esperada como compensación) es la base del concepto de *liquidity premium* en asset pricing, formalizado por primera vez en el paper clásico de Amihud y Mendelson (1986), *"Asset pricing and the bid-ask spread"*.

Es también un puente directo hacia [[sistema-trading-cuantitativo]]: cualquier estrategia que backtestees debe tener en cuenta que el coste de liquidez (spread, impacto de mercado) no es constante — se dispara justo en los momentos de estrés donde más falta hace poder salir de una posición. Es exactamente lo que tu prueba de "slippage and commission variation" en el motor de backtesting está pensada para capturar.

## 🔗 Relacionado
- [[curso-microestructura-coursera]]
- [[liquidez-de-mercado-y-bid-ask-spread]]
- [[descubrimiento-de-precios]]
- [[sistema-trading-cuantitativo]]
