# structure — 構造を1枚起こす

<!-- 決断が課した形を、L3_structures に図として書く -->

## Background

決断は形を課す。個数、順序、状態遷移、包含。図にしないと、同じ制約が
複数の設計にばらばらに書き写される。

## Availability

- **A1** 決断を指定して起動すると、その決断が課した形が図として1枚起きる

- **A2** 図は複数枚置け、それぞれに `D` 番号が付く

- **A3** 図に使う語は L3_terms にあるものに限られる

- **A4** design を捨てても残る形だけが置かれる

- **A5** 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる

### Coverage

| availability | spec | design |
| --- | --- | --- |
| A1 | R1 | T1, T2 |
| A2 | R4 | T2 |
| A3 | R2 | T1, T3 |
| A4 | R3 | T1 |
| A5 | R5 | T1 |

## Articles
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_articles/output-language-follows-project.md)
- [配布物は英語で書く](../L4_articles/distributed-content-in-english.md)
- [スキルは文書の要素ごとに割る](../L4_articles/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_articles/command-is-feature.md)
- [参照はファイル単位で張る](../L4_articles/references-are-file-scoped.md)

## References

### Specs

- [structure](../L2_specs/structure.md)

### Designs

- [structure](../L2_designs/structure.md)
