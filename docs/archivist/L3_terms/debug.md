# debug — 実行検証

成果物を実環境で実際に動かし、その内容が約束通りかを判定するもの。spec の V が
実現された姿。

- Aliases: デバッグ, 実行検証, acceptance
- Details: 実装における**内容 (What)** の検証にあたる。判定の根拠は spec にしか
  無く、design を読まずに書ける。
- Details: 実現形は問わない。人が上から通すチェックリストも、自動で走る E2E や
  受け入れテストも debug に属する。どちらであるかは V が `Means:` の行で宣言する。
- Details: design の改訂では壊れない。壊れたなら、約束そのものが変わっている。
- Details: V がそれだけで debug を書ける詳しさに達していないなら、判定の内容が
  足りていない。

## Terms
- [spec](spec.md)

## Articles
- [debug は spec だけを読んで書ける](../L4_articles/debug-from-spec-alone.md)
- [検証は自分の手段を宣言する](../L4_articles/verification-declares-its-means.md)
