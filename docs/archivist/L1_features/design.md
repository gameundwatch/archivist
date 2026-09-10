# design — 設計を1枚起こす

<!-- 条項が要求する中身を、L2_designs に材料と規則と検証として書く -->

## Background

何をどのファイルに宿し、どんな制約をかけるかが書かれないと、実装者が毎回
同じことを考え直す。仕様は約束だけを述べ、中身には触れない。両者は互いを
待たずに書かれ、突き合わされるのは feature の対応表になる。

## Availability

- **A1** 条項を指定して起動すると、それを解く設計が1枚起きる

- **A2** 影響するファイルが材料として列挙され、各行に `T` 番号が付く

- **A3** 実装のための規則が、由来となる条項とともに並ぶ

- **A4** 検証は、それだけを読んで test が書ける詳しさで書かれる

- **A5** 仕様を引かない。仕様とは互いを待たずに書ける

- **A6** 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる

### Coverage

| availability | spec | design |
| --- | --- | --- |
| A1 | R2 | T1, T2, T3 |
| A2 | R1, R2 | T2 |
| A3 | R3 | T1, T2 |
| A4 | R6 | T1, T2 |
| A5 | R4 | T1 |
| A6 | R5 | T1 |

## Articles
- [test は design を読んで書く](../L4_articles/test-from-design.md)
- [spec と design は互いを引かない](../L4_articles/spec-design-independent.md)
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_articles/output-language-follows-project.md)
- [配布物は英語で書く](../L4_articles/distributed-content-in-english.md)
- [スキルは文書の要素ごとに割る](../L4_articles/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_articles/command-is-feature.md)
- [参照はファイル単位で張る](../L4_articles/references-are-file-scoped.md)

## References

### Specs

- [design](../L2_specs/design.md)

### Designs

- [design](../L2_designs/design.md)
