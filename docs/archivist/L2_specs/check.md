# check — 検査の要件

## Requirements

<a id="R1"></a>

### R1 リンクが解決するか判定する

- 文書間の相対パスと、アンカーの実在を確かめる

<a id="R2"></a>

### R2 層を飛んでいないか判定する

- 行き先が直下の層、同じ層でグラフが向きを定めた相手、同じノードの中、
  L4_decisions のいずれかであることを確かめる
- グラフが定めた層内の向きは `design --> spec` と `structure --> terms`

<a id="R3"></a>

### R3 循環していないか判定する

- 同じノードの中の参照が閉路を作っていないことを確かめる

<a id="R4"></a>

### R4 `_` と実現先の食い違いを報告する

- 印が付いた文書のうち、実現先が実在するものを挙げる
- 判定は実現先の実在で行い、実現先を動かして得られる生成物では行わない
- 決断が公開すると定めた単位と機能の集合の差を挙げる

<a id="R5"></a>

### R5 何も書き換えない

- 読むだけで、ファイルの内容も名前も変えない

<a id="R6"></a>

### R6 検証がテストを書ける詳しさに達しているか判定する

- 各 V が spec 以外を読まずに実装できるかを確かめる
- 内部の作りを前提とする V を挙げる

<a id="R7"></a>

### R7 検証の手段が揃っているか判定する

- `手段:` を持たない V を挙げる
- ファイルパスを宣言していて実在しないものを挙げる

<a id="R8"></a>

### R8 印を層ごとの条件で判定する

- design は Parts の `target_file` 列のファイルの実在で測る。`IN` と `OUT` は見ない
- spec は全ての V が手段を持つかで測る
- feature は参照する spec と design が両方事実かで測る
- structure と terms と decisions は対象にしない

<a id="R9"></a>

### R9 形が英語で保たれているか判定する

- 見出し、アンカー、フィールド名が英語であることを確かめる
- 散文の言語は判定しない。プロジェクトごとに異なる

<a id="R10"></a>

### R10 図と説明文と実態が食い違っていないか判定する

- 説明文が図と食い違っていないかを確かめる。図に描けない構造の補足は問題ない
- 図が描いていることが、リポジトリの現状と合っているかを確かめる
- 図のラベルがパスや宣言された名前の形をしているなら、その実在を確かめる
- 雛形の穴を含む名前と、Parts の `IN` `OUT` に由来するラベルは対象にしない

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | [リンクの解決](#V1) | [R1](#R1) |
| 2 | [層の段差](#V2) | [R2](#R2) |
| 3 | [閉路の検出](#V3) | [R3](#R3) |
| 4 | [印の食い違い](#V4) | [R4](#R4) |
| 5 | [無変更](#V5) | [R5](#R5) |
| 6 | [検証の詳しさ](#V6) | [R6](#R6) |
| 7 | [手段の実在](#V7) | [R7](#R7) |
| 8 | [層ごとの印](#V8) | [R8](#R8) |
| 9 | [形の言語](#V9) | [R9](#R9) |
| 10 | [図の一致](#V10) | [R10](#R10) |

<a id="V1"></a>

### V1 リンクの解決

- Means: checklist
- リンク切れを含む文書群を与え、その全てが挙がることを見る

<a id="V2"></a>

### V2 層の段差

- Means: checklist
- 層を飛ぶ参照を含む文書を与え、それが挙がることを見る

<a id="V3"></a>

### V3 閉路の検出

- Means: checklist
- 相互に参照する2枚を与え、それが挙がることを見る

<a id="V4"></a>

### V4 印の食い違い

- Means: checklist
- 実現先が実在する `_` 付き文書を置き、それが挙がることを見る

<a id="V5"></a>

### V5 無変更

- Means: checklist
- 起動の前後でファイルの内容と名前が一致することを見る

<a id="V6"></a>

### V6 検証の詳しさ

- Means: checklist
- 内部の作りを前提とする V を含む spec を置き、それが挙がることを見る

<a id="V7"></a>

### V7 手段の実在

- Means: checklist
- 存在しないファイルを手段に宣言した V を置き、それが挙がることを見る

<a id="V8"></a>

### V8 層ごとの印

- Means: checklist
- 印を付けた structure を置き、それが誤りとして挙がることを見る
- 実現先が揃った spec と design に印が残っている状態を置き、それが挙がることを見る

<a id="V9"></a>

### V9 形の言語

- Means: checklist
- 日本語の見出しやフィールド名を含む文書を置き、それが挙がることを見る

<a id="V10"></a>

### V10 図の一致

- Means: checklist
- 説明文が述べている辺を1本欠いた図を置き、それが挙がることを見る
- 存在しない名前をラベルに持つ図を置き、それが挙がることを見る

## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [印が付くのは実現先を持つ層だけ](../L4_decisions/mark-only-where-realized.md)
- [検証は自分の手段を宣言する](../L4_decisions/verification-declares-its-means.md)
- [テストコードは spec だけを読んで書ける](../L4_decisions/test-from-spec-alone.md)
- [`_` を外す作業は check から分ける](../L4_decisions/promote-separate-from-check.md)

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
- [mark](../L3_terms/mark.md)
