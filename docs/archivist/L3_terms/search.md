# search — 検索

盤面から語を引き、その語を持つ文書に辿り着く手段。表題・ファイル名・パス・本文の
すべてが対象になる。

- Aliases: 全文検索, 検索バー
- Details: 参照グラフが示さないものを補う。位置と参照は文書どうしの関係を示すが、
  語の在り処は示さない。
  分かち書きに依存しない実装を使う。日本語では語が空白で割れないため。
  結果から開いたものは紙になり、木の根になる。別の閲覧面を作らない。
  実装は外から取り込む。取得できなければ検索は現れない。

## Terms
- [whiteboard](../L3_terms/whiteboard.md)
- [paper](../L3_terms/paper.md)
- [tree](../L3_terms/tree.md)

## Articles
- [検索は本文まで届く](../L4_articles/whiteboard-search-reaches-the-body.md)
- [できあいの実装は生成時に取り込む](../L4_articles/whiteboard-outside-implementations.md)
