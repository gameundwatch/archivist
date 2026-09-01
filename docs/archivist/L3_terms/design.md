# design — 設計

要件に対する how。実装の中身。

- Aliases: 設計, DESIGN
- Details: 実装ファイルを名指しできる唯一の層になる。spec を引くが、spec からは
  引き返さない。code として実現され、test は design を読まずに書ける。

## Terms
- [spec](spec.md)

## Decisions
- [テストコードは spec だけを読んで書ける](../L4_decisions/test-from-spec-alone.md)
