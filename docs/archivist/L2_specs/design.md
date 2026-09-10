# design — 設計を起こす要件

## Requirements

### R1 材料の各行は番号を持つ

- Parts の各行は `T1`, `T2`, ... の番号を持ち、文書の中で重複させない
- 番号は文書の中で材料を数えるためのもので、上の feature はこの文書をファイルとして指す

### R2 影響するファイルを材料として挙げる

- 実装対象のファイルと、その入出力を持つ
- ファイルとして数えるのは `target_file` 列だけ。`IN` と `OUT` は流れの説明で、
  生成物や雛形の穴を書いてよく、実在を問わない
- これは実装の対応であり、参照の順序には数えない

### R3 規則は由来となる条項を持つ

- 条項から導けない規則を書かない

### R4 spec を引かない

- 生成した design は L2_specs のいかなる文書も参照しない
- spec の側からも引かれない。両者は対等な並列で、互いを待たずに書ける
- 整合を担保するのは上の feature であり、この層ではない

### R5 散文は対象プロジェクトの言語で書く

- 既存の文書が無いときは、条項が書かれている言語に合わせる
- 見出しとフィールド名は言語に依らず英語で固定する

### R6 検証はそれだけで test が書ける詳しさで書く

- 各材料に対し、それが design の通りに作られているかを判定する項目を持つ
- 判定は成果物の全体を動かさず、パーツ単位に働く
- 手段はテストコードのファイルパスを取る
- spec を引かない。約束が満たされているかは debug の担当であり、この層は見ない

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | V1 材料の番号 | R1 |
| 2 | V2 材料の実在 | R2 |
| 3 | V3 規則の由来 | R3 |
| 4 | V4 参照の向き | R4 |
| 5 | V5 言語の追随 | R5 |
| 6 | V6 test の実装可能性 | R6 |

### V1 材料の番号

- Means: checklist
- Parts の各行が `T1` から連番で振られ、番号が重複しないことを見る

### V2 材料の実在

- Means: checklist
- 印が外れた文書で、`target_file` 列のファイルが実在することを見る
- `IN` と `OUT` にパスの形をした生成物を書いた設計を置き、実在を問われないことを見る

### V3 規則の由来

- Means: checklist
- 各規則が条項を指しており、その条項が実在することを見る

### V4 spec 非参照

- Means: checklist
- 生成された design に `../L2_specs/` を含むリンクが一つも無いことを見る
- 対応する spec にも design への参照が無いことを見る

### V5 言語の追随

- Means: checklist
- 既存の文書が日本語のプロジェクトで起動し、生成物の散文が日本語であることを見る
- 同じ生成物の見出しとフィールド名が英語のままであることを見る

### V6 test の実装可能性

- Means: checklist
- 生成された各 V について、design 以外を読まずにテストコードが書けることを見る
- 全ての材料が、いずれかの V から指されていることを見る

## Articles
- [test は design を読んで書く](../L4_articles/test-from-design.md)
- [spec と design は互いを引かない](../L4_articles/spec-design-independent.md)
- [検証は自分の手段を宣言する](../L4_articles/verification-declares-its-means.md)
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_articles/output-language-follows-project.md)
- [配布物は英語で書く](../L4_articles/distributed-content-in-english.md)
- [層は飛ばさない。articles だけが例外](../L4_articles/no-layer-skip.md)
- [参照はファイル単位で張る](../L4_articles/references-are-file-scoped.md)

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
