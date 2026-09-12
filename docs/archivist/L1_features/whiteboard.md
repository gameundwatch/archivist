# whiteboard — 参照グラフを1枚の盤面にする

<!-- docs/archivist/ を読み、参照グラフと文書の中身を1枚の HTML にまとめる -->

## Background

文書が増えると、参照の全体はファイルビューアでは追えなくなる。索引は全体を1つの表に
するが、表は密なところと孤立したところを見せない。どの条項が効いているか、どの層が
薄いかは、形にして初めて読める。

読むだけなら文書を1枚ずつ開けば足りる。足りないのは、参照を辿りながら全体のどこに
いるかを見失わないことで、これは盤面と中身を同時に見るしかない。

## Availability

- **A1** 起動すると盤面が1枚できる
    - `docs/archivist/` の文書と索引から組む
    - 索引が無くても組める

- **A2** 出力を単体で開ける
    - 他のファイルを置かなくてよい
    - 開くときにネットワークを要らない

- **A3** 同じグラフを別の並びで見られる
    - 配置を閲覧中に切り替えられる

- **A4** 配置を足せる
    - 座標を返す規則を1本足すと選べるようになる
    - 既存の配置は書き換えない

- **A5** 切り替えても読んでいたものが残る
    - 開いている紙は閉じない
    - 注目していた文書は注目されたまま残る

- **A6** どの層の文書かがピンで読める
    - 色は層を、形は同じ層の中の割れ方を示す
    - 盤面・紙・本文中の参照・凡例で同じピンになる

- **A7** 文書を盤面の上で開ける
    - 開いた紙は元のノードと繋がって見える
    - 2枚以上を並べられる

- **A8** 紙を2通りで閉じられる
    - 開いた元のノードを押す
    - 紙自身のピンを押す

- **A9** 図が描かれた状態で読める
    - 図は生成時に取得した実装が描く
    - 取得できなかったときは図を持たない盤面になる

- **A10** 盤面をいくら触っても文書は変わらない
    - ノードを動かしても保存されない
    - `docs/archivist/` へ書き戻さない

- **A11** 盤面を掴んで動かせる
    - 背景を掴むと盤面全体が動く
    - ノードを掴むとその点だけが動く

- **A12** 寄っても対象が逃げない
    - カーソルの下にあるものを固定点に拡大縮小する
    - 拡大率を直接動かす手段も持つ

- **A13** 切り替えが移動として見える
    - 点は消えずに新しい座標へ動く
    - 動いている間も盤面を触れる

- **A14** 既定は広く開き、引けば全体が入る
    - 開いた直後、盤面は画面に収まっていない
    - 拡大率を下げると全体に到達できる

- **A15** 視点は持ち越さない
    - 開き直すと既定の視点に戻る

### Coverage

| availability | spec | design |
| ------------ | ---- | ------ |
| A1 | R1 | T1, T2, T3 |
| A2 | R3 | T2, T3 |
| A3 | R4 | T2 |
| A4 | R4 | T2 |
| A5 | R5 | T2 |
| A6 | R6, R7 | T2 |
| A7 | R9 | T2 |
| A8 | R10 | T2 |
| A9 | R8 | T1, T2 |
| A10 | R2 | T1 |
| A11 | R11 | T2 |
| A12 | R12 | T2 |
| A13 | R13 | T2 |
| A14 | R14 | T2 |
| A15 | R15 | T2 |

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
- [コマンド1本を feature 1枚とする](../L4_articles/command-is-feature.md)
- [スキルは文書の要素ごとに割る](../L4_articles/skill-per-element.md)

## References

### Specs

- [whiteboard](../L2_specs/whiteboard.md)

### Designs

- [whiteboard](../L2_designs/whiteboard.md)
