---
name: archivist-feature
description: Write the feature a decision defines into docs/archivist/L1_features/. Use when the unit a user can name gets settled, or when something is invocable but has no promise written for it.
---

# archivist-feature

Read `TEMPLATE.md` in this directory for the form. It is not copied here.

## What to read

The decision, `docs/archivist/L2_*/`, and the set of entry points a user can invoke.

## The starting point is the decision

**Do not build it as a summary of the specs and designs.** The decomposition into
features does not come out of L2. What comes out of L2 is not the answer to "what
can a user name" - that is a decision about what the product exposes.

Treated as a summary, and because reduction travels upward, by the time L1 is
reached there is no moment left to question the decomposition. It merely ratifies
how the layers below were written.

## The unit

**One invocable command is one feature.** Set the entry points against the features.

| Difference | Meaning |
| --- | --- |
| More commands | Nameable, but no promise written |
| More features | A promise with nothing to invoke |

## Availability

What a user can do, as a bullet list. Do not step into requirements or design -
those belong to L2.

Background carries why it was needed.

## One file per run

## Language

Write the prose in the language the project's existing documents use.
