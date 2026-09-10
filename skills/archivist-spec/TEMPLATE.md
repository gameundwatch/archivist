<!--
    LARGE_SNAKE_CASE is a placeholder. Replace every one with content.
    Everything else is written as it stands, field names included.
    A line holding only `...` means repeat as needed; delete the line.
-->

# SPEC_NAME

## Requirements
<!-- 
    What the subject must make work and must achieve.
    Keep to what can be confirmed from outside the spec. The inside belongs to design.
    Each detail lists firing conditions - when it works and when it does not -
    and scope: what is covered and what is not.
-->

### R1 REQUIREMENT_NAME_1

- DETAIL_1
- DETAIL_2

### R2 REQUIREMENT_NAME_2

- DETAIL_1
- DETAIL_2
- DETAIL_3

### R3 REQUIREMENT_NAME_3

- DETAIL_1

### R4 REQUIREMENT_NAME_4

- DETAIL_1
- DETAIL_2

### R5 REQUIREMENT_NAME_5

- DETAIL_1
- DETAIL_2
...

## Verify

<!--
    Items that decide whether a REQUIREMENT is met. This section is the checklist.
    One item is one judgement; running them top to bottom completes the verification.
    The table above holds which VERIFY checks which REQUIREMENT.
    Details carry the procedure and the condition under which it counts as met.
    Means carries what runs the check: a file path for automated debug
    (E2E, acceptance), or `checklist` when a person runs it by hand.

    Verification here is debug: the artefact is actually run and its content
    is judged. Write each item detailed enough that the debug can be written
    from this spec alone, without reading the design.
-->

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | V1 VERIFY_NAME_1 | R1 |
| 2 | V2 VERIFY_NAME_2 | R1, R2 |
| 3 | V3 VERIFY_NAME_3 | R3 |
| 4 | V4 VERIFY_NAME_4 | R2, R4 |
| 5 | V5 VERIFY_NAME_5 | R5 |
...

### V1 VERIFY_NAME_1

- Means: checklist
- DETAIL_1

### V2 VERIFY_NAME_2

- Means: debug/DEBUG_FILE
- DETAIL_1

### V3 VERIFY_NAME_3

- Means: checklist
- DETAIL_1

### V4 VERIFY_NAME_4

- Means: debug/DEBUG_FILE
- DETAIL_1

### V5 VERIFY_NAME_5

- Means: checklist
- DETAIL_1
...

## Articles
<!-- Decisions this document rests on -->
- [ARTICLE_NAME_1](../L4_articles/ARTICLE_NAME_1.md)
- [ARTICLE_NAME_2](../L4_articles/ARTICLE_NAME_2.md)
- [ARTICLE_NAME_3](../L4_articles/ARTICLE_NAME_3.md)
...

## References
<!-- Links to what this document cites -->

### Specs

- [SPEC_NAME_1](../L2_specs/SPEC_NAME_1.md)
- [SPEC_NAME_2](../L2_specs/SPEC_NAME_2.md)
- [SPEC_NAME_3](../L2_specs/SPEC_NAME_3.md)
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
