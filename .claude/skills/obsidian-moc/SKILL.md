---
name: obsidian-moc
description: Crea o actualiza un Map of Content (MOC), una nota índice que organiza y enlaza otras notas de la bóveda de Obsidian por tema o subtema. Úsalo cuando el usuario pida "organiza mis notas sobre X", "crea un índice", "haz un MOC", o cuando una carpeta o tema acumule varias notas sin una nota que las conecte.
---

# Map of Content (MOC)

Un MOC es una nota cuyo contenido es, mayoritariamente, una lista organizada de wikilinks a otras notas relacionadas por tema — es la forma recomendada en Obsidian de crear estructura sin depender solo de carpetas.

## 1. Reúne las notas relevantes

1. Busca en la bóveda (Grep/Glob) todas las notas relacionadas con el tema pedido: por nombre, por contenido, por etiqueta (`#tema`) o por carpeta.
2. Si ya existe un MOC para ese tema, actualízalo: añade las notas nuevas que falten y elimina o corrige enlaces a notas borradas o renombradas. No lo reescribas desde cero si ya tiene estructura útil.

## 2. Organiza, no solo listes

- Agrupa los enlaces bajo encabezados de subtema (`## Subtema`), no como una lista plana si hay más de ~8-10 notas.
- Ordena cada grupo de forma sensata (cronológico, alfabético o por importancia) según lo que ya se use en la bóveda.
- Usa una frase breve junto a cada enlace solo si aporta contexto que el título de la nota no da; evita anotar lo obvio.

## 3. Formato

```markdown
# MOC: <Tema>

## <Subtema A>
- [[Nota 1]]
- [[Nota 2]] — nota breve de contexto si hace falta

## <Subtema B>
- [[Nota 3]]
```

- Sigue las convenciones de wikilinks de la skill `obsidian-markdown`.
- Si la bóveda usa una etiqueta o carpeta específica para MOCs (por ejemplo `#moc` o carpeta `MOCs/`), respétala; si no existe ninguna convención, sugiere una y pregunta antes de generalizarla a toda la bóveda.

## 4. Evita notas huérfanas

- Cuando termines, comprueba que toda nota relevante encontrada en el paso 1 quedó enlazada desde el MOC. Una nota que nadie enlaza es difícil de encontrar de nuevo en Obsidian.
- Si el MOC crece demasiado (decenas de entradas en un mismo subtema), sugiere dividirlo en sub-MOCs enlazados entre sí en vez de seguir añadiendo a una lista larga.
