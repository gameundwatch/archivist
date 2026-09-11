# check — 揃っているかを判定する

<!-- docs/archivist/ を読み、文書群が出荷の条件を満たすか答える -->

## Background

層と参照の規則は文書に書かれているが、守られているかを見る手が無い。
リンク切れ、層飛び、循環、実現先の欠落は、目で追う限り必ず漏れる。

## Availability

- **A1** 条項と docs/archivist/ 全体を読み、判定が返る

- **A2** リンクが解決するか、層を飛んでいないか、循環していないかが分かる

- **A3** 実現先が揃っていない文書が報告される

- **A4** 何も書き換えない

- **A5** 検証が自分の層だけを読んで実装できるかが分かる

- **A6** 仕様と設計の対応表の欠落が、どちらの側の不備かとともに分かる

- **A7** 形が英語で保たれているか、図が実態と合っているかが分かる

### Coverage

| availability | spec | design |
| --- | --- | --- |
| A1 | R1 | T1, T2 |
| A2 | R1, R2, R3 | T1 |
| A3 | R4, R8 | T1 |
| A4 | R5 | T1 |
| A5 | R6, R7 | T1 |
| A6 | R11 | T1, T2 |
| A7 | R9, R10 | T1, T2 |

## Articles
- [debug は spec だけを読んで書ける](../L4_articles/debug-from-spec-alone.md)
- [test は design を読んで書く](../L4_articles/test-from-design.md)
- [spec と design の整合を担保するのは feature だけ](../L4_articles/feature-joins-spec-and-design.md)
- [印を置かず、実現先の実在は判定で読む](../L4_articles/no-mark-on-documents.md)
- [検証は自分の手段を宣言する](../L4_articles/verification-declares-its-means.md)
- [スキルは文書の要素ごとに割る](../L4_articles/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_articles/command-is-feature.md)

## References

### Specs

- [check](../L2_specs/check.md)

### Designs

- [check](../L2_designs/check.md)
