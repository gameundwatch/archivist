# mark — 印

ファイル名の先頭に付く `_`。その文書がまだ実装に届いていないことを示す。

- Aliases: 印, アンダースコア
- Details: 文書に持たせてよい唯一の時間的な要素になる。付くのは実現先を持つ層に限られ、
  feature / spec / design が対象。structure と terms と decisions には付かない。
  `ls` に現れるので、どこまでが現物でどこからが予定かが一覧で読める。

## Decisions
- [印が付くのは実現先を持つ層だけ](../L4_decisions/mark-only-where-realized.md)
- [時間的な要素を文書に持たせない](../L4_decisions/no-time-factor.md)
