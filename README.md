# Seamless Scatter Maker — Cloudflare Pages 公開用

このフォルダは、そのまま静的サイトとしてCloudflare Pagesへデプロイできます。

## 最短の公開手順

### A. Cloudflare Pagesへ直接アップロード
1. Cloudflare Dashboardを開く
2. Workers & Pages → Create → Pages
3. Direct Upload（または同等の静的サイトアップロード）を選ぶ
4. このフォルダの中身をアップロード
5. 発行された `*.pages.dev` URLで動作確認

### B. GitHub経由
1. このフォルダの中身をGitHubリポジトリへ入れる
2. Cloudflare PagesでGitHubリポジトリを接続
3. Framework preset: None
4. Build command: 空欄
5. Build output directory: `/` またはリポジトリのルート
6. Deploy

## 公開前に必ず直すもの

### 1. contact.html
`YOUR-CONTACT@example.com` を実際の問い合わせ先へ変更してください。

### 2. 独自ドメイン取得後
`sitemap.xml.example` の `YOUR-DOMAIN.example` を実際のドメインへ置換し、
`sitemap.xml` にリネームしてください。

### 3. AdSense承認後
- `adsense-snippet.example.html` を参考にAdSenseコードを追加
- `ads.txt.example` の `pub-YOUR_PUBLISHER_ID` を実際のIDへ変更
- `ads.txt` にリネーム
- index.html の `ADSENSE_BOTTOM_SLOT_START` ～ `ADSENSE_BOTTOM_SLOT_END`
  の位置に広告ユニットを置く

広告は「生成」「PNG書き出し」などの操作ボタンのすぐ近くには置かない想定です。

## 同梱ページ
- index.html — ツール本体
- how-to.html — 使い方
- privacy.html — プライバシーポリシー
- terms.html — 利用規約
- contact.html — 問い合わせ
- 404.html — 404ページ
- site.css — 公開ページ共通CSS
- _headers — Cloudflare Pages向け基本セキュリティヘッダー
- robots.txt — クロール許可
- ads.txt.example — AdSense用テンプレート
- adsense-snippet.example.html — 広告コード設置メモ
- sitemap.xml.example — サイトマップ雛形

## プライバシー上の設計
ツールへ読み込んだPNG/SVGは、このツール自身の処理ではサーバーへ送信せず、
ブラウザ内で配置・合成・PNG書き出しを行います。

AdSenseなど第三者広告を有効にすると、広告事業者による通常のWeb通信やCookie利用は発生し得ます。
必要な地域ではCMP/同意管理も設定してください。

## ローカル確認
フォルダ内で簡易HTTPサーバーを起動すると確認しやすいです。

Python例:
`python -m http.server 8000`

その後:
`http://localhost:8000/`
