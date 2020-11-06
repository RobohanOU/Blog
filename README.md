# Robohan Blog

[![Actions Status](https://github.com/RobohanOU/Blog/workflows/github%20pages/badge.svg)](https://github.com/RobohanOU/Blog/actions)

## 概要

* Hugo
* GitHub Actions
* Git Submodule

## 環境構築

0. Git, VScodeの環境構築を行う。
1. [参考リンク](https://www.hahahahaha-nnn.work/post/hugo_in_windows/)をもとに、Hugoの環境構築を行う。
2. 下記コマンドをgit cloneしたいディレクトリで実行する。

``` bash
git clone https://github.com/RobohanOU/Blog.git
```

3. 下記コマンドを実行して、git submoduleをcloneする。

``` bash
cd Blog
git submodule init
git submodule update
```

4. 下記コマンドを実行して、ブラウザでhttp://localhost:8080/ にアクセスしてサイトを確認できるか見る。

``` bash
hugo server
```

<!--以下、テンプレREADME-->
# hugoBasicExample

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
