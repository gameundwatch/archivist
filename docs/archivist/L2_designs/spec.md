# spec — 仕様を起こす設計

## Parts

| No | target_name | target_file | IN | OUT |
| -- | ----------- | ----------- | -- | --- |
| T1 | spec | skills/archivist-spec/SKILL.md | 条項, L3 | L2_specs/SPEC_NAME.md |
| T2 | template | skills/archivist-spec/TEMPLATE.md | - | 書式 |
| T3 | l3 | docs/archivist/L3_*/ | 語と構造 | 参照先 |

### Relation

```mermaid
flowchart LR
    TP["template"] -.書式.-> S["spec"]
    IN["条項, L3"] --> S --> OUT["L2_specs/SPEC_NAME.md"]
```

## Rules
- 内部の作りに触れそうになったら design に回す
- 1回の起動で1ファイルだけ書く

## Verify

| No | VERIFY_NAME | TARGET |
| -- | ----------- | ------ |
| 1 | V1 スキルの入力範囲 | T1 |
| 2 | V2 型紙の検証欄 | T2 |
| 3 | V3 語と構造の参照先 | T3 |

### V1 スキルの入力範囲

- Means: checklist
- `SKILL.md` の What to read が条項と L3 だけを挙げ、`L2_designs/` を挙げていないことを見る
- design を引かないことが Reference direction に書かれていることを見る

### V2 型紙の検証欄

- Means: checklist
- `TEMPLATE.md` の Verify の注記が debug を宛先として名指していることを見る
- `Means:` の値域がファイルパスと `checklist` の二つであることを見る

### V3 語と構造の参照先

- Means: checklist
- `docs/archivist/L3_*/` が入力として `SKILL.md` に挙がっていることを見る

## Articles
- [debug は spec だけを読んで書ける](../L4_articles/debug-from-spec-alone.md)
- [spec と design は互いを引かない](../L4_articles/spec-design-independent.md)
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_articles/output-language-follows-project.md)
- [配布物は英語で書く](../L4_articles/distributed-content-in-english.md)
- [検証は自分の手段を宣言する](../L4_articles/verification-declares-its-means.md)
- [テンプレートはスキルの中に置く](../L4_articles/template-belongs-to-skill.md)
- [スキルは文書の要素ごとに割る](../L4_articles/skill-per-element.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [language-split](../L3_structures/language-split.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [article](../L3_terms/article.md)
- [reference](../L3_terms/reference.md)
