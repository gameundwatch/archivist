# feature — 機能を起こす要件

## Requirements

### R1 条項から機能を起こす

- 仕様と設計の要約として作らない
- 機能の分解そのものが条項であることを前提とする

### R2 利用者が名指しできる単位を一つとする

- 何を一つの単位とするかは条項が決める。実装の分割から導かない

### R3 何ができるかを箇条書きで示す

- 要件と設計には踏み込まない
- なぜ必要とされたかを背景として持つ
- 各項目は `A1`, `A2`, ... の番号を持ち、下の表はこの番号で行を立てる

### R4 仕様と設計を availability ごとの表で突き合わせる

- 一行が一つの availability。spec 列は `R` の番号を、design 列は `T` の番号を置く
- どの spec と design の文書を指すかは References が持つ。表は番号だけを並べる
- spec と design は互いを引かないため、両者が出会う場所はこの表だけになる
- 空欄は不備であり、出荷を止める
    - spec 列が空 — 約束せずに作った
    - design 列が空 — 約束したが解いていない
- どの行からも指されない `R` や `T` は、同じ不備を下から見たものになる

### R5 散文は対象プロジェクトの言語で書く

- 既存の文書が無いときは、条項が書かれている言語に合わせる
- 見出しとフィールド名は言語に依らず英語で固定する

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | V1 起点の確認 | R1 |
| 2 | V2 単位との対応 | R2 |
| 3 | V3 層の越境 | R3 |
| 4 | V4 対応表の網羅 | R4 |
| 5 | V5 言語の追随 | R5 |

### V1 起点の確認

- Means: checklist
- 仕様と設計だけを与えて起動し、条項が無い機能が起きないことを見る

### V2 単位との対応

- Means: checklist
- 条項が公開すると定めた単位の集合と機能の集合が一致することを見る

### V3 層の越境

- Means: checklist
- 記述に要件や設計の内容が混ざっていないことを見る
- 各項目が `A` 番号を持ち、番号が重複しないことを見る

### V4 対応表の網羅

- Means: checklist
- 各 availability が一行を持ち、spec 列と design 列が共に埋まっていることを見る
- 片方の列だけ空の行を含む文書を与え、どちらが空かを言い当てて止まることを見る
- 仕様の全 `R` と設計の全 `T` が、いずれかの行から指されていることを見る

### V5 言語の追随

- Means: checklist
- 既存の文書が日本語のプロジェクトで起動し、生成物の散文が日本語であることを見る
- 同じ生成物の見出しとフィールド名が英語のままであることを見る

## Articles
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_articles/output-language-follows-project.md)
- [配布物は英語で書く](../L4_articles/distributed-content-in-english.md)
- [機能が何かは条項であり、下層の要約ではない](../L4_articles/features-come-from-articles.md)
- [spec と design の整合を担保するのは feature だけ](../L4_articles/feature-joins-spec-and-design.md)
- [spec と design は互いを引かない](../L4_articles/spec-design-independent.md)
- [参照はファイル単位で張る](../L4_articles/references-are-file-scoped.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [form](../L3_terms/form.md)
- [feature](../L3_terms/feature.md)
- [article](../L3_terms/article.md)
- [spec](../L3_terms/spec.md)
- [design](../L3_terms/design.md)
