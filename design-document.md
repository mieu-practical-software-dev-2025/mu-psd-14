# Webアプリ仕様書

## 1. 概要

テキスト情報（具体的なものが望ましい）を入力として、LLMを用いて、
回答（これも具体的に指定）を表示するアプリ。
testttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttt

## 2. 主な機能

### 2.1 入出力フォーム機能
- テキストエリアでユーザーが質問・指示を入力
- 2.2 生成AIリクエストAPIを実行し、応答を取得する。
- 同一画面上に回答を表示する。

### 2.2 生成AIリクエスト API
- ユーザー入力と定型プロンプトを合成し、LLMに渡すコンテキストを生成
- その際に、適切なコンテキストを追加し、望ましい回答を得られるように情報を付加する。
- OpenRouter経由で各種LLM（例：GPT-4, Claude, Geminiなど）へリクエスト
- 応答をJSON形式でフロントエンドに返す。


## 3. 使用技術

| 分類         | 技術・ライブラリ |
|--------------|------------------|
| フロントエンド | Vue.js / HTML5 + CSS3 |
| バックエンド  | Flask |
| 通信方式     | Fetch API / JSON |
| LLMモデル    | OpenRouter API（OpenAI, Anthropic, Mistral等） |

## 4. 入出力例

### 入力
- ユーザー入力：「竹取物語」

- 付与コンテキスト：あなたは太宰治です。小難しい近代風のしゃべり方をします。

### 出力

- 出力例：月の光が眩しい。眩しすぎて、なんだか吐き気がする。老夫婦が見つけた竹の中から、あの憎らしいほど可愛らしい女の子が出てきたらしい。