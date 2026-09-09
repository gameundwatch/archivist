# structure — 構造を起こす設計

## Parts

| No | target_name | target_file | IN | OUT |
| -- | ----------- | ----------- | -- | --- |
| <a id="T1"></a>T1 | structure | skills/archivist-structure/SKILL.md | 決断, 語 | L3_structures/STRUCTURE_NAME.md |
| <a id="T2"></a>T2 | template | skills/archivist-structure/TEMPLATE.md | - | 書式 |
| <a id="T3"></a>T3 | terms | docs/archivist/L3_terms/ | 既存の語 | 図に使える語の集合 |

### Relation

```mermaid
flowchart LR
    TP["template"] -.書式.-> S["structure"]
    IN["決断, 語"] --> S --> OUT["L3_structures/STRUCTURE_NAME.md"]
```

## Rules
- 台帳に無い語が要るときは書かずに止まる
- 1回の起動で1ファイルだけ書く

## Verify

| No | VERIFY_NAME | TARGET |
| -- | ----------- | ------ |
| 1 | [スキルの停止条件](#V1) | [T1](#T1) |
| 2 | [型紙の欄](#V2) | [T2](#T2) |
| 3 | [語の台帳](#V3) | [T3](#T3) |

<a id="V1"></a>

### V1 スキルの停止条件

- Means: checklist
- 台帳に無い語が要るときは書かずに止まる、と `SKILL.md` に書かれていることを見る

<a id="V2"></a>

### V2 型紙の欄

- Means: checklist
- `TEMPLATE.md` が図と、その図が何であるかを述べる散文の欄を対で持つことを見る

<a id="V3"></a>

### V3 語の台帳

- Means: checklist
- `docs/archivist/L3_terms/` が入力として `SKILL.md` に挙がっていることを見る


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

- [layer](../L3_terms/layer.md)
- [reference](../L3_terms/reference.md)
