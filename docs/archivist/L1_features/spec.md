# spec — 仕様を1枚起こす

<!-- 決断から導ける約束を、L2_specs に要件と検証として書く -->

## Background

決断は約束を生む。何ができ、何をしないか。約束が書かれないと、実装が
何を満たせば終わりなのか誰にも言えない。

## Availability

- 決断を指定して起動すると、要件とその検証が1枚起きる
- 要件は外から観測できることだけに留まる
- 検証はそのままチェックリストとして通せる
- どの要件がどの検証で確かめられるかが表で読める
- 検証は、それだけを読んでテストコードが書ける詳しさで書かれる
## Decisions
- [生成する文書の言語は対象プロジェクトに合わせる](../L4_decisions/output-language-follows-project.md)
- [配布物は英語で書く](../L4_decisions/distributed-content-in-english.md)
- [検証は自分の手段を宣言する](../L4_decisions/verification-declares-its-means.md)
- [テストコードは spec だけを読んで書ける](../L4_decisions/test-from-spec-alone.md)
- [スキルは文書の要素ごとに割る](../L4_decisions/skill-per-element.md)
- [コマンド1本を feature 1枚とする](../L4_decisions/command-is-feature.md)


## References

### Specs

- [spec](../L2_specs/spec.md)

### Designs

- [spec](../L2_designs/spec.md)
