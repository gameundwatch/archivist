# adopt — 外にある決断を L4 に取り込む

<!-- 決断記述の並ぶディレクトリを読み、突き合わせて、採ったものを置く -->

## Background

archivist は `L4_decisions/` に置かれたものしか読まない。既に動いている
プロジェクトでは、決断が ADR や別ツールの出力として外に散らばっており、
入口が無いまま archivist を起動しても書けるものが無い。

写すだけなら手で足りる。手に負えないのは、既にある決断と同じことを
言っていないか、矛盾していないかを一枚ずつ確かめるところになる。

## Availability

- 決断記述が並ぶディレクトリを指定して起動すると、候補が一枚ずつ提示される
- 提示には、既存の決断のうち同義のもの・矛盾するものが添う
- 採ると答えたものだけが、決断の書式に整えて `L4_decisions/` に置かれる
- 答えなければ何も置かれない。既にある決断は上書きされない
- `L4_decisions/` が空のまま archivist を起動すると、このコマンドが案内される

## Decisions
- [決断の取り込みは archivist の外に置く](../L4_decisions/adoption-outside-archivist.md)
- [取り込むかどうかは人が答える](../L4_decisions/adoption-needs-consent.md)
- [取り込みの入力は決断記述が並ぶディレクトリ](../L4_decisions/adoption-input-is-a-directory.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)

## References

### Specs

- [adopt](../L2_specs/adopt.md)

### Designs

- [adopt](../L2_designs/adopt.md)
