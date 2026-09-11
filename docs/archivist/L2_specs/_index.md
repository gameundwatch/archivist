# index — 索引の要件

## Requirements

### R1 文書1枚を1行とする

- `docs/archivist/` の全ての `.md` が1行を持つことを保つ
- 参照を1本も持たない文書も1行を持つ
- 行と文書の対応は1対1で、同じ文書が2行に現れない

### R2 参照はその行の中に持つ

- ある文書が指す先を、その文書の行の中に並べる
- 参照1本を1行としない

### R3 まるごと書き直す

- 起動のたびに `index.csv` の全体を置き換える
- 既存の索引を読んで差分を当てない

### R4 索引に印を付けない

- ファイル名に `_` を付けない
- 索引は実現先を持たないため、印の対象にならない

### R5 索引を他の文書の前提にしない

- `index.csv` を削除しても、文書群が満たすべき条件は変わらない
- 索引を読まなければ成り立たない記述を、どの層にも足さない

### R6 文書だけから組み直せる

- 入力は `docs/archivist/` の文書に限る
- 同じ文書群からは同じ索引が出る

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | V1 行と文書の対応 | R1 |
| 2 | V2 孤立文書の在席 | R1 |
| 3 | V3 参照の収まり | R2 |
| 4 | V4 全置換 | R3 |
| 5 | V5 印の不在 | R4 |
| 6 | V6 索引の可削除性 | R5 |
| 7 | V7 再現性 | R6 |

### V1 行と文書の対応

- Means: checklist
- 索引の行数が `docs/archivist/` の `.md` の枚数と一致することを見る

### V2 孤立文書の在席

- Means: checklist
- 参照を持たない条項を置き、それが1行を持つことを見る

### V3 参照の収まり

- Means: checklist
- 参照を複数持つ文書が1行に収まっていることを見る

### V4 全置換

- Means: checklist
- 手で1行を壊した索引を置いて起動し、その行が残らないことを見る

### V5 印の不在

- Means: checklist
- 生成された索引のファイル名に `_` が無いことを見る

### V6 索引の可削除性

- Means: checklist
- 索引を削除した状態で `/archivist-check` を通し、判定が変わらないことを見る

### V7 再現性

- Means: checklist
- 文書を変えずに二度起動し、同じ内容が出ることを見る

## Articles
- [生成される索引は層に属さない](../L4_articles/index-outside-layers.md)
- [索引は点を1行とする](../L4_articles/index-rows-are-nodes.md)
- [参照はファイル単位で張る](../L4_articles/references-are-file-scoped.md)
- [印が付くのは実現先を持つ層だけ](../L4_articles/mark-only-where-realized.md)
- [検証は自分の手段を宣言する](../L4_articles/verification-declares-its-means.md)
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_articles/output-language-follows-project.md)

## References

### Structures

- [directory-layout](../L3_structures/directory-layout.md)
- [skill-composition](../L3_structures/skill-composition.md)

### Terms

- [index](../L3_terms/index.md)
- [reference](../L3_terms/reference.md)
- [mark](../L3_terms/mark.md)
