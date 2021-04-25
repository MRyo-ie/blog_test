---
title: "hugo のページに画像を挿入する方法"
date: 2021-04-01T12:29:43+09:00
## draft: true
toc: true
comments: false
images:
tags: 
  - hugo
---

## 概要
Hugo で技術ブログを立ち上げてみたが、画像の挿入が想像以上に難しかった...。

具体的には、テーマによって以下のような違いがあった。
- 記法
  - マークダウン
  - テーマが用意しているオリジナルの（複数種類）
  - そもそも画像が挿入できない
- 保存場所
  - `post/`
  - `static/`
  - `resources/`

その上、関連する情報がググってもすぐには出てこなかったので、時間を使ってしまった...。

なので、メモも兼ねて、調べた手順などを軽くまとめてみることにした。

## 記法の違いについて
### マークダウン記法 の場合
- `![]()` でできる。

### テーマごとのオリジナルの記法 の場合
- テーマによって、記法が微妙に違う。
- 画像挿入ができない（マークダウン記法が使えず、オリジナルもない）テーマもある。


## 各テーマの画像挿入方法
### 調べ方
以下の流れで調べるのが良さそう。
1. 各テーマの README.md を探してみる。
    - 例）[Clarity](https://themes.gohugo.io/hugo-clarity/#images)
      - `Images` 以下にある。
    - 例）[fuji](https://themes.gohugo.io/hugo-theme-fuji/#-image-zoom-and-lazyload-settings)
      - `Image zoom and lazyload settings` の項にある。
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


### （参考）私の環境の場合
- テーマ： Clarity
- 画像の保存場所
  - `【リポジトリRoot】/content/post/【記事名】/〜.png`
  - （一応、`【リポジトリRoot】/static/〜/〜.png` もできるっぽい？）
- 主に使っている記法
  - マークダウン方式
  - `![](〜/〜.png)`


<!-- #### (theme) Fuji
- 画像の保存場所： 
- マークダウン上での書き方

#### (theme) Fuji
- 画像の保存場所： 
- マークダウン上での書き方 -->


### 参考
- [image processing in hugo ep18](https://mertbakir.gitlab.io/hugo/image-processing-in-hugo/)

