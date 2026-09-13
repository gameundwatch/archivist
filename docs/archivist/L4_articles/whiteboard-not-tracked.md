# ホワイトボードは git で追わない

`archivist-whiteboard` は、対象プロジェクトの `.gitignore` に
`docs/archivist/whiteboard.html` を載せる。すでに載っていれば何もしない。

盤面は文書から毎回まるごと組み直す生成物で、消えても何も失われない。取得した実装を
埋め込むため大きく、生成のたびに全体が差分になる。
