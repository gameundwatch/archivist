# structure — 構造を1枚起こす

<!-- 決断が課した形を、L3_structures に図として書く -->

## Background

決断は形を課す。個数、順序、状態遷移、包含。図にしないと、同じ制約が
複数の設計にばらばらに書き写される。

## Availability

<a id="A1"></a>
- **A1** 決断を指定して起動すると、その決断が課した形が図として1枚起きる

<a id="A2"></a>
- **A2** 図は複数枚置け、それぞれにアンカーが付く

<a id="A3"></a>
- **A3** 図に使う語は L3_terms にあるものに限られる

<a id="A4"></a>
- **A4** design を捨てても残る形だけが置かれる

<a id="A5"></a>
- **A5** 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる

### Coverage

| availability | spec | design |
| --- | --- | --- |
| [A1](#A1) | [R1](../L2_specs/structure.md#R1) | [T1](../L2_designs/structure.md#T1), [T2](../L2_designs/structure.md#T2) |
| [A2](#A2) | [R4](../L2_specs/structure.md#R4) | [T2](../L2_designs/structure.md#T2) |
| [A3](#A3) | [R2](../L2_specs/structure.md#R2) | [T1](../L2_designs/structure.md#T1), [T3](../L2_designs/structure.md#T3) |
| [A4](#A4) | [R3](../L2_specs/structure.md#R3) | [T1](../L2_designs/structure.md#T1) |
| [A5](#A5) | [R5](../L2_specs/structure.md#R5) | [T1](../L2_designs/structure.md#T1) |

## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)


## References

### Specs

- [structure](../L2_specs/structure.md)

### Designs

- [structure](../L2_designs/structure.md)
