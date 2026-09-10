# promote — 実現先が揃った印を外す

<!-- `_` を除去し、流入リンクを書き換える -->

## Background

実現先が揃っても、印が残ったままだと予定と現物の区別が付かなくなる。
外す作業はリネームと全流入リンクの書き換えを伴い、索引が無いため
手で追うと漏れる。

## Availability

- **A1** check の報告を指定して起動すると、対象の `_` が外れる

- **A2** その文書を指している全てのリンクが追随して書き換わる

- **A3** 実現先が実在しない文書には触れない

### Coverage

| availability | spec | design |
| --- | --- | --- |
| A1 | R1 | T1 |
| A2 | R2 | T1, T2 |
| A3 | R3 | T1 |

## Decisions
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)
- [`_` を外す作業は check から分ける](../L4_decisions/promote-separate-from-check.md)

## References

### Specs

- [promote](../L2_specs/promote.md)

### Designs

- [promote](../L2_designs/promote.md)
