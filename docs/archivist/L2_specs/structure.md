# structure — 構造を起こす要件

## Requirements

### R1 決断が課した形だけを図にする

- 個数、順序、状態遷移、包含などの制約を対象とする
- 決断が課していない形は描かない

### R2 図に使う語は L3_terms にあるものに限る

- 台帳に無い語で描かない
- 必要な語が無いときは書かずに止まる

### R3 design を捨てても残る形だけを置く

- ある design 固有の処理フローは対象にしない
- プロジェクト成果物の全体を見渡す図は対象に含む

### R4 図ごとに番号を持つ

- D1 から順に番号を振り、文書の中で重複させない
- 番号は文書の中で図を数えるためのもので、上の層はこの文書をファイルとして指す

### R5 散文は対象プロジェクトの言語で書く

- 既存の文書が無いときは、決断が書かれている言語に合わせる
- 見出しとフィールド名は言語に依らず英語で固定する

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | V1 形の限定 | R1 |
| 2 | V2 語の在処 | R2 |
| 3 | V3 寿命の判定 | R3 |
| 4 | V4 図の番号 | R4 |
| 5 | V5 言語の追随 | R5 |

### V1 形の限定

- Means: checklist
- 形を課さない決断を与え、図が起きないことを見る

### V2 語の在処

- Means: checklist
- 図中の全ての語について、L3_terms に対応するファイルが在ることを見る

### V3 寿命の判定

- Means: checklist
- 生成された図が、特定の design を消しても意味を保つことを見る

### V4 図の番号

- Means: checklist
- 各図が D1 から連番で振られ、番号が重複しないことを見る

### V5 言語の追随

- Means: checklist
- 既存の文書が日本語のプロジェクトで起動し、生成物の散文が日本語であることを見る
- 同じ生成物の見出しとフィールド名が英語のままであることを見る

## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [層は飛ばさない。decisions だけが例外](../L4_decisions/no-layer-skip.md)
- [参照はファイル単位で張る](../L4_decisions/references-are-file-scoped.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [form](../L3_terms/form.md)
- [layer](../L3_terms/layer.md)
- [reference](../L3_terms/reference.md)
