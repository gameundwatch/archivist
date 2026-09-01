# document-layers — 文書の層と参照の向き

## Diagrams

<a id="D1"></a>

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
    subgraph L4[L4 decisions]
        decision[decisions: L4_decisions/*]
    end
    subgraph L5[L5 sources]
        code[code: src/*]
        test[test: test/*]
    end
    L1 --> L2 --> L3 --> L4 --> L5
    L1 --> L4
    L2 --> L4
    design --> spec
    structure --> terms
    test --> code
    design -.-> code
    spec -.-> test
```

実線は参照の方向で、上の層から直下の層へ引く。破線は実装の対応を示し、
参照の順序には数えない。decisions だけは例外で、どの層からも直接指せる。

破線が spec から test へ、design から code へ分かれているのは、test が spec だけを
読んで書けるためにある。design から test への線は引かない。

<a id="D2"></a>

### D2 還元の向き

```mermaid
flowchart BT
    D["L4 decisions"] --> T["L3 terms"] --> S["L3 structures"]
    S --> SP["L2 specs"] --> DE["L2 designs"] --> F["L1 features"]
```

参照は上から下へ張るが、書き起こしは下から上へ進む。この向きが
archivist の起動順そのものになる。

<a id="D3"></a>

### D3 印が付く層

```mermaid
flowchart LR
    F["feature"] -->|"spec と design が事実なら"| M["印が外れる"]
    S["spec"] -->|"全 V に手段が在れば"| M
    D["design"] -->|"Parts のファイルが在れば"| M
    ST["structure"] --- N["印が付かない"]
    T["terms"] --- N
    DC["decisions"] --- N
```

実現先を持つ三層にだけ印が付く。structure と terms は決断の像であり、
実装の有無で状態が変わらない。

## Decisions
- [印が付くのは実現先を持つ層だけ](../L4_decisions/mark-only-where-realized.md)
- [テストコードは spec だけを読んで書ける](../L4_decisions/test-from-spec-alone.md)
- [層は飛ばさない。decisions だけが例外](../L4_decisions/no-layer-skip.md)
- [時間的な要素を文書に持たせない](../L4_decisions/no-time-factor.md)

## References

### Terms

- [layer](../L3_terms/layer.md)
- [reference](../L3_terms/reference.md)
- [reduction](../L3_terms/reduction.md)
- [test](../L3_terms/test.md)
- [mark](../L3_terms/mark.md)
