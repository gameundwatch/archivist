# check — 揃っているかを判定する

<!-- docs/archivist/ を読み、文書群が出荷の条件を満たすか答える -->

## Background

層と参照の規則は文書に書かれているが、守られているかを見る手が無い。
リンク切れ、層飛び、循環、実現先と印の食い違いは、目で追う限り必ず漏れる。

## Availability

<a id="A1"></a>
- **A1** 決断と docs/archivist/ 全体を読み、判定が返る

<a id="A2"></a>
- **A2** リンクが解決するか、層を飛んでいないか、循環していないかが分かる

<a id="A3"></a>
- **A3** `_` が付いた文書のうち、実現先が実在するものが報告される

<a id="A4"></a>
- **A4** 何も書き換えない

<a id="A5"></a>
- **A5** 検証が自分の層だけを読んで実装できるかが分かる

<a id="A6"></a>
- **A6** 仕様と設計の対応表の欠落が、どちらの側の不備かとともに分かる

<a id="A7"></a>
- **A7** 形が英語で保たれているか、図が実態と合っているかが分かる

### Coverage

| availability | spec | design |
| --- | --- | --- |
| [A1](#A1) | [R1](../L2_specs/check.md#R1) | [T1](../L2_designs/check.md#T1), [T2](../L2_designs/check.md#T2) |
| [A2](#A2) | [R1](../L2_specs/check.md#R1), [R2](../L2_specs/check.md#R2), [R3](../L2_specs/check.md#R3) | [T1](../L2_designs/check.md#T1) |
| [A3](#A3) | [R4](../L2_specs/check.md#R4), [R8](../L2_specs/check.md#R8) | [T1](../L2_designs/check.md#T1) |
| [A4](#A4) | [R5](../L2_specs/check.md#R5) | [T1](../L2_designs/check.md#T1) |
| [A5](#A5) | [R6](../L2_specs/check.md#R6), [R7](../L2_specs/check.md#R7) | [T1](../L2_designs/check.md#T1) |
| [A6](#A6) | [R11](../L2_specs/check.md#R11) | [T1](../L2_designs/check.md#T1), [T2](../L2_designs/check.md#T2) |
| [A7](#A7) | [R9](../L2_specs/check.md#R9), [R10](../L2_specs/check.md#R10) | [T1](../L2_designs/check.md#T1), [T2](../L2_designs/check.md#T2) |

## Decisions
- [debug は spec だけを読んで書ける](../L4_decisions/debug-from-spec-alone.md)
- [test は design を読んで書く](../L4_decisions/test-from-design.md)
- [spec と design の整合を担保するのは feature だけ](../L4_decisions/feature-joins-spec-and-design.md)
- [印が付くのは実現先を持つ層だけ](../L4_decisions/mark-only-where-realized.md)
- [検証は自分の手段を宣言する](../L4_decisions/verification-declares-its-means.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)
- [`_` を外す作業は check から分ける](../L4_decisions/promote-separate-from-check.md)

## References

### Specs

- [check](../L2_specs/check.md)

### Designs

- [check](../L2_designs/check.md)
