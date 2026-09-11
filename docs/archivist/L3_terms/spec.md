# spec — 仕様

要件を満たす what。外から観測できる約束と、その検証。

- Aliases: 仕様, SPEC, contract
- Details: 内部の作りには触れない。それは design が担当する。約束は R として、
  その検証は V として持ち、V は spec だけを読んで debug が書ける
  詳しさで書く。
- Details: design を引かない。両者は対等な並列で、互いを待たずに
  書ける。整合は上の feature が担保する。

## Articles
- [debug は spec だけを読んで書ける](../L4_articles/debug-from-spec-alone.md)
- [spec と design は互いを引かない](../L4_articles/spec-design-independent.md)
- [検証は自分の手段を宣言する](../L4_articles/verification-declares-its-means.md)
