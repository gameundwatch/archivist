# document-layers — 文書の層と参照の向き

## Diagrams

### D1 層のグラフ

```mermaid
flowchart TD
    subgraph L1[L1 features]
        feature[features: L1_features/*]
    end
    subgraph L2[L2 solutions]
        design[design: L2_designs/*]
        spec[spec: L2_specs/*]
    end
    subgraph L3[L3 domains]
        terms[terms: L3_terms/*]
        structure[structure: L3_structures/*]
    end
    subgraph L4[L4 articles]
        article[articles: L4_articles/*]
    end
    subgraph L5[L5 sources]
        code[code: src/*]
        test[test: test/*]
        debug[debug: e2e/* or checklist]
    end
    L1 --> L2 --> L3 --> L4 --> L5
    structure --> terms
    test --> code
    debug --> code
```

線は参照の方向で、上の層から直下の層へ引く。

L2 の二つに線は無い。spec と design は対等な並列で、どちらの向きにも引かない。
両者が矛盾していないことは feature の Coverage 表が担保する。

### D2 articles への参照

```mermaid
flowchart TD
    subgraph L1[L1 features]
        feature[features: L1_features/*]
    end
    subgraph L2[L2 solutions]
        design[design: L2_designs/*]
        spec[spec: L2_specs/*]
    end
    subgraph L3[L3 domains]
        terms[terms: L3_terms/*]
        structure[structure: L3_structures/*]
    end
    subgraph L4[L4 articles]
        article[articles: L4_articles/*]
    end
    L1 --> L4
    L2 --> L4
    L3 --> L4
```

articles だけは D1 の例外で、どの層からも直接指せる。L3 から L4 への線は
D1 の直下への参照と重なる。

### D3 実装の対応

```mermaid
flowchart TD
    subgraph L2[L2 solutions]
        design[design: L2_designs/*]
        spec[spec: L2_specs/*]
    end
    subgraph L5[L5 sources]
        code[code: src/*]
        test[test: test/*]
        debug[debug: e2e/* or checklist]
    end
    design --> code
    design --> test
    spec --> debug
```

線は実装の対応で、参照の順序には数えない。

線が spec から debug へ、design から test へ分かれているのは、二つの検証が
別のものを判定するためにある。debug は成果物を動かして約束を判定し、test は
材料をパーツ単位で判定する。spec から test へも、design から debug へも線は引かない。

### D4 還元の向き

```mermaid
flowchart BT
    D["L4 articles"] --> T["L3 terms"] --> S["L3 structures"]
    S --> SP["L2 specs"] --> F["L1 features"]
    S --> DE["L2 designs"] --> F
```

参照は上から下へ張るが、書き起こしは下から上へ進む。この向きが
archivist の起動順そのものになる。

L2 で経路が二叉に割れる。specs と designs は互いを待たないので、順不同に書ける。
合流するのは features ただ一つで、そこで初めて両方が揃っている必要が出る。

## Articles
- [印を置かず、実現先の実在は判定で読む](../L4_articles/no-mark-on-documents.md)
- [debug は spec だけを読んで書ける](../L4_articles/debug-from-spec-alone.md)
- [test は design を読んで書く](../L4_articles/test-from-design.md)
- [spec と design は互いを引かない](../L4_articles/spec-design-independent.md)
- [spec と design の整合を担保するのは feature だけ](../L4_articles/feature-joins-spec-and-design.md)
- [層は飛ばさない。articles だけが例外](../L4_articles/no-layer-skip.md)
- [時間的な要素を文書に持たせない](../L4_articles/no-time-factor.md)

## References

### Terms

- [layer](../L3_terms/layer.md)
- [reference](../L3_terms/reference.md)
- [reduction](../L3_terms/reduction.md)
- [test](../L3_terms/test.md)
- [debug](../L3_terms/debug.md)
