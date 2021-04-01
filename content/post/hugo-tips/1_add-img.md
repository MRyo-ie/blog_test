---
title: "hugo のページに画像を挿入する方法"
date: 2021-04-01T12:29:43+09:00
draft: true
comments: false
images:
---

# 概要
## hugo とは
- 

## マークダウン に画像を挿入する場合
- `![]()` でできる。
- hugo のテーマによって、記法が微妙に違うらしい。


# 各テーマの画像挿入方法
## 調べ方
以下の流れで調べるのが良さそう。
1. 各テーマの README.md を探してみる。
    - 例）[fuji](https://themes.gohugo.io/hugo-theme-fuji/#-image-zoom-and-lazyload-settings)
2. 実際に挿入してみる。
    - 大抵は、一発では表示されないです...。
    - 画像のデフォルトの保存場所が、テーマによって違うため（？）
    - 一般的には、`【リポジトリRoot】/static/` か `【リポジトリRoot】/assets/` の[ようです](https://mertbakir.gitlab.io/hugo/image-processing-in-hugo/)。
3. 画像が表示されない場合...
    - 画像を「新しいタブで開く」して、パスを確認する。
      - 例） 
        - マークダウン → `![Alt text](20210327_155116.png)`
        - パス（URL） → `http://localhost:1313/【Root】/post/hugo_init/〜.png`
      - ↑ の場合は、
        - `【Root】/assets/post/hugo_init/〜.png` または、
        - `【Root】/static/post/hugo_init/〜.png` 
          に保存すると、表示されるかも。


## テンプレ
基本的には、以下の流れでOK。
- 画像の保存場所： `【リポジトリRoot】/static/〜/〜.png`
- マークダウン上での書き方
  1. `![](〜/〜.png)`
  2. 

## (theme) Fuji
- 画像の保存場所
- マークダウン上での書き方

