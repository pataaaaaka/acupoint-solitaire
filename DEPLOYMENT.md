# 📦 GitHub + Vercel デプロイガイド

## 🚀 ステップバイステップ手順

### 1️⃣ GitHubリポジトリの作成

1. [GitHub](https://github.com)にログイン
2. 右上の「+」→「New repository」をクリック
3. リポジトリ情報を入力：
   - **Repository name**: `acupoint-solitaire`（お好みで変更可）
   - **Description**: `WHO標準361経穴を学べるビー玉ソリティアゲーム（PWA対応）`
   - **Public** または **Private** を選択
   - **Add a README file**: チェック不要（既にREADME.mdがあるため）
   - **Add .gitignore**: チェック不要（既に.gitignoreがあるため）
   - **Choose a license**: MIT を推奨
4. 「Create repository」をクリック

### 2️⃣ ローカルでGitを初期化してプッシュ

ダウンロードしたファイルを配置したフォルダで以下を実行：

```bash
# Gitの初期化
git init

# すべてのファイルを追加
git add .

# 最初のコミット
git commit -m "Initial commit: 361穴経穴ビー玉ソリティアゲーム（PWA対応）"

# GitHubリポジトリを追加（URLは自分のリポジトリに変更）
git remote add origin https://github.com/yourusername/acupoint-solitaire.git

# メインブランチに変更（必要な場合）
git branch -M main

# プッシュ
git push -u origin main
```

### 3️⃣ Vercelでデプロイ

1. [Vercel](https://vercel.com)にアクセス
2. 「Sign Up」でアカウント作成（GitHubアカウントで連携推奨）
3. ダッシュボードで「Add New...」→「Project」をクリック
4. 「Import Git Repository」セクションで：
   - GitHubリポジトリを検索
   - `acupoint-solitaire`を選択
   - 「Import」をクリック
5. プロジェクト設定：
   - **Framework Preset**: Other
   - **Root Directory**: `./`（デフォルト）
   - **Build Command**: 空欄（静的サイトなので不要）
   - **Output Directory**: 空欄
   - **Install Command**: 空欄
6. 「Deploy」をクリック

### 4️⃣ デプロイ完了！

- 数十秒でデプロイ完了
- Vercelが自動で生成したURLが表示されます（例：`https://acupoint-solitaire.vercel.app`）
- このURLでゲームにアクセス可能！

---

## 🔧 必要なファイル構成

デプロイには以下のファイルが必要です：

```
📁 プロジェクトルート/
├── 📄 index.html              ← メインファイル（必須）
├── 📄 manifest.json           ← PWAマニフェスト（必須）
├── 📄 sw.js                   ← Service Worker（必須）
├── 🖼️ icon-192.svg            ← アプリアイコン（必須）
├── 🖼️ icon-512.svg            ← アプリアイコン（必須）
├── 📄 vercel.json             ← Vercel設定（推奨）
├── 📄 README.md               ← 説明文書（推奨）
├── 📄 .gitignore              ← Git除外設定（推奨）
└── 📁 data/ （オプション）
    ├── 📄 acupoints_361_dict.json
    ├── 📄 acupoints_361_array.json
    ├── 📄 acupoints_361_simple.json
    └── 📄 acupoints_361_full.json
```

---

## ✅ デプロイ後の確認事項

### PWA動作確認

1. **Chrome DevToolsで確認**
   - F12でDevToolsを開く
   - 「Application」タブ
   - 左メニューの「Manifest」→ マニフェストが読み込まれているか確認
   - 「Service Workers」→ Service Workerが登録されているか確認

2. **モバイルでの確認**
   - スマホのブラウザでアクセス
   - 「ホーム画面に追加」が表示されるか確認
   - インストール後、オフラインでも動作するか確認

3. **Lighthouse スコア**
   - Chrome DevTools → 「Lighthouse」タブ
   - 「PWA」カテゴリをチェック
   - スコアを確認（目標：緑色の90点以上）

---

## 🔄 更新方法

ファイルを変更した後：

```bash
# 変更をステージング
git add .

# コミット
git commit -m "変更内容の説明"

# プッシュ
git push

# Vercelが自動で再デプロイします！
```

---

## 🌐 カスタムドメイン設定（オプション）

Vercelで独自ドメインを使う場合：

1. Vercelダッシュボードでプロジェクトを開く
2. 「Settings」→「Domains」
3. 「Add Domain」で独自ドメインを入力
4. DNS設定の指示に従う
5. 完了！

---

## 🐛 トラブルシューティング

### デプロイが失敗する場合

1. **ファイル構成を確認**
   - `index.html`がルートディレクトリにあるか
   - ファイル名が正確か（大文字小文字に注意）

2. **vercel.jsonの確認**
   - JSON形式が正しいか
   - 不要なカンマがないか

3. **GitHubへのプッシュ確認**
   - `git status`で状態確認
   - `git log`でコミット履歴確認

### PWAがインストールできない場合

1. **HTTPSが必要**
   - Vercelは自動でHTTPSを提供するので問題なし
   - ローカル開発時は`localhost`であればOK

2. **manifest.jsonの確認**
   - JSONが正しいか
   - アイコンファイルが存在するか

3. **Service Workerの確認**
   - `sw.js`が正しく配置されているか
   - ブラウザのコンソールにエラーがないか

---

## 📞 サポート

問題が解決しない場合：

- [Vercel Documentation](https://vercel.com/docs)
- [GitHub Issues](https://github.com/yourusername/acupoint-solitaire/issues)

---

**Happy Deploying! 🚀**
