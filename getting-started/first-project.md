---
layout: default
title: 最初のプロジェクト
parent: 環境構築
nav_order: 5
permalink: /getting-started/first-project/
---

# 🎯 VSCodeで最初のプロジェクトを作成
{: .no_toc }

VSCodeを使って、Vibecodingプロジェクトを作成し、開発を始めましょう。
{: .fs-6 .fw-300 }

## 目次
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 📋 事前準備の確認

開始前に、以下が完了していることを確認してください：

✅ Node.jsがインストール済み
✅ Gitがインストール済み
✅ VSCodeがインストール済み
✅ VSCode拡張機能がインストール済み
✅ gemini-cliとcodex-cliがインストール済み

## 📁 Step 1: プロジェクトフォルダの作成と準備

### 1.1 VSCodeを起動

1. **Windows**: スタートメニューから「Visual Studio Code」を選択
2. **Mac**: LaunchpadまたはApplicationsから「Visual Studio Code」を選択

### 1.2 新しいフォルダをVSCodeで開く

#### 方法A: VSCodeから直接作成

1. VSCodeのメニューバーから：
   - **ファイル** → **フォルダーを開く**（Windows）
   - **File** → **Open Folder**（Mac）
2. 任意の場所（例：ドキュメントフォルダ）を選択
3. **新しいフォルダー**ボタンをクリック
4. フォルダ名を入力：`my-vibecoding-project`
5. **フォルダーの選択**をクリック

#### 方法B: エクスプローラーから開く

1. エクスプローラー（Windows）またはFinder（Mac）で新規フォルダを作成
2. フォルダを右クリック
3. **「Codeで開く」**を選択（VSCodeインストール時に追加されたメニュー）

### 1.3 VSCodeの画面構成を確認

開いたVSCodeの画面には以下の要素があります：

```
┌─────────────────────────────────────────────┐
│  メニューバー（ファイル、編集、表示...）         │
├────┬────────────────────────────────────────┤
│    │                                        │
│ サ │          エディタエリア                   │
│ イ │      （ファイルの編集画面）               │
│ ド │                                        │
│ バ │                                        │
│ ｜ │────────────────────────────────────────│
│    │      ターミナル（コマンド実行）           │
└────┴────────────────────────────────────────┘
```

## 💻 Step 2: VSCode統合ターミナルの活用

### 2.1 ターミナルを開く

以下のいずれかの方法でターミナルを開きます：

1. **ショートカット**: `` Ctrl+` ``（Windows）/ `` Cmd+` ``（Mac）
2. **メニュー**: **表示** → **ターミナル**
3. **上部メニュー**: **Terminal** → **New Terminal**

### 2.2 ターミナルの確認

ターミナルが開いたら、現在のディレクトリが正しいか確認：

```bash
# 現在のディレクトリを確認
pwd
```

出力例：
```
C:\Users\YourName\Documents\my-vibecoding-project  # Windows
/Users/YourName/Documents/my-vibecoding-project     # Mac
```

## 🚀 Step 3: Vibecodingプロジェクトの初期化

### 3.1 プロジェクトの初期化コマンド

VSCodeのターミナルで以下を実行：

```bash
codex /init
```

### 3.2 対話型セットアップ

ターミナル内で対話型のセットアップが始まります：

```bash
? プロジェクト名を入力してください: my-first-app
? プロジェクトの説明を入力してください: VSCodeで作る最初のVibecodingアプリ
? 使用するフレームワークを選択してください:
  ❯ React
    Vue
    Angular
    Node.js (バックエンド)
    その他
```

**入力のヒント**：
- 矢印キー（↑↓）で選択
- Enterで決定
- 日本語入力も可能

### 3.3 初期化の完了

初期化が完了すると、左側のエクスプローラーに新しいファイルが表示されます：

```
my-vibecoding-project/
├── 📄 package.json
├── 📄 .gitignore
├── 📁 src/
└── 📄 README.md
```

## 📝 Step 4: VSCodeで要件定義

### 4.1 要件定義の開始

ターミナルで以下のコマンドを実行：

```bash
codex requirements
```

### 4.2 対話型要件定義

AIアシスタントとの対話がターミナル内で進行します：

```bash
AI: どのようなアプリケーションを作成しますか？

あなた: タスク管理アプリを作りたいです

AI: タスク管理アプリですね。以下の機能について確認します：
    1. タスクの追加・削除
    2. タスクの完了マーク
    3. 優先度設定
    4. カテゴリ分け

    必要な機能を教えてください。

あなた: 1と2だけで、シンプルに作りたいです
```

### 4.3 要件定義の完了とコード生成

```bash
要件定義が完了しました。
コードを生成中...

✅ src/App.js を生成しました
✅ src/components/TaskList.js を生成しました
✅ src/components/TaskItem.js を生成しました
✅ package.json を更新しました

生成が完了しました！
```

## 🎨 Step 5: VSCodeでのコード確認と編集

### 5.1 生成されたファイルを開く

1. **エクスプローラーパネル**（左サイドバー）でファイルをクリック
2. または `Ctrl+P`（Mac: `Cmd+P`）でファイル名を入力して開く

### 5.2 コードの確認

生成されたコードがエディタに表示されます。VSCodeの機能：

