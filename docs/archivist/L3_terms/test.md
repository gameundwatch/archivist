# test — 部品検証

design が定めた材料が、その通りに作られているかを確かめるもの。design の V が
実現された姿。

- Aliases: テスト, 単体テスト
- Details: 実装における**手法 (How)** の検証にあたる。ヘルパやサービス関数、変数と
  いったパーツ単位に働き、成果物の全体を動かさない。
- Details: 判定の根拠は design にしかない。spec は内部に触れないので、test の
  宛先にならない。実現形はテストコードで、`Means:` はそのパスを取る。
- Details: design の改訂で壊れてよい。壊れることが、設計が変わった事実の表出に
  なる。約束が変わっていないことは [debug](debug.md) が別に守る。
- Details: 実装内容の細部に口を出すものは test ではなく lint にあたり、そちらも
  design の側に属する。

## Terms
- [design](design.md)
- [debug](debug.md)

## Articles
- [test は design を読んで書く](../L4_articles/test-from-design.md)
- [検証は自分の手段を宣言する](../L4_articles/verification-declares-its-means.md)
