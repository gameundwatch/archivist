<!--
    LARGE_SNAKE_CASE is a placeholder. Replace every one with content.
    Everything else is written as it stands, field names included.
    A line holding only `...` means repeat as needed; delete the line.
-->

# FEATURE_NAME — about feature

<!-- FEATURE description... -->

## Background

<!-- Why this is needed: the situation, the premise, what one must know -->

## Availability

<!--
What a user can do with this FEATURE_NAME, as a bullet list.
Each item carries an anchor, A1, A2, ..., so the table below can cite it.

Write the prose in the language the project already uses.
-->

<a id="A1"></a>
- **A1** AVAILABILITY_ITEMS_1
    - DETAIL_1
    - DETAIL_2

<a id="A2"></a>
- **A2** AVAILABILITY_ITEMS_2
    - DETAIL_1

<a id="A3"></a>
- **A3** AVAILABILITY_ITEMS_3
    - DETAIL_1
...

### Coverage

<!--
    spec and design never cite each other. This table is the only place the two
    meet, so it is the only place their disagreement can be seen.

    One row is one availability item.
    spec: the R anchors in L2_specs that promise this item. May be several.
    design: the T anchors in L2_designs that solve it. May be several.

    A blank cell is a defect and stops shipping.
    An empty spec cell means it was built without being promised.
    An empty design cell means it was promised without being solved.
    An R or a T that appears in no row is the same defect seen from below.
-->

| availability | spec | design |
| ------------ | ---- | ------ |
| [A1](#A1) | [R1](../L2_specs/SPEC_NAME.md#R1) | [T1](../L2_designs/DESIGN_NAME.md#T1) |
| [A2](#A2) | [R2](../L2_specs/SPEC_NAME.md#R2), [R3](../L2_specs/SPEC_NAME.md#R3) | [T2](../L2_designs/DESIGN_NAME.md#T2) |
| [A3](#A3) | [R4](../L2_specs/SPEC_NAME.md#R4) | [T3](../L2_designs/DESIGN_NAME.md#T3), [T4](../L2_designs/DESIGN_NAME.md#T4) |
...


## Decisions
<!-- Decisions this document rests on -->
- [DECISION_NAME_1](../L4_decisions/DECISION_NAME_1.md)
- [DECISION_NAME_2](../L4_decisions/DECISION_NAME_2.md)
- [DECISION_NAME_3](../L4_decisions/DECISION_NAME_3.md)
...

## References

### Features

- [FEATURE_NAME_1](../L1_features/FEATURE_NAME_1.md)
- [FEATURE_NAME_2](../L1_features/FEATURE_NAME_2.md)
- [FEATURE_NAME_3](../L1_features/FEATURE_NAME_3.md)
- ...

### Specs

- [SPEC_NAME_1](../L2_specs/SPEC_NAME_1.md)
- [SPEC_NAME_2](../L2_specs/SPEC_NAME_2.md)
- [SPEC_NAME_3](../L2_specs/SPEC_NAME_3.md)
- ...

### Designs

- [DESIGN_NAME_1](../L2_designs/DESIGN_NAME_1.md)
- [DESIGN_NAME_2](../L2_designs/DESIGN_NAME_2.md)
- [DESIGN_NAME_3](../L2_designs/DESIGN_NAME_3.md)
- ...
