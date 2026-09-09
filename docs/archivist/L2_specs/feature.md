# feature — 機能を起こす要件

## Requirements

<a id="R1"></a>

### R1 決断から機能を起こす

- 仕様と設計の要約として作らない
- 機能の分解そのものが決断であることを前提とする

<a id="R2"></a>

### R2 利用者が名指しできる単位を一つとする

- 何を一つの単位とするかは決断が決める。実装の分割から導かない

<a id="R3"></a>

### R3 何ができるかを箇条書きで示す

- 要件と設計には踏み込まない
- なぜ必要とされたかを背景として持つ
- 各項目は `A1`, `A2`, ... の錨を持ち、下の表から指せる

<a id="R4"></a>

### R4 仕様と設計を availability ごとの表で突き合わせる

- 一行が一つの availability。spec 列は `R` の錨を、design 列は `T` の錨を持つ
- spec と design は互いを引かないため、両者が出会う場所はこの表だけになる
- 空欄は不備であり、出荷を止める
    - spec 列が空 — 約束せずに作った
    - design 列が空 — 約束したが解いていない
- どの行からも指されない `R` や `T` は、同じ不備を下から見たものになる

<a id="R5"></a>

### R5 散文は対象プロジェクトの言語で書く

- 既存の文書が無いときは、決断が書かれている言語に合わせる
- 見出し、アンカー、フィールド名は言語に依らず英語で固定する

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | [起点の確認](#V1) | [R1](#R1) |
| 2 | [単位との対応](#V2) | [R2](#R2) |
| 3 | [層の越境](#V3) | [R3](#R3) |
| 4 | [対応表の網羅](#V4) | [R4](#R4) |
| 5 | [言語の追随](#V5) | [R5](#R5) |

<a id="V1"></a>

### V1 起点の確認

- Means: checklist
- 仕様と設計だけを与えて起動し、決断が無い機能が起きないことを見る

<a id="V2"></a>

### V2 単位との対応

- Means: checklist
- 決断が公開すると定めた単位の集合と機能の集合が一致することを見る

<a id="V3"></a>

### V3 層の越境

- Means: checklist
- 記述に要件や設計の内容が混ざっていないことを見る
- 各項目が `A` 番号と `<a id>` を持つことを見る

<a id="V4"></a>

### V4 対応表の網羅

- Means: checklist
- 各 availability が一行を持ち、spec 列と design 列が共に埋まっていることを見る
- 片方の列だけ空の行を含む文書を与え、どちらが空かを言い当てて止まることを見る
- 仕様の全 `R` と設計の全 `T` が、いずれかの行から指されていることを見る

<a id="V5"></a>

### V5 言語の追随

- Means: checklist
- 既存の文書が日本語のプロジェクトで起動し、生成物の散文が日本語であることを見る
- 同じ生成物の見出しとフィールド名が英語のままであることを見る

## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [機能が何かは決断であり、下層の要約ではない](../L4_decisions/features-come-from-decisions.md)
- [spec と design の整合を担保するのは feature だけ](../L4_decisions/feature-joins-spec-and-design.md)
- [spec と design は互いを引かない](../L4_decisions/spec-design-independent.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [form](../L3_terms/form.md)
- [feature](../L3_terms/feature.md)
- [decision](../L3_terms/decision.md)
- [spec](../L3_terms/spec.md)
- [design](../L3_terms/design.md)
