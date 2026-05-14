# caloriecam

CalorieCamは、OpenAIのGPT-4o Vision APIを活用して、写真から食事のカロリーを推定するシンプルなウェブアプリケーションです。カメラを料理に向け、写真を撮るだけで、AIによる栄養素の推定値を取得できます。

## 機能

- **AIによる分析**: OpenAI GPT-4o Vision APIを使用して、食べ物の写真からカロリーを推定します。
- **ライブカメラプレビュー**: デバイスのカメラを使用し、ブラウザ上にライブ映像を直接表示します。
- **シンプルなインターフェース**: ボタン1つで画像を撮影し、カロリー推定結果を受け取ることができます。

## はじめに

アプリケーションをローカルで実行するには、以下の手順に従ってください。

### 前提条件

- [Deno](https://deno.land/) ランタイムのインストール。
- [OpenAI](https://platform.openai.com/api-keys) のAPIキー。

### セットアップとインストール

1.  **リポジトリのクローン:**
    ```sh
    git clone https://github.com/code4fukui/caloriecam.git
    cd caloriecam
    ```

2.  **環境変数の設定ファイルの作成:**
    プロジェクトのルートディレクトリに `.env` ファイルを作成します。このファイルにAPIキーを保存します。

3.  **APIキーの追加:**
    OpenAIのAPIキーを `.env` ファイルに追加します。正しいフォーマットについては、依存ライブラリである [openai-imagerecog](https://github.com/code4fukui/openai-imagerecog/) の手順を参照してください。
    ```
    # .env
    OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxx
    ```

### アプリケーションの実行

1.  **サーバーの起動:**
    ターミナルで以下のコマンドを実行します。`8000` の部分は任意のポート番号に変更可能です。
    ```sh
    deno run -A caloriecam.js 8000
    ```

2.  **アプリケーションを開く:**
    ウェブブラウザで `http://localhost:8000` にアクセスします。カメラのアクセス許可を求められた場合は、許可してください。

## 使用技術

- **バックエンド**: サーバーは軽量なDenoアプリケーションです。
- **API**: 本プロジェクトでは、画像の分析にOpenAI Vision APIを使用しています。APIとの接続はヘルパーライブラリの [openai-imagerecog](https://github.com/code4fukui/openai-imagerecog/) によって処理されます。
- **フロントエンド**: プレーンなHTML、CSS、JavaScript。

## ライセンス

MIT License — 詳細は [LICENSE](LICENSE) を参照してください。
