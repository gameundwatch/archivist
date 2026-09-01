# reference — 参照

文書から文書へ張る、読む順序の線。名前付きアンカーで指す。

- Aliases: 参照, リンク
- Details: 上の層のノードから直下の層のノードへ引く。同じノードの中でも引けるが、
  循環させない。どちらが元本かが決まらなくなるため。
  decisions だけは例外で、どの層からも直接指せる。

## Decisions
- [層は飛ばさない。decisions だけが例外](../L4_decisions/no-layer-skip.md)
