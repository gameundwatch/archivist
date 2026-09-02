<!--
    LARGE_SNAKE_CASE is a placeholder. Replace every one with content.
    Everything else is written as it stands, field names included.
    A line holding only `...` means repeat as needed; delete the line.
-->

# DESIGN_NAME

## Needs

<!-- What each cited requirement needs. Not a restatement of the requirement. -->
| spec | needs |
| ---- | ----- |
| [R1](../L2_specs/SPEC_NAME.md#R1) | NEEDS_1 |
| [R2](../L2_specs/SPEC_NAME.md#R2) | NEEDS_2 |
| [R3](../L2_specs/SPEC_NAME.md#R3) | NEEDS_3 |


## Parts
<!--
    Materials for the implementation.
    List the files this design touches, with their inputs and outputs.
    target_name: name of the target
    target_file: file it lives in
    IN: input (optional)
    OUT: output (optional)
-->

| target_name | target_file | IN | OUT |
| ----------- | ---------------- | -- | --- |
| TARGET_NAME_1 | src/TARGET_FILE_1 | IN_1 | OUT_1 |
| TARGET_NAME_2 | src/TARGET_FILE_2 | IN_2 | - |
| TARGET_NAME_3 | src/TARGET_FILE_3 | - | OUT_3 |
| TARGET_NAME_4 | src/TARGET_FILE_4 | - | - |
| ... | ... | ... | ... |
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
