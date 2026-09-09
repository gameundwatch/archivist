# promote — 印を外す設計

## Parts

| No | target_name | target_file | IN | OUT |
| -- | ----------- | ----------- | -- | --- |
| <a id="T1"></a>T1 | promote | skills/archivist-promote/SKILL.md | check の報告 | リネームとリンクの書き換え |
| <a id="T2"></a>T2 | docs | docs/archivist/ | 全文書 | 流入リンクの走査対象 |

### Relation

```mermaid
flowchart LR
    TP["template"] -.書式.-> S["promote"]
    IN["check の報告"] --> S --> OUT["リネームとリンクの書き換え"]
```

## Rules
- 実現先の実在は自分で判定しない。報告に従う
- 索引を持たないため、走査で流入リンクを見つける

## Verify

| No | VERIFY_NAME | TARGET |
| -- | ----------- | ------ |
| 1 | [判定の委譲](#V1) | [T1](#T1) |
| 2 | [流入リンクの走査](#V2) | [T2](#T2) |

<a id="V1"></a>

### V1 判定の委譲

- Means: checklist
- 実現先の実在を自分で判定しないと `SKILL.md` に書かれていることを見る

<a id="V2"></a>

### V2 流入リンクの走査

- Means: checklist
- 索引を持たず走査で流入リンクを見つけると `SKILL.md` に書かれていることを見る


## Decisions
- [`_` を外す作業は check から分ける](../L4_decisions/promote-separate-from-check.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [reference](../L3_terms/reference.md)
