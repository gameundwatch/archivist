# adopt — 取り込みの要件

## Requirements

<a id="R1"></a>

### R1 入力は決断記述が並ぶディレクトリ一つ

- 引数はディレクトリのパス一つ。既定値を持たず、省略されたら問う
- そこに並ぶファイルが一枚一文の決断記述であることだけを前提にする
- 特定のツールの出力形式を条件にしない。満たさないファイルは飛ばして報告する

<a id="R2"></a>

### R2 既存の決断と突き合わせる

- 候補ごとに、`L4_decisions/` の中で同じことを言う一枚を探して示す
- 矛盾する一枚があれば、矛盾する箇所を示す
- 対応が無いものは新規として示す

<a id="R3"></a>

### R3 採否は人が答える

- 候補を一枚ずつ提示し、答えを待つ
- 答えの無いまま書き込まない
- 件数が多くても一括の採択に切り替えない

<a id="R4"></a>

### R4 採ったものだけを `L4_decisions/` に整形して置く

- 決断の書式に整えて置く。原文をそのまま写さない
- 人が書いた既存の決断を上書きしない。名前が衝突したら報告して止まる

<a id="R5"></a>

### R5 決断を下さない

- 候補に無いことを書き足さない
- 上層の文書を一枚も書かない

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | [入力の限定](#V1) | [R1](#R1) |
| 2 | [突き合わせの提示](#V2) | [R2](#R2) |
| 3 | [無回答では書かない](#V3) | [R3](#R3) |
| 4 | [衝突で止まる](#V4) | [R4](#R4) |
| 5 | [範囲の限定](#V5) | [R4](#R4), [R5](#R5) |

<a id="V1"></a>

### V1 入力の限定

- Means: checklist
- 引数なしで起動し、ディレクトリを問われることを見る
- 決断記述でないファイルを混ぜ、飛ばされた旨が報告に出ることを見る

<a id="V2"></a>

### V2 突き合わせの提示

- Means: checklist
- 既存と同じことを言う候補を与え、その一枚が示されることを見る

<a id="V3"></a>

### V3 無回答では書かない

- Means: checklist
- 提示に答えずに終えたとき、`L4_decisions/` が増えていないことを見る

<a id="V4"></a>

### V4 衝突で止まる

- Means: checklist
- 既存と同じファイル名になる候補を採り、上書きされず報告が出ることを見る

<a id="V5"></a>

### V5 範囲の限定

- Means: checklist
- 実行後に増えた文書が `L4_decisions/` の中だけであることを見る

## Decisions
- [決断の取り込みは archivist の外に置く](../L4_decisions/adoption-outside-archivist.md)
- [取り込むかどうかは人が答える](../L4_decisions/adoption-needs-consent.md)
- [取り込みの入力は決断記述が並ぶディレクトリ](../L4_decisions/adoption-input-is-a-directory.md)
- [還元はするが、決断はしない](../L4_decisions/reduction-not-decision.md)

## References

### Structures

- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [adoption](../L3_terms/adoption.md)
- [decision](../L3_terms/decision.md)
