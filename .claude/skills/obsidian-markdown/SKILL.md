---
name: obsidian-markdown
description: Formatea correctamente notas Markdown al estilo Obsidian (wikilinks, embeds, callouts, propiedades/frontmatter, etiquetas, referencias de bloque). Úsalo siempre que crees o edites un archivo .md dentro de esta bóveda, o cuando el usuario pregunte por sintaxis de Obsidian, enlaces internos, callouts, propiedades o tags.
---

# Obsidian Flavored Markdown

Esta bóveda usa Obsidian, que añade sintaxis propia sobre Markdown estándar. Al crear o editar cualquier nota `.md` de esta bóveda, sigue estas convenciones en vez de Markdown "plano".

## Wikilinks (enlaces internos)

- `[[Nombre de la nota]]` enlaza por el nombre de archivo exacto (sin `.md`).
- `[[Nombre de la nota|texto visible]]` muestra un alias en vez del nombre real.
- `[[Nombre de la nota#Encabezado]]` enlaza a un encabezado concreto.
- `[[Nombre de la nota#^id-bloque]]` enlaza a un bloque marcado con `^id-bloque`.
- Usa wikilinks (no `[texto](archivo.md)`) para todo enlace interno de la bóveda: Obsidian los indexa, autocompleta y los reescribe solo si renombras la nota.

## Embeds (transclusión)

- `![[Nombre de la nota]]` incrusta el contenido completo de otra nota.
- `![[Nombre de la nota#Encabezado]]` incrusta solo una sección.
- `![[imagen.png]]` incrusta una imagen; `![[imagen.png|400]]` fija el ancho en píxeles.

## Callouts

```
> [!note] Título opcional
> Contenido del callout.
```

- Tipos habituales: `note`, `tip`, `info`, `warning`, `danger`, `important`, `success`, `question`, `quote`, `example`.
- Añade `-` tras el tipo para que aparezca plegado por defecto: `> [!note]- Título`.

## Propiedades (frontmatter)

```yaml
---
tags:
  - proyecto/nombre
aliases:
  - Alias alternativo
created: 2026-07-27
---
```

- YAML delimitado por `---` al principio absoluto del archivo (sin líneas en blanco antes).
- Campos habituales: `tags`, `aliases`, `created`, `status`, `cssclasses`.
- Antes de inventar un campo nuevo, revisa notas existentes (`grep -rl "^tags:" .` o similar) para no fragmentar las convenciones ya usadas en la bóveda.

## Etiquetas

- `#etiqueta` en el cuerpo, o listadas en `tags:` del frontmatter.
- Soportan jerarquía: `#proyecto/subproyecto`.
- Solo letras, números, `-`, `_` y `/`; nada de espacios ni acentos si se puede evitar, para que sean clicables de forma fiable.

## Referencias de bloque

- Añade `^id-bloque` al final de un párrafo para poder enlazarlo desde otra nota con `[[Nota#^id-bloque]]`.
- El id debe ser corto y único dentro de la nota (`^resumen`, `^2026-07-27-decision`).

## Buenas prácticas al escribir o editar

1. Antes de crear una nota nueva, busca notas relacionadas en la bóveda (Grep/Glob sobre `**/*.md`) y enlázalas con wikilinks en vez de duplicar contenido.
2. El nombre de archivo ES el identificador del enlace: si renombras una nota, busca y actualiza todas las referencias `[[Nombre viejo]]` en el resto de la bóveda antes de dar el cambio por terminado.
3. Mantén el frontmatter mínimo pero consistente con lo que ya exista en la bóveda; no agregues campos que nadie más usa sin preguntar.
4. No metas HTML ni Markdown "genérico" (enlaces `[]()`, imágenes `![]()`) para contenido interno de la bóveda; usa siempre la sintaxis de wikilink/embed.
