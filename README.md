# 経穴ビー玉ソリティア - 361穴学習ゲーム 🎮

WHO標準化361経穴を楽しく学べる教育ゲーム（PWA対応）

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![PWA](https://img.shields.io/badge/PWA-Ready-orange)

## 🌟 特徴

- ✅ **361穴完全収録** - WHO標準化の全361経穴データベース
- 🎯 **ゲームで学習** - ビー玉ソリティアで楽しく経穴を覚える
- 📱 **PWA対応** - オフラインでも使える、インストール可能
- 🌐 **レスポンシブ** - スマホ・タブレット・PCに対応
- 🔍 **詳細情報** - 長押しで各経穴の位置・経絡・備考を表示
- ⚡ **高速動作** - 軽量でサクサク動く

## 🎮 遊び方

1. ビー玉を選択（短押し）
2. 移動先を選択して飛び越える
3. 飛び越えたビー玉が消える
4. 最後の1個を目指す
5. 長押しで経穴情報を表示

## 🚀 デモ

[**ライブデモを見る →**](https://your-vercel-app.vercel.app)

## 📦 収録データ

### 14経絡 361穴
- 手太陰肺経（11穴）
- 手陽明大腸経（20穴）
- 足陽明胃経（45穴）
- 足太陰脾経（21穴）
- 手少陰心経（9穴）
- 手太陽小腸経（19穴）
- 足太陽膀胱経（67穴）← 最多
- 足少陰腎経（27穴）
- 手厥陰心包経（9穴）
- 手少陽三焦経（23穴）
- 足少陽胆経（44穴）
- 足厥陰肝経（14穴）
- 督脈（28穴）
- 任脈（24穴）

## 🛠️ 技術スタック

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **PWA**: Service Worker, Web App Manifest
- **Data**: JSON形式の経穴データベース
- **Hosting**: Vercel
- **Version Control**: Git/GitHub

## 📥 インストール

### ローカル開発

```bash
# リポジトリをクローン
git clone https://github.com/yourusername/acupoint-solitaire.git
cd acupoint-solitaire

# ローカルサーバーで起動（例：Python）
python -m http.server 8000

# ブラウザで開く
open http://localhost:8000
```

### Vercelへのデプロイ

1. GitHubにリポジトリをプッシュ
2. [Vercel](https://vercel.com)にログイン
3. "New Project" → GitHubリポジトリを選択
4. "Deploy" をクリック
5. 完了！自動でデプロイされます

## 📁 プロジェクト構造

```
acupoint-solitaire/
├── index.html              # メインゲームファイル（PWA対応）
├── manifest.json           # PWAマニフェスト
├── sw.js                   # Service Worker
├── icon-192.svg            # アプリアイコン（小）
├── icon-512.svg            # アプリアイコン（大）
├── README.md               # このファイル
├── data/
│   ├── acupoints_361_dict.json    # 経穴データ（オブジェクト形式）
│   ├── acupoints_361_array.json   # 経穴データ（配列形式）
│   ├── acupoints_361_simple.json  # 経穴データ（シンプル版）
│   └── acupoints_361_full.json    # 経穴データ（完全版）
└── LICENSE                 # ライセンス
```

## 🔧 カスタマイズ

### データの更新
`acupoints_361_*.json`ファイルを編集して経穴データを更新できます。

### スタイルの変更
`index.html`内の`<style>`セクションでデザインをカスタマイズできます。

### ゲームルールの変更
JavaScriptセクションで難易度やルールを調整できます。

## 📱 PWA機能

- ✅ オフライン対応
- ✅ ホーム画面に追加可能
- ✅ アプリのような体験
- ✅ 高速キャッシング
- ✅ 自動更新

### インストール方法

**スマホ（iOS/Android）:**
1. ブラウザでサイトを開く
2. 「ホーム画面に追加」を選択
3. アプリとして起動可能

**PC（Chrome/Edge）:**
1. アドレスバーの「インストール」アイコンをクリック
2. アプリとして使用可能

## 🎓 教育用途

このゲームは以下の用途に最適です：

- 🏥 **鍼灸学生** - 試験対策、経穴の位置暗記
- 👨‍⚕️ **鍼灸師** - 知識の復習、継続学習
- 📚 **教育機関** - 授業の補助教材
- 🏋️ **セルフケア** - ツボの位置を学びたい一般の方

## 📄 ライセンス

MIT License - 自由に使用・改変・配布可能

## 🤝 コントリビューション

プルリクエスト歓迎！

1. このリポジトリをフォーク
2. 新しいブランチを作成 (`git checkout -b feature/amazing-feature`)
3. 変更をコミット (`git commit -m 'Add amazing feature'`)
4. ブランチにプッシュ (`git push origin feature/amazing-feature`)
5. プルリクエストを作成

## 📞 お問い合わせ

質問や提案があれば、Issueを作成してください。

## 🙏 謝辞

- WHO標準経穴位置データベース
- ペグソリティアゲームデザイン

---

**Made with ❤️ for Traditional Chinese Medicine Education**
