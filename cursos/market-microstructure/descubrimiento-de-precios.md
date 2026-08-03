---
curso: "[[curso-microestructura-coursera]]"
tags:
  - apunte
---

# Descubrimiento de precios (Price Discovery)

## 📝 Resumen
El descubrimiento de precios es el proceso por el cual el mercado determina el valor "verdadero" de un activo (p. ej. una acción), recopilando y utilizando rápidamente toda la información dispersa entre compradores y vendedores.

Imagina un grupo de personas intentando ponerse de acuerdo sobre el precio de una carta de béisbol rara: cada persona conoce solo una parte (el estado de conservación, la rareza, la demanda...), pero nadie tiene el cuadro completo. A medida que hablan y negocian, van revelando pistas a través de sus ofertas y demandas, y poco a poco todos convergen hacia un precio justo. Esto es exactamente lo que ocurre en los mercados financieros: los precios se ajustan a medida que los traders reaccionan a la nueva información.

**Ejemplo: el accidente del Challenger (1986)**
- Tras la explosión del transbordador espacial Challenger, el mercado tardó solo 15 minutos en identificar qué empresa proveedora era responsable de la pieza defectuosa — mucho antes de que el informe oficial lo confirmara dos semanas después.
- El precio de las acciones de esa empresa cayó bruscamente, mostrando cómo el mercado "descubrió" la verdad agregando pequeños fragmentos de información dispersos entre muchas operaciones.

**El lado incómodo de un descubrimiento de precios rápido**
- Cuando el descubrimiento de precios es muy rápido, quienes tienen mejor información pueden tener ventaja sobre el resto.
- Esto puede hacer que otros participantes duden o dejen de operar temporalmente para evitar pérdidas (una forma de selección adversa).

## 🔑 Conceptos clave
- **Price discovery (descubrimiento de precios):** proceso de agregación de información dispersa entre los participantes del mercado, que se traduce en el precio observado.
- **Información dispersa/asimétrica:** ningún participante individual tiene toda la información, pero el proceso de negociación (órdenes, precios) la agrega colectivamente.
- **Selección adversa:** riesgo de negociar con alguien que tiene mejor información; ante un descubrimiento de precios muy rápido, los menos informados pueden retirarse temporalmente del mercado para protegerse.

## 💬 Nota complementaria
El caso del Challenger es un ejemplo clásico y muy citado en la literatura de microestructura: el estudio académico de referencia es Maloney y Mulherin (2003), *"The complexity of price discovery in an efficient market: the stock market reaction to the Challenger crash"* (Journal of Financial Economics). Mostraron que el mercado identificó a Morton Thiokol (el proveedor de los O-rings defectuosos) como responsable en cuestión de minutos, penalizando su cotización mucho antes de la confirmación oficial — evidencia de que el precio agrega información dispersa de forma extremadamente eficiente.

Esto conecta con [[liquidez-de-mercado-y-bid-ask-spread]]: la selección adversa que se menciona aquí (informados vs. no informados) es precisamente uno de los tres componentes del bid-ask spread vistos antes (junto a procesamiento de órdenes e inventario). Cuanto más rápido y agresivo es el descubrimiento de precios, mayor es el riesgo de selección adversa que el market maker debe cubrir ensanchando el spread.

## 🔗 Relacionado
- [[curso-microestructura-coursera]]
- [[precios-mercados-perfectos-vs-reales]]
- [[liquidez-de-mercado-y-bid-ask-spread]]
