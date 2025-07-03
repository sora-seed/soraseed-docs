# SoraSeed Documentation

このリポジトリは、ドローンシミュレータ「DSim」のユーザードキュメントを Nextra でホスティングするためのサイトプロジェクトです。

## 開発環境のセットアップ

```bash
# 依存パッケージのインストール
pnpm install  # または npm install / yarn install

# 開発サーバーの起動
pnpm dev      # http://localhost:3000 でプレビュー
```

## ディレクトリ構成

| パス | 役割 |
|------|------|
| `docs/` | 各種ドキュメント (`.mdx`) を配置するルート |
| `theme.config.tsx` | Nextra テーマ設定 |
| `next.config.js` | Next.js + Nextra 設定 |

## デプロイ
Vercel にプッシュするだけで自動ビルド・デプロイされます。 

## ドキュメント目次

| 章 | ページ |
|----|--------|
| 概要 | [/docs](./docs) |
| システム要件 | [/docs/requirements](./docs/requirements) |
| コントローラー | [/docs/features/controller](./docs/features/controller) |
| 飛行準備 | [/docs/usage/preparation](./docs/usage/preparation) |
| 操作方法 | [/docs/usage/operation](./docs/usage/operation) |
| 画面構成 | [/docs/features/screen](./docs/features/screen) |
| 設定メニュー | [/docs/features/settings](./docs/features/settings) |
| ミッション | [/docs/features/mission](./docs/features/mission) | 