# spec — 仕様

要件を満たす what。外から観測できる約束と、その検証。

- Aliases: 仕様, SPEC, contract
- Details: 内部の作りには触れない。それは design が担当する。約束は R として、
  その検証は V として持ち、V は spec だけを読んでテストが書ける詳しさで書く。
  design より動きにくく、design が spec を引く。

## Terms
- [test](test.md)

## Decisions
- [テストコードは spec だけを読んで書ける](../L4_decisions/test-from-spec-alone.md)
- [検証は自分の手段を宣言する](../L4_decisions/verification-declares-its-means.md)
