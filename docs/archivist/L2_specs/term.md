# term — 語を起こす要件

## Requirements

<a id="R1"></a>

### R1 決断が意味を確定させた語だけを起こす

- 判定は「その語を別の意味に取ると決断が別の内容になるか」で行う
- 既に意味が定まっている語を使っているだけの場合は起こさない

<a id="R2"></a>

### R2 1語1ファイルとし、ファイル名を語そのものとする

- 一つの語は一つのファイルにだけ置く
- 複数の語を1枚にまとめない

<a id="R3"></a>

### R3 既存の語が決断と食い違えば書き直す

- 指すだけで済ませない
- 書き直したとき、元の決断への参照は残す

<a id="R4"></a>

### R4 起こした語は自分を確定させた決断を指す

- Decisions 節に起点の決断を持つ

<a id="R5"></a>

### R5 散文は対象プロジェクトの言語で書く

- 既存の文書が無いときは、決断が書かれている言語に合わせる
- 見出し、アンカー、フィールド名は言語に依らず英語で固定する

## Verify

| No | VERIFY_NAME | REQUIREMENT |
| -- | ----------- | ----------- |
| 1 | [対象語の判定](#V1) | [R1](#R1) |
| 2 | [ファイルの単位](#V2) | [R2](#R2) |
| 3 | [書き直し](#V3) | [R3](#R3) |
| 4 | [決断への到達](#V4) | [R4](#R4) |
| 5 | [言語の追随](#V5) | [R5](#R5) |

<a id="V1"></a>

### V1 対象語の判定

- Means: checklist
- 意味を変えても内容が変わらない語を含む決断を与え、その語が起きないことを見る

<a id="V2"></a>

### V2 ファイルの単位

- Means: checklist
- 生成物を数え、1ファイルに語が一つだけであり、ファイル名が語と一致することを見る

<a id="V3"></a>

### V3 書き直し

- Means: checklist
- 決断と食い違う定義を置いた状態で起動し、その定義が書き直されることを見る

<a id="V4"></a>

### V4 決断への到達

- Means: checklist
- 生成物の Decisions 節を辿り、起点の決断に到達することを見る

<a id="V5"></a>

### V5 言語の追随

- Means: checklist
- 既存の文書が日本語のプロジェクトで起動し、生成物の散文が日本語であることを見る
- 同じ生成物の見出しとフィールド名が英語のままであることを見る

## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)

## References

### Structures

- [document-layers](../L3_structures/document-layers.md)
- [skill-composition](../L3_structures/skill-composition.md)
- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [form](../L3_terms/form.md)
- [decision](../L3_terms/decision.md)
- [reduction](../L3_terms/reduction.md)
