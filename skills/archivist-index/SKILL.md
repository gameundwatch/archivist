---
name: archivist-index
description: Rebuild docs/archivist/index.csv, one row per document, from the documents alone. Use after documents are added, renamed or rewritten, or whenever the whole reference graph has to be read at once.
---

# archivist-index

## Input

Every `.md` under `docs/archivist/`. Nothing else.

**Do not read the existing `index.csv`.** It is the output, never the input. An
index built from an index carries forward whatever was already wrong in it.

## Output

`docs/archivist/index.csv`, rewritten whole on every run. No diff is applied, and
no row is preserved because it looks unchanged.

Three columns, no header row:

```
path,title,refs
```

- `path` — the file, relative to `docs/archivist/`
- `title` — the text of the first `# ` heading in the file
- `refs` — every file the document links to, joined by `;`, each one relative to
  `docs/archivist/`

Every value is quoted, and a `"` inside one is doubled to `""`. A document that
links to nothing carries an empty `refs`, never no row.

Sort the rows by `path`. The same documents must produce the same file, byte for
byte.

## What it does not do

- **No column that another column yields.** The layer is the directory in `path`,
  and in-degree is the `refs` column counted. Neither is a column
- **No row for `index.csv` itself.** It is not a document
- **No judgement.** Whether a link resolves, a layer is skipped, or a realization
  exists is `archivist-check`'s work. Record the link as written, broken or not

## Standing

The index is generated. Deleting it must lose nothing, so nothing may be written
anywhere that only holds while the index exists. Where a document would have to
read the index to be true, the document is wrong, not the index.
