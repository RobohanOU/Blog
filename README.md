# Robohan Blog

[![Actions Status](https://github.com/RobohanOU/Blog/workflows/github%20pages/badge.svg)](https://github.com/RobohanOU/Blog/actions)

## 概要

Robohan Blog

URL；https://robohanou.github.io/Blog/

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

参考；https://www.hahahahaha-nnn.work/post/hugo_in_windows/

## Git Clone

下記コマンドにてgit clone & git submodule 更新ができる。

git submodule はテンプレートテーマに適用されている。

```bash
git clone git@github.com:RobohanOU/Blog.git
cd Blog
git submodule init
git submodule update
```

## 新規記事投稿

下記コマンドにて投稿記事の追加ができる。拡張子(.md)がないとページとして認識されないので注意。

```bash
hugo new post/(投稿日時).md
```

## ローカル動作確認

下記コマンドを動作後、http://localhost:1313/Blog/ にアクセスするとサイトの動作確認ができる。

```bash
hugo server
```
