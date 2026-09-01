---
name: archivist
description: Rebuild documents from decisions. Starting from docs/archivist/L4_decisions/, reduce upward through L3 to L1. Use when a decision is added, when a decision changes, or when the document set has drifted from the decisions.
---

# archivist

Take a set of decisions and write up what they demand of the layers above.
**Do not make decisions.**

Documents live under `docs/archivist/` in six directories, one per node.
Directory names are plural. Names the project fills in are LARGE_SNAKE_CASE;
headings are PascalCase.

## Input

Decisions placed in `docs/archivist/L4_decisions/`. Any range - one file,
all of them, any subset. A topic with no document there is out of scope;
making decisions is not this skill's work.

## Order

Write upward. Never skip a layer.

1. `archivist-term` — words the decision fixed the meaning of
2. `archivist-structure` — forms the decision imposes
3. `archivist-spec` — promises derivable from the decision
4. `archivist-design` — what satisfies those requirements
5. `archivist-feature` — the unit a user can name

Skip a step when it has nothing to write. **Not skipping layers and writing one
document per layer are different things.**

## How far it travels

When an existing decision changed, find the documents citing it. There is no index.

```
grep -rl 'DECISION_FILE_NAME' docs/archivist/
```

Rewrite what you find, then find what cites those. Stop when nothing above is reached.

A new decision returns nothing from this search. Judge from its content where it
lands. The more a decision is written in the vocabulary of L1, the more carefully
check L3 first - a decision often fixes the meaning of the very words it uses.

## Stopping

On reaching something the decision does not yield, stop without writing it and say
what is missing. Filling that gap is a decision, and decisions are made elsewhere.

## Language

Write documents in the language the project's existing documents use. Where none
exist, follow the language the decisions are written in. Headings, anchors and
field names stay in English - they are form, not prose.

## When done

Run `archivist-check`.
