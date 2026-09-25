# GeoInfoView — Website

GeoInfoView の公開ページ。日英切り替え（EN/日本語）、ビルド不要の静的ページ。

- `index.html` — 紹介ページ（特長・プライバシーとデータ出典・よくある質問・お問い合わせ）。App Store の「サポートURL」「マーケティングURL」にも使う
- `privacy.html` — プライバシーポリシー（App Store の「プライバシーポリシーURL」）
- `assets/icon.png`, `assets/apple-touch-icon.png` — アプリアイコン、`assets/shots/` — 画面（`screenshot/raw/` を幅600に縮小）
- `.nojekyll` — GitHub Pages でそのまま配信する

## 公開（GitHub Pages）
1. このフォルダの中身を `GeoInfoView` リポジトリ（例: https://github.com/hideto0926/GeoInfoView ）のルートに push する
2. リポジトリ → Settings → Pages → Source: *Deploy from a branch*、branch = default、folder = `/ (root)`
3. 1分ほど待って https://hideto0926.github.io/GeoInfoView/ を開く
4. リポジトリ名を変えたら、`AppStore.md` の URL も直す

## 公開前にやること
- App Store の URL が決まったら、`index.html` の App Store ボタンの `href="#"` と「近日公開」表記を差し替える
- 画面の中の写真は、標高データから描いた見本（`screenshot/README.md`）。実機の写真があれば差し替える
- プライバシーポリシーはアプリの実装（2026-09-25 時点）に合わせてある。外部への送信を増やしたら更新する
  - 送っているのは、地図・標高・山名を取り寄せるための範囲だけ（国土地理院・AWS Terrain Tiles・OpenStreetMap Overpass・Apple マップ）
