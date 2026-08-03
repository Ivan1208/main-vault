---
curso: "[[curso-microestructura-coursera]]"
tags:
  - apunte
---

# Mercados de orden límite vs. mercados de dealers

## 📝 Resumen
Este contenido explica los dos mecanismos fundamentales de negociación en los mercados de valores.

**Mercados de orden límite (limit order markets)**
- Son mercados centralizados que permiten a los participantes negociar directamente entre sí, sin intermediarios.
- Las órdenes se enrutan a un "subastador" (*auctioneer*) que equilibra oferta y demanda mediante un proceso de subasta automatizado; ejemplos: las bolsas electrónicas de París, Madrid, Milán y Tokio.

**Mercados de dealers (dealership markets)**
- Son mercados descentralizados que implican intermediarios llamados *dealers*.
- Los *dealers* publican cotizaciones de compra y venta y negocian por cuenta propia; los mercados OTC son un ejemplo claro de mercado de dealers.

## 🔑 Conceptos clave
- **Order-driven market (mercado dirigido por órdenes):** término habitual para lo que aquí se llama "mercado de orden límite" — un libro de órdenes centralizado (*central limit order book*, CLOB) donde las órdenes de compra y venta de los propios inversores se cruzan directamente, con prioridad precio-tiempo, sin que un intermediario tenga que tomar la otra parte.
- **Auctioneer / motor de casación (matching engine):** el mecanismo (hoy, un sistema informático) que ordena las órdenes entrantes y las cruza según sus reglas de prioridad.
- **Quote-driven market (mercado dirigido por cotizaciones):** término habitual para "mercado de dealers" — los inversores no negocian entre sí directamente, sino contra la cotización de un *dealer*, que es siempre la contraparte.
- **Centralizado vs. descentralizado:** en un mercado de orden límite hay un único libro de órdenes visible para todos; en un mercado de dealers, cada *dealer* fija sus propias cotizaciones y no existe necesariamente un único precio de referencia compartido.

## 💬 Nota complementaria
Esta distinción retoma directamente lo visto en [[participantes-buy-side-y-sell-side]]: un mercado de dealers es, literalmente, un mercado donde el *sell side* (los *dealers*) es imprescindible como contraparte de toda operación; un mercado de orden límite permite en cambio que dos participantes del *buy side* negocien entre sí sin que ningún *dealer* tenga que intermediar.

Conviene matizar la dicotomía "limpia" de esta clase introductoria: en la práctica, la mayoría de las bolsas modernas son mercados **híbridos**. Por ejemplo, la NYSE combina un libro de órdenes límite con *designated market makers* que tienen obligación de cotizar y dar liquidez en momentos de desequilibrio; el NASDAQ nació como mercado de dealers puro y ha ido incorporando cada vez más funcionalidad de libro de órdenes. Es probable que el curso profundice en estos modelos híbridos más adelante — esta clase parece sentar la base conceptual antes de entrar en esos matices.

Para [[sistema-trading-cuantitativo]]: al operar CFDs/forex vía un bróker como Darwinex, es casi con toda seguridad un mercado de dealers (quote-driven) más que un libro de órdenes límite compartido — otro motivo, junto con lo visto en [[ciclo-de-vida-de-una-orden]], para no asumir que tu ejecución simulada en backtesting con datos de un CLOB tradicional se parece a tu ejecución real contra la cotización de un único dealer.

## 🔗 Relacionado
- [[curso-microestructura-coursera]]
- [[participantes-buy-side-y-sell-side]]
- [[plataformas-y-mecanismos-de-negociacion]]
- [[ciclo-de-vida-de-una-orden]]
- [[sistema-trading-cuantitativo]]
