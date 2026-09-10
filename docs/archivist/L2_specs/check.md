# check — 検査の要件

## Requirements

### R1 リンクが解決するか判定する

- 文書間の相対パスが解決することを確かめる
- 指し先はファイルまで。ファイルの中の位置は判定しない

### R2 層を飛んでいないか判定する

- 行き先が直下の層、同じ層でグラフが向きを定めた相手、同じノードの中、
  L4_decisions のいずれかであることを確かめる
- グラフが定めた層内の向きは `structure --> terms` の一つだけ
- `spec` と `design` はその相手にあたらない。どちらの向きの参照も違反として挙げる

### R3 循環していないか判定する

- 同じノードの中の参照が閉路を作っていないことを確かめる

### R4 `_` と実現先の食い違いを報告する

- 印が付いた文書のうち、実現先が実在するものを挙げる
- 判定は実現先の実在で行い、実現先を動かして得られる生成物では行わない
- 決断が公開すると定めた単位と機能の集合の差を挙げる

### R5 何も書き換えない

- 読むだけで、ファイルの内容も名前も変えない

### R6 検証が実装できる詳しさに達しているか判定する

- spec の V は、spec 以外を読まずに debug が実装できるかを確かめる。内部の作りを
  前提とする V を挙げる
- design の V は、design 以外を読まずに test が実装できるかを確かめる。spec を
  引く V と、外向きの約束を言い直しただけの V を挙げる

### R7 検証の手段が揃っているか判定する

- `手段:` を持たない V を挙げる
- ファイルパスを宣言していて実在しないものを挙げる

### R8 印を層ごとの条件で判定する

- design は Parts の `target_file` 列のファイルの実在で測る。`IN` と `OUT` は見ない
- spec は全ての V が手段を持つかで測る
- feature は Coverage 表が指す spec と design が両方事実かで測る
- structure と terms と decisions は対象にしない

### R9 形が英語で保たれているか判定する

- 見出しとフィールド名が英語であることを確かめる
- 散文の言語は判定しない。プロジェクトごとに異なる

### R10 図と説明文と実態が食い違っていないか判定する

- 説明文が図と食い違っていないかを確かめる。図に描けない構造の補足は問題ない
- 図が描いていることが、リポジトリの現状と合っているかを確かめる
- 図のラベルがパスや宣言された名前の形をしているなら、その実在を確かめる
- 雛形の穴を含む名前と、Parts の `IN` `OUT` に由来するラベルは対象にしない

### R11 対応表の欠落を判定する

- feature の Coverage 表で、spec 列または design 列が空の行を挙げる
- どの行からも指されない spec の `R` と design の `T` を挙げる
- 三つとも出荷を止める不備として扱う
- spec が緩いのか design が緩いのか、どちらの側の不備かを報告に含める

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | V1 リンクの解決 | R1 |
| 2 | V2 層の段差 | R2 |
| 3 | V3 閉路の検出 | R3 |
| 4 | V4 印の食い違い | R4 |
| 5 | V5 無変更 | R5 |
| 6 | V6 検証の詳しさ | R6 |
| 7 | V7 手段の実在 | R7 |
| 8 | V8 層ごとの印 | R8 |
| 9 | V9 形の言語 | R9 |
| 10 | V10 図の一致 | R10 |
| 11 | V11 対応表の欠落 | R11 |

### V1 リンクの解決

- Means: checklist
- リンク切れを含む文書群を与え、その全てが挙がることを見る

### V2 層の段差

- Means: checklist
- 層を飛ぶ参照を含む文書を与え、それが挙がることを見る

### V3 閉路の検出

- Means: checklist
- 相互に参照する2枚を与え、それが挙がることを見る

### V4 印の食い違い

- Means: checklist
- 実現先が実在する `_` 付き文書を置き、それが挙がることを見る

### V5 無変更

- Means: checklist
- 起動の前後でファイルの内容と名前が一致することを見る

### V6 検証の詳しさ

- Means: checklist
- 内部の作りを前提とする V を含む spec を置き、それが挙がることを見る
- spec を引く V を含む design を置き、それが挙がることを見る

### V7 手段の実在

- Means: checklist
- 存在しないファイルを手段に宣言した V を置き、それが挙がることを見る

### V8 層ごとの印

- Means: checklist
- 印を付けた structure を置き、それが誤りとして挙がることを見る
- 実現先が揃った spec と design に印が残っている状態を置き、それが挙がることを見る

### V9 形の言語

- Means: checklist
- 日本語の見出しやフィールド名を含む文書を置き、それが挙がることを見る

### V10 図の一致

- Means: checklist
- 説明文が述べている辺を1本欠いた図を置き、それが挙がることを見る
- 存在しない名前をラベルに持つ図を置き、それが挙がることを見る

### V11 対応表の欠落

- Means: checklist
- 片方の列だけ空の行を含む feature を置き、どちらの側の不備かを添えて挙がることを見る
- どの行からも指されない `R` を含む spec と、`T` を含む design を置き、両方が
  挙がることを見る

## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [印が付くのは実現先を持つ層だけ](../L4_decisions/mark-only-where-realized.md)
- [検証は自分の手段を宣言する](../L4_decisions/verification-declares-its-means.md)
- [debug は spec だけを読んで書ける](../L4_decisions/debug-from-spec-alone.md)
- [test は design を読んで書く](../L4_decisions/test-from-design.md)
- [spec と design は互いを引かない](../L4_decisions/spec-design-independent.md)
- [spec と design の整合を担保するのは feature だけ](../L4_decisions/feature-joins-spec-and-design.md)
- [`_` を外す作業は check から分ける](../L4_decisions/promote-separate-from-check.md)
- [参照はファイル単位で張る](../L4_decisions/references-are-file-scoped.md)

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
