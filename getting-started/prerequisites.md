---
layout: default
title: 前提条件の確認
parent: 環境構築
nav_order: 1
permalink: /getting-started/prerequisites/
---

# 📋 前提条件の確認

Vibecoding を使い始める前に、お使いのPCに必要なツールがインストールされているか確認しましょう。

## 🔍 確認が必要なツール

1. **Node.js** (バージョン 16.0 以上)
2. **Git** (バージョン 2.0 以上)

## 📊 現在の環境を確認する

### Node.js のバージョン確認

ターミナル（コマンドプロンプト）を開いて、以下のコマンドを実行してください：

```bash
node --version
```

**期待される出力例：**
```
v18.17.0
```

✅ **成功**: `v16.0.0` 以上のバージョンが表示されればOKです
❌ **失敗**: コマンドが認識されない、または古いバージョンの場合はインストールが必要です

### Git のバージョン確認

同じくターミナルで以下のコマンドを実行します：

```bash
git --version
```

**期待される出力例：**
```
git version 2.42.0
```

✅ **成功**: `2.0.0` 以上のバージョンが表示されればOKです
❌ **失敗**: コマンドが認識されない場合はインストールが必要です

## 🖥️ ターミナルの開き方

### Windows の場合

以下のいずれかの方法でターミナルを開けます：

1. **コマンドプロンプト**
   - `Windows キー + R` を押す
   - `cmd` と入力して Enter

2. **PowerShell** (推奨)
   - `Windows キー + X` を押す
   - 「Windows PowerShell」を選択

3. **Windows Terminal** (Windows 11)
   - `Windows キー` を押す
   - 「Terminal」と入力して Enter

### Mac の場合

1. **ターミナル**
   - `Command + Space` を押す（Spotlight検索）
   - 「Terminal」または「ターミナル」と入力
   - Enter キーを押す

2. **または**
   - Finder を開く
   - アプリケーション → ユーティリティ → ターミナル

## ⚠️ トラブルシューティング

### 「コマンドが見つかりません」エラーが出る場合

このエラーは、ツールがインストールされていないか、パスが通っていないことを示しています。

**解決方法：**
- お使いのOSに応じたセットアップガイドに進んでください
- [Windows セットアップ](/getting-started/windows-setup)
- [Mac セットアップ](/getting-started/mac-setup)

### バージョンが古い場合

既にインストール済みでもバージョンが古い場合は、アップデートが必要です。セットアップガイドでアップデート方法を説明しています。

## 📝 チェックリスト

インストール作業に進む前に、以下を確認してください：

- [ ] ターミナル（コマンドプロンプト）を開ける
- [ ] Node.js のバージョンを確認した
- [ ] Git のバージョンを確認した
- [ ] 必要に応じてインストールまたはアップデートが必要か判断した

## 🎯 次のステップ

環境確認が完了したら、お使いのOSに応じてセットアップを進めましょう：

<div class="navigation-buttons">
  <a href="{{ site.baseurl }}/getting-started/windows-setup" class="os-button windows">
    🪟 Windows セットアップへ進む
  </a>
  <a href="{{ site.baseurl }}/getting-started/mac-setup" class="os-button mac">
    🍎 Mac セットアップへ進む
  </a>
</div>

<style>
.navigation-buttons {
  display: flex;
  gap: 1rem;
  margin: 2rem 0;
  flex-wrap: wrap;
}

.os-button {
  flex: 1;
  min-width: 200px;
  padding: 1rem;
  text-align: center;
  border: 2px solid #ddd;
  border-radius: 8px;
  text-decoration: none;
  transition: all 0.3s;
  font-weight: bold;
}

.os-button.windows {
  background-color: #00bcf2;
  color: white;
  border-color: #00bcf2;
}

.os-button.windows:hover {
  background-color: #0099cc;
}

.os-button.mac {
  background-color: #555;
  color: white;
  border-color: #555;
}

.os-button.mac:hover {
  background-color: #333;
}
</style>