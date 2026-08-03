---
name: obsidian-daily-note
description: Crea o actualiza la nota diaria (daily note) de esta bóveda de Obsidian, añadiendo entradas nuevas sin sobrescribir lo ya escrito. Úsalo cuando el usuario pida registrar algo en "la nota de hoy", "mi diario", "daily note", o pida un resumen o planificación del día.
---

# Nota diaria (Daily Note)

## 1. Detecta la configuración real antes de asumir nada

El plugin core `daily-notes` está activo en esta bóveda. Su configuración (carpeta, formato de fecha, plantilla) vive en `.obsidian/daily-notes.json` **solo si el usuario la ha personalizado** desde Ajustes → Notas diarias.

- Si `.obsidian/daily-notes.json` existe, léelo y usa sus campos `folder`, `format` y `template` tal cual.
- Si no existe, usa los valores por defecto de Obsidian: archivo `YYYY-MM-DD.md` en la raíz de la bóveda, sin plantilla.
- El formato de fecha sigue la sintaxis de Moment.js (`YYYY-MM-DD`, `YYYY-MM-DD dddd`, etc.); respeta exactamente el formato configurado, no lo cambies.

## 2. Crear vs. actualizar

1. Calcula el nombre esperado de la nota de hoy con el formato detectado.
2. Comprueba si el archivo ya existe.
   - **Si existe:** añade la entrada nueva al final, o bajo el encabezado correspondiente si la nota ya tiene secciones (`## Tareas`, `## Notas`, `## Registro`, etc.). Nunca sobrescribas contenido existente.
   - **Si no existe:** créalo. Si hay una plantilla configurada, aplica su estructura; si no, usa una estructura mínima razonable (título con la fecha, y una sección para lo que pida el usuario).
3. Si el usuario pide "la nota de ayer" o una fecha concreta, calcula el nombre de archivo para esa fecha con el mismo formato, sin asumir que existe.

## 3. Enlaza, no dupliques

- Si la entrada menciona un proyecto, persona o tema con nota propia en la bóveda, enlázalo con `[[wikilink]]` (ver skill `obsidian-markdown`) en vez de repetir información.
- Si el usuario pide "resumen del día" o "planificación", busca primero la nota diaria anterior para dar continuidad (tareas pendientes, temas abiertos) en vez de partir de cero.

## 4. Formato de cada entrada

- Antepone la hora si el usuario no la da explícitamente pero el contexto lo pide (útil para bitácoras de trabajo): `- HH:MM entrada`.
- Sigue las convenciones de `obsidian-markdown` para wikilinks, callouts y etiquetas dentro de la entrada.
