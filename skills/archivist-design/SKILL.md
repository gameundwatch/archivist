---
name: archivist-design
description: Write what satisfies the requirements into docs/archivist/L2_designs/ as materials and rules. Use when settling what is needed, which files it lives in, and what constrains it.
---

# archivist-design

Read `TEMPLATE.md` in this directory for the form. It is not copied here.

## What to read

The decision and `docs/archivist/L3_*/`. **Not the spec.**

## Parts

List the files touched, with inputs and outputs. Citing `src/` and `test/` directly
is correct here. This is the **implementation correspondence**, not a reference in
the layer order.

Each row carries an anchor, `T1`, `T2`, ..., because the feature cites targets by
anchor. Only `target_file` names a file. `IN` and `OUT` describe what flows through it, and
may hold what the run produces or a name with a placeholder in it; neither column is
ever judged for existence. The mark comes off this design when the `target_file`
column exists — not when anything it outputs has been produced.

## Rules

Each rule carries the decision it comes from. Do not write a rule the decision does
not yield. Wanting to write one means it is a decision, and decisions are made
elsewhere.

## Verify

Each item decides whether a target is built as this design says. Its realisation is
**test**: parts exercised on their own, without running the whole artefact. Means is
a path to test code.

Write each item detailed enough that the test can be written from this design alone.

## Reference direction

**Never cite a spec.** The two sit side by side and neither waits for the other; a
citation either way lets one document's rewrite break the other. Whether this design
answers the promise is settled in the feature, not here.

## One file per run

## Language

Write the prose in the language the project's existing documents use.
