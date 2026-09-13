# archivist — 還元の要件

## Requirements

### R1 条項の集合を起点にする

- 起点は L4_articles に置かれた文書。単体でも、全件でも、任意の部分集合でもよい
- 実装コードは事実として読むだけで、起点にしない
- L4 に文書が無い話題は扱わない

### R2 下から上へ、層を飛ばさずに進む

- 起動順は term → structure → spec → design → feature
- 生成した文書の参照は直下の層にだけ張る。articles は例外として直接指せる
- どこで止まるかは条項の中身が決める。上まで届かない条項は途中で止まる

### R3 出力は決まったことであり、案ではない

- 起点の条項から導けることだけを書く
- 導けないものが必要になったとき、archivist は書かずに止まる

### R4 条項群から再構成する

- 既にある文書が足りていても、指すだけで済ませない
- 条項と食い違う記述は書き直す

### R5 還元の跡を辿れる

- 生成した各文書は Articles 節を持ち、起点の条項を指す
- どの条項からも指されない記述を残さない

### R6 条項が一枚も無いときは取り込みを案内する

- `L4_articles/` が空のとき、何も書かずに取り込みのスキルを案内して止まる
- 案内するだけで、呼ばない
- 空でないときは案内しない

### R7 組み直しの後に索引、続けて盤面を更新する

- 文書を書き終えた後に索引を1回だけ組み直す
- 索引の後に盤面を1回だけ組み直す。これが起動順の最終段になる
- 索引が無い状態でも、組み直し自体は成立する
- 索引の中身を読んで還元の判断を変えない

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | V1 起点の限定 | R1 |
| 2 | V2 参照の段差 | R2 |
| 3 | V3 停止の報告 | R3 |
| 4 | V4 再構成 | R4 |
| 5 | V5 跡の到達 | R5 |
| 6 | V6 空の入力 | R6 |
| 7 | V7 索引の追随 | R7 |

### V1 起点の限定

- Means: checklist
- L4_articles に無い話題を与えて起動し、何も生成されないことを見る

### V2 参照の段差

- Means: checklist
- 生成された全文書のリンクを集め、行き先の層が自分の直下か L4_articles のいずれかであることを見る

### V3 停止の報告

- Means: checklist
- 条項から導けない箇所が必要になる条項を与え、その箇所を書かずに、
  何が足りないかを述べて止まることを見る

### V4 再構成

- Means: checklist
- 条項と食い違う文書を置いた状態で起動し、その文書が書き直されることを見る

### V5 跡の到達

- Means: checklist
- 生成された全文書の Articles 節を辿り、起点の条項に到達することを見る

### V6 空の入力

- Means: checklist
- `L4_articles/` を空にして起動し、取り込みが案内され、勝手に起動しないことを見る

### V7 索引の追随

- Means: checklist
- 文書を1枚書き直して起動し、索引がその内容に追随していることを見る
- 索引を削除した状態で起動し、組み直しが最後まで進むことを見る
- 盤面が索引の後に組み直され、新しい文書を含んでいることを見る

## Articles
- [ホワイトボードは還元の最後に、索引の後で組み直す](../L4_articles/whiteboard-follows-index.md)
- [生成される索引は層に属さない](../L4_articles/index-outside-layers.md)
- [還元はするが、条項は立てない](../L4_articles/reduction-not-article.md)
- [層は飛ばさない。articles だけが例外](../L4_articles/no-layer-skip.md)
- [条項の取り込みは archivist の外に置く](../L4_articles/adoption-outside-archivist.md)

## References

### Specs

- [term](term.md)
- [structure](structure.md)
- [spec](spec.md)
- [design](design.md)
- [feature](feature.md)
- [check](check.md)
- [adopt](adopt.md)
- [index](index.md)
- [whiteboard](whiteboard.md)

### Structures

- [document-layers](../L3_structures/document-layers.md)

### Terms

- [reduction](../L3_terms/reduction.md)
- [article](../L3_terms/article.md)
- [layer](../L3_terms/layer.md)
- [adoption](../L3_terms/adoption.md)