- **シンタックスハイライト**: コードが色分けされて見やすい
- **IntelliSense**: 自動補完が効く（`.`を打つと候補が出る）
- **エラー表示**: 問題があれば赤い波線で表示
- **ホバー情報**: 変数や関数にマウスを乗せると説明が表示

### 5.3 コードの編集

必要に応じてコードを編集：

1. 編集したい箇所をクリック
2. 入力または削除
3. `Ctrl+S`（Mac: `Cmd+S`）で保存
4. **自動フォーマット**: Prettierが自動で整形

## ▶️ Step 6: アプリケーションの実行

### 6.1 依存関係のインストール

ターミナルで実行：

```bash
npm install
```

進捗がターミナルに表示されます：
```
added 234 packages, and audited 235 packages in 15s
found 0 vulnerabilities
```

### 6.2 開発サーバーの起動

```bash
npm start
```

### 6.3 ブラウザでの確認

起動メッセージ：
```
Compiled successfully!

You can now view my-first-app in the browser.

  Local:            http://localhost:3000
  On Your Network:  http://192.168.1.5:3000

Note that the development build is not optimized.
To create a production build, use npm run build.
```

- ブラウザが自動的に開きます
- 開かない場合は `http://localhost:3000` にアクセス

### 6.4 ライブリロード

VSCodeでコードを編集して保存すると：
1. 自動的にコンパイル
2. ブラウザが自動更新
3. 変更が即座に反映

## 🐛 Step 7: VSCodeのデバッグ機能

### 7.1 デバッグの設定

1. 左サイドバーの**デバッグアイコン**をクリック（虫のアイコン）
2. **「launch.jsonファイルを作成します」**をクリック
3. **「Chrome」**を選択
4. 自動的に`.vscode/launch.json`が作成される

### 7.2 ブレークポイントの設定

1. コードの行番号の左側をクリック
2. 赤い点（ブレークポイント）が表示される
3. F5キーでデバッグ開始
4. ブレークポイントで実行が停止

### 7.3 デバッグ時の操作

- **F10**: ステップオーバー（次の行へ）
- **F11**: ステップイン（関数の中へ）
- **Shift+F11**: ステップアウト（関数から出る）
- **F5**: 続行

## 🔀 Step 8: VSCodeのGit統合

### 8.1 ソース管理を開く

1. 左サイドバーの**ソース管理アイコン**をクリック（分岐アイコン）
2. または `Ctrl+Shift+G`（Mac: `Cmd+Shift+G`）

### 8.2 変更の確認

- **変更**タブに編集したファイルが表示
- ファイルをクリックで差分表示
- 緑：追加された行
- 赤：削除された行

### 8.3 コミット

1. 変更したいファイルの「+」をクリック（ステージング）
2. コミットメッセージを入力
3. ✓（チェックマーク）をクリックしてコミット

## 📚 Step 9: VSCodeの便利な機能

### 9.1 マルチカーソル

- **Alt+クリック**（Mac: Option+クリック）: 複数箇所を同時編集
- **Ctrl+D**（Mac: Cmd+D）: 同じ単語を順次選択

### 9.2 エメット（Emmet）

HTMLを素早く記述：
```
div.container>ul>li*3
```
Tabキーで展開：
```html
<div class="container">
  <ul>
    <li></li>
    <li></li>
    <li></li>
  </ul>
</div>
```

### 9.3 スニペット

`rfc` + Tabで React Functional Component のテンプレートが展開

### 9.4 ファイル検索

- **Ctrl+P**（Mac: Cmd+P）: ファイル名で検索
- **Ctrl+Shift+F**（Mac: Cmd+Shift+F）: プロジェクト全体を検索

## 🎯 まとめ

VSCodeを使ったVibecodingプロジェクトの基本的な流れ：

1. ✅ VSCodeでプロジェクトフォルダを開く
2. ✅ 統合ターミナルでコマンド実行
3. ✅ `/init`でプロジェクト初期化
4. ✅ 要件定義でコード生成
5. ✅ VSCodeで編集・デバッグ
6. ✅ Git統合でバージョン管理

## 🆘 トラブルシューティング

### ターミナルが文字化けする

**解決方法**：
1. ターミナルの設定を開く（歯車アイコン）
2. 「Select Default Profile」を選択
3. PowerShell または Git Bash を選択

### npm startでエラーが出る

**解決方法**：
```bash
# node_modulesを削除して再インストール
rm -rf node_modules package-lock.json
npm install
npm start
```

### ポート3000が使用中

**解決方法**：
```bash
# 別のポートで起動
PORT=3001 npm start  # Mac/Linux
set PORT=3001 && npm start  # Windows
```

## 🚀 次のステップ

基本的な開発フローを理解したら、以下に挑戦してみましょう：

- 🎨 UIのカスタマイズ
- 🔧 新機能の追加
- 📱 レスポンシブデザイン
- 🚀 本番環境へのデプロイ

---

<div class="success-message">
  <h3>🎉 おめでとうございます！</h3>
  <p>VSCodeを使ったVibecodingプロジェクトの作成に成功しました。これで本格的な開発を始める準備が整いました！</p>
</div>

<style>
.success-message {
  background: linear-gradient(135deg, #84fab0 0%, #8fd3f4 100%);
  color: #2c3e50;
  padding: 2rem;
  border-radius: 10px;
  margin-top: 3rem;
  text-align: center;
}

.success-message h3 {
  margin-top: 0;
  color: #2c3e50;
}
</style>