# check — 揃っているかを判定する

<!-- docs/archivist/ を読み、文書群が出荷の条件を満たすか答える -->

## Background

層と参照の規則は文書に書かれているが、守られているかを見る手が無い。
リンク切れ、層飛び、循環、実装と印の食い違いは、目で追う限り必ず漏れる。

## Availability

- 決断と docs/archivist/ 全体を読み、判定が返る
- リンクが解決するか、層を飛んでいないか、循環していないかが分かる
- `_` が付いた文書のうち、実装が届いたものが報告される
- 何も書き換えない
- 検証が design を前提にしていないかが分かる
## Decisions
- [印が付くのは実現先を持つ層だけ](../L4_decisions/mark-only-where-realized.md)
- [検証は自分の手段を宣言する](../L4_decisions/verification-declares-its-means.md)
- [テストコードは spec だけを読んで書ける](../L4_decisions/test-from-spec-alone.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)
- [`_` を外す作業は check から分ける](../L4_decisions/promote-separate-from-check.md)

## References

### Specs

- [check](../L2_specs/check.md)

### Designs

- [check](../L2_designs/check.md)
