# Hugo README

- [HUGO](https://gohugo.io/)
- [jakejarvis/hugo-docker](https://github.com/jakejarvis/hugo-docker)

## ホスト

    $ docker-compose up -d
    $ docker container exec -it project-hugo bash

### テーマのインストール

    $ cd themes
    $ git clone https://github.com/budparr/gohugo-theme-ananke.git

テーマの定義はconfig.tomlに記述する。


## コンテナ内

### プロジェクト作成

[example] はプロジェクト名

    $ hugo new site [example]

### サーバー起動

#### 入る

    $ docker container exec -it project-hugo bash

#### コンテナ内で作業

    $ cd [example]
    $ hugo server --buildDrafts --buildFuture --bind 0.0.0.0

### ファイルやフォルダの作成

    $ hugo new posts/example1.md

### 静的HTMLファイルの作成

まだ試していない。

    $ hugo

## 参照

- [静的サイトジェネレータ「Hugo」と技術文書公開向けテーマ「Docsy」でOSSサイトを作る(さくらのナレッジ)](https://knowledge.sakura.ad.jp/22908/)
- [Hugo を利用するための環境構築](https://qiita.com/ub0t0/items/4ac2f2d8c3e8fbdfcfad)
- [Hugo v0.89.0 以降の tweet shortcode で発生する warn を修正する](https://blog.foresta.me/posts/fix-tweet-shortcode-warn-hugo-v0_91_0/)