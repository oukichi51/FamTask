# FamTask - 家事管理ウェブアプリ

## 概要
FamTaskは、家事を管理するためのシンプルなウェブアプリケーションです。このアプリは、タスクの追加、表示、削除を行うことができ、Tailwind CSSを使用してスタイリングされています。

## プロジェクト構成
```
FamTask
├── docker/
│   └── Dockerfile        # Docker設定ファイル
├── docker-compose.yml    # Docker Compose設定ファイル
├── package.json          # プロジェクトの依存関係とスクリプト
├── tailwind.config.js    # Tailwind CSS設定ファイル
├── postcss.config.js     # PostCSS設定ファイル
├── src/
│   ├── css/
│   │   └── input.css     # Tailwind CSSエントリポイント
│   └── html/
│       └── index.html    # HTMLファイル
├── dist/
│   └── output.css        # ビルド後のCSS（自動生成）
└── README.md             # プロジェクトのドキュメント
```

## セットアップ手順

1. **リポジトリのクローン**
   ```
   git clone <repository-url>
   cd FamTask
   ```

2. **依存関係のインストール**
   Tailwind CSSを使用するために、Node.js環境をセットアップし、以下のコマンドを実行します。
   ```
   npm install
   ```

3. **CSSのビルド**
   以下のコマンドでCSSをビルドします。
   ```
   npm run build:css
   ```

4. **アプリケーションの起動**
   以下のコマンドでローカルサーバーを起動します。
   ```
   npm start
   ```

5. **ブラウザでアクセス**
   ブラウザで以下のURLにアクセスしてください。
   ```
   http://localhost:3000
   ```

## Dockerを使用したセットアップ

1. **DockerとDocker Composeのインストール**
   DockerとDocker Composeがインストールされていることを確認してください。

2. **Dockerイメージのビルド**
   以下のコマンドを実行してDockerイメージをビルドします。
   ```
   docker-compose build
   ```

3. **コンテナの起動**
   以下のコマンドを実行してコンテナを起動します。
   ```
   docker-compose up
   ```

4. **アプリケーションへのアクセス**
   ブラウザで以下のURLにアクセスしてください。
   ```
   http://localhost:3000
   ```

## 使用方法
1. アプリケーションをブラウザで開きます。
2. 家事名、担当者、日付を入力し、「追加」ボタンをクリックしてタスクを追加します。
3. タスクは一覧に表示され、完了チェックや削除が可能です。

## ライセンス
このプロジェクトはMITライセンスの下で提供されています。