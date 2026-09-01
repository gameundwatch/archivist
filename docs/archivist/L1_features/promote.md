# promote — 実装が届いた印を外す

<!-- `_` を除去し、流入リンクを書き換える -->

## Background

実装が届いても、印が残ったままだと予定と現物の区別が付かなくなる。
外す作業はリネームと全流入リンクの書き換えを伴い、索引が無いため
手で追うと漏れる。

## Availability

- check の報告を指定して起動すると、対象の `_` が外れる
- その文書を指している全てのリンクが追随して書き換わる
- 実装が届いていない文書には触れない

## Decisions
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)
- [`_` を外す作業は check から分ける](../L4_decisions/promote-separate-from-check.md)

## References

### Specs

- [promote](../L2_specs/promote.md)

### Designs

- [promote](../L2_designs/promote.md)
