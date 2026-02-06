# 口コミ振り分けアプリ (kuchi-colle)

顧客の満足度に応じてレビュー先を振り分けるシンプルな1ページWebアプリ。

## 仕組み

- 評価 **5** or **4** → 外部レビューサイト（Googleマップ等）へ遷移
- 評価 **3以下** → Googleフォーム（非公開フィードバック）へ遷移

## セットアップ

1. `index.html` 内の `CONFIG` を編集

```js
const CONFIG = {
  storeName: '店舗名',
  highRatingUrl: 'https://g.page/r/xxx/review',
  lowRatingUrl: 'https://docs.google.com/forms/d/xxx',
};
```

2. ブラウザで `index.html` を開く、または静的サイトとしてデプロイ

## 技術スタック

- HTML / CSS / JavaScript（フレームワーク・外部ライブラリなし）
- 静的ファイルのみ（サーバー不要）
