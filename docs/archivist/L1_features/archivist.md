# archivist — 決断から文書を組み直す

決断の集合を起点に、それが要求する上層の文書を書き起こす。

## Background

ADR は部分解であり、その集合だけでは実装に必要な文書群にならない。決断と
実装方針の中間に整理されない決断が残り、実装時に未考慮の部分を取りこぼす。
決断はあるのに、それが語の意味を変えたのか、仕様を変えたのか、設計を変えたのかが
誰も書かないまま積もる。

## Availability

- 決断を指定して起動すると、それが届く範囲の文書が組み直される
- 範囲は任意で、1件でも全件でもよい
- 決断から導けない箇所に達したとき、何が足りないかを述べて止まる
- 組み直された文書は、どの決断から来たかを自身に持つ
- 決断が一枚も無いときは、取り込みのコマンドを案内して止まる

## Decisions
- [還元はするが、決断はしない](../L4_decisions/reduction-not-decision.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [決断の取り込みは archivist の外に置く](../L4_decisions/adoption-outside-archivist.md)

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
