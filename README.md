# Personal Kakeibo Web

iOS・iPadOS向け個人用家計簿アプリ **Personal Kakeibo** の公式Webサイト・マーケティングページです。[EmDash](https://github.com/emdash-cms/emdash) CMSおよびAstroで構築されています。

## 特徴

- **Personal Kakeibo アプリの訴求・紹介**:
  - 3列ジャンル選択、長押し初期固定、00キー、ワンタップ全消去などの高速入力機能
  - ジャンル別の日額・月額予算設定とリアルタイム残額表示
  - 朝・昼・夕の最大3枠カスタムリマインダー通知
  - Swift Chartsによる月別・12か月推移の視覚的グラフ
  - SwiftDataローカル保存 & iCloud Private Database (CloudKit) による完全なプライバシー保護
  - CSVエクスポート & プレビュー付きJSONバックアップ/復元
- **EmDash CMS 統合**:
  - 管理画面（`/_emdash/admin`）からブロック単位（Hero、Features、Testimonials、Pricing、FAQ）のコンテンツ編集が可能
  - SQLiteローカルデータベース (`data.db`) と `seed/seed.json` によるスキーマ・コンテンツ管理
- **デザイン・UI**:
  - Appleデザインに親和性の高いエメラルド/ティール調のカラーパレット
  - 高精細 iPhone 16 Pro アプリUIモックアップイラスト (`hero-visual.svg`)
  - ライト / ダーク / システム自動切替対応のテーマスイッチャー

## ページ構成

| ページ | パス | 内容 |
|---|---|---|
| ホーム | `/` | ヒーロー、特徴一覧、設計思想、よくある質問 (FAQ) |
| 料金 | `/pricing` | 完全無料プラン（個人利用 / iCloud同期）と料金FAQ |
| お問い合わせ | `/contact` | GitHubリポジトリ、フィードバック、サポート窓口 |

## 開発・起動方法

```bash
# 依存関係のインストール
npm install

# シードデータの適用 (必要な場合)
npx emdash seed seed/seed.json --on-conflict=update

# 開発サーバーの起動 (ポート 4321)
npm run dev

# プロダクションビルド
npm run build

# プロダクションプレビュー起動
npm run start
```

- Webサイト: `http://localhost:4321`
- CMS管理画面: `http://localhost:4321/_emdash/admin`
