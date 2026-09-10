---
name: archivist-term
description: Write one word the article fixed the meaning of into docs/archivist/L3_terms/. Use when an article first settles what a word means, or when an existing definition contradicts an article.
---

# archivist-term

Read `TEMPLATE.md` in this directory for the form. It is not copied here.

## What to read

The article only. Do not read layers above.

## Picking the words

Not every noun in the article. The test:

> **Read the word in another sense - does the article now say something else?**

If it does, this article fixes that word's meaning. If it does not, the article
is merely using a word that already means something, and it is not in scope.

## Writing

One word per file. The file name is the word itself. Never gather several words
into one file.

| State | Action |
| --- | --- |
| Absent | Write it. Cite the article under Articles |
| Present, no conflict | Leave it |
| Present, conflicts | Rewrite the definition. Add the article under Articles |

Do not settle the third row by citing alone. When an article changes, the documents
standing on it get rewritten.

## Citing other words

The definition may cite other words by relative path. Cite **only more basic words**.
Vocabulary has a floor. A cycle leaves no way to tell which is the original.

## One file per run

When several words are needed, the caller repeats.

## Language

Write the prose in the language the project's existing documents use. Field names
(`Aliases`, `Details`) stay in English.
