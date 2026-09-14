# Seamless Scatter Maker

複数のPNG・SVGなどの画像素材を自動で散らして、シームレスパターンを作成できる無料ブラウザツールです。

**公開サイト:**  
https://seamless-scatter-maker.pages.dev/

## 特徴

- 複数のPNG / SVG / WebP / JPEGを読み込み可能
- 素材をランダム・均等・グリッドなどで自動配置
- 上下左右につながるシームレスパターンを生成
- 素材ごとに重み、最低配置数、サイズ、回転、左右反転を設定可能
- Main / Subグループを使った配置バランス調整
- 配置後のドラッグ微調整
- Undo / Redo対応
- PNG書き出し
- 日本語 / English対応
- PC・スマートフォン対応

## 画像データについて

Seamless Scatter MakerはAI生成サービスではありません。

読み込んだ画像素材の配置・合成・書き出しはブラウザ内で処理されます。  
画像ファイルを、このサイトのサーバーやAIサービスへ送信する処理はありません。

画像をAIの解析や学習に使用することもありません。

※通常のWebアクセスに伴う通信や、第三者広告サービスを利用する場合の通信は別です。

## 使い方

1. PNG / SVGなどの画像素材を追加
2. 配置数や各素材の設定を調整
3. 「生成」を押す
4. 必要に応じて配置をドラッグして微調整
5. 「PNG書き出し」で保存

詳しい使い方は公開サイトの **How to** ページをご覧ください。

## CLIP STUDIOとの使い分け

CLIP STUDIOの整列機能は、規則的に素材を並べる用途には便利です。

一方で、複数の素材をランダムに散らして、端まで自然につながるシームレスパターンを作るには手作業が多くなるため、その作業を簡単にする目的でSeamless Scatter Makerを作りました。

## 商用利用

Seamless Scatter Makerで作成した画像は商用利用できます。

ただし、読み込んだ画像素材そのものの著作権や利用規約については、各素材の権利者が定める条件に従ってください。

詳しくは公開サイトの **Terms** をご確認ください。

## 公開環境

このサイトはGitHubリポジトリとCloudflare Pagesを接続して公開しています。

GitHubへ変更をコミットすると、Cloudflare Pagesへ自動デプロイされます。

### Cloudflare Pages設定

- Framework preset: `None`
- Build command: なし
- Build output directory: リポジトリのルート

## 主なファイル

- `index.html` — ツール本体
- `how-to.html` — 使い方
- `privacy.html` — プライバシーポリシー
- `terms.html` — 利用規約
- `contact.html` — お問い合わせ
- `404.html` — 404ページ
- `site.css` — 共通CSS
- `_headers` — Cloudflare Pages向けヘッダー設定
- `robots.txt` — クローラー向け設定
- `sitemap.xml` — サイトマップ

## ローカルで確認する

フォルダ内で簡易HTTPサーバーを起動すると確認できます。

```bash
python -m http.server 8000
```

その後、ブラウザで以下を開きます。

```text
http://localhost:8000/
```

## サイト運用

- Google Search Console登録済み
- `sitemap.xml` / `robots.txt` 対応
- SEO向け説明・FAQをトップページに掲載
- Google AdSenseは審査・承認後に広告表示を行う予定

---

Bug reports, feedback, and other inquiries are welcome through the Contact page on the website.
