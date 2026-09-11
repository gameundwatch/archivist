# index — 索引の設計

## Parts

| No | target_name | target_file | IN | OUT |
| -- | ----------- | ----------- | -- | --- |
| T1 | index | skills/archivist-index/SKILL.md | docs/archivist/ の全文書 | 索引の全体 |
| T2 | csv | docs/archivist/index.csv | 索引の全体 | 文書1枚1行の表 |

### Relation

```mermaid
flowchart LR
    DOCS["docs/archivist/**.md"] --> S["index"] --> CSV["docs/archivist/index.csv"]
    S -.読まない.-> OLD["既存の index.csv"]
```

## Rules
- 走査で組む。既存の索引を入力にしない
- 書き出しは全置換。行の追記も差し替えもしない
- 列は `path` `title` `refs` の3つ。ヘッダ行を持たない
- 値は全て引用符で囲み、値の中の `"` は `""` に倍にする。`refs` は `;` でつなぐ
- 参照はリンクの指し先をそのまま持ち、`docs/archivist/` からの相対で揃える
- 行は `path` で並べる。同じ文書群からは同じ内容が出る
- 索引自身は行を持たない。文書ではないため

## Verify

| No | VERIFY_NAME | TARGET |
| -- | ----------- | ------ |
| 1 | V1 入力の限定 | T1 |
| 2 | V2 全置換の書き出し | T1 |
| 3 | V3 パスの基点 | T2 |
| 4 | V4 索引自身の除外 | T2 |
| 5 | V5 列の構成 | T2 |
| 6 | V6 引用と連結 | T2 |

### V1 入力の限定

- Means: checklist
- 既存の索引を読まないと `SKILL.md` に書かれていることを見る

### V2 全置換の書き出し

- Means: checklist
- 差分を当てず全体を書き直すと `SKILL.md` に書かれていることを見る

### V3 パスの基点

- Means: checklist
- 索引の中のパスが `docs/archivist/` を基点に揃っていることを見る

### V4 索引自身の除外

- Means: checklist
- `index.csv` を指す行が索引に無いことを見る

### V5 列の構成

- Means: checklist
- 各行が3つの値を持ち、ヘッダ行が無いことを見る
- 層を値に持つ列が無いことを見る

### V6 引用と連結

- Means: checklist
- `"` を含むタイトルの文書を置き、その行で `""` に倍になっていることを見る
- 参照を複数持つ文書の行で、指し先が `;` でつながれていることを見る

## Articles
- [生成される索引は層に属さない](../L4_articles/index-outside-layers.md)
- [索引は点を1行とする](../L4_articles/index-rows-are-nodes.md)
- [索引の列は path と title と refs の3つとする](../L4_articles/index-columns-are-three.md)
- [参照はファイル単位で張る](../L4_articles/references-are-file-scoped.md)
- [配布物は英語で書く](../L4_articles/distributed-content-in-english.md)
- [テンプレートはスキルが持つ](../L4_articles/template-belongs-to-skill.md)

## References

### Structures

- [directory-layout](../L3_structures/directory-layout.md)
- [skill-composition](../L3_structures/skill-composition.md)

### Terms

- [index](../L3_terms/index.md)
- [reference](../L3_terms/reference.md)
