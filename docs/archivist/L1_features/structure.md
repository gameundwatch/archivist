# structure — 構造を1枚起こす

<!-- 決断が課した形を、L3_structures に図として書く -->

## Background

決断は形を課す。個数、順序、状態遷移、包含。図にしないと、同じ制約が
複数の設計にばらばらに書き写される。

## Availability

- 決断を指定して起動すると、その決断が課した形が図として1枚起きる
- 図は複数枚置け、それぞれにアンカーが付く
- 図に使う語は L3_terms にあるものに限られる
- design を捨てても残る形だけが置かれる
- 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる
## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)


## References

### Specs

- [structure](../L2_specs/structure.md)

### Designs

- [structure](../L2_designs/structure.md)
