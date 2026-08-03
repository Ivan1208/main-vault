---
name: obsidian-vault-health
description: Audita la bóveda de Obsidian en busca de wikilinks rotos, notas huérfanas (sin enlaces entrantes ni salientes), frontmatter inconsistente y etiquetas duplicadas o mal escritas, y reporta o corrige lo encontrado. Úsalo cuando el usuario pida "revisa mi bóveda", "busca enlaces rotos", "limpia mis notas", o antes de una reorganización grande.
---

# Auditoría de salud de la bóveda

No modifiques nada de forma masiva sin mostrar antes un resumen de lo encontrado; esto es una auditoría, no una limpieza automática. Pide confirmación antes de aplicar cambios que afecten a muchos archivos.

## 1. Enlaces rotos

1. Lista todos los wikilinks de la bóveda: `grep -rohE '\[\[[^]|#^]+' --include='*.md' .` (ajusta la expresión para capturar `[[Nombre]]`, `[[Nombre|alias]]`, `[[Nombre#Encabezado]]`).
2. Para cada nombre de nota referenciado, comprueba que existe un archivo `.md` con ese nombre exacto en algún lugar de la bóveda.
3. Reporta los wikilinks que no resuelven a ningún archivo, agrupados por la nota que los contiene.

## 2. Notas huérfanas

- Notas sin ningún enlace entrante (`grep` inverso: ninguna otra nota tiene `[[Nombre de esta nota]]`) ni saliente (no contienen wikilinks).
- Repórtalas como candidatas a enlazar desde un MOC (ver skill `obsidian-moc`) o desde notas relacionadas.

## 3. Frontmatter inconsistente

- Compara las claves de frontmatter usadas en toda la bóveda (`tags`, `aliases`, `created`, etc.).
- Señala variantes que probablemente sean el mismo campo mal escrito (`tag` vs `tags`, `Created` vs `created`) o formatos de fecha inconsistentes.
- Señala notas sin frontmatter si la mayoría de la bóveda sí lo usa.

## 4. Etiquetas

- Lista todas las etiquetas (`#etiqueta` en cuerpo y `tags:` en frontmatter).
- Señala variantes que parecen duplicados por may/minúsculas o singular/plural (`#proyecto` vs `#Proyecto` vs `#proyectos`).

## 5. Reporte

Presenta los hallazgos como una lista accionable, agrupada por tipo de problema, con la ruta del archivo afectado. Solo aplica correcciones (arreglar un enlace, renombrar una etiqueta en todos sus usos, etc.) si el usuario lo pide explícitamente tras ver el reporte.
