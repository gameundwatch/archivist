# whiteboard — ホワイトボードの構成

## Diagrams

### D1 生成の流れ

```mermaid
flowchart LR
    MD["docs/archivist/**.md"] --> GEN["whiteboard"]
    IDX["docs/archivist/index.csv"] --> GEN
    LIB["mermaid"] -.生成時に取得.-> GEN
    GEN --> OUT["whiteboard.html"]
    GEN -.書き戻さない.-> MD
```

入力は `docs/archivist/` の文書と索引だけで、出力は HTML 1枚になる。図を描く実装は
生成の時点で取得し、出力へ埋め込む。閲覧時に取りに行かないので、出力は単体で開ける。
取得できなかったときは図を持たない出力になる。代わりの描画は持たない。
生成は文書へ何も書き戻さない。向きは常に文書から出力への一方向になる。

### D2 盤面の要素

```mermaid
flowchart TD
    subgraph WB["whiteboard.html"]
        BOARD["盤面"]
        subgraph SLOT["配置スロット"]
            L1["配置 1"]
            L2["配置 2"]
            L3["配置 n"]
        end
        TABLE["ピンの表"]
        PAPER["紙"]
    end
    SLOT --> BOARD
    TABLE --> BOARD
    TABLE --> PAPER
    BOARD --> PAPER
    PAPER -.糸.-> BOARD
```

盤面は配置スロットから座標を、ピンの表から色と形を受け取る。配置は複数あり、
どれも同じ盤面に差し込める。ピンの表は1つで、盤面と紙の両方がそこから引く。
紙は盤面の上に開き、開いた元のノードへ糸で繋がる。盤面の外へは出ない。

### D3 紙の開閉

```mermaid
stateDiagram-v2
    [*] --> 閉じている
    閉じている --> 開いている: ノードを押す
    閉じている --> 開いている: 本文中の参照を押す
    開いている --> 閉じている: 同じノードを押す
    開いている --> 閉じている: 紙のピンを押す
```

紙は開くと閉じるの2状態しか持たない。開く操作は2つ、閉じる操作は2つになる。
閉じる操作を元のノードと紙自身の両方に持たせるのは、盤面の外へ出さない以上、
紙が盤面のどこにあっても手が届く必要があるため。
複数の紙が同時に開いている状態を許す。この図は紙1枚の状態を示す。

### D4 配置の切り替え

```mermaid
flowchart LR
    A["配置 A の座標"] -- 同じ点が移動する --> B["配置 B の座標"]
    A -.描き替えない.-> X["別の盤面"]
    B --> KEEP["開いている紙と注目は残る"]
```

切り替えは点の移動として起きる。盤面を描き替えないので、どの点がどこへ行ったかが
そのまま情報になる。保たれるのは点の同一性と、開いている紙、注目しているノードで、
移動の速さや軌跡は条件に入らない。移動の途中でも盤面は触れる。

### D5 視点の操作

```mermaid
flowchart TD
    DRAG["背景を掴む"] --> VIEW["視点"]
    NODE["ノードを掴む"] --> POS["その点の座標"]
    WHEEL["拡大縮小"] -- カーソルを固定点に --> VIEW
    SLIDER["拡大率を直接動かす"] -- 画面の中心を固定点に --> VIEW
    AUTO["自動追従"] -.手の操作に負ける.-> VIEW
    VIEW -.保存しない.-> STORE["どこにも残らない"]
```

視点を変える操作は2系統に分かれる。掴む操作は、背景なら視点が、ノードならその点の
座標が動く。拡大縮小はカーソルの下を固定点にし、拡大率を直接動かす手段だけは
指す対象を持たないので中心を固定点にする。自動追従を持つ場合、手が触れた時点で外れる。

## Articles
- [ホワイトボードは文書から生成され、文書を書き換えない](../L4_articles/whiteboard-generates-from-documents.md)
- [盤面の配置に正解を1つ置かない](../L4_articles/whiteboard-layout-has-no-single-answer.md)
- [ピンは一つの表から引く](../L4_articles/whiteboard-pins-come-from-one-table.md)
- [図は自前で描かない](../L4_articles/whiteboard-diagrams-are-not-ours.md)
- [文書は盤面の上で開く](../L4_articles/whiteboard-documents-open-on-the-board.md)
- [盤面は掴んで動かす](../L4_articles/whiteboard-the-board-is-dragged.md)
- [ズームはカーソルを固定点にする](../L4_articles/whiteboard-zoom-anchors-at-the-cursor.md)
- [配置の切り替えは点の移動で行う](../L4_articles/whiteboard-layout-change-is-a-move.md)
- [盤面は画面より広く開く](../L4_articles/whiteboard-opens-wider-than-the-screen.md)

## References

### Structures

- [directory-layout](../L3_structures/directory-layout.md)

### Terms

- [whiteboard](../L3_terms/whiteboard.md)
- [layout](../L3_terms/layout.md)
- [pin](../L3_terms/pin.md)
- [paper](../L3_terms/paper.md)
- [view](../L3_terms/view.md)
