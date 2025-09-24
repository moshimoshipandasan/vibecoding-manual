---
layout: default
title: VSCode セットアップ
parent: 環境構築
nav_order: 2
permalink: /getting-started/vscode-setup/
---

# Visual Studio Code セットアップ
{: .no_toc }

Vibecodingの開発に最適なエディタ、Visual Studio Code（VSCode）のインストールと設定を行います。
{: .fs-6 .fw-300 }

## 目次
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 📥 VSCodeのインストール

### Windows

1. [VSCode公式サイト](https://code.visualstudio.com/)にアクセス
2. 「Download for Windows」をクリック
3. ダウンロードした `VSCodeUserSetup-x64-X.XX.X.exe` を実行
4. インストーラーの指示に従って進む
   - ✅ 「PATHへの追加」にチェック（重要）
   - ✅ 「エクスプローラーのコンテキストメニューに追加」にチェック
5. 「インストール」をクリック
6. PCを再起動

### Mac

1. [VSCode公式サイト](https://code.visualstudio.com/)にアクセス
2. 「Download for Mac」をクリック
3. ダウンロードした `VSCode-darwin-universal.zip` を解凍
4. `Visual Studio Code.app` をアプリケーションフォルダにドラッグ
5. Launchpadから起動

### 起動確認

```bash
# ターミナルでVSCodeが起動できるか確認
code --version
```

## 🌐 日本語化

VSCodeを日本語で使いたい場合は、以下の手順で日本語パックをインストールします。

### 手順

1. VSCodeを起動
2. 左側のアクティビティバーから「Extensions」アイコンをクリック（または `Ctrl+Shift+X` / `Cmd+Shift+X`）
3. 検索ボックスに「Japanese」と入力
4. 「Japanese Language Pack for Visual Studio Code」を選択
5. 「Install」をクリック
6. インストール完了後、右下の「Change Language and Restart」をクリック
7. VSCodeが再起動し、日本語表示になります

## 🧩 必須拡張機能のインストール

Vibecoding開発に必要な拡張機能をインストールします。

### インストール方法

1. VSCodeの拡張機能タブを開く（`Ctrl+Shift+X` / `Cmd+Shift+X`）
2. 以下の拡張機能を検索してインストール

### 必須拡張機能リスト

#### 1. **ESLint**
- **用途**: JavaScriptのコード品質チェック
- **検索**: `dbaeumer.vscode-eslint`
- コードの問題をリアルタイムで検出

#### 2. **Prettier - Code formatter**
- **用途**: コード自動整形
- **検索**: `esbenp.prettier-vscode`
- 保存時に自動でコードを整形

#### 3. **Node.js Modules IntelliSense**
- **用途**: Node.jsモジュールの自動補完
- **検索**: `leizongmin.node-module-intellisense`
- `require`や`import`文で自動補完

#### 4. **npm Intellisense**
- **用途**: npmパッケージの自動補完
- **検索**: `christian-kohler.npm-intellisense`
- package.jsonの依存関係を認識

#### 5. **Path Intellisense**
- **用途**: ファイルパスの自動補完
- **検索**: `christian-kohler.path-intellisense`
- ファイルパスの入力を支援

#### 6. **GitLens**
- **用途**: Git統合の強化
- **検索**: `eamodio.gitlens`
- コードの変更履歴を可視化

#### 7. **JavaScript (ES6) code snippets**
- **用途**: ES6スニペット
- **検索**: `xabikos.javascriptsnippets`
- よく使うコードパターンを簡単入力

#### 8. **Live Server**
- **用途**: ローカルサーバー起動
- **検索**: `ritwickdey.liveserver`
- HTMLファイルをライブプレビュー

### 一括インストール（コマンド）

VSCodeのターミナルで以下のコマンドを実行すると、一括でインストールできます：

```bash
# Windows (PowerShell) / Mac (Terminal)
code --install-extension dbaeumer.vscode-eslint
code --install-extension esbenp.prettier-vscode
code --install-extension leizongmin.node-module-intellisense
code --install-extension christian-kohler.npm-intellisense
code --install-extension christian-kohler.path-intellisense
code --install-extension eamodio.gitlens
code --install-extension xabikos.javascriptsnippets
code --install-extension ritwickdey.liveserver
```

## ⚙️ VSCodeの推奨設定

### 設定ファイルの作成

プロジェクトごとに最適な設定を行うため、`.vscode/settings.json`を作成します。

1. VSCodeでプロジェクトフォルダを開く
2. `.vscode`フォルダを作成
3. `settings.json`ファイルを作成
4. 以下の内容を貼り付け：

```json
{
  // エディタ設定
  "editor.fontSize": 14,
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "editor.minimap.enabled": true,
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },

  // ファイル設定
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1000,
  "files.exclude": {
    "**/node_modules": true,
    "**/.git": true
  },

  // Prettier設定
  "prettier.singleQuote": true,
  "prettier.semi": true,
  "prettier.tabWidth": 2,

  // ターミナル設定
  "terminal.integrated.fontSize": 14,
  "terminal.integrated.defaultProfile.windows": "PowerShell",
  "terminal.integrated.defaultProfile.osx": "zsh",

  // Git設定
  "git.autofetch": true,
  "git.confirmSync": false
}
```

## 🎨 テーマとアイコン（オプション）

### 人気のテーマ

見やすいテーマを選ぶことで、長時間の作業でも目が疲れにくくなります。

#### ダークテーマ
- **One Dark Pro**: `zhuangtongfa.material-theme`
- **Dracula Official**: `dracula-theme.theme-dracula`
- **Tokyo Night**: `enkia.tokyo-night`

#### ライトテーマ
- **GitHub Light Theme**: `github.github-vscode-theme`
- **Atom One Light**: `akamud.vscode-theme-onelight`

### アイコンテーマ

ファイルアイコンを見やすくします：

- **Material Icon Theme**: `pkief.material-icon-theme`
- **VSCode Icons**: `vscode-icons-team.vscode-icons`

## 🔧 VSCodeの基本操作

### よく使うショートカット

| 操作 | Windows | Mac |
|------|---------|-----|
| コマンドパレット | `Ctrl+Shift+P` | `Cmd+Shift+P` |
| ファイル検索 | `Ctrl+P` | `Cmd+P` |
| 統合ターミナル | `Ctrl+`` | `Cmd+`` |
| サイドバー切替 | `Ctrl+B` | `Cmd+B` |
| ファイル保存 | `Ctrl+S` | `Cmd+S` |
| すべて保存 | `Ctrl+K S` | `Cmd+K S` |
| 検索 | `Ctrl+F` | `Cmd+F` |
| 置換 | `Ctrl+H` | `Cmd+H` |
| コメント切替 | `Ctrl+/` | `Cmd+/` |
| 行の複製 | `Shift+Alt+↓` | `Shift+Option+↓` |

### 統合ターミナルの使い方

1. `` Ctrl+` `` (Mac: `` Cmd+` ``) でターミナルを開く
2. 複数ターミナルの管理：
   - 新規ターミナル: `Ctrl+Shift+``
   - ターミナル切替: `Ctrl+PageUp/PageDown`
3. ターミナルの種類を選択：
   - Windows: PowerShell, Command Prompt, Git Bash
   - Mac: zsh, bash

## ✅ セットアップ完了の確認

以下のチェックリストで、VSCodeの準備が整っているか確認しましょう：

- [ ] VSCodeが起動する
- [ ] 日本語表示になっている（希望者のみ）
- [ ] 必須拡張機能がインストール済み
- [ ] 統合ターミナルが開ける
- [ ] `code`コマンドがターミナルで使える

## 🎯 次のステップ

VSCodeの準備ができたら、[最初のプロジェクト作成]({{ site.baseurl }}/getting-started/first-project/)に進みましょう！

---

<div class="next-step-box">
  <h3>💡 ヒント</h3>
  <p>VSCodeの設定は後から変更できます。まずは基本設定で始めて、慣れてきたら自分好みにカスタマイズしていきましょう。</p>
</div>

<style>
.next-step-box {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 1.5rem;
  border-radius: 10px;
  margin-top: 2rem;
}

.next-step-box h3 {
  margin-top: 0;
  color: white;
}
</style>