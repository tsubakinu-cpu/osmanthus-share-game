# 金木犀のおすそわけ

**ふたりのカップに、秋をひとさじ。**

Godot 4.6.3で制作した、60秒の小さな金木犀キャッチゲームです。

[ブラウザーで遊ぶ](https://tsubakinu-cpu.github.io/osmanthus-share-game/)

WebGL 2.0に対応したブラウザーが必要です。

## 遊び方

- 「秋をあつめる」で開始
- マウス、指のドラッグ、左右キー、または A / D でカップを移動
- 橙の金木犀は10点、光る金木犀は30点
- 5回連続で集めるごとにボーナスが増え、1個あたり最大25点を追加
- 葉っぱを取る・花を落とすと連続記録が途切れます。点数は減りません
- 60秒で終了。得点、集めた個数、最大連続数を表示します
- ハイスコアは端末・ブラウザー内に保存します

音は起動時OFFです。「音 OFF」または M で切り替えられます。
一時停止ボタン、P、Escapeで休憩。EnterまたはSpaceで開始・再開できます。
スマートフォンは横向き推奨。タッチ操作は実装済みですが、実機での確認は未実施です。

## 公開用ファイル

このリポジトリには、ブラウザー実行用の書き出しとGitHub Pagesへの公開設定を置いています。
`game-web.zip` をGitHub Actionsで展開し、そのままGitHub Pagesへ配信します。
ゲーム部分をHTMLで作り直したものではなく、GodotのWeb書き出しを実行します。

公開設定は Settings → Pages → Build and deployment → Source を **GitHub Actions** にします。
`main`への更新、またはActions画面の手動実行で配信できます。

ローカル確認ではZIPを展開し、そのフォルダーで `python3 -m http.server 8000` を実行して
`http://localhost:8000/` を開きます。`index.html` のダブルクリックでは実行できません。

## プライバシーとクレジット

ゲームにログイン、解析タグ、広告はありません。ゲームが保存するのは最高得点のみです。
初回読み込み時に、この公開サイトからGodotエンジンとゲームデータを取得します。

- ゲーム、ベクター描画、効果音：このプロジェクトのために作成
- エンジン：Godot Engine 4.6.3 / MIT License
- フォント：Noto Sans CJK JP / SIL Open Font License 1.1

エンジンとフォントのライセンス文は `game-web.zip` 内の
`GODOT-LICENSE.txt` と `FONT-LICENSE.txt` に同梱しています。
