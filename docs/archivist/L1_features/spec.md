# spec — 仕様を1枚起こす

<!-- 決断から導ける約束を、L2_specs に要件と検証として書く -->

## Background

決断は約束を生む。何ができ、何をしないか。約束が書かれないと、実装が
何を満たせば終わりなのか誰にも言えない。

## Availability

<a id="A1"></a>
- **A1** 決断を指定して起動すると、要件とその検証が1枚起きる

<a id="A2"></a>
- **A2** 要件は外から観測できることだけに留まる

<a id="A3"></a>
- **A3** 検証はそのままチェックリストとして通せる

<a id="A4"></a>
- **A4** どの要件がどの検証で確かめられるかが表で読める

<a id="A5"></a>
- **A5** 検証は、それだけを読んで debug が書ける詳しさで書かれる

<a id="A6"></a>
- **A6** 設計を引かない。設計とは互いを待たずに書ける

<a id="A7"></a>
- **A7** 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる

### Coverage

| availability | spec | design |
| --- | --- | --- |
| [A1](#A1) | [R1](../L2_specs/spec.md#R1), [R2](../L2_specs/spec.md#R2) | [T1](../L2_designs/spec.md#T1), [T2](../L2_designs/spec.md#T2) |
| [A2](#A2) | [R1](../L2_specs/spec.md#R1) | [T1](../L2_designs/spec.md#T1), [T3](../L2_designs/spec.md#T3) |
| [A3](#A3) | [R3](../L2_specs/spec.md#R3) | [T2](../L2_designs/spec.md#T2) |
| [A4](#A4) | [R4](../L2_specs/spec.md#R4) | [T2](../L2_designs/spec.md#T2) |
| [A5](#A5) | [R5](../L2_specs/spec.md#R5), [R6](../L2_specs/spec.md#R6) | [T1](../L2_designs/spec.md#T1), [T2](../L2_designs/spec.md#T2) |
| [A6](#A6) | [R8](../L2_specs/spec.md#R8) | [T1](../L2_designs/spec.md#T1) |
| [A7](#A7) | [R7](../L2_specs/spec.md#R7) | [T1](../L2_designs/spec.md#T1) |

## Decisions
- [debug は spec だけを読んで書ける](../L4_decisions/debug-from-spec-alone.md)
- [spec と design は互いを引かない](../L4_decisions/spec-design-independent.md)
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [検証は自分の手段を宣言する](../L4_decisions/verification-declares-its-means.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)


## References

### Specs

- [spec](../L2_specs/spec.md)

### Designs

- [spec](../L2_designs/spec.md)
