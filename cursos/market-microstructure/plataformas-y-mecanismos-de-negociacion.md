---
curso: "[[curso-microestructura-coursera]]"
tags:
  - apunte
---

# Plataformas y mecanismos de negociación

## 📝 Resumen
Este contenido explica los distintos tipos de plataformas y mecanismos de negociación donde se compran y venden valores.

**Plataformas de negociación y participantes de mercado**
- La negociación ocurre cuando las órdenes de compra se cruzan con las órdenes de venta de los participantes del mercado.
- Las plataformas de negociación tradicionales eran bolsas reguladas (*regulated exchanges*), como la Bolsa de Nueva York (NYSE) y Euronext.

**Sistemas alternativos de negociación (ATS — Alternative Trading Systems)**
- Las redes de comunicación electrónica (ECN — *Electronic Communication Networks*) muestran las mejores cotizaciones de compra/venta (*best bid and ask*) y cruzan órdenes automáticamente; ejemplos: Instinet y NYSE Arca.
- Las *crossing networks* cruzan órdenes a precios tomados de otros mercados y no contribuyen al descubrimiento de precios; ejemplos: Liquidnet y Goldman Sachs Sigma X.
- Muchas *crossing networks* operan como *dark pools*, donde los detalles de las órdenes permanecen ocultos para reducir la filtración de información (*information leakage*).

**Otros centros de negociación**
- Los mercados OTC (*over-the-counter*) son descentralizados y operados por *dealers*, a menudo no regulados, y en ellos se negocian valores como bonos y derivados.
- La internalización ocurre cuando los *broker-dealers* cruzan las órdenes de sus clientes entre sí o negocian contra su propio inventario; en la UE, los internalizadores sistemáticos (*systematic internalizers*) deben mostrar cotizaciones para acciones líquidas, mientras que en EE.UU. a los grandes internalizadores a veces se les llama *wholesalers*.

## 🔑 Conceptos clave
- **Bolsa regulada (regulated exchange):** centro de negociación tradicional, sujeto a supervisión regulatoria, con reglas de admisión y transparencia (NYSE, Euronext).
- **ECN:** ATS totalmente electrónico que publica sus mejores cotizaciones de compra/venta y cruza órdenes automáticamente — funciona de forma muy parecida a una bolsa, pero con menos carga regulatoria.
- **Crossing network / dark pool:** centro de negociación donde las órdenes se cruzan sin publicar cotizaciones propias; suele usar como referencia el precio medio (*midpoint*) del NBBO (mejor bid/ask nacional) vigente en los mercados "lit" (transparentes). Al no publicar sus propias cotizaciones, no contribuyen al descubrimiento de precios: lo "importan" de otros mercados.
- **OTC (over-the-counter):** negociación bilateral entre un cliente y un *dealer*, sin un libro de órdenes centralizado; típico de bonos, derivados y activos poco estandarizados.
- **Internalización / systematic internalizer / wholesaler:** el propio intermediario actúa como contraparte de sus clientes en vez de enviar la orden a un mercado externo. En EE.UU., firmas como Citadel Securities o Virtu Financial actúan como *wholesalers*, ejecutando gran parte del flujo minorista (*retail order flow*) internamente.

## 💬 Nota complementaria
Esta clase conecta directamente con [[descubrimiento-de-precios]]: el hecho de que las *dark pools* y *crossing networks* "no contribuyan al descubrimiento de precios" es clave — se limitan a copiar el precio ya descubierto en los mercados transparentes (normalmente el punto medio del NBBO), en vez de generar información nueva sobre el valor del activo. Esto genera un debate regulatorio real: si demasiado volumen migra a venues oscuros, el proceso de descubrimiento de precios en los mercados "lit" (que todos los demás usan como referencia) podría degradarse por falta de volumen — un tema que probablemente se trate más adelante en el curso junto con el trading de alta frecuencia.

Para [[sistema-trading-cuantitativo]]: esto importa sobre todo para modelar la ejecución de forma realista. En el mercado de acciones, el volumen negociado fuera de las bolsas tradicionales (dark pools + internalización) representa una fracción muy significativa del total (del orden de un 40-45% del volumen en EE.UU. según los años) — el precio "de pantalla" de una bolsa no siempre representa dónde se ejecutaría realmente una orden. En tu caso, al operar vía MT5/Darwinex Zero probablemente sea ejecución OTC/vía dealer en la práctica, así que conviene no dar por hecho que el fill que simules en backtesting con datos de una única fuente se parece al fill real.

## 🔗 Relacionado
- [[curso-microestructura-coursera]]
- [[descubrimiento-de-precios]]
- [[liquidez-de-mercado-y-bid-ask-spread]]
- [[sistema-trading-cuantitativo]]
