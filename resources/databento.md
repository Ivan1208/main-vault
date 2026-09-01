---
url: "https://databento.com/portal/browse"
tipo: plataforma-datos
estado: pendiente
tags:
  - recurso
---

# Databento

## 📝 Descripción
Plataforma de datos de mercado vía API, directa desde instalaciones de coubicación (sin intermediarios de terceros).

**Cobertura:**
- Acciones: 15 bolsas + 30 ATS, todas las acciones y ETFs de EEUU.
- Futuros: CME, CBOT, NYMEX, COMEX, ICE, CFE, Eurex, EEX — +650.000 símbolos (futuros, spreads, opciones).
- Opciones: las 18 bolsas de opciones sobre acciones de EEUU.
- Forex: "próximamente" (+100 pares) — **de momento no cubre EUR/USD**, así que no sustituye aún a la fuente de datos ya usada para la estrategia de reversión Z-Score.

**Datos:** histórico hasta 15 años normalizado, tiempo real (streaming), tick-by-tick con profundidad completa del libro de órdenes, OHLCV agregado (segundo/minuto/hora/día). Formatos CSV, JSON, binario (DBN).

**Precio:** pago por uso o tarifa fija por datos ilimitados; $125 de crédito gratis para nuevos usuarios.

## 🛠 Aplicación práctica
Relevante para [[sistema-trading-cuantitativo]] sobre todo de cara a estrategias en **futuros y acciones/opciones de EEUU** (cobertura ya disponible ahora), como la de rotura Donchian + Chandelier Exit si se aplica a futuros. Para forex (EUR/USD) toca esperar a que salga de "próximamente".

## 🔗 Relacionado
- [[sistema-trading-cuantitativo]]
