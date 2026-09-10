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
Each item carries a number, A1, A2, ..., so the table below can cite it.

Write the prose in the language the project already uses.
-->


- **A1** AVAILABILITY_ITEMS_1
    - DETAIL_1
    - DETAIL_2


- **A2** AVAILABILITY_ITEMS_2
    - DETAIL_1


- **A3** AVAILABILITY_ITEMS_3
    - DETAIL_1
...

### Coverage

<!--
    spec and design never cite each other. This table is the only place the two
    meet, so it is the only place their disagreement can be seen.

    One row is one availability item.
    spec: the R numbers in the L2_specs document that promise this item. May be several.
    design: the T numbers in the L2_designs document that solve it. May be several.
    Write the numbers alone. Which documents they live in is held by References,
    which links each of them as a whole file.

    A blank cell is a defect and stops shipping.
    An empty spec cell means it was built without being promised.
    An empty design cell means it was promised without being solved.
    An R or a T that appears in no row is the same defect seen from below.
-->

| availability | spec | design |
| ------------ | ---- | ------ |
| A1 | R1 | T1 |
| A2 | R2, R3 | T2 |
| A3 | R4 | T3, T4 |
...


## Articles
<!-- Articles this document rests on -->
- [ARTICLE_NAME_1](../L4_articles/ARTICLE_NAME_1.md)
- [ARTICLE_NAME_2](../L4_articles/ARTICLE_NAME_2.md)
- [ARTICLE_NAME_3](../L4_articles/ARTICLE_NAME_3.md)
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
