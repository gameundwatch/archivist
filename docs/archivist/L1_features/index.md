# index — 参照の全体図を索引にする

<!-- docs/archivist/ を読み、文書1枚1行の索引を index.csv に組み直す -->

## Background

文書が増えると、どれがどれを指しているかはファイルを開いて回るまで分からない。
参照は相対パスで張られているので機械的に辿れるが、辿った結果を置く場所が無い。
どの文書からも指されないものや、指し先を失ったものは、目で追う限り必ず漏れる。

## Availability

- **A1** 起動すると `docs/archivist/index.csv` が組み直される

- **A2** 参照を持たない文書も索引に現れる

- **A3** ある文書が指す先が、その文書の1行で読める

- **A4** 索引を削除しても、文書群の判定は変わらない

- **A5** 索引には印が付かず、層の一覧にも現れない

- **A6** 索引の列は3つで、同じ行の他の列から導ける列を持たない

### Coverage

| availability | spec | design |
| --- | --- | --- |
| A1 | R3, R6 | T1, T2 |
| A2 | R1 | T1 |
| A3 | R2 | T2 |
| A4 | R5 | T1 |
| A5 | R4 | T2 |
| A6 | R7 | T2 |

## Articles
- [生成される索引は層に属さない](../L4_articles/index-outside-layers.md)
- [索引は点を1行とする](../L4_articles/index-rows-are-nodes.md)
- [索引の列は path と title と refs の3つとする](../L4_articles/index-columns-are-three.md)
- [スキルは文書の要素ごとに割る](../L4_articles/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_articles/command-is-feature.md)

## References

### Specs

- [index](../L2_specs/index.md)

### Designs

- [index](../L2_designs/index.md)
