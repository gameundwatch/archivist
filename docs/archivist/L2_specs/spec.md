# spec — 仕様を起こす要件

## Requirements

<a id="R1"></a>

### R1 外から観測できることだけを要件にする

- 内部の作りには触れない
- いつ動きいつ動かないかの発火条件と、対応するかしないかのスコープを含む

<a id="R2"></a>

### R2 各要件にアンカーを持つ

- R1 から順に番号を振る
- 上層から要件単位で指せること

<a id="R3"></a>

### R3 検証はそのままチェックリストとして通せる

- 一項目が一つの判定である
- 判定の手順と、満たしたと言える条件を持つ

<a id="R4"></a>

### R4 要件と検証の対応が表で読める

- どの検証からも指されない要件が、表から見つかること

<a id="R5"></a>

### R5 検証はそれだけでテストコードが書ける詳しさで書く

- パス名、外に公開された名前、入力と期待される出力など、外から観測できる語彙は書いてよい
- 内部の作りを前提とする記述は design に回す
- 書けないなら、判定の内容が足りていない

<a id="R6"></a>

### R6 各検証は自分の手段を宣言する

- テストコードならそのファイルパス、人が上から通すなら checklist と書く
- 手段が揃った時点で spec は事実になる。通ったかどうかは範囲にない

<a id="R7"></a>

### R7 散文は対象プロジェクトの言語で書く

- 既存の文書が無いときは、決断が書かれている言語に合わせる
- 見出し、アンカー、フィールド名は言語に依らず英語で固定する

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | [観測の外側](#V1) | [R1](#R1) |
| 2 | [要件の指し先](#V2) | [R2](#R2) |
| 3 | [通し検証](#V3) | [R3](#R3) |
| 4 | [未検証の検出](#V4) | [R4](#R4) |
| 5 | [テストの実装可能性](#V5) | [R5](#R5) |
| 6 | [手段の宣言](#V6) | [R6](#R6) |
| 7 | [言語の追随](#V7) | [R7](#R7) |

<a id="V1"></a>

### V1 観測の外側

- Means: checklist
- 生成された要件が、実装を読まずに判定できる記述だけであることを見る

<a id="V2"></a>

### V2 要件の指し先

- Means: checklist
- 各要件の直前にアンカーが在ることを見る

<a id="V3"></a>

### V3 通し検証

- Means: checklist
- 検証を上から順に実行し、判定が全て下せることを見る

<a id="V4"></a>

### V4 未検証の検出

- Means: checklist
- 検証を持たない要件を含む決断を与え、表の欠落として現れることを見る

<a id="V5"></a>

### V5 テストの実装可能性

- Means: checklist
- 生成された各 V について、spec 以外を読まずにテストコードが書けることを見る

<a id="V6"></a>

### V6 手段の宣言

- Means: checklist
- 生成された全ての V が `手段:` の行を持つことを見る

<a id="V7"></a>

### V7 言語の追随

- Means: checklist
- 既存の文書が日本語のプロジェクトで起動し、生成物の散文が日本語であることを見る
- 同じ生成物の見出しとフィールド名が英語のままであることを見る

## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [検証は自分の手段を宣言する](../L4_decisions/verification-declares-its-means.md)
- [テストコードは spec だけを読んで書ける](../L4_decisions/test-from-spec-alone.md)
- [層は飛ばさない。decisions だけが例外](../L4_decisions/no-layer-skip.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [form](../L3_terms/form.md)
- [decision](../L3_terms/decision.md)
- [test](../L3_terms/test.md)
- [reference](../L3_terms/reference.md)
