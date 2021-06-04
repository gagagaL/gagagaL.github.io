---
title: 0円で作るGatsby + Github Pagesの静的ブログ 2
date: "2021-02-26T22:12:03.284Z"
description: "このブログにタグ機能を追加する"
tags: ["Gatsby", "GraphQL"]
---

今のままだと該当記事に辿り着くのがいずれ大変になってきそうなので、タグ検索機能を追加します。

・各記事Markdownファイルにタグ項目追加  
・各タグの一覧ページを作る
・

## 各記事Markdownファイルにタグ項目追加  

各記事のMarkdownファイルの上部に**frontmatter**という形式でメタ情報を書き込む箇所があるが、そこにtagsという項目を追加する。 

今回の記事で言うと

```
---
title: Gatsby + Github Pagesで0円静的ブログ作り 2
date: "2021-02-26T22:12:03.284Z"
description: "このブログにタグ機能を追加する"
tags: ["Gatsby", "GraphQL"]
---
```
のようにする。

GraqhQLでの**allMarkdownRemark**と**markdownRemark**というクエリでMarkdownファイルを取得し、frontmatterのメタ情報はここに含まれる。

```aidl
npm run develop
```

で [http://localhost:8000/___graphql](http://localhost:8000/___graphql) にアクセスすることでGraphQLのクエリを投げた際の挙動を確認できる。


## 各タグの一覧ページを作る  

