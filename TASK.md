# 家事管理ウェブアプリ - 開発タスク一覧（1時間以内）

## 🧱 フェーズ 1：UI設計と基本構造

### 1. プロジェクトの初期構成（15分）
- フォルダ作成
- `index.html`, `app.js`, `tailwind.css` の作成
- HTMLの基本構造を記述（`<!DOCTYPE html>`など）

### 2. Tailwind CSS の導入（30〜45分）

#### ✅ CDN版（簡易・学習用途向け）
- `index.html` に以下を追記：
  `<script src="https://cdn.tailwindcss.com"></script>`

#### ✅ またはビルド版（本格開発向け）

1. 初期化コマンド（Node.js環境が必要）  
   `npm init -y`  
   `npm install -D tailwindcss`  
   `npx tailwindcss init`

2. `tailwind.config.js` の設定（HTML/JSを対象に）  
   ```js
   module.exports = {
     content: ["./*.html", "./*.js"],
     theme: {
       extend: {},
     },
     plugins: [],
   }
   ```

3. `src/input.css` を作成し、以下を記述  
   - `@tailwind base;`  
   - `@tailwind components;`  
   - `@tailwind utilities;`

4. CSSをビルドして出力  
   `npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch`

5. `index.html` にビルド済CSSを読み込む  
   `<link href="./dist/output.css" rel="stylesheet">`

---

### 3. 入力フォームのHTML構築（30分）
- 家事名、担当者、日付の入力欄
- 「追加」ボタンを設置
- Tailwindでスタイル設定（例：`class="p-2 border rounded"`）

### 4. 家事一覧テーブルのHTML構築（30分）
- テーブルヘッダー行：日付 / 家事名 / 担当者 / 完了 / 削除
- `<tbody>` にJavaScriptで動的行を追加予定
- Tailwindでスタイリング（例：`class="table-auto w-full border"`）

---

## 💻 フェーズ 2：JavaScriptでの基本機能構築

### 5. タスク追加機能の実装（30分）
- 入力内容を取得し、JavaScriptオブジェクトへ変換
- `taskList`配列に追加

### 6. 一覧表示機能の実装（30分）
- `taskList`配列の内容をHTMLテーブルに反映
- `innerHTML` または `createElement` による描画

### 7. ローカルストレージ保存機能（30分）
- `localStorage.setItem` で保存
- ページ読み込み時に復元（`window.onload`）

---

## ✅ フェーズ 3：操作性と補助機能

### 8. 完了チェック切り替え機能（30分）
- チェックボックスのON/OFF状態を更新
- 完了タスクに取り消し線を追加（例：`line-through`）

### 9. タスク削除機能の実装（30分）
- 各行に削除ボタンを配置
- 配列とローカルストレージから該当データ削除

---

## 🧪 フェーズ 4：仕上げとテスト

### 10. 表示の微調整（30分）
- Tailwindクラスの追加・修正（余白、カラーなど）
- モバイル向けの簡易レイアウト確認

### 11. テストと動作確認（30分）
- 入力 → 表示 → 完了チェック → 削除の一連動作確認
- 保存データがリロード後も保持されているか確認

---

## 📝 合計：5〜6時間でMVP完成
- 最低限の家事管理機能が動作する構成を目指す
- Tailwind CSS により開発スピードと見た目の統一感を確保
- 拡張機能（カレンダー表示、担当者フィルターなど）は別フェーズで検討
