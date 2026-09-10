# spec — 仕様を起こす要件

## Requirements

### R1 外から観測できることだけを要件にする

- 内部の作りには触れない
- いつ動きいつ動かないかの発火条件と、対応するかしないかのスコープを含む

### R2 各要件に番号を振る

- R1 から順に番号を振り、文書の中で重複させない
- 番号は文書の中で要件を数えるためのもので、上層はこの文書をファイルとして指す

### R3 検証はそのままチェックリストとして通せる

- 一項目が一つの判定である
- 判定の手順と、満たしたと言える条件を持つ

### R4 要件と検証の対応が表で読める

- どの検証からも指されない要件が、表から見つかること

### R5 検証はそれだけで debug が書ける詳しさで書く

- パス名、外に公開された名前、入力と期待される出力など、外から観測できる語彙は書いてよい
- 内部の作りを前提とする記述は design に回す
- 書けないなら、判定の内容が足りていない

### R6 各検証は自分の手段を宣言する

- 自動で走る debug ならそのファイルパス、人が上から通すなら checklist と書く
- 手段が揃った時点で spec は事実になる。通ったかどうかは範囲にない

### R7 散文は対象プロジェクトの言語で書く

- 既存の文書が無いときは、決断が書かれている言語に合わせる
- 見出しとフィールド名は言語に依らず英語で固定する

### R8 design を引かない

- 生成した spec は L2_designs のいかなる文書も参照しない
- design の側からも引かれない。両者は対等な並列で、互いを待たずに書ける
- 整合を担保するのは上の feature であり、この層ではない

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | V1 観測の外側 | R1 |
| 2 | V2 要件の番号 | R2 |
| 3 | V3 通し検証 | R3 |
| 4 | V4 未検証の検出 | R4 |
| 5 | V5 debug の実装可能性 | R5 |
| 6 | V6 手段の宣言 | R6 |
| 7 | V7 言語の追随 | R7 |
| 8 | V8 design 非参照 | R8 |

### V1 観測の外側

- Means: checklist
- 生成された要件が、実装を読まずに判定できる記述だけであることを見る

### V2 要件の番号

- Means: checklist
- 各要件が R1 から連番で振られ、番号が重複しないことを見る

### V3 通し検証

- Means: checklist
- 検証を上から順に実行し、判定が全て下せることを見る

### V4 未検証の検出

- Means: checklist
- 検証を持たない要件を含む決断を与え、表の欠落として現れることを見る

### V5 debug の実装可能性

- Means: checklist
- 生成された各 V について、spec 以外を読まずに debug が書けることを見る
- 内部の作りを前提とする記述が V に残っていないことを見る

### V6 手段の宣言

- Means: checklist
- 生成された全ての V が `手段:` の行を持つことを見る

### V7 言語の追随

- Means: checklist
- 既存の文書が日本語のプロジェクトで起動し、生成物の散文が日本語であることを見る
- 同じ生成物の見出しとフィールド名が英語のままであることを見る

### V8 design 非参照

- Means: checklist
- 生成された spec に `../L2_designs/` を含むリンクが一つも無いことを見る

## Articles
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_articles/output-language-follows-project.md)
- [配布物は英語で書く](../L4_articles/distributed-content-in-english.md)
- [検証は自分の手段を宣言する](../L4_articles/verification-declares-its-means.md)
- [debug は spec だけを読んで書ける](../L4_articles/debug-from-spec-alone.md)
- [spec と design は互いを引かない](../L4_articles/spec-design-independent.md)
- [層は飛ばさない。decisions だけが例外](../L4_articles/no-layer-skip.md)
- [参照はファイル単位で張る](../L4_articles/references-are-file-scoped.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [form](../L3_terms/form.md)
- [decision](../L3_terms/decision.md)
- [debug](../L3_terms/debug.md)
- [design](../L3_terms/design.md)
- [reference](../L3_terms/reference.md)
