# SPEC_NAME — about spec

## Requirements
<!-- 
    What the subject must make work and must achieve.
    Keep to what can be confirmed from outside the spec. The inside belongs to design.
    Each detail lists firing conditions - when it works and when it does not -
    and scope: what is covered and what is not.
-->

<a id="R1"></a>

### R1 REQUIREMENT_NAME_1

- details
- details

<a id="R2"></a>

### R2 REQUIREMENT_NAME_2

- details
- details
- details

<a id="R3"></a>

### R3 REQUIREMENT_NAME_3

- details

<a id="R4"></a>

### R4 REQUIREMENT_NAME_4

- details
- details

<a id="R5"></a>

### R5 REQUIREMENT_NAME_5

- details
- details
...

## Verify

<!--
    Items that decide whether a REQUIREMENT is met. This section is the checklist.
    One item is one judgement; running them top to bottom completes the verification.
    The table above holds which VERIFY checks which REQUIREMENT.
    Details carry the procedure and the condition under which it counts as met.
    Means carries what runs the check: a file path for test code, or `checklist`
    when a person runs it by hand.

    Write each item detailed enough that the test can be written from this spec
    alone, without reading the design.
-->

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | [VERIFY_NAME_1](#V1) | [R1](#R1) |
| 2 | [VERIFY_NAME_2](#V2) | [R1](#R1), [R2](#R2) |
| 3 | [VERIFY_NAME_3](#V3) | [R3](#R3) |
| 4 | [VERIFY_NAME_4](#V4) | [R2](#R2), [R4](#R4) |
| 5 | [VERIFY_NAME_5](#V5) | [R5](#R5) |
...

<a id="V1"></a>

### V1 VERIFY_NAME_1

- Means: checklist
- details

<a id="V2"></a>

### V2 VERIFY_NAME_2

- Means: test/TEST_FILE
- details

<a id="V3"></a>

### V3 VERIFY_NAME_3

- Means: checklist
- details

<a id="V4"></a>

### V4 VERIFY_NAME_4

- Means: test/TEST_FILE
- details

<a id="V5"></a>

### V5 VERIFY_NAME_5

- Means: checklist
- details
...

## Decisions
<!-- Decisions this document rests on -->
- [DECISION_NAME_1](../L4_decisions/DECISION_NAME_1.md)
- [DECISION_NAME_2](../L4_decisions/DECISION_NAME_2.md)
- [DECISION_NAME_3](../L4_decisions/DECISION_NAME_3.md)
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
