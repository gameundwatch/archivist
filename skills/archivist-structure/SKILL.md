---
name: archivist-structure
description: Write the form a decision imposes as a diagram in docs/archivist/L3_structures/. Use when a decision settles a count, an order, a state transition or a containment, or when a diagram taking in the whole of the output is needed.
---

# archivist-structure

Read `TEMPLATE.md` in this directory for the form. It is not copied here.

## What to read

The decision, and the words in `docs/archivist/L3_terms/`.

## What becomes a diagram

Constraints the decision imposes that a diagram can carry: counts (exactly one,
one to one), order, state transitions, containment.

Place only **forms that survive the design being thrown away**: types, schemas,
relations between components, and diagrams that take in the whole of what the
project produces. A processing flow belonging to one design stays inside
`docs/archivist/L2_designs/`.

A list written from a set of decisions also belongs here, however many entries it
holds. The test: **is it a decision or the implementation that changes this list?**
A decision means structure; the implementation means design.

## The vocabulary constraint

Words used in a diagram must exist in `L3_terms`. Drawing with a word that has no
entry lets structure reach past terms and coin its own vocabulary.

When a needed word is absent, **stop without writing**. Run `archivist-term` first.

## Diagram granularity

One diagram carries one subject. Several may sit in one file. Put an anchor directly
before each so upper layers can cite it.

Draw so a reader can judge from it: a missing half should show up as a missing row.

## One file per run

## Language

Write the prose in the language the project's existing documents use.
