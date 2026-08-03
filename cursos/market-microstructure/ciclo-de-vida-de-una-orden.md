---
curso: "[[curso-microestructura-coursera]]"
tags:
  - apunte
---

# Ciclo de vida de una orden

## 📝 Resumen
El ciclo de vida de una orden en la negociación de valores implica varias etapas clave que aseguran que se procese desde su inicio hasta su finalización.

**Enrutamiento y ejecución**
- La orden se enruta primero a un centro de negociación (bolsa regulada, ECN, o *dealer* OTC), normalmente a través de un bróker.
- La ejecución ocurre en la plataforma de negociación o por parte del *dealer*, pero existe riesgo de no-ejecución si no hay contrapartes que casen con el precio de la orden.

**Compensación (clearing)**
- Una vez ejecutada, la orden se compensa (*clearing*), a menudo a través de una contraparte central (CCP — *Central Counterparty*) que valida la operación, establece las obligaciones de comprador y vendedor, y puede realizar *netting* (compensación de posiciones).
- El *clearing* es opcional para operaciones OTC e internalización donde la contraparte es un *dealer* o internalizador.

**Liquidación (settlement)**
- La etapa final casa los detalles de comprador y vendedor, transfiriendo los valores al comprador y los fondos al vendedor, normalmente mediante registros electrónicos en bases de datos de bancos custodios.
- La liquidación puede no ser necesaria para operaciones internalizadas, donde los cambios de registro ocurren dentro de la misma institución que gestiona la operación.

## 🔑 Conceptos clave
- **Routing (enrutamiento):** decisión de a qué centro de negociación enviar la orden (bolsa, ECN, *dealer* OTC) — normalmente decidida por el bróker (*smart order routing*).
- **Riesgo de no-ejecución:** una orden límite puede no ejecutarse nunca si el precio de mercado no llega a alcanzar el límite fijado.
- **Clearing (compensación):** proceso post-negociación que valida la operación y gestiona el riesgo de contraparte, típicamente vía una CCP (p. ej. la DTCC en EE.UU.).
- **Netting:** compensación de múltiples obligaciones entre las mismas partes en una única obligación neta, reduciendo el número de transferencias necesarias.
- **Settlement (liquidación):** entrega final, física o electrónica, de los valores a cambio de los fondos. El ciclo estándar en la mayoría de mercados de acciones es T+1 o T+2 (liquidación 1-2 días después de la negociación).
- **Riesgo de contraparte/liquidación:** riesgo de que una de las partes no cumpla su obligación en la ventana entre ejecución y liquidación — la razón de ser de las CCP.

## 💬 Nota complementaria
Esta clase completa el recorrido: antes vimos cómo se forma el precio (descubrimiento de precios) y dónde se ejecuta la orden ([[plataformas-y-mecanismos-de-negociacion]]); esta clase añade lo que pasa *después* de la ejecución, que suele quedar invisible para el trader minorista pero es donde se materializa buena parte del riesgo operativo del sistema financiero. De hecho, una de las reformas poscrisis más relevantes para la renta variable en EE.UU. fue acortar el ciclo de *settlement*, primero de T+3 a T+2, y más recientemente a T+1 (2024), precisamente para reducir el riesgo de contraparte durante esa ventana.

Para [[sistema-trading-cuantitativo]]: esto es relevante sobre todo de cara a la Fase 4 (integración con MT5). En CFDs/forex operados vía un *dealer* como Darwinex normalmente no hay *clearing*/*settlement* real de un activo subyacente (es una operación internalizada/bilateral con el bróker): el "riesgo de contraparte" pasa a ser directamente el riesgo de que el propio bróker cumpla, más que un riesgo de mercado gestionado por una CCP. Merece la pena tenerlo en cuenta al evaluar dónde operar en real.

## 🔗 Relacionado
- [[curso-microestructura-coursera]]
- [[plataformas-y-mecanismos-de-negociacion]]
- [[participantes-buy-side-y-sell-side]]
- [[sistema-trading-cuantitativo]]
