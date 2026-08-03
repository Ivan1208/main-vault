---
curso: "[[curso-microestructura-coursera]]"
tags:
  - apunte
---

# Microestructura, diseño de mercado y regulación

## 📝 Resumen
Este contenido muestra cómo la microestructura de mercado informa el diseño de mercado y la regulación, a través de estudios empíricos sobre reformas en los mecanismos de negociación.

**Efectos de las reformas de transparencia de mercado**
- La introducción del reporte de operaciones (*trade reporting*) en el mercado de bonos corporativos de EE.UU. en 2002 aumentó la transparencia post-negociación.
- Esta reforma mejoró la liquidez, especialmente para operaciones pequeñas, según muestra el estudio de Goldstein, Hotchkiss y Sirri (2007).

**Impacto de los cambios en el mecanismo de negociación**
- La Bolsa de Tel Aviv pasó de subasta periódica (*call auction*) a negociación continua entre 1997 y 1998.
- La investigación de Kalay et al. (2002) encontró que los inversores prefieren la negociación continua: tanto el volumen como los rendimientos aumentaron para las acciones que cambiaron de mecanismo.

**Consecuencias de las prohibiciones de venta en corto (short selling bans)**
- Las prohibiciones de venta en corto durante la crisis financiera de 2007-2009 variaron según el país y la acción.
- Los estudios muestran que estas prohibiciones redujeron la liquidez, particularmente en acciones de pequeña capitalización, y ralentizaron el descubrimiento de precios, especialmente en mercados bajistas.
- El curso abordará más adelante cómo el trading de alta frecuencia (HFT) afecta a la liquidez y a la regulación.

## 🔑 Conceptos clave
- **Transparencia post-negociación (post-trade transparency):** disponibilidad pública de información sobre operaciones ya ejecutadas (precio, volumen); distinta de la transparencia pre-negociación (ver el libro de órdenes antes de negociar).
- **Call auction (subasta periódica):** mecanismo donde las órdenes se acumulan y se cruzan todas juntas en momentos discretos, a un único precio de equilibrio.
- **Negociación continua (continuous trading):** las órdenes se cruzan en tiempo real a medida que llegan, dando lugar a una secuencia de precios de transacción.
- **Short selling ban (prohibición de venta en corto):** restricción regulatoria que impide o limita apostar a la baja sobre un valor; suele imponerse en crisis para intentar frenar caídas de precio.

## 💬 Nota complementaria
Los tres casos de esta clase son "experimentos naturales" muy citados en la literatura de microestructura, porque permiten aislar el efecto causal de un cambio regulatorio/de diseño de mercado sobre la liquidez. Son referencias habituales en cualquier curso de microestructura por esa misma razón: son cambios de regla "de un día para otro" que permiten comparar el antes y el después de forma bastante limpia.

**Fuentes exactas** (confirmadas en [[resumen-modulo-1-parte-1]]):
- Goldstein, M. A., Hotchkiss, E. S., y Sirri, E. R., "Transparency and Liquidity: A Controlled Experiment on Corporate Bonds," The Review of Financial Studies, vol. 20, nº 2, marzo 2007, pp. 235–273.
- Kalay, Avner, et al., "Continuous Trading or Call Auctions: Revealed Preferences of Investors at the Tel Aviv Stock Exchange," The Journal of Finance, vol. 57, nº 1, 2002, pp. 523–542.
- Beber, A. y Pagano, M., "Short-Selling Bans Around the World: Evidence from the 2007–09 Crisis," The Journal of Finance, vol. 68, nº 1, febrero 2013.

El patrón común a los tres casos (transparencia, mecanismo de negociación, prohibiciones de venta en corto) es que **el diseño de mercado no es neutral**: reglas aparentemente "técnicas" tienen efectos medibles, y a veces contraintuitivos, sobre la liquidez y el descubrimiento de precios. El caso de las prohibiciones de venta en corto es el más llamativo: la intención regulatoria (proteger el mercado) produjo el efecto contrario (menos liquidez, descubrimiento de precios más lento).

Esto es relevante para [[sistema-trading-cuantitativo]]: cualquier estrategia que dependa de poder vender en corto debe tener en cuenta que esa posibilidad puede desaparecer justo en los momentos de mayor estrés de mercado — que es precisamente cuando más se necesita poder cubrir posiciones.

## 🔗 Relacionado
- [[curso-microestructura-coursera]]
- [[liquidez-de-mercado-y-bid-ask-spread]]
- [[descubrimiento-de-precios]]
- [[importancia-de-la-liquidez-de-mercado]]
- [[resumen-modulo-1-parte-1]]
- [[sistema-trading-cuantitativo]]
