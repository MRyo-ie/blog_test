---
title: "Slackbot に 機械学習・Deep Learning モデルを接続してみた。 【実装編】"
date: 2021-03-27T17:01:45+09:00
# draft: true
toc: false
tags: 
  - Slackbot
  - docker-compose
  - AI
  - DeepLearning
---


# 概要
[前回](../紹介/) 紹介した『Slackbot - ML/DL model tester』の、実装部分の解説記事です。

## やりたいこと
- ![fashion mnist で QA](fashion_mnist.png)
  - X： （服などの）画像
  - Q： "fashion_mnist"

  を、Slack で bot に送ると、
  - A： "服の種類"（class,label）

  を返信してくれる。


## 作ったもの
- [GitHub](https://github.com/MRyo-ie/slackbot_ML_model_tester) に公開しています。


# 実装

## やったこと
- 現在の開発状況： 1. のプロトタイプを作った。
  - 画像分類モデル（fashion mnist）を bot に接続した。
  - 対話モデルを bot に接続した。
- システムイメージ
  - ![プロトタイプ構成](system_img-simple.png)

## システム イメージ


# （おまけ）ログ
### （未）Ubuntu に docker インストール
- https://www.softek.co.jp/SID/support/sidfmvm/guide/install-docker-ubuntu1804.html
- https://qiita.com/tkyonezu/items/0f6da57eb2d823d2611d



