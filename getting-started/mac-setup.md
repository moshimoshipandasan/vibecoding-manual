---
layout: default
title: Mac セットアップ
parent: 環境構築
nav_order: 3
permalink: /getting-started/mac-setup/
---

# 🍎 Mac セットアップガイド

macOS環境でVibecoding開発環境を構築する手順を説明します。

## 🛠️ Step 1: Homebrew のインストール（推奨）

Homebrewは、Macでソフトウェアを簡単にインストールできるパッケージマネージャーです。

### 1.1 Homebrewのインストール

ターミナルを開いて以下のコマンドを実行：

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

インストール中にパスワードを求められたら、Macのログインパスワードを入力してください。

### 1.2 インストールの確認

```bash
brew --version
```

✅ バージョン番号が表示されれば成功です！

## 📦 Step 2: Node.js のインストール

### 方法A: Homebrew を使用（推奨）

```bash
# Node.jsとnpmをインストール
brew install node

# インストール確認
node --version
npm --version
```

### 方法B: 公式インストーラーを使用

1. [Node.js 公式サイト](https://nodejs.org/) にアクセス
2. **「LTS」バージョン**（推奨版）をクリック
3. macOS用の `.pkg` ファイルをダウンロード
4. ダウンロードしたファイルをダブルクリック
5. インストーラーの指示に従って進める
6. インストール完了

### インストール確認

新しいターミナルウィンドウを開いて：

```bash
node --version
npm --version
```

## 🔧 Step 3: Git のインストールと設定

### 3.1 Git のインストール確認

macOSには通常Gitがプリインストールされています：

```bash
git --version
```

もしインストールされていない場合は、以下のいずれかの方法でインストール：

#### 方法A: Xcode Command Line Tools（自動）

```bash
git --version
```
このコマンドを実行すると、自動的にインストールダイアログが表示されます。

#### 方法B: Homebrew を使用

```bash
brew install git
```

### 3.2 Git の初期設定

ユーザー情報を設定します（自分の情報に置き換えてください）：

```bash
git config --global user.name "あなたの名前"
git config --global user.email "your.email@example.com"
```

**例：**
```bash
git config --global user.name "Taro Yamada"
git config --global user.email "taro@example.com"
```

### 3.3 設定の確認

```bash
git config --list
```

## 🚀 Step 4: Vibecoding CLI ツールのインストール

### 4.1 gemini-cli のインストール

ターミナルで以下のコマンドを実行：

```bash
npm install -g @genkit-ai/cli
```

インストール確認：
```bash
genkit --version
```

### 4.2 codex-cli のインストール

```bash
npm install -g @vibecoding/codex-cli
```

インストール確認：
```bash
codex --version
```

> ⚠️ **権限エラーが出る場合の対処法**

npmのグローバルインストールで権限エラーが出る場合：

**解決方法1: npmのプレフィックスを変更**
```bash
# npmのディレクトリを作成
mkdir ~/.npm-global

# npmの設定を変更
npm config set prefix '~/.npm-global'

# パスを追加（zshの場合）
echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.zshrc
source ~/.zshrc

# bashの場合
echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.bash_profile
source ~/.bash_profile
```

その後、再度インストールコマンドを実行してください。

## 🎨 Step 5: 開発環境の最終確認

すべてのツールが正しくインストールされているか確認しましょう：

```bash
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

### command not found エラー

**原因**: パスが通っていない

**解決方法**:
1. シェルの設定ファイルを確認：
   ```bash
   echo $SHELL  # 使用中のシェルを確認
   ```

2. zshの場合：
   ```bash
   echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.zshrc
   source ~/.zshrc
   ```

3. bashの場合：
   ```bash
   echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile
   source ~/.bash_profile
   ```

### Homebrew の警告メッセージ

**解決方法**:
```bash
# Homebrewを最新版に更新
brew update

# 問題を診断
brew doctor
```

診断結果に従って修正を行ってください。

### macOS のセキュリティ警告

「開発元が未確認のため開けません」というエラーが出る場合：

**解決方法**:
1. システム環境設定 → セキュリティとプライバシー
2. 「一般」タブ
3. 「このまま開く」をクリック

## ✅ セットアップ完了！

おめでとうございます！Mac環境でのVibecoding開発環境の構築が完了しました。

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