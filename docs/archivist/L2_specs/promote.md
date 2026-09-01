# promote — 印を外す要件

## Requirements

<a id="R1"></a>

### R1 check の報告を入力にする

- 自分では実装の到達を判定しない

<a id="R2"></a>

### R2 `_` を外し、流入リンクを追随させる

- その文書を指す全てのリンクを書き換える
- 索引を持たないため、文書群を走査して見つける

<a id="R3"></a>

### R3 実装が届いていない文書には触れない

- 報告に挙がっていないものを変えない

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | [入力の限定](#V1) | [R1](#R1) |
| 2 | [リンクの追随](#V2) | [R2](#R2) |
| 3 | [範囲の限定](#V3) | [R3](#R3) |

<a id="V1"></a>

### V1 入力の限定

- Means: checklist
- 報告を与えずに起動し、何も変わらないことを見る

<a id="V2"></a>

### V2 リンクの追随

- Means: checklist
- 印を外した後、切れたリンクが一本も無いことを見る

<a id="V3"></a>

### V3 範囲の限定

- Means: checklist
- 報告に無い `_` 付き文書が、印を保ったままであることを見る

## Decisions
- [印が付くのは実現先を持つ層だけ](../L4_decisions/mark-only-where-realized.md)
- [`_` を外す作業は check から分ける](../L4_decisions/promote-separate-from-check.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [reference](../L3_terms/reference.md)
- [mark](../L3_terms/mark.md)
