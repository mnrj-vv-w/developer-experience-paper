# Contributing Guidelines

本プロジェクトへの貢献ガイドラインです。

## 🎯 プロジェクトの目的

本論考は、開発者体験（Developer Experience）の改善を目的とした提言書です。VCの短期圧力が生む構造的問題を分析し、「クッション層」による解決策を提案します。

## 📝 貢献の種類

### 歓迎する貢献

- ✅ 誤字・脱字の修正
- ✅ 事実誤認の指摘と修正
- ✅ 追加データ・事例の提供
- ✅ 翻訳（英語版等）
- ✅ 図表の改善
- ✅ 文章表現の改善提案

### 慎重に検討する貢献

- ⚠️ 論旨の大幅な変更
- ⚠️ セクションの追加・削除
- ⚠️ 主張の根本的な修正

## 🔄 貢献プロセス

### 1. Issue を立てる

変更内容が大きい場合は、まず Issue で議論してください。
```
タイトル例:
- [誤字] セクション3のTRON年代表記
- [提案] VCへの問いかけセクションの表現改善
- [データ] 追加の統計情報
```

### 2. Branch を作成
```bash
git checkout -b fix/typo-section-3
git checkout -b feat/add-english-version
git checkout -b refactor/improve-section-5
```

### 3. 変更を加える

- コミット規約に従う（[COMMIT_CONVENTIONS.md](COMMIT_CONVENTIONS.md) 参照）
- 意味のある単位でコミット
- コミットメッセージは日本語でも英語でもOK

### 4. Pull Request を作成
```markdown
## 変更内容

- セクション3のTRON開始年を1984年に修正

## 理由

公式ドキュメントによると正確には1984年

## 影響範囲

- article/sections/03-tron-linux.md
- article/main.md
```

### 5. レビュー・マージ

- メンテナが確認
- 必要に応じて修正
- 承認後マージ

## 📊 データ提供について

プラットフォーム変更の記録やアンケート結果など、データの提供を歓迎します。

形式：
```
/data/
  platform-changes/
    YYYY-MM-platform-name.json
  surveys/
    YYYY-MM-description.csv
```

## 🌐 翻訳について

英語版などの翻訳を歓迎します。

配置：
```
/translations/
  en/
    main.md
    sections/
```

翻訳時の注意：
- 文化的文脈の調整は許可
- 主張の本質は変えない
- ローカライズは推奨（例: 米国のVC事例追加）

## 🚫 禁止事項

- ❌ 攻撃的・侮辱的な表現
- ❌ 特定企業・個人への誹謗中傷
- ❌ 事実に基づかない主張
- ❌ 著作権侵害

## 📧 連絡先

質問・相談は Issue または以下へ：
- GitHub: @mnrj-vv-w
- Email: mnrj.vv@gmail.com

---

**ご協力ありがとうございます！**