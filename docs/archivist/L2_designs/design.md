# design — 設計を起こす設計

## Needs

| spec | needs |
| ---- | ----- |
| [R1](../L2_specs/design.md#R1) | 要件ごとに何が必要かを書き出す手 |
| [R2](../L2_specs/design.md#R2) | 影響するファイルを列挙する手 |
| [R3](../L2_specs/design.md#R3) | 規則に由来の決断を付ける手 |
| [R4](../L2_specs/design.md#R4) | 仕様を参照として張る手 |
| [R5](../L2_specs/design.md#R5) | 既存の文書から言語を見分ける手 |
## Parts

| target_name | target_file | IN | OUT |
| ----------- | ----------- | -- | --- |
| design | skills/archivist-design/SKILL.md | 決断, L3, spec | L2_designs/DESIGN_NAME.md |
| template | skills/archivist-design/TEMPLATE.md | - | 書式 |
| specs | docs/archivist/L2_specs/ | 要件 | Needs 表の左列 |

### Relation

```mermaid
flowchart LR
    TP["template"] -.書式.-> S["design"]
    IN["決断, L3, spec"] --> S --> OUT["L2_designs/DESIGN_NAME.md"]
```

## Rules
- 仕様への参照は一方向。仕様側に設計を書き足さない
- 1回の起動で1ファイルだけ書く

## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [テンプレートはスキルの中に置く](../L4_decisions/template-belongs-to-skill.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [層は飛ばさない。decisions だけが例外](../L4_decisions/no-layer-skip.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [language-split](../L3_structures/language-split.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [reference](../L3_terms/reference.md)
- [layer](../L3_terms/layer.md)
