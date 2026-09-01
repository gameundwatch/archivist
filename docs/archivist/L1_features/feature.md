# feature — 機能を1枚起こす

<!-- 利用者が名指しできる単位を、L1_features に書く -->

## Background

利用者が名指しできるものが何かは、仕様や設計から出てこない。製品が外に
何を晒すかの決断であり、書かれないと名指しできるのに約束が無い機能が残る。

## Availability

- 決断を指定して起動すると、その決断が定めた機能が1枚起きる
- 何ができるかが箇条書きで読める
- なぜ必要とされたかが背景として残る
- 仕様と設計への参照が張られる
- 機能の分解は決断から来る。仕様と設計の要約ではない
- 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる
## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [機能が何かは決断であり、下層の要約ではない](../L4_decisions/features-come-from-decisions.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)


## References

### Specs

- [feature](../L2_specs/feature.md)

### Designs

- [feature](../L2_designs/feature.md)
