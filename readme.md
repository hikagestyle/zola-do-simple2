# まえがき

Zola（静的サイトジェネレーター）のテーマ。

タグのページ送り:有り（ページネーション）

個人的なファイル一式。

修正や加工ほか、ご利用は自己責任で。


## 環境

- x230(Lenovo ThinkPad)
- LinuxMint 20.2


## 補足

Zolaのクイックスタートをベースに、少しアレンジをしたシンプルなテーマ。

5時間くらいで作ったので、わりとヤッツケです。（2022-01-16）


### 2022-08-20（修正）

- templates/blog-page.html
	- v0.15.3,v0.16.0,v0.16.1で記事の前後ナビ対策


### 2022-01-22（修正）

- static/css/style.css


## 基本的な仕様

ドメイン直下、サブディレクトリでも、とりあえず使えるはず。（config.tomlのbase_urlによる）

- Zola v0.15.2
- pure.css
- config.toml
	- base_url（最後のスラッシュ無し）
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


## 完成イメージ

デモサイト

https://zola-do-simple2.netlify.app/


## 公式サイト

- [Zola](https://www.getzola.org/)
- [Pure](https://purecss.io/)

