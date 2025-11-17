# Workflow Guide

本プロジェクトの作業フロー・運用ルールです。

## 🗂️ ディレクトリ構造
```
developer-experience-paper/
├── article/          # 記事本体
├── assets/           # 図表・データ
├── translations/     # 翻訳版
├── versions/         # バージョン履歴
├── drafts/           # 下書き・メモ
├── publication/      # プラットフォーム別版
└── docs/             # ドキュメント
```

## 📝 編集ワークフロー

### 軽微な修正（誤字等）
```bash
# 1. 直接mainで編集
git checkout main
vim article/sections/03-tron-linux.md

# 2. コミット
git add article/sections/03-tron-linux.md
git commit -m "fix: セクション3の誤字修正"

# 3. プッシュ
git push origin main
```

### 大きな変更（セクション追加等）
```bash
# 1. ブランチ作成
git checkout -b feat/add-section-8

# 2. 編集
vim article/sections/08-new-section.md

# 3. コミット（複数回OK）
git add article/sections/08-new-section.md
git commit -m "feat: セクション8のドラフト作成"

git add article/sections/08-new-section.md
git commit -m "refactor: セクション8の表現改善"

# 4. mainにマージ
git checkout main
git merge feat/add-section-8

# 5. プッシュ
git push origin main

# 6. ブランチ削除
git branch -d feat/add-section-8
```

## 📊 データ管理

### プラットフォーム変更の記録
```bash
# 1. データファイル作成
cat > assets/data/platform-changes/2024-11-app-store-connect.json << EOF
{
  "date": "2024-11-15",
  "platform": "App Store Connect",
  "change_type": "UI",
  "description": "ダッシュボードのレイアウト変更",
  "impact": "high",
  "documentation_updated": false
}
EOF

# 2. コミット
git add assets/data/platform-changes/2024-11-app-store-connect.json
git commit -m "data: App Store Connect 2024年11月変更記録"
```

### アンケートデータ
```
assets/data/surveys/2024-11-developer-satisfaction.csv
```

形式：
```csv
date,platform,satisfaction_score,comment
2024-11-15,App Store Connect,2,UI変更が頻繁すぎる
2024-11-16,Expo EAS,3,ドキュメントが古い
```

## 🌐 翻訳ワークフロー

### 英語版作成
```bash
# 1. ブランチ作成
git checkout -b translate/en-sections-1-3

# 2. 翻訳ファイル作成
mkdir -p translations/en/sections
vim translations/en/sections/01-intro.md

# 3. コミット
git add translations/en/sections/01-intro.md
git commit -m "translate: 英語版セクション1完成"

# 4. 繰り返し
# ...

# 5. mainにマージ
git checkout main
git merge translate/en-sections-1-3
```

## 📋 バージョン管理

### 公開時のバージョン作成
```bash
# 1. 現在の状態をコピー
cp article/main.md versions/v1.0-initial.md

# 2. コミット
git add versions/v1.0-initial.md
git commit -m "chore: v1.0公開版をアーカイブ"

# 3. タグ作成
git tag -a v1.0 -m "初回公開版"
git push origin v1.0
```

### バージョン番号ルール

- **Major（1.x.x）**: 構造的な大幅変更
  - 例: セクション追加、論旨変更
- **Minor（x.1.x）**: 内容の拡充
  - 例: データ追加、事例追加
- **Patch（x.x.1）**: 軽微な修正
  - 例: 誤字修正、表現改善

## 🚀 公開ワークフロー

### note/Zenn公開時
```bash
# 1. プラットフォーム別ファイル作成
cp article/main.md publication/note-version.md
vim publication/note-version.md  # リード文追加等

# 2. コミット
git add publication/note-version.md
git commit -m "docs: note公開版作成"

# 3. 実際に公開

# 4. 公開記録
echo "- 2024-11-17: note公開 https://note.com/..." >> CHANGELOG.md
git add CHANGELOG.md
git commit -m "docs: note公開を記録"
```

## 🔄 定期メンテナンス

### 月次レビュー
```bash
# データの確認
ls assets/data/platform-changes/

# 統計の更新
# （必要に応じて）

# CHANGELOGの更新
vim CHANGELOG.md
```

### 四半期レビュー

- 記事内容の見直し
- 古くなった情報の更新
- 新しいデータの追加

## 🤝 コラボレーション

### 外部からの貢献受け入れ

1. Issue確認
2. 議論
3. Pull Request レビュー
4. 承認・マージ
5. 貢献者に感謝

### レビュー基準

- ✅ 事実の正確性
- ✅ 論旨の一貫性
- ✅ 表現の適切性
- ✅ コミット規約の遵守

## 📧 コミュニケーション

- GitHub Issue: 技術的議論
- Email: 個別相談
- X (Twitter): 公開討論

---

**効率的な運用で、プロジェクトの質を維持します。**