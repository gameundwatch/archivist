# design — 設計を1枚起こす

<!-- 要件を満たす中身を、L2_designs に材料と規則として書く -->

## Background

要件だけでは実装できない。何が要るか、どのファイルに宿るか、どんな制約が
かかるかが書かれないと、実装者が毎回同じことを考え直す。

## Availability

- 仕様を指定して起動すると、それを満たす設計が1枚起きる
- 各要件に対して何が必要かが表で読める
- 影響するファイルが材料として列挙される
- 実装のための規則が、由来となる決断とともに並ぶ
- 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる
## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)


## References

### Specs

- [design](../L2_specs/design.md)

### Designs

- [design](../L2_designs/design.md)
