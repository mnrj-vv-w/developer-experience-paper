# Commit Message Conventions

本プロジェクトのコミットメッセージ規約です。

## 📝 基本形式
```
<type>: <subject>

<body>（任意）

<footer>（任意）
```

## 🏷️ Type（必須）

### 主要なType

| Type | 説明 | 例 |
|------|------|-----|
| `feat` | 新機能・新セクション追加 | `feat: セクション8追加 - 海外事例` |
| `fix` | 誤字・事実誤認の修正 | `fix: TRONの開始年を1984年に修正` |
| `docs` | ドキュメント（README等） | `docs: CONTRIBUTINGに翻訳ガイド追加` |
| `refactor` | 表現の改善（内容は不変） | `refactor: セクション2の表現を強化` |
| `style` | フォーマット・空白等 | `style: 見出しレベルを統一` |
| `data` | データ追加・更新 | `data: 2024年11月のプラットフォーム変更記録` |
| `translate` | 翻訳 | `translate: 英語版セクション1-3完成` |
| `chore` | その他（ビルド、設定等） | `chore: .gitignore更新` |

### 補助的なType

| Type | 説明 |
|------|------|
| `perf` | パフォーマンス改善 |
| `test` | テスト追加・修正 |
| `revert` | コミットの取り消し |

## 📋 Subject（必須）

- 50文字以内推奨
- 命令形（「追加する」ではなく「追加」）
- 末尾にピリオド不要
- 日本語・英語どちらでもOK

### Good Examples
```
✅ fix: セクション3のTRON年代を修正
✅ feat: 英語版README追加
✅ refactor: VCへの問いかけを丁寧な表現に
✅ data: Stack Overflow 2024調査データ追加
```

### Bad Examples
```
❌ fix typo（何を修正したか不明）
❌ update（何を更新したか不明）
❌ セクション3を修正しました。（typeがない）
❌ feat: セクション3のTRONの記述について、開始年が1983年と書いてあったが正しくは1984年なので修正した（長すぎる）
```

## 📝 Body（任意）

詳細な説明が必要な場合に使用。

- 72文字で改行推奨
- 「なぜ」変更したかを記載
- 複数行OK

例：
```
fix: TRONの開始年を1984年に修正

TRON協会の公式資料によると、TRONプロジェクトの
開始は1984年。従来の記述（1983年）は誤りだった。

参考: https://www.tron.org/...
```

## 🔖 Footer（任意）

Issue番号等を記載。
```
Closes #123
Related to #456
```

## 🌳 Branch命名規約
```
<type>/<short-description>

例:
fix/typo-section-3
feat/add-english-version
refactor/improve-vc-section
data/2024-11-platform-changes
translate/en-sections-1-3
```

## 📊 実例集

### 記事内容の修正
```bash
# 誤字修正
git commit -m "fix: セクション2の誤字修正（開発社→開発者）"

# 事実修正
git commit -m "fix: RevenueCatの調達額を77億円に修正

Index Venturesからの累計調達額は77億円。
従来の記述（50億円）は古い情報だった。"

# 表現改善
git commit -m "refactor: セクション5のVCへの問いかけを柔らかい表現に"
```

### 新規追加
```bash
# セクション追加
git commit -m "feat: セクション8追加 - 欧米の先行事例"

# データ追加
git commit -m "data: 2024年11月App Store Connect変更記録"

# 翻訳
git commit -m "translate: 英語版セクション1-3完成"
```

### ドキュメント
```bash
# README更新
git commit -m "docs: READMEに引用ガイド追加"

# 新規ドキュメント
git commit -m "docs: CITATION.md作成 - 学術引用ガイド"
```

### その他
```bash
# フォーマット
git commit -m "style: Markdown見出しレベルを統一"

# 設定
git commit -m "chore: .gitignoreにmacOS一時ファイル追加"
```

## 🤝 複数の変更がある場合

できるだけ1コミット1変更を推奨。

やむを得ず複数の変更がある場合：
```
fix: 複数箇所の誤字修正

- セクション2: 開発社→開発者
- セクション4: 年間→年次
- セクション7: ジョズブ→ジョブズ
```

## 🚫 避けるべきパターン
```
❌ git commit -m "update"
❌ git commit -m "fix"
❌ git commit -m "いろいろ修正"
❌ git commit -m "WIP"（作業中はコミットしない）
❌ git commit -m "aaa"（意味不明）
```

## 📚 参考

この規約は以下に基づいています：
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Angular Commit Guidelines](https://github.com/angular/angular/blob/master/CONTRIBUTING.md)

---

**一貫性のあるコミット履歴が、プロジェクトの質を高めます。**