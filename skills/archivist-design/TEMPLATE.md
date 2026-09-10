<!--
    LARGE_SNAKE_CASE is a placeholder. Replace every one with content.
    Everything else is written as it stands, field names included.
    A line holding only `...` means repeat as needed; delete the line.
-->

# DESIGN_NAME

## Parts
<!--
    Materials for the implementation.
    List the files this design touches, with their inputs and outputs.
    No: the number a feature cites this target by. T1, T2, ...
    target_name: name of the target
    target_file: file it lives in. The only column judged for existence
    IN: input (optional). Describes the flow, never judged for existence
    OUT: output (optional). Describes the flow, never judged for existence
-->

| No | target_name | target_file | IN | OUT |
| -- | ----------- | ---------------- | -- | --- |
| T1 | TARGET_NAME_1 | src/TARGET_FILE_1 | IN_1 | OUT_1 |
| T2 | TARGET_NAME_2 | src/TARGET_FILE_2 | IN_2 | - |
| T3 | TARGET_NAME_3 | src/TARGET_FILE_3 | - | OUT_3 |
| T4 | TARGET_NAME_4 | src/TARGET_FILE_4 | - | - |
| ... | ... | ... | ... | ... |
...

<!-- Add diagrams that stay inside this design, where they help -->
### Relation
```mermaid

```

## Rules
<!-- Rules and constraints for the implementation. Each traces to a decision -->
- DESIGN_RULES_1
    - DETAIL_1
    - DETAIL_2
- DESIGN_RULES_2
    - DETAIL_1
- DESIGN_RULES_3
...

## Verify

<!--
    Items that decide whether a TARGET is built as this design says.
    Verification here is test: parts are exercised on their own, without
    running the whole artefact. One item is one judgement.
    The table below holds which VERIFY checks which TARGET.
    Details carry the procedure and the condition under which it counts as met.
    Means carries what runs the check: a file path for test code, or `checklist`
    when the target cannot be exercised by code.

    Write each item detailed enough that the test can be written from this
    design alone. Do not cite a spec - the promise is verified by debug,
    which this document never reads.
-->

| No | VERIFY_NAME | TARGET |
| -- | ----------- | ------ |
| 1 | V1 VERIFY_NAME_1 | T1 |
| 2 | V2 VERIFY_NAME_2 | T1, T2 |
| 3 | V3 VERIFY_NAME_3 | T3 |
...

### V1 VERIFY_NAME_1

- Means: test/TEST_FILE
- DETAIL_1

### V2 VERIFY_NAME_2

- Means: test/TEST_FILE
- DETAIL_1

### V3 VERIFY_NAME_3

- Means: test/TEST_FILE
- DETAIL_1
...


## Decisions
<!-- Decisions this document rests on -->
- [DECISION_NAME_1](../L4_decisions/DECISION_NAME_1.md)
- [DECISION_NAME_2](../L4_decisions/DECISION_NAME_2.md)
- [DECISION_NAME_3](../L4_decisions/DECISION_NAME_3.md)
...

## References

### Designs

- [DESIGN_NAME_1](../L2_designs/DESIGN_NAME_1.md)
- [DESIGN_NAME_2](../L2_designs/DESIGN_NAME_2.md)
- [DESIGN_NAME_3](../L2_designs/DESIGN_NAME_3.md)
...

### Structures

- [STRUCTURE_NAME_1](../L3_structures/STRUCTURE_NAME_1.md)
- [STRUCTURE_NAME_2](../L3_structures/STRUCTURE_NAME_2.md)
- [STRUCTURE_NAME_3](../L3_structures/STRUCTURE_NAME_3.md)
...

### Terms

- [TERM_NAME_1](../L3_terms/TERM_NAME_1.md)
- [TERM_NAME_2](../L3_terms/TERM_NAME_2.md)
- [TERM_NAME_3](../L3_terms/TERM_NAME_3.md)
...
