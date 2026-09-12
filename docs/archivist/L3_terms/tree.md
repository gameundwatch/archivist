# tree — 木

開いている文書を根として、その参照を辿れる形に並べたもの。盤面の外に置かれる。

- Aliases: 参照の木, サイドバー
- Details: 指している先と指されている元の両方を持つ。
  根は開いている紙で決まる。ポインタでは変わらない。
  同じ文書が枝の中で再び現れたら、そこで枝が止まる。参照は循環しうるもので、
  木は循環を表現できない。
  盤面の上に重なるが、面を持たない。行以外のところは盤面として振る舞う。

## Terms
- [whiteboard](../L3_terms/whiteboard.md)
- [paper](../L3_terms/paper.md)
- [reference](../L3_terms/reference.md)

## Articles
- [開いている文書の周りは木として出す](../L4_articles/whiteboard-open-document-shows-its-tree.md)
