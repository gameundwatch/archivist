# check — 検査の設計

## Parts

| No | target_name | target_file | IN | OUT |
| -- | ----------- | ----------- | -- | --- |
| <a id="T1"></a>T1 | check | skills/archivist-check/SKILL.md | 決断, docs/archivist/ | 判定の報告 |
| <a id="T2"></a>T2 | docs | docs/archivist/ | 全文書 | 走査の対象 |

### Relation

```mermaid
flowchart LR
    TP["template"] -.書式.-> S["check"]
    IN["docs/archivist/"] --> S --> OUT["判定の報告"]
```

## Rules
- 書き込みを一切行わない
- 報告は promote がそのまま食える形で出す

## Verify

| No | VERIFY_NAME | TARGET |
| -- | ----------- | ------ |
| 1 | [無変更](#V1) | [T1](#T1) |
| 2 | [報告の形](#V2) | [T2](#T2) |

<a id="V1"></a>

### V1 無変更

- Means: checklist
- `SKILL.md` が書き込みを行わないと明記していることを見る
- 判定の一覧に、書き換えを伴う項目が無いことを見る

<a id="V2"></a>

### V2 報告の形

- Means: checklist
- 報告が promote の入力の形であると `SKILL.md` に書かれていることを見る


## Decisions
- [debug は spec だけを読んで書ける](../L4_decisions/debug-from-spec-alone.md)
- [test は design を読んで書く](../L4_decisions/test-from-design.md)
- [spec と design の整合を担保するのは feature だけ](../L4_decisions/feature-joins-spec-and-design.md)
- [印が付くのは実現先を持つ層だけ](../L4_decisions/mark-only-where-realized.md)
- [検証は自分の手段を宣言する](../L4_decisions/verification-declares-its-means.md)
- [`_` を外す作業は check から分ける](../L4_decisions/promote-separate-from-check.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [reference](../L3_terms/reference.md)
- [layer](../L3_terms/layer.md)
