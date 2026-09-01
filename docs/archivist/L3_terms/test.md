# test — 検証

仕様が満たされているかを確かめるもの。spec の V が実現された姿。

- Aliases: テスト, 検証
- Details: 実現形は二つある。自動で走るテストコードと、人が上から通すチェックリスト。どちらであるかは V が `手段:` の行で宣言する。
- Details: spec だけを読んで書ける。design を読む必要は無い。実装内容の細部に
  口を出すものは test ではなく lint にあたり、そちらは design の側に属する。
  V がそれだけでテストを書ける詳しさに達していないなら、判定の内容が足りていない。

## Decisions
- [検証は自分の手段を宣言する](../L4_decisions/verification-declares-its-means.md)
- [テストコードは spec だけを読んで書ける](../L4_decisions/test-from-spec-alone.md)
