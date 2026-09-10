# reference — 参照

文書から文書へ張る、読む順序の線。相対パスでファイルを指す。

- Aliases: 参照, リンク
- Details: 上の層のノードから直下の層のノードへ引く。同じノードの中でも引けるが、
  循環させない。どちらが元本かが決まらなくなるため。
  decisions だけは例外で、どの層からも直接指せる。
  指すのはファイルまでで、ファイルの中の位置は指さない。

## Articles
- [層は飛ばさない。decisions だけが例外](../L4_articles/no-layer-skip.md)
- [参照はファイル単位で張る](../L4_articles/references-are-file-scoped.md)
