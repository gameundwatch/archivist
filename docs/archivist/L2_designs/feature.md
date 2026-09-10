# feature — 機能を起こす設計

## Parts

| No | target_name | target_file | IN | OUT |
| -- | ----------- | ----------- | -- | --- |
| T1 | feature | skills/archivist-feature/SKILL.md | 条項, L2 | L1_features/FEATURE_NAME.md |
| T2 | template | skills/archivist-feature/TEMPLATE.md | - | 書式 |

### Relation

```mermaid
flowchart LR
    TP["template"] -.書式.-> S["feature"]
    IN["条項, L2"] --> S --> OUT["L1_features/FEATURE_NAME.md"]
```

## Rules
- 仕様と設計の要約にしない。起点は条項に置く
- 仕様と設計が出会う場所はこの層の対応表だけになる。空欄は出荷を止める
- 1回の起動で1ファイルだけ書く

## Verify

| No | VERIFY_NAME | TARGET |
| -- | ----------- | ------ |
| 1 | V1 スキルの起点 | T1 |
| 2 | V2 型紙の対応表 | T2 |

### V1 スキルの起点

- Means: checklist
- 仕様と設計の要約にしないことが `SKILL.md` に書かれていることを見る
- Coverage の節が spec 列と design 列の空欄の意味を書き分けていることを見る

### V2 型紙の対応表

- Means: checklist
- `TEMPLATE.md` の Availability の各項目が `A1`, `A2`, ... の番号を持つことを見る
- Coverage 表の spec 列と design 列が番号だけを置き、リンクを持たないことを見る
- Coverage 表が availability, spec, design の三列を持つことを見る

## Articles
- [spec と design の整合を担保するのは feature だけ](../L4_articles/feature-joins-spec-and-design.md)
- [spec と design は互いを引かない](../L4_articles/spec-design-independent.md)
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_articles/output-language-follows-project.md)
- [配布物は英語で書く](../L4_articles/distributed-content-in-english.md)
- [テンプレートはスキルの中に置く](../L4_articles/template-belongs-to-skill.md)
- [機能が何かは条項であり、下層の要約ではない](../L4_articles/features-come-from-articles.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [language-split](../L3_structures/language-split.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [feature](../L3_terms/feature.md)
- [article](../L3_terms/article.md)
