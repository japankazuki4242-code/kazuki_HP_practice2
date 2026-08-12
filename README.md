# コーディング課題 — 入門編

HTMLとCSSの基礎を使って制作した、Webページのコーディング練習作品です。

このREADMEは、ホームページをどのようなHTML構造で作ったのか、制作を通して何を学んだのかを後から振り返るための学習記録です。

## 公開ページ

[完成したホームページをブラウザで見る](https://japankazuki4242-code.github.io/kazuki_HP_practice2/)

GitHub Pagesで公開している完成版を確認できます。

## ファイルの説明

- [index.html](./index.html) — 見出し、文章、画像など、ページの構造を作るファイル
- [style.css](./style.css) — 色、文字サイズ、余白、横並びなど、ページの見た目とレイアウトを整えるファイル
- `script.js` — 今回は未使用

## ページ全体のHTML構造

ページ全体は、大きく分けて `header → main → footer` の順番で構成されています。インデントが深くなるほど、その要素が上の要素の中に入っている「子要素」であることを表します。

```text
body
├── header
│   └── div.header-inner
│       ├── div.logo-box
│       │   └── h1.header-logo
│       │       └── a（LOGO）
│       └── nav.header-menu
│           └── ul
│               ├── li.header-menu-list（Home）
│               ├── li.header-menu-list（About）
│               └── li.header-menu-list（Contact）
├── main
│   ├── div.fv
│   └── section.feature
│       └── div.feature-inner
│           ├── h2.heading-title（Feature）
│           └── div.feature-box
│               ├── div.img-area
│               │   └── figure
│               │       └── img
│               └── div.text-area
│                   ├── h3.text-area-title
│                   ├── p.text-area-desc
│                   ├── p.text-area-desc
│                   └── a.cta-btn（Read More）
└── footer
    ├── div.footer-logo（LOGO）
    └── small.copyright（著作権表示）
```

## 各部分の役割

- `header` — ページ上部の領域です。ロゴとナビゲーションメニューをまとめています。
- `header-inner` — ヘッダーの内容を中央に収め、ロゴとメニューを横並びにするための内側の枠です。
- `main` — ファーストビューやFeatureセクションなど、ページの中心となる内容をまとめています。
- `fv` — ページを開いたときに最初に大きく見える「ファーストビュー」です。背景画像を表示しています。
- `feature` — このページで紹介したい内容を掲載するセクションです。
- `feature-inner` — Featureセクションの幅や上下左右の余白を整えるための内側の枠です。
- `img-area` — Featureセクションの画像をまとめる領域です。
- `text-area` — Featureセクションのタイトル、説明文、CTAボタンをまとめる領域です。
- `footer` — ページ最下部の領域です。ロゴと著作権表示を配置しています。

なお、`feature-box` は `img-area` と `text-area` をまとめ、通常は横並びにするための親要素です。CTAボタンは、閲覧者に「Read More」という次の行動を案内するリンクです。

## この作品で学習したこと

- HTMLの基本構造
- 親要素・子要素を意識したページ構成
- CSSによるレイアウトと装飾
- Flexboxを使った、ヘッダーやFeatureセクションの横並びレイアウト
- Featureセクション、CTAボタン、フッターの実装
- 画面幅が871px以下のときにFeatureの画像と文章を縦並びにするレスポンシブ対応
- 画面幅が520px以下のときにファーストビューの高さ、画像幅、メニューの文字サイズを調整するレスポンシブ対応
- Git / GitHubを使ったバージョン管理
- GitHub Pagesを使ったWebページの公開
