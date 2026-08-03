---
name: obsidian-note-capture
description: Crea una nota nueva y bien formada en la bóveda de Obsidian, buscando primero notas relacionadas para enlazarlas en vez de duplicar contenido, y siguiendo la estructura de carpetas y frontmatter ya existentes. Úsalo cuando el usuario pida "crea una nota sobre X", "apunta esto", "resume esto en una nota", o pegue contenido (texto, artículo, transcripción) para guardar en la bóveda.
---

# Captura de notas nuevas

## 1. Investiga antes de crear

1. Busca en la bóveda (Grep sobre `**/*.md`) notas que ya traten el mismo tema, para:
   - Enlazarlas desde la nota nueva con `[[wikilink]]` en vez de repetir su contenido.
   - Detectar si ya existe una nota con ese título (si existe, pregunta si se debe actualizar en vez de crear un duplicado).
2. Observa 2-3 notas existentes similares para copiar sus convenciones reales: carpeta donde viven, forma del frontmatter, estilo de encabezados. No inventes una convención nueva si la bóveda ya tiene una.
   - Si la bóveda no tiene aún ninguna convención (vacía o casi vacía), usa una estructura mínima razonable y avisa al usuario de la convención elegida por si quiere ajustarla.

## 2. Dónde guardar la nota

- Si existen carpetas temáticas (`Proyectos/`, `Recursos/`, `Personas/`, etc.), coloca la nota en la que corresponda por contenido.
- Si no hay estructura de carpetas todavía, no inventes una jerarquía compleja: pregunta al usuario o guarda en la raíz, y deja que la organización emerja con MOCs (ver skill `obsidian-moc`) en vez de carpetas rígidas.

## 3. Contenido de la nota

- Frontmatter mínimo y consistente con el resto de la bóveda (ver skill `obsidian-markdown`): como mínimo `tags` si la bóveda ya los usa.
- Título de archivo = título canónico de la nota; que sea corto, descriptivo y sin caracteres problemáticos (`/ \ : * ? " < > |`).
- Si la nota captura contenido externo (artículo, transcripción, conversación), resume o extrae lo esencial en vez de pegar todo el texto en bruto, salvo que el usuario pida explícitamente guardarlo completo. Cita la fuente (URL o referencia) en una propiedad `source:` o al final de la nota.
- Cierra la nota enlazando notas relacionadas encontradas en el paso 1 (sección `## Relacionado` si la bóveda no tiene ya otra convención para esto).

## 4. Después de crear

- Si la nota nueva encaja en un Map of Content (MOC) existente, añade el enlace a esa nota nueva desde el MOC correspondiente (ver skill `obsidian-moc`) para que no quede huérfana.
