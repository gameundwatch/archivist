---
name: archivist-promote
description: Strip the `_` from documents whose implementation has arrived and rewrite every incoming link. Use on the report from archivist-check.
---

# archivist-promote

## Input

The report from `archivist-check`. **Do not judge arrival on your own.** Anything
absent from the report stays as it is.

Invoked without a report, change nothing and finish.

Only feature, spec and design can carry a mark. A mark on a structure, a term or a
decision is not stripped - `archivist-check` raises it as an error.

## What it does

1. Strip the leading `_` from the target file
2. Rewrite every link pointing at that file

There is no index. Find incoming links by scanning.

```
grep -rl '_TARGET_NAME\.md' docs/archivist/
```

Where the file is cited with an anchor, as in `../L2_specs/_SPEC_NAME.md#R1`,
rewrite the path alone. The anchor is unchanged.

## When done

Run `archivist-check` again and confirm not one link is broken. A missed incoming
link surfaces nowhere else.
