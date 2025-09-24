---
layout: default
title: Windows セットアップ
parent: 環境構築
nav_order: 3
permalink: /getting-started/windows-setup/
---

# 🪟 Windows セットアップガイド

Windows環境でVibecoding開発環境を構築する手順を説明します。

## 📦 Step 1: Node.js のインストール

### 1.1 インストーラーのダウンロード

1. [Node.js 公式サイト](https://nodejs.org/) にアクセス
2. **「LTS」バージョン**（推奨版）をクリック
3. ダウンロードが自動的に開始されます

> 💡 **LTS版を選ぶ理由**: 長期サポート版で安定性が高く、初心者に最適です

### 1.2 インストール手順

1. ダウンロードした `node-vXX.XX.X-x64.msi` をダブルクリック
2. インストーラーが起動したら「Next」をクリック
3. ライセンス同意画面で「I accept...」にチェックを入れて「Next」
4. インストール先はデフォルトのままで「Next」
5. **重要**: 「Automatically install the necessary tools...」にチェックを入れる
6. 「Install」をクリック
7. 管理者権限を求められたら「はい」を選択
8. インストール完了後、「Finish」をクリック

### 1.3 インストールの確認

PowerShell または コマンドプロンプトを**新しく開いて**以下を実行：

```powershell
node --version
npm --version
```

✅ バージョン番号が表示されれば成功です！

## 🔧 Step 2: Git のインストール

### 2.1 Git for Windows のダウンロード

1. [Git for Windows](https://git-scm.com/download/win) にアクセス
2. 「Download」ボタンをクリック
3. ダウンロードが開始されます

### 2.2 インストール手順

1. ダウンロードした `Git-X.XX.X-64-bit.exe` をダブルクリック
2. インストーラーが起動したら「Next」をクリック
3. インストール先はデフォルトのままで「Next」
4. コンポーネント選択画面：
   - ✅ 「Git Bash Here」にチェック
   - ✅ 「Git GUI Here」にチェック
   - 「Next」をクリック
5. デフォルトエディタの選択：
   - 初心者は「Use Notepad as Git's default editor」を選択
   - 「Next」をクリック
6. 残りの設定はすべてデフォルトのまま「Next」を連続クリック
7. 「Install」をクリック
8. 「Finish」をクリック

### 2.3 Git の初期設定

PowerShell を開いて以下のコマンドを実行（自分の情報に置き換えてください）：

```powershell
git config --global user.name "あなたの名前"
git config --global user.email "your.email@example.com"
```

**例：**
```powershell
git config --global user.name "Taro Yamada"
git config --global user.email "taro@example.com"
```

### 2.4 設定の確認

```powershell
git config --list
```

自分の名前とメールアドレスが表示されれば成功です！

## 🚀 Step 3: Vibecoding CLI ツールのインストール

### 3.1 gemini-cli のインストール

PowerShell で以下のコマンドを実行：

```powershell
npm install -g @genkit-ai/cli
```

インストール確認：
```powershell
genkit --version
```

### 3.2 codex-cli のインストール

```powershell
npm install -g @vibecoding/codex-cli
```

インストール確認：
```powershell
codex --version
```

> ⚠️ **権限エラーが出る場合**: PowerShellを**管理者として実行**してから再度試してください
> - Windowsキーを右クリック
> - 「Windows PowerShell (管理者)」を選択

## 🎨 Step 4: 開発環境の最終確認

すべてのツールが正しくインストールされているか確認しましょう：

```powershell
# Node.js の確認
node --version

# npm の確認
npm --version

# Git の確認
git --version

# gemini-cli の確認
genkit --version

# codex-cli の確認
codex --version
```

すべてのコマンドでバージョン番号が表示されれば、環境構築は完了です！

## 🆘 トラブルシューティング

### npm コマンドが認識されない

**解決方法：**
1. PowerShellを再起動
2. それでもダメな場合は、PCを再起動
3. 環境変数PATHにNode.jsのパスが追加されているか確認

### 権限エラー (EACCES/EPERM)

**解決方法：**
PowerShellを管理者権限で実行：
1. Windowsキーを右クリック
2. 「Windows PowerShell (管理者)」を選択
3. コマンドを再実行

### ウイルス対策ソフトの警告

一部のウイルス対策ソフトはnpmパッケージのインストールを妨げることがあります。

**解決方法：**
1. 一時的にリアルタイム保護を無効化
2. インストールを実行
3. インストール後、保護を再度有効化

## ✅ セットアップ完了！

おめでとうございます！Windows環境でのVibecoding開発環境の構築が完了しました。

<div class="next-step-box">
  <h3>🎯 次のステップ</h3>
  <p>環境構築が完了したら、最初のプロジェクトを作成してみましょう！</p>
  <a href="{{ site.baseurl }}/getting-started/first-project" class="start-button">
    最初のプロジェクトを始める →
  </a>
</div>

<style>
.next-step-box {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 2rem;
  border-radius: 10px;
  margin-top: 3rem;
  text-align: center;
}

.next-step-box h3 {
  margin-top: 0;
  font-size: 1.5rem;
}

.start-button {
  display: inline-block;
  background-color: white;
  color: #667eea;
  padding: 0.75rem 2rem;
  border-radius: 25px;
  text-decoration: none;
  font-weight: bold;
  margin-top: 1rem;
  transition: transform 0.3s;
}

.start-button:hover {
  transform: translateY(-2px);
}
</style>