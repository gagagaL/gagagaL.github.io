---
title: 0円で作るGatsby + Github Pagesの静的ブログ 1
date: "2021-02-24T22:12:03.284Z"
description: "Gatsby + Github Pagesで無料静的ブログ作り"
tags: ["ブログ", "Github Pages", "Gatsby"]
---

## はじめに

作業報告などを他の人の目を考えずにもっと気軽にしたいなと思い、Qiitaとは違う技術ブログを1から作りたいと思って色々調べました。  
  
Reactも勉強したいものの一つだったので、Reactベースで静的ブログを作るGatsbyを採用して、Github Pagesにて無料で公開することを目指しました。  

とりあえず一旦はデザインなどを凝らずに、アップすることを第一目標に。
  
## いざ作る  
  
そもそもGatsby自体がGithub Pagesで公開されるパターンも想定しているので、割りとスムーズに開発できました。  
  
まず、__(ユーザー名).github.io__ という名前のリポジトリをGithubで作成し、クローン。  

そのリポジトリ内で、  
```aidl
npm install -g gatsby-cli
gatsby new blog https://github.com/gatsbyjs/gatsby-starter-blog
```
かなりベーシックながらブログチックで拡張しやすい構成を最初から提示してくれるgatsby-starter-blogを採用。  
  
"blog"という名前のディレクトリが作成されますが、この名前は別に何でも大丈夫みたいです。  

そして、
```aidl
cd blog
npm install --save gh-pages
```

さらに、package.jsonのscriptに
```aidl
"deploy": "gatsby build && gh-pages -d public -b master"
```
を追記。  
  
すると、
```aidl
npm run deploy
```
でデプロイ。 
  
GithubのリポジトリのSettingからGithub PagesのURLに飛べば、反映されていることが確認できる。  
  
  
### 今後やりたいこと

- [ ] タグ機能追加  
- [ ] デザイン調整  
- [ ] ページネーション(可能なら)  
- [ ] ドメイン変更    