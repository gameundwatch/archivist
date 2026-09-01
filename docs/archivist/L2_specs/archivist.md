# archivist — 還元の要件

## Requirements

<a id="R1"></a>

### R1 決断の集合を起点にする

- 起点は L4_decisions に置かれた文書。単体でも、全件でも、任意の部分集合でもよい
- 実装コードは事実として読むだけで、起点にしない
- L4 に文書が無い決断は扱わない

<a id="R2"></a>

### R2 下から上へ、層を飛ばさずに進む

- 起動順は term → structure → spec → design → feature
- 生成した文書の参照は直下の層にだけ張る。decisions は例外として直接指せる
- どこで止まるかは決断の中身が決める。上まで届かない決断は途中で止まる

<a id="R3"></a>

### R3 出力は決断であり、案ではない

- 起点の決断から導けることだけを書く
- 導けないものが必要になったとき、archivist は書かずに止まる

<a id="R4"></a>

### R4 決断群から再構成する

- 既にある文書が足りていても、指すだけで済ませない
- 決断と食い違う記述は書き直す

<a id="R5"></a>

### R5 還元の跡を辿れる

- 生成した各文書は Decisions 節を持ち、起点の決断を指す
- どの決断からも指されない記述を残さない

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | [起点の限定](#V1) | [R1](#R1) |
| 2 | [参照の段差](#V2) | [R2](#R2) |
| 3 | [停止の報告](#V3) | [R3](#R3) |
| 4 | [再構成](#V4) | [R4](#R4) |
| 5 | [跡の到達](#V5) | [R5](#R5) |

<a id="V1"></a>

### V1 起点の限定

- Means: checklist
- L4_decisions に無い話題を与えて起動し、何も生成されないことを見る

<a id="V2"></a>

### V2 参照の段差

- Means: checklist
- 生成された全文書のリンクを集め、行き先の層が自分の直下か L4_decisions のいずれかであることを見る

<a id="V3"></a>

### V3 停止の報告

- Means: checklist
- 決断から導けない箇所が必要になる決断を与え、その箇所を書かずに、
  何が足りないかを述べて止まることを見る

<a id="V4"></a>

### V4 再構成

- Means: checklist
- 決断と食い違う文書を置いた状態で起動し、その文書が書き直されることを見る

<a id="V5"></a>

### V5 跡の到達

- Means: checklist
- 生成された全文書の Decisions 節を辿り、起点の決断に到達することを見る

## Decisions
- [還元はするが、決断はしない](../L4_decisions/reduction-not-decision.md)
- [層は飛ばさない。decisions だけが例外](../L4_decisions/no-layer-skip.md)

## References

### Specs

- [term](term.md)
- [structure](structure.md)
- [spec](spec.md)
- [design](design.md)
- [feature](feature.md)
- [check](check.md)
- [promote](promote.md)

### Structures

- [document-layers](../L3_structures/document-layers.md)

### Terms

- [reduction](../L3_terms/reduction.md)
- [decision](../L3_terms/decision.md)
- [layer](../L3_terms/layer.md)
