# design — 設計を起こす要件

## Requirements

<a id="R1"></a>

### R1 各要件に対して何が必要かを示す

- 要件はアンカーで指す
- 要件そのものの言い換えにしない

<a id="R2"></a>

### R2 影響するファイルを材料として挙げる

- 実装対象のファイルと、その入出力を持つ
- ファイルとして数えるのは `target_file` 列だけ。`IN` と `OUT` は流れの説明で、
  生成物や雛形の穴を書いてよく、実在を問わない
- これは実装の対応であり、参照の順序には数えない

<a id="R3"></a>

### R3 規則は由来となる決断を持つ

- 決断から導けない規則を書かない

<a id="R4"></a>

### R4 仕様を参照する。仕様は設計を参照しない

- 向きは design から spec への一方向

<a id="R5"></a>

### R5 散文は対象プロジェクトの言語で書く

- 既存の文書が無いときは、決断が書かれている言語に合わせる
- 見出し、アンカー、フィールド名は言語に依らず英語で固定する

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | [要件との対応](#V1) | [R1](#R1) |
| 2 | [材料の実在](#V2) | [R2](#R2) |
| 3 | [規則の由来](#V3) | [R3](#R3) |
| 4 | [参照の向き](#V4) | [R4](#R4) |
| 5 | [言語の追随](#V5) | [R5](#R5) |

<a id="V1"></a>

### V1 要件との対応

- Means: checklist
- 各要件に対応する行が在り、要件の写しでないことを見る

<a id="V2"></a>

### V2 材料の実在

- Means: checklist
- 印が外れた文書で、`target_file` 列のファイルが実在することを見る
- `IN` と `OUT` にパスの形をした生成物を書いた設計を置き、実在を問われないことを見る

<a id="V3"></a>

### V3 規則の由来

- Means: checklist
- 各規則が決断を指しており、その決断が実在することを見る

<a id="V4"></a>

### V4 参照の向き

- Means: checklist
- 対応する仕様に設計への参照が無いことを見る

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
- [reference](../L3_terms/reference.md)
- [layer](../L3_terms/layer.md)
