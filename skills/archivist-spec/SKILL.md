---
name: archivist-spec
description: Write the promises derivable from a decision into docs/archivist/L2_specs/ as requirements and their verification. Use when what is covered and what is not gets settled, or when defining what the implementation must satisfy to be done.
---

# archivist-spec

Read `TEMPLATE.md` in this directory for the form. It is not copied here.

## What to read

The decision, plus `docs/archivist/L3_terms/` and `L3_structures/`.

## Requirements

Keep to **what can be confirmed from outside the spec**. The inside belongs to
design. When writing starts to touch the inside, send it to design.

Each detail lists firing conditions - when it works and when it does not - and
scope: what is covered and what is not. A decision of the form "we will not do X"
lands here.

Number requirements from `R1` and put an anchor directly before each, so upper
layers can cite one requirement.

## Verify

This section is the checklist. One item is one judgement; running them top to
bottom completes the verification. Details carry the procedure and the condition
under which it counts as met.

Its realisation is **debug**: the artefact is actually run in a real environment and
its content judged. E2E and acceptance checks land here; whether a person or a
machine runs it makes no difference.

**Write each item detailed enough that the debug can be written from this spec alone.**
Paths, names exposed to the outside, inputs and expected outputs are vocabulary observable from
outside - write them. Only what presumes the internal make-up goes to design. If
the debug cannot be written, the judgement is not yet stated.

Each item carries `Means:` - a file path for automated debug, or `checklist` when a
person runs it by hand. Browser checks and targets that cannot be automated leave
only the latter. Without the declaration there is no measuring whether the spec
has become fact.

Debug asks whether the spec is met. Something that judges the parts on their own is
a **test**, and test is verified from design. Something that dictates the fine
detail of the implementation is a lint, and lint belongs to design too.

The table above holds which item checks which requirement. **A requirement no item
points at is unverified** - look for an R absent from the REQUIREMENT column.

## Reference direction

**Never cite a design.** The two sit side by side and neither waits for the other.
Whether a design answers this promise is settled in the feature, not here.

## One file per run

## Language

Write the prose in the language the project's existing documents use.
