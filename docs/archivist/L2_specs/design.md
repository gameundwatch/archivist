# design — 設計を起こす要件

## Requirements

<a id="R1"></a>

### R1 材料の各行はアンカーで指せる

- Parts の各行は `T1`, `T2`, ... の番号を持ち、その位置に `<a id>` が在る
- 上の feature がこの錨で材料を指す

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

### R4 spec を引かない

- 生成した design は L2_specs のいかなる文書もアンカーも参照しない
- spec の側からも引かれない。両者は対等な並列で、互いを待たずに書ける
- 整合を担保するのは上の feature であり、この層ではない

<a id="R5"></a>

### R5 散文は対象プロジェクトの言語で書く

- 既存の文書が無いときは、決断が書かれている言語に合わせる
- 見出し、アンカー、フィールド名は言語に依らず英語で固定する

<a id="R6"></a>

### R6 検証はそれだけで test が書ける詳しさで書く

- 各材料に対し、それが design の通りに作られているかを判定する項目を持つ
- 判定は成果物の全体を動かさず、パーツ単位に働く
- 手段はテストコードのファイルパスを取る
- spec を引かない。約束が満たされているかは debug の担当であり、この層は見ない

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | [材料の錨](#V1) | [R1](#R1) |
| 2 | [材料の実在](#V2) | [R2](#R2) |
| 3 | [規則の由来](#V3) | [R3](#R3) |
| 4 | [参照の向き](#V4) | [R4](#R4) |
| 5 | [言語の追随](#V5) | [R5](#R5) |
| 6 | [test の実装可能性](#V6) | [R6](#R6) |

<a id="V1"></a>

### V1 材料の錨

- Means: checklist
- Parts の各行が `T` 番号を持ち、同じ id の `<a id>` が在ることを見る
- 上の feature からその錨を指すリンクが解決することを見る

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

### V4 spec 非参照

- Means: checklist
- 生成された design に `../L2_specs/` を含むリンクが一つも無いことを見る
- 対応する spec にも design への参照が無いことを見る

<a id="V5"></a>

### V5 言語の追随

- Means: checklist
- 既存の文書が日本語のプロジェクトで起動し、生成物の散文が日本語であることを見る
- 同じ生成物の見出しとフィールド名が英語のままであることを見る

<a id="V6"></a>

### V6 test の実装可能性

- Means: checklist
- 生成された各 V について、design 以外を読まずにテストコードが書けることを見る
- 全ての材料が、いずれかの V から指されていることを見る

## Decisions
- [test は design を読んで書く](../L4_decisions/test-from-design.md)
- [spec と design は互いを引かない](../L4_decisions/spec-design-independent.md)
- [検証は自分の手段を宣言する](../L4_decisions/verification-declares-its-means.md)
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
- [test](../L3_terms/test.md)
- [spec](../L3_terms/spec.md)
