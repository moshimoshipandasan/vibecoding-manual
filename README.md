# 📚 Vibecoding スタートガイド - マニュアルプロジェクト

プログラミング初心者向けのVibecoding入門マニュアルです。
このリポジトリはMarkdownで書かれたドキュメントを、GitHub ActionsでJekyllビルドし、同一リポジトリの`gh-pages`ブランチで自動公開する仕組みになっています。

## 🏗️ アーキテクチャ

```
[main ブランチ] → [GitHub Actions] → [gh-pages ブランチ] → [GitHub Pages]
ソースコード         Jekyll Build      ビルド済みHTML        公開サイト
```

## 🚀 セットアップ手順

### 1. リポジトリのクローンまたはフォーク

```bash
git clone https://github.com/YOUR_USERNAME/vibecoding-manual.git
cd vibecoding-manual
```

### 2. GitHub Pages の設定

1. GitHubリポジトリの **Settings** タブを開く
2. 左メニューから **Pages** を選択
3. **Source** で **Deploy from a branch** を選択
4. **Branch** で **gh-pages** / **/ (root)** を選択
5. **Save** をクリック

### 3. 初回デプロイの実行

mainブランチへのプッシュで自動デプロイが開始されます：

```bash
git add .
git commit -m "Update content"
git push origin main
```

または、GitHub Actionsから手動実行：
1. **Actions** タブを開く
2. **Build and Deploy to GitHub Pages** を選択
3. **Run workflow** をクリック

## 📝 コンテンツの更新方法

### ローカルで編集
```bash
# 1. 変更を加える
vim getting-started/windows-setup.md

# 2. コミット
git add .
git commit -m "Update Windows setup guide"

# 3. プッシュ（自動デプロイが開始）
git push origin main
```

### GitHub上で直接編集
1. GitHubのWebインターフェースでファイルを編集
2. 「Commit changes」をクリック
3. 自動的にデプロイが開始されます

## 🔧 ローカル開発環境

### Jekyllをローカルで実行
```bash
# 依存関係をインストール
bundle install

# 開発サーバーを起動
bundle exec jekyll serve

# ブラウザで確認
# http://localhost:4000
```

## 📁 ディレクトリ構造

```
vibecoding-manual/
├── _config.yml              # Jekyll設定
├── index.md                 # ホームページ
├── getting-started/         # ガイドセクション
│   ├── prerequisites.md     # 前提条件
│   ├── windows-setup.md     # Windows向け
│   ├── mac-setup.md        # Mac向け
│   └── first-project.md    # 初めてのプロジェクト
├── .github/
│   └── workflows/
│       └── deploy.yml      # 自動デプロイ設定
├── Gemfile                 # Ruby依存関係
└── README.md              # このファイル
```

## 🎨 カスタマイズ

### テーマの変更
`_config.yml` の `theme` を変更:

```yaml
theme: jekyll-theme-minimal  # 現在
# theme: just-the-docs       # ドキュメント特化型
# theme: jekyll-theme-cayman # シンプルで美しい
```

### ナビゲーションの追加
`_config.yml` の `navigation` セクションに追加:

```yaml
navigation:
  - title: 新しいセクション
    url: /new-section/
```

## 🐛 トラブルシューティング

### ビルドが失敗する
- Actionsタブでエラーログを確認
- Gemfileの依存関係を確認
- Jekyll設定の構文エラーをチェック

### ページが404になる
- リポジトリがパブリックか確認
- GitHub Pages が有効か確認（Settings → Pages）
- gh-pagesブランチが存在するか確認
- ビルドが成功しているか確認
- 数分待ってから再度アクセス

### GitHub Actions エラー
- permissions設定を確認
- GITHUB_TOKENが正しく使用されているか確認
- ワークフローファイルの構文を確認

## 📖 リソース

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/pages)
- [GitHub Actions Documentation](https://docs.github.com/actions)

## 📄 ライセンス

このプロジェクトは教育目的で作成されています。
自由に使用、改変、配布してください。

## 🤝 コントリビューション

改善提案やバグ報告は Issues からお願いします。
プルリクエストも歓迎です！

---

**公開URL**: `https://YOUR_USERNAME.github.io/vibecoding-manual/`