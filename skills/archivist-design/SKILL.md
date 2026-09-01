---
name: archivist-design
description: Write what satisfies the requirements into docs/archivist/L2_designs/ as materials and rules. Use when settling what is needed, which files it lives in, and what constrains it.
---

# archivist-design

Read `TEMPLATE.md` in this directory for the form. It is not copied here.

## What to read

The decision, `docs/archivist/L3_*/`, and the spec in question.

## Needs

What each requirement needs. Cite the requirement by anchor.

```
| [R1](../L2_specs/SPEC_NAME.md#R1) | NEEDS_1 |
```

**Not a restatement of the requirement.** R says what must be achieved; needs says
what it takes. If the two read the same, nothing has been added yet.

## Parts

List the files touched, with inputs and outputs. Citing `src/` and `test/` directly
is correct here. This is the **implementation correspondence**, not a reference in
the layer order.

## Rules

Each rule carries the decision it comes from. Do not write a rule the decision does
not yield. Wanting to write one means it is a decision, and decisions are made
elsewhere.

## Reference direction

Design to spec, one way. Never add a citation back into the spec. A cycle leaves no
way to tell which is the original.

## One file per run

## Language

Write the prose in the language the project's existing documents use.
