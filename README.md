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

This repository offers an example site for [Hugo](https://gohugo.io/) and also it provides the default content for demos hosted on the [Hugo Themes Showcase](https://themes.gohugo.io/).

# Using

1. [Install Hugo](https://gohugo.io/overview/installing/)
2. Clone this repository
```bash
git clone https://github.com/gohugoio/hugoBasicExample.git
cd hugoBasicExample
```
3. Clone the repository you want to test. If you want to test all Hugo Themes then follow the instructions provided [here](https://github.com/gohugoio/hugoThemes#installing-all-themes)
4. Run Hugo and select the theme of your choosing
```bash
hugo server -t YOURTHEME
```
5. Under `/content/` this repository contains the following:
- A section called `/post/` with sample markdown content
- A headless bundle called `homepage` that you may want to use for single page applications. You can find instructions about headless bundles over [here](https://gohugo.io/content-management/page-bundles/#headless-bundle)
- An `about.md` that is intended to provide the `/about/` page for a theme demo
6. If you intend to build a theme that does not fit in the content structure provided in this repository, then you are still more than welcome to submit it for review at the [Hugo Themes](https://github.com/gohugoio/hugoThemes/issues) respository

