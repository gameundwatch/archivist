# layout — 配置

ホワイトボード上でノードの座標を決める規則。文書1枚につき1つの座標を返す。

- Aliases: 盤面の配置, レイアウト
- Details: 複数を持ち、どれかを唯一の正解としない。既定は選ぶが、優劣は決めない。
  配置ごとに読めるものが違う。1つに絞ると、絞った時点で見えなくなる問いが出る。
  足すときは座標を返す規則を1つ増やすだけで済む。足すことが仕様変更にならない。
  座標は毎回導かれるもので、文書が持つ情報ではない。

## Terms
- [whiteboard](../L3_terms/whiteboard.md)

## Articles
- [盤面の配置に正解を1つ置かない](../L4_articles/whiteboard-layout-has-no-single-answer.md)
