---
curso: "[[curso-microestructura-coursera]]"
tags:
  - apunte
---

# Participantes del mercado: buy side y sell side

## 📝 Resumen
Este contenido explica quiénes participan en la negociación de valores y qué papel desempeña cada uno.

**Participantes del mercado de valores**
- Los participantes se dividen en dos grupos: el *buy side* y el *sell side*.
- El *buy side* incluye a quienes **compran servicios de negociación**: traders minoristas (*retail*), instituciones, fondos de inversión, fondos de pensiones, empresas y gobiernos.

**Roles en el sell side**
- El *sell side* está formado por quienes **venden servicios de negociación**: *dealers*, que negocian por cuenta propia, y *brokers*, que negocian en nombre de sus clientes.
- Los *broker-dealers* (o "dual traders") desempeñan ambos roles a la vez, comprando y vendiendo servicios de negociación.

**Distinciones clave**
- Los términos *buy side* y *sell side* se refieren a si el participante compra o vende **servicios de negociación**, no valores en sí mismos (un fondo del buy side vende acciones constantemente, pero sigue siendo "buy side" porque compra el servicio de ejecutar esas operaciones).
- Los *brokers* actúan como intermediarios que canalizan las órdenes del cliente sin asumir riesgo de inventario; los *dealers* son contraparte directa de los inversores y sí asumen riesgo de inventario.
- Algunas firmas, como Goldman Sachs y JP Morgan, operan como *broker-dealers*, ofreciendo ambos servicios.

## 🔑 Conceptos clave
- **Buy side:** compradores de servicios de negociación (no confundir con "compradores de acciones"). Ejemplos: gestoras de fondos (mutual funds), fondos de pensiones, hedge funds, traders minoristas, empresas y gobiernos.
- **Sell side:** vendedores de servicios de negociación. Incluye *dealers* y *brokers*.
- **Dealer:** negocia por cuenta propia, es contraparte del inversor, asume riesgo de inventario y se remunera vía el *bid-ask spread* (ver [[liquidez-de-mercado-y-bid-ask-spread]]) — es, de hecho, el mismo rol que antes llamamos *market maker*.
- **Broker:** actúa como agente, ejecuta órdenes por cuenta del cliente sin tomar posición propia, y se remunera vía comisión — no asume riesgo de inventario.
- **Broker-dealer / dual trader:** firma (o trader) que combina ambos roles, según la operación (ej. Goldman Sachs, JP Morgan).

## 💬 Nota complementaria
Este marco conceptual (buy side / sell side, broker / dealer) es el vocabulario base sobre el que se apoyan casi todas las clases anteriores: el "market maker" que absorbía las órdenes en [[precios-mercados-perfectos-vs-reales]] es, formalmente, un *dealer*; los *broker-dealers* que hacen internalización en [[plataformas-y-mecanismos-de-negociacion]] combinan ambos roles según la orden que reciben.

Aplicado a ti mismo dentro de [[sistema-trading-cuantitativo]]: al operar a través de MT5 sobre una cuenta de Darwinex Zero, tú actúas como **buy side** (compras el servicio de que te ejecuten tus órdenes), y el bróker/dealer detrás de la plataforma actúa como **sell side** — probablemente como *dealer* (contraparte de tus operaciones, especialmente en CFDs/forex) más que como simple *broker* que enruta a un mercado externo. Vale la pena confirmar en qué modelo opera exactamente Darwinex (dealer/market maker vs. STP/ECN que enruta a terceros), porque afecta a cómo se forma tu precio de ejecución y tu slippage real.

## 🔗 Relacionado
- [[curso-microestructura-coursera]]
- [[precios-mercados-perfectos-vs-reales]]
- [[liquidez-de-mercado-y-bid-ask-spread]]
- [[plataformas-y-mecanismos-de-negociacion]]
- [[sistema-trading-cuantitativo]]
