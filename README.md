# Robohan Blog

[![Actions Status](https://github.com/RobohanOU/Blog/workflows/github%20pages/badge.svg)](https://github.com/RobohanOU/Blog/actions)

## 概要

大阪大学ロボット製作団体 Robohan 公式ブログ リポジトリ

URL：[http://blog2.robohan.net/](http://blog2.robohan.net/)

### 構成

- [Hugo](https://gohugo.io/)
- [Clarity](https://themes.gohugo.io/hugo-clarity/)(Hugo Theme)
- [GitHub Actions](https://github.com/RobohanOU/Blog/actions)

[サンプルページ](http://blog2.robohan.net/sample/)

## 環境構築

### Windows

Powershellを起動して、下記コマンドを実行。

```bash
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
iwr -useb get.scoop.sh | iex
```

その後、下記コマンドが実行できるか確認する。<br>
（このコマンドが実行できなかったらちゃんとインストールできてないので再度試してみること）

```bash
scoop help
```

最後に、下記コマンドを実行してhugo extendedをインストールする。

```bash
scoop install hugo-extended
```

[参考リンク](https://www.hahahahaha-nnn.work/post/hugo_in_windows/)

ここまで出来たらPowerShellを一度閉じて、もう一度PowerShellを開いて下記コマンドを実行する

```bash
hugo
```

ここで、コマンドが存在しない系のエラーが出たら、環境変数であるPATHがうまく通っていないので修正をする。

## 作業手順

1. git cloneする
2. develop/masterをcheckoutする
3. develop/（ブランチ名）を作成・checkoutする
4. 編集して、commit、pushする
5. develop/（ブランチ名）からdevelop/masterブランチへPull requestしてmergeする
6. develop/masterブランチからmasterへPull requestしてmergeする

適宜、issueを立てて問題解決を行うようにするとよい。

### branch構成

- master
  - このbranchにコミットすると、GitHub Actionsが実行さる
  - Hugoの静的ページ（Markdown→HTML）生成が行われる
  - そして、出来たものをgh-pagesにpushしてくれて公開される
- develop/master
  - 編集段階のメインブランチ
  - ここから、masterブランチへPull requestしてmergeする
- develop/（ブランチ名）
  - 編集段階のサブブランチ
  - ここから、develop/masterブランチへPull requestしてmergeする

## Git Clone

下記コマンドにてgit clone & git submodule 更新ができる。

git submodule はテンプレートテーマに適用されている。

```bash
git clone https://github.com/RobohanOU/Blog.git
cd Blog
git submodule init
git submodule update
```

## git branch

基本的にmasterはPull requestにてコミットすること！（masterにコミットすると、ページとして公開されてしまうため）

- master ->これにcommitすると、GitHub Actionsが動作してgh-pagesにコミットされ、サイトが公開される
- develop/master - 編集段階の元

### branch作業方法

1. develop/masterをもとに作業用ブランチを、develop/(ブランチ名)で作成する。
2. develop/(ブランチ名)で作業を行ってcommit&pushを行う。
3. [Pull request](https://github.com/RobohanOU/Blog/pulls)にてdevelop/(ブランチ名)→develop/masterへmargeの申請を行う。
4. 問題がなければ、mergeを行う。
5. 記事を更新するときは、[Pull request](https://github.com/RobohanOU/Blog/pulls)にてdevelop/master→masterへmargeの申請を行い、mergeを行う。

## 新規記事投稿

下記コマンドにて投稿記事の追加ができる。拡張子(.md)がないとページとして認識されないので注意。

```bash
hugo new post/(投稿日時).md
```

## ローカル動作確認

下記コマンドを動作後、http://localhost:1313/ にアクセスするとサイトの動作確認ができる。

```bash
hugo server
```
