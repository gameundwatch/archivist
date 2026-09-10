# promote — 印を外す要件

## Requirements

### R1 check の報告を入力にする

- 自分では実現先の実在を判定しない

### R2 `_` を外し、流入リンクを追随させる

- その文書を指す全てのリンクを書き換える
- 索引を持たないため、文書群を走査して見つける

### R3 実現先が実在しない文書には触れない

- 報告に挙がっていないものを変えない

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | V1 入力の限定 | R1 |
| 2 | V2 リンクの追随 | R2 |
| 3 | V3 範囲の限定 | R3 |

### V1 入力の限定

- Means: checklist
- 報告を与えずに起動し、何も変わらないことを見る

### V2 リンクの追随

- Means: checklist
- 印を外した後、切れたリンクが一本も無いことを見る

### V3 範囲の限定

- Means: checklist
- 報告に無い `_` 付き文書が、印を保ったままであることを見る

## Articles
- [印が付くのは実現先を持つ層だけ](../L4_articles/mark-only-where-realized.md)
- [`_` を外す作業は check から分ける](../L4_articles/promote-separate-from-check.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [reference](../L3_terms/reference.md)
- [mark](../L3_terms/mark.md)
