# design — 設計を1枚起こす

<!-- 決断が要求する中身を、L2_designs に材料と規則と検証として書く -->

## Background

何をどのファイルに宿し、どんな制約をかけるかが書かれないと、実装者が毎回
同じことを考え直す。仕様は約束だけを述べ、中身には触れない。両者は互いを
待たずに書かれ、突き合わされるのは feature の対応表になる。

## Availability

<a id="A1"></a>
- **A1** 決断を指定して起動すると、それを解く設計が1枚起きる

<a id="A2"></a>
- **A2** 影響するファイルが材料として列挙され、各行がアンカーで指せる

<a id="A3"></a>
- **A3** 実装のための規則が、由来となる決断とともに並ぶ

<a id="A4"></a>
- **A4** 検証は、それだけを読んで test が書ける詳しさで書かれる

<a id="A5"></a>
- **A5** 仕様を引かない。仕様とは互いを待たずに書ける

<a id="A6"></a>
- **A6** 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる

### Coverage

| availability | spec | design |
| --- | --- | --- |
| [A1](#A1) | [R2](../L2_specs/design.md#R2) | [T1](../L2_designs/design.md#T1), [T2](../L2_designs/design.md#T2), [T3](../L2_designs/design.md#T3) |
| [A2](#A2) | [R1](../L2_specs/design.md#R1), [R2](../L2_specs/design.md#R2) | [T2](../L2_designs/design.md#T2) |
| [A3](#A3) | [R3](../L2_specs/design.md#R3) | [T1](../L2_designs/design.md#T1), [T2](../L2_designs/design.md#T2) |
| [A4](#A4) | [R6](../L2_specs/design.md#R6) | [T1](../L2_designs/design.md#T1), [T2](../L2_designs/design.md#T2) |
| [A5](#A5) | [R4](../L2_specs/design.md#R4) | [T1](../L2_designs/design.md#T1) |
| [A6](#A6) | [R5](../L2_specs/design.md#R5) | [T1](../L2_designs/design.md#T1) |

## Decisions
- [test は design を読んで書く](../L4_decisions/test-from-design.md)
- [spec と design は互いを引かない](../L4_decisions/spec-design-independent.md)
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)


## References

### Specs

- [design](../L2_specs/design.md)

### Designs

- [design](../L2_designs/design.md)
