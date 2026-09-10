# archivist — 条項から文書を組み直す

条項の集合を起点に、それが要求する上層の文書を書き起こす。

## Background

ADR は部分解であり、その集合だけでは実装に必要な文書群にならない。条項と
実装方針の中間に整理されない条項が残り、実装時に未考慮の部分を取りこぼす。
条項はあるのに、それが語の意味を変えたのか、仕様を変えたのか、設計を変えたのかが
誰も書かないまま積もる。

## Availability

- **A1** 条項を指定して起動すると、それが届く範囲の文書が組み直される

- **A2** 範囲は任意で、1件でも全件でもよい

- **A3** 文書は下から上へ、層を飛ばさずに組まれる。仕様と設計は互いを待たない

- **A4** 条項から導けない箇所に達したとき、何が足りないかを述べて止まる

- **A5** 組み直された文書は、どの条項から来たかを自身に持つ

- **A6** 条項が一枚も無いときは、取り込みのコマンドを案内して止まる

### Coverage

| availability | spec | design |
| --- | --- | --- |
| A1 | R1, R4 | T1, T2, T3, T4, T5, T6 |
| A2 | R1 | T1 |
| A3 | R2 | T1, T4, T5 |
| A4 | R3 | T1 |
| A5 | R5 | T2, T3, T4, T5, T6 |
| A6 | R6 | T1 |

## Articles
- [還元はするが、条項は立てない](../L4_articles/reduction-not-article.md)
- [スキルは文書の要素ごとに割る](../L4_articles/skill-per-element.md)
- [条項の取り込みは archivist の外に置く](../L4_articles/adoption-outside-archivist.md)

## References

### Features

- [term](term.md)
- [structure](structure.md)
- [spec](spec.md)
- [design](design.md)
- [feature](feature.md)
- [check](check.md)
- [promote](promote.md)
- [adopt](adopt.md)

### Specs

- [archivist](../L2_specs/archivist.md)

### Designs

- [archivist](../L2_designs/archivist.md)
