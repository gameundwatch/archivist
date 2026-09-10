# skill-composition — スキルの構成

## Diagrams

### D1 スキルの構成と起動順

```mermaid
flowchart LR
    A["/archivist"]
    A --> T["/archivist-term"] --> S["/archivist-structure"]
    S --> SP["/archivist-spec"] --> F["/archivist-feature"]
    S --> D["/archivist-design"] --> F
    A --> C["/archivist-check"] -.報告.-> P["/archivist-promote"]
    DEC["( decision )"] --> C
    EXT["( 外の決断記述 )"] --> AD["/archivist-adopt"] --> DEC
    DEC --> A
    A -.decision が無いとき案内.-> AD
```

archivist がオーケストレーターとして伝播を司る。起動順は還元の向きに従う。
spec と design は structure の後で二叉に割れ、互いを待たない。合流するのは
feature ただ一つで、そこで両者が対応表として突き合わされる。
check も decisions を受け取るが、書かずに読むだけで判定を返す。
promote は check の報告を受け、`_` の除去と流入リンクの書き換えを行う。
decision は すでに存在するものとし、このskillでは作成しない。
adopt は Order の外に立ち、archivist が回り始める前に decision を用意する。
archivist は decision が一枚も無いときだけ adopt を案内し、呼びはしない。

### D2 コマンドと feature の対応

```mermaid
flowchart LR
    S0["/archivist"] ---|1対1| F0["feature: archivist"]
    S1["/archivist-term"] ---|1対1| F1["feature: term"]
    S2["/archivist-structure"] ---|1対1| F2["feature: structure"]
    S3["/archivist-spec"] ---|1対1| F3["feature: spec"]
    S4["/archivist-design"] ---|1対1| F4["feature: design"]
    S5["/archivist-feature"] ---|1対1| F5["feature: feature"]
    S6["/archivist-check"] ---|1対1| F6["feature: check"]
    S7["/archivist-promote"] ---|1対1| F7["feature: promote"]
    S8["/archivist-adopt"] ---|1対1| F8["feature: adopt"]
```

起動できるコマンド1本が feature 1枚に対応する。片方だけが増えた状態は、
名指しできるのに約束が無いか、約束だけあって起動できないかのいずれかを意味する。

## Decisions
- [決断が増減させる一覧は structure に置く](../L4_decisions/enumeration-as-mapping.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)
- [`_` を外す作業は check から分ける](../L4_decisions/promote-separate-from-check.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [還元はするが、決断はしない](../L4_decisions/reduction-not-decision.md)
- [決断の取り込みは archivist の外に置く](../L4_decisions/adoption-outside-archivist.md)

## References

### Terms

- [reduction](../L3_terms/reduction.md)
- [feature](../L3_terms/feature.md)
- [decision](../L3_terms/decision.md)
- [adoption](../L3_terms/adoption.md)
