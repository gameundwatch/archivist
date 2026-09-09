# feature — 機能を1枚起こす

<!-- 利用者が名指しできる単位を、L1_features に書く -->

## Background

利用者が名指しできるものが何かは、仕様や設計から出てこない。製品が外に
何を晒すかの決断であり、書かれないと名指しできるのに約束が無い機能が残る。

## Availability

<a id="A1"></a>
- **A1** 決断を指定して起動すると、その決断が定めた機能が1枚起きる

<a id="A2"></a>
- **A2** 何ができるかが箇条書きで読め、各項目にアンカーが付く

<a id="A3"></a>
- **A3** なぜ必要とされたかが背景として残る

<a id="A4"></a>
- **A4** 仕様と設計が availability ごとの表で突き合わされ、空欄が不備として見える

<a id="A5"></a>
- **A5** 機能の分解は決断から来る。仕様と設計の要約ではない

<a id="A6"></a>
- **A6** 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる

### Coverage

| availability | spec | design |
| --- | --- | --- |
| [A1](#A1) | [R1](../L2_specs/feature.md#R1) | [T1](../L2_designs/feature.md#T1), [T2](../L2_designs/feature.md#T2) |
| [A2](#A2) | [R3](../L2_specs/feature.md#R3) | [T2](../L2_designs/feature.md#T2) |
| [A3](#A3) | [R3](../L2_specs/feature.md#R3) | [T2](../L2_designs/feature.md#T2) |
| [A4](#A4) | [R4](../L2_specs/feature.md#R4) | [T1](../L2_designs/feature.md#T1), [T2](../L2_designs/feature.md#T2) |
| [A5](#A5) | [R1](../L2_specs/feature.md#R1), [R2](../L2_specs/feature.md#R2) | [T1](../L2_designs/feature.md#T1) |
| [A6](#A6) | [R5](../L2_specs/feature.md#R5) | [T1](../L2_designs/feature.md#T1) |

## Decisions
- [spec と design の整合を担保するのは feature だけ](../L4_decisions/feature-joins-spec-and-design.md)
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [機能が何かは決断であり、下層の要約ではない](../L4_decisions/features-come-from-decisions.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)


## References

### Specs

- [feature](../L2_specs/feature.md)

### Designs

- [feature](../L2_designs/feature.md)
