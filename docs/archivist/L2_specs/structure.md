# structure — 構造を起こす要件

## Requirements

<a id="R1"></a>

### R1 決断が課した形だけを図にする

- 個数、順序、状態遷移、包含などの制約を対象とする
- 決断が課していない形は描かない

<a id="R2"></a>

### R2 図に使う語は L3_terms にあるものに限る

- 台帳に無い語で描かない
- 必要な語が無いときは書かずに止まる

<a id="R3"></a>

### R3 design を捨てても残る形だけを置く

- ある design 固有の処理フローは対象にしない
- プロジェクト成果物の全体を見渡す図は対象に含む

<a id="R4"></a>

### R4 図ごとにアンカーを持つ

- 上の層から図単位で指せること

<a id="R5"></a>

### R5 散文は対象プロジェクトの言語で書く

- 既存の文書が無いときは、決断が書かれている言語に合わせる
- 見出し、アンカー、フィールド名は言語に依らず英語で固定する

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | [形の限定](#V1) | [R1](#R1) |
| 2 | [語の在処](#V2) | [R2](#R2) |
| 3 | [寿命の判定](#V3) | [R3](#R3) |
| 4 | [図の指し先](#V4) | [R4](#R4) |
| 5 | [言語の追随](#V5) | [R5](#R5) |

<a id="V1"></a>

### V1 形の限定

- Means: checklist
- 形を課さない決断を与え、図が起きないことを見る

<a id="V2"></a>

### V2 語の在処

- Means: checklist
- 図中の全ての語について、L3_terms に対応するファイルが在ることを見る

<a id="V3"></a>

### V3 寿命の判定

- Means: checklist
- 生成された図が、特定の design を消しても意味を保つことを見る

<a id="V4"></a>

### V4 図の指し先

- Means: checklist
- 各図の直前にアンカーが在り、上層から図単位で指せることを見る

<a id="V5"></a>

### V5 言語の追随

- Means: checklist
- 既存の文書が日本語のプロジェクトで起動し、生成物の散文が日本語であることを見る
- 同じ生成物の見出しとフィールド名が英語のままであることを見る

## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [層は飛ばさない。decisions だけが例外](../L4_decisions/no-layer-skip.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [form](../L3_terms/form.md)
- [layer](../L3_terms/layer.md)
- [reference](../L3_terms/reference.md)
