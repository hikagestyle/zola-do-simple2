+++
title = "あばうと"
date = 2022-01-01T00:00:00+09:00
template = "static.html"
+++

あばうとのページ。

![サンプル画像](../images/1920x1080.jpg)

固定ページと記事投稿は、相対リンクの階層が異なるので、記述に注意する。


## 環境

- x230（Lenovo ThinkPad）
- LinuxMint 20.2


## このサイトについて

Zolaのクイックスタートをベースに、少しアレンジをしたシンプルなテーマ。

5時間くらいで作ったので、わりとヤッツケです。（2022-01-16）


## 基本的な仕様

ドメイン直下、サブディレクトリでも、とりあえず使えるはず。（config.tomlのbase_urlによる）

- Zola v0.15.2
- pure.css
- カテゴリー無し
- タグ（taxonomies）有効
	- 日本語のタグ付けは、zolaの仕様で自動的に英数字へ変換される
- ページ送り:デフォルトで10件ごと（content/blog）
- タグのページ送り:デフォルトで5件ごと
	- config.tomlから変更可
	- テンプレートの場所:templates/tags/single.html
- 投稿のURL=ファイル名（.mdファイル）
- 固定ページのテンプレート
	- 日付表示はコメントアウト
	- templates/static.html


## GitHub

基本的なファイル一式はGitHubに置いておきます。

規模や好みでチョイス。

- このサイトと同じテーマ（タグのページ送り有り）
	- <a href="https://github.com/hikagestyle/zola-do-simple2" target="_blank" rel="nofollow noopener noreferrer">zola-do-simple2</a>
- 外観は同じテーマ（タグのページ送り無し）
	- <a href="https://github.com/hikagestyle/zola-do-simple" target="_blank" rel="nofollow noopener noreferrer">zola-do-simple</a>


## このテーマの基本的な使い方

- config.tomlの編集
	- base_url（最後にスラッシュなし）
	- title
	- description
- templatesを必要に応じて編集
	- _analytics.html
	- _sidebar.html
	- index.html
- 投稿をする（記事作成、ページ作成）
	- content/blog（記事作成、タグ付け可）
	- content（ページ作成、タグ付け不可）
- ローカルチェック（zola serve or zola serve --drafts）
- ビルド（zola build or zola build --drafts）
- publicフォルダが生成される


## ビルドまでの流れ

投稿のURL=ファイル名（.mdファイル）

シンプルに「content/blog」へ記事作成（.md）をしてビルド。（タグ付け可）

固定ページは「content」にページ作成（.md）をしてビルド。（タグ付け不可）

