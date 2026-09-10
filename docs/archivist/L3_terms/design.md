# design — 設計

要件に対する how。実装の中身。

- Aliases: 設計, DESIGN
- Details: 実装ファイルを名指しできる唯一の層になる。材料は Parts として持ち、
  各行は `T1`, `T2`, ... の番号を持ち、feature の表がその番号で指す。code として実現される。
- Details: 検証は V として持ち、V は design だけを読んで [test](test.md) が書ける
  詳しさで書く。
- Details: [spec](spec.md) を引かない。両者は対等な並列で、互いを待たずに書ける。
  整合は上の feature が担保する。

## Terms
- [test](test.md)
- [spec](spec.md)

## Articles
- [test は design を読んで書く](../L4_articles/test-from-design.md)
- [spec と design は互いを引かない](../L4_articles/spec-design-independent.md)
