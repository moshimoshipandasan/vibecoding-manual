# 📚 Vibecoding スタートガイド - マニュアルプロジェクト

プログラミング初心者向けのVibecoding入門マニュアルです。
このリポジトリはMarkdownで書かれたドキュメントを、GitHub ActionsでJekyllビルドし、GitHub Pagesで自動公開する仕組みになっています。

## 🏗️ アーキテクチャ

```
[ソースリポジトリ] → [GitHub Actions] → [ビルドリポジトリ] → [GitHub Pages]
vibecoding-manual      Jekyll Build     vibecoding-manual-site   公開サイト
```

## 🚀 セットアップ手順

### 1. リポジトリの作成

#### 1.1 ソースリポジトリ
1. GitHubで `vibecoding-manual` という名前の**パブリック**リポジトリを作成
2. このプロジェクトのファイルをプッシュ

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/vibecoding-manual.git
git push -u origin main
```

#### 1.2 ビルドリポジトリ
1. GitHubで `vibecoding-manual-site` という名前の**パブリック**リポジトリを作成
2. 初期化は不要（GitHub Actionsが自動で行います）

### 2. Personal Access Token (PAT) の設定

#### 2.1 PATの作成
1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. 「Generate new token」をクリック
3. 名前: `DEPLOY_TOKEN`
4. 有効期限: お好みで設定
5. スコープ: `repo` にチェック
6. 「Generate token」をクリック
7. **トークンをコピー**（この画面を離れると二度と見られません！）

#### 2.2 Secretsに登録
1. ソースリポジトリ（vibecoding-manual）の Settings → Secrets and variables → Actions
2. 「New repository secret」をクリック
3. Name: `DEPLOY_TOKEN`
4. Secret: コピーしたトークンを貼り付け
5. 「Add secret」をクリック

### 3. GitHub Pages の設定

#### 3.1 ビルドリポジトリでPages有効化
1. `vibecoding-manual-site` リポジトリの Settings → Pages
2. Source: Deploy from a branch
3. Branch: `main` / `/ (root)`
4. 「Save」をクリック

### 4. 自動デプロイの実行

1. ソースリポジトリの Actions タブを確認
2. ワークフローが自動実行されているか確認
3. 初回は手動実行も可能:
   - Actions → Build and Deploy to GitHub Pages → Run workflow

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
- GitHub Pages が有効か確認
- ビルドが成功しているか確認
- 数分待ってから再度アクセス

### Personal Access Tokenエラー
- トークンの有効期限を確認
- `repo` スコープが有効か確認
- Secretsに正しく登録されているか確認

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

**公開URL**: `https://YOUR_USERNAME.github.io/vibecoding-manual-site/`