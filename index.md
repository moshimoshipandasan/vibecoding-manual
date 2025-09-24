---
layout: home
title: Vibecoding スタートガイド
---

# 🎉 Vibecoding へようこそ！

このガイドは、プログラミング初心者の方でも **Vibecoding** を使って開発を始められるように作成されたクイックスタートマニュアルです。

## 📚 このガイドで学べること

- ✅ 開発環境の準備（Windows/Mac対応）
- ✅ 必要なツールのインストール方法
- ✅ Vibecoding プロジェクトの初期化
- ✅ 要件定義から開発スタートまでの流れ

## 🚀 クイックナビゲーション

### 1. 環境構築
開発を始める前の準備作業です。お使いのOSに合わせて進めてください。

<div class="quick-links">
  <a href="{{ site.baseurl }}/getting-started/prerequisites" class="button">
    📋 前提条件の確認
  </a>
  <a href="{{ site.baseurl }}/getting-started/windows-setup" class="button">
    🪟 Windows セットアップ
  </a>
  <a href="{{ site.baseurl }}/getting-started/mac-setup" class="button">
    🍎 Mac セットアップ
  </a>
</div>

### 2. 最初のプロジェクト
環境構築が完了したら、実際にプロジェクトを作成してみましょう。

<div class="quick-links">
  <a href="{{ site.baseurl }}/getting-started/first-project" class="button">
    🎯 プロジェクトを始める
  </a>
</div>

## 💡 Vibecoding とは？

Vibecoding は、AIの力を借りて効率的にコーディングを進めるための開発支援ツールです。以下の特徴があります：

- **対話型開発**: AIと対話しながら要件定義を進められます
- **自動生成**: 要件に基づいてコードを自動生成します
- **初心者にやさしい**: プログラミング知識が少なくても始められます

## 🎯 対象読者

このガイドは以下の方を対象としています：

- プログラミングを始めたばかりの初心者
- Vibecoding を初めて使う方
- 効率的な開発環境を構築したい方

## 📖 ガイドの進め方

1. **前提条件の確認**: お使いのPCで必要なツールが揃っているか確認します
2. **環境構築**: Node.js と Git をインストールします
3. **CLI ツール導入**: gemini-cli と codex-cli をインストールします
4. **プロジェクト開始**: `/init` コマンドで最初のプロジェクトを作成します

## 🆘 サポート

問題が発生した場合は、各セクションの「トラブルシューティング」を参照してください。

---

<div class="navigation-footer">
  <a href="{{ site.baseurl }}/getting-started/prerequisites" class="next-page">
    次へ: 前提条件の確認 →
  </a>
</div>

<style>
.quick-links {
  display: flex;
  gap: 1rem;
  margin: 1rem 0;
  flex-wrap: wrap;
}

.quick-links .button {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  background-color: #0066cc;
  color: white;
  text-decoration: none;
  border-radius: 5px;
  transition: background-color 0.3s;
}

.quick-links .button:hover {
  background-color: #0052a3;
}

.navigation-footer {
  margin-top: 3rem;
  padding-top: 2rem;
  border-top: 1px solid #e0e0e0;
  text-align: right;
}

.next-page {
  display: inline-block;
  padding: 0.5rem 1rem;
  background-color: #28a745;
  color: white;
  text-decoration: none;
  border-radius: 3px;
}

.next-page:hover {
  background-color: #218838;
}
</style>