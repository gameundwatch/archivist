# term — 語を1枚起こす

<!-- 決断が意味を確定させた語を、L3_terms に1ファイルとして書く -->

## Background

決断は語を使う。その語の意味が決断によって初めて定まるとき、意味はどこにも
書かれないまま上層へ運ばれる。読み手ごとに違う意味で読まれる余地が残る。

## Availability

- **A1** 決断を指定して起動すると、その決断が意味を確定させた語が1枚起きる

- **A2** 既に語がある場合、決断と食い違う定義が書き直される

- **A3** 語は1ファイル1語で、ファイル名が語そのものになる

- **A4** 起きた語は、自分を確定させた決断を持つ

- **A5** 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる

### Coverage

| availability | spec | design |
| --- | --- | --- |
| A1 | R1 | T1, T2 |
| A2 | R3 | T1, T3 |
| A3 | R2 | T2 |
| A4 | R4 | T2 |
| A5 | R5 | T1 |

## Articles
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_articles/output-language-follows-project.md)
- [配布物は英語で書く](../L4_articles/distributed-content-in-english.md)
- [スキルは文書の要素ごとに割る](../L4_articles/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_articles/command-is-feature.md)

## References

### Specs

- [term](../L2_specs/term.md)

### Designs

- [term](../L2_designs/term.md)
