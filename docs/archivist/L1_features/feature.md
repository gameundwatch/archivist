# feature — 機能を1枚起こす

<!-- 利用者が名指しできる単位を、L1_features に書く -->

## Background

利用者が名指しできるものが何かは、仕様や設計から出てこない。製品が外に
何を晒すかは条項が定めるもので、書かれないと名指しできるのに約束が無い機能が残る。

## Availability

- **A1** 条項を指定して起動すると、その条項が定めた機能が1枚起きる

- **A2** 何ができるかが箇条書きで読め、各項目に `A` 番号が付く

- **A3** なぜ必要とされたかが背景として残る

- **A4** 仕様と設計が availability ごとの表で突き合わされ、空欄が不備として見える

- **A5** 機能の分解は条項から来る。仕様と設計の要約ではない

- **A6** 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる

### Coverage

| availability | spec | design |
| --- | --- | --- |
| A1 | R1 | T1, T2 |
| A2 | R3 | T2 |
| A3 | R3 | T2 |
| A4 | R4 | T1, T2 |
| A5 | R1, R2 | T1 |
| A6 | R5 | T1 |

## Articles
- [spec と design の整合を担保するのは feature だけ](../L4_articles/feature-joins-spec-and-design.md)
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_articles/output-language-follows-project.md)
- [配布物は英語で書く](../L4_articles/distributed-content-in-english.md)
- [機能が何かは条項であり、下層の要約ではない](../L4_articles/features-come-from-articles.md)
- [スキルは文書の要素ごとに割る](../L4_articles/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_articles/command-is-feature.md)
- [参照はファイル単位で張る](../L4_articles/references-are-file-scoped.md)

## References

### Specs

- [feature](../L2_specs/feature.md)

### Designs

- [feature](../L2_designs/feature.md)
