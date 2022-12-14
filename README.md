# book-ml-transformers

- 以下書籍の読解用である。
  - 機械学習エンジニアのためのTransformers (2022-08にリリース)
  - https://www.oreilly.co.jp/books/9784873119953/

- 原書側では改訂版があるようだ。
  - Natural Language Processing with Transformers (2022-06に改訂)
  - https://www.oreilly.com/library/view/natural-language-processing/9781098136789/

- 公式のGitHubは以下。
  - https://github.com/nlp-with-transformers/notebooks

- このレポジトリは各章をノートブックで構成し、内容は以下で記述する。
  - 書籍の要点を箇条書き
  - 書籍のコード実行
  - その他補足事項の記載

- 一部公式の書籍から図を拝借しているため置き換えが必要。

|Chapter|Pages|Title(en)|Title(ja)|Colab|
|:---|:---|:---|:---|:---|
|chap00|i～xxviii               |                        |序文・はじめに                          |<a href="https://colab.research.google.com/github/nokomoro3/book-ml-transformers/blob/main/ml-transformers-chap00.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|
|chap01|p.1～p.22 (22 pages)    |Introduction            |入門Transformers                        |<a href="https://colab.research.google.com/github/nokomoro3/book-ml-transformers/blob/main/ml-transformers-chap01-introduction.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|
|chap02|p.23～p.60 (38 pages)   |Text Classification     |テキスト分類                            |<a href="https://colab.research.google.com/github/nokomoro3/book-ml-transformers/blob/main/ml-transformers-chap02-text-classification.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|
|chap03|p.61～p.90 (30 pages)   |Transformer Anatomy     |Transformerの詳細                       |<a href="https://colab.research.google.com/github/nokomoro3/book-ml-transformers/blob/main/ml-transformers-chap03-transformer-anatomy.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|
|chap04|p.91～p.128 (38 pages)  |Multilingal NER         |多言語の固有表現認識                    |<a href="https://colab.research.google.com/github/nokomoro3/book-ml-transformers/blob/main/ml-transformers-chap04-multilingal-ner.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>|
|chap05|p.129～p.148 (20 pages) |Text Generation         |テキスト生成                            ||
|chap06|p.149～p.172 (24 pages) |Summarization           |要約                                    ||
|chap07|p.173～p.220 (58 pages) |Question Answering      |質問応答                                ||
|chap08|p.221～p.262 (42 pages) |Model Compression       |Transformersの高速化                    ||
|chap09|p.263～p.310 (48 pages) |Few to No Labels        |ラベルのないまたは少ない状況への対応方法||
|chap10|p.311～p.357 (47 pages) |Transformer from scratch|Transformerをゼロから学習する           ||
|chap11|p.359～p.386 (28 pages) |Future Directions       |Transformerの未来                       ||

## 0. [はじめに](ml-transformers-chap00.ipynb)

- 本書の対象や基礎となる書籍、リンク
- 実行環境について

## 1. [Introduction](ml-transformers-chap01-introduction.ipynb)

- Transformerの発展の歴史
- Transformersのライブラリとしての概要概要
- 解くことが可能なタスクについて一通り説明
  - テキスト分類
  - NER
  - 要約
  - 翻訳
  - テキスト生成

## 2. [Text Classification](ml-transformers-chap02-text-classification.ipynb)

- Twitterのセンチメント分類を題材に事前学習モデルを使用した分類モデルの構築を学ぶ。
- 以下が主な内容です。
  - データセットの使用方法
  - 入力系列のトークン化
  - 分類器の学習（以下２パターンで実施）
    - 事前学習モデルのパラメータを更新せず、特徴量抽出器として使用するパターン
    - 事前学習モデルのパラメータを含めてモデル全体をチューニング（fine-tuning）するパターン
  - PyTorch APIとTensorFlow APIについて

## 3. [Transformer Anatomy](ml-transformers-chap03-transformer-anatomy.ipynb)

- TransformerをPyTorchで実装する。
- エンコーダがメインであり、デコーダの一部の詳細は省略されている。
- またTransformerの系統についても概要を記載している。
