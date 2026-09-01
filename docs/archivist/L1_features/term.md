# term — 語を1枚起こす

<!-- 決断が意味を確定させた語を、L3_terms に1ファイルとして書く -->

## Background

決断は語を使う。その語の意味が決断によって初めて定まるとき、意味はどこにも
書かれないまま上層へ運ばれる。読み手ごとに違う意味で読まれる余地が残る。

## Availability

- 決断を指定して起動すると、その決断が意味を確定させた語が1枚起きる
- 既に語がある場合、決断と食い違う定義が書き直される
- 語は1ファイル1語で、ファイル名が語そのものになる
- 起きた語は、自分を確定させた決断を持つ
- 散文は対象プロジェクトの言語で書かれ、見出しとフィールド名は英語のままになる
## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)


## References

### Specs

- [term](../L2_specs/term.md)

### Designs

- [term](../L2_designs/term.md)
