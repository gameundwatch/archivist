---
name: archivist-adopt
description: Read a directory of outside article statements, match them against docs/archivist/L4_articles/, and place the ones a person accepts. Use when a project already holds articles elsewhere, or when L4_articles/ is empty.
---

# archivist-adopt

Bring articles that already exist outside into `docs/archivist/L4_articles/`.
**Do not decide what is adopted.** A person answers, one candidate at a time.

This skill stands outside the Order. It runs before `archivist` starts, and
`archivist` never calls it.

## Input

One directory path, given as the argument. There is no default - **ask for it when
it is missing** and write nothing until it is given.

The only thing assumed of the files there is that each holds one article, stated
once. No tool's output format is a condition.

A file that is not a single article statement is skipped, and named in the report.
Do not guess at it, and do not split it.

## Matching

Read `docs/archivist/L4_articles/` first. For every candidate, say which of the
three it is.

| Result | What is shown |
| --- | --- |
| Same | the existing article that says it, by file name |
| Conflicting | the existing article, and the point the two disagree on |
| New | that nothing there corresponds |

Read the articles only. Layers above rest on them and add nothing to this match.

## Asking

Present one candidate with its match, then wait.

**Nothing is written before an answer.** An answer that never comes leaves
`L4_articles/` as it was. Do not offer to take the rest in one go, however many
are left - narrowing the input is the caller's work.

## Writing

Read `TEMPLATE.md` in this directory for the form. It is not copied here.

Shape what was accepted into that form. **Do not copy the original text across.**
Where the original came from belongs in the report, not in the document.

The file name is the article, in the naming the directory already uses.

| State | Action |
| --- | --- |
| No such name | Write it |
| Name taken | Skip it, and report the collision |

A article a person wrote is never overwritten, and never escaped with a number
on the end.

## What it does not do

Write only inside `L4_articles/`. Not one document in the layers above - that is
`archivist`, and it runs afterwards.

Nothing enters an article that was not in its candidate. On finding a gap the
candidate does not fill, leave it and say so.

## Language

Write the articles in the language the project's existing articles use. Where
none exist, follow the language of the candidates.

## When done

Report, in one place: what was placed, what was skipped as not an article statement,
what collided, and what was declined. Then say that `archivist` is what reduces
the placed articles upward.
