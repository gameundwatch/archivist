# adopt — 外にある条項を L4 に取り込む

<!-- 条項記述の並ぶディレクトリを読み、突き合わせて、採ったものを置く -->

## Background

archivist は `L4_articles/` に置かれたものしか読まない。既に動いている
プロジェクトでは、条項が ADR や別ツールの出力として外に散らばっており、
入口が無いまま archivist を起動しても書けるものが無い。

写すだけなら手で足りる。手に負えないのは、既にある条項と同じことを
言っていないか、矛盾していないかを一枚ずつ確かめるところになる。

## Availability

- **A1** 条項記述が並ぶディレクトリを指定して起動すると、候補が一枚ずつ提示される

- **A2** 提示には、既存の条項のうち同義のもの・矛盾するものが添う

- **A3** 採ると答えたものだけが、条項の書式に整えて `L4_articles/` に置かれる

- **A4** 答えなければ何も置かれない。既にある条項は上書きされない

- **A5** `L4_articles/` が空のまま archivist を起動すると、このコマンドが案内される

### Coverage

| availability | spec | design |
| --- | --- | --- |
| A1 | R1, R2 | T1 |
| A2 | R2 | T1 |
| A3 | R4 | T1, T2 |
| A4 | R3, R5 | T1 |
| A5 | R1 | T1 |

## Articles
- [条項の取り込みは archivist の外に置く](../L4_articles/adoption-outside-archivist.md)
- [取り込むかどうかは人が答える](../L4_articles/adoption-needs-consent.md)
- [取り込みの入力は条項記述が並ぶディレクトリ](../L4_articles/adoption-input-is-a-directory.md)
- [コマンド1本を feature 1枚とする](../L4_articles/command-is-feature.md)

## References

### Specs

- [adopt](../L2_specs/adopt.md)

### Designs

- [adopt](../L2_designs/adopt.md)
