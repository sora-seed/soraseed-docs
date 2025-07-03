# SoraSeed Documentation


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

## 記述ルール

1. ドキュメントは日本語で執筆します。
2. 形式は **MDX (`.mdx`)** を使用し、Nextra によりレンダリングされることを前提とします。
3. 図やフローは **Mermaid**、データ列挙は **Markdown Table** を活用。
4. コンテンツは `docs/` フォルダにまとめます。
5. 外部・内部リンクは GFM 構文 (`[text](./path)`) を用い、パスは **相対指定** を原則とします。
6. 各ページの最上位は `# タイトル` を 1 つだけ置き、見出し階層で内容を整理してください。
7. 画像を利用する場合は `docs/images/`（または同階層の `images/`）に保存し、ファイル名は `kebab-case`、拡張子は `webp/png` を推奨。MDX では `![alt](./images/example.webp)` のように **相対パス** で参照します（Nextra が自動的に `<Image>` に変換）。
   - ページ固有の画像は **同じフォルダ内の `images/` サブフォルダ** に置くと可搬性が高くなる。
   - 複数ページで再利用するものは `docs/images/common/` へ置き、path を `../images/common/foo.webp` で指定。
   - **Next.js の最適化** を使いたい場合は `next.config.mjs` で `images.unoptimized=false` とし、相対パスのままで OK（Nextra が自動で `<Image>` に置換）。
8. Nextra の組み込みコンポーネント（例: `<Callout>`, `<Table>`）を積極的に利用し、一貫した UX を保ちます。 

---

## 使用できる記法サンプル

| 目的 | 記法例 | 備考 |
|------|--------|------|
| 見出し | `## セクション名` | `#` はページに 1 回まで |
| 段落改行 | 空行を 1 行挟む | Markdown 標準 |
| 強調 | `**強調**` / `*斜体*` | |
| 箇条書き | `- 項目` / `1. 番号付き` | ネストも可 |
| 表 | ```\n| 列1 | 列2 |\n|----|----|\n| a  | b  |\n``` | 自動で `<Table>` へ変換 |
| コードブロック | ```ts\nconsole.log('hello')\n``` | 言語指定でシンタックスハイライト |
| Callout (注目) | `<Callout emoji="💡">ポイント</Callout>` | Nextra 組み込み |
| Mermaid | ```mermaid\nflowchart LR; A-->B;\n``` | ダイアグラム描画 |
| 画像 | `![説明](./images/sample.webp)` | README のルール 7 を参照 |
| 内部リンク | `[準備](./usage/preparation)` | 相対パス |
| 外部リンク | `[Next.js](https://nextjs.org)` | 自動で ↗ 付与 |

> **Tip:** MDX では React コンポーネントを直接書けます。例えば `<Button />` やカスタム図表も利用可能です。 
