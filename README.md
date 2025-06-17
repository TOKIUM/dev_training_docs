# Dev Training Docs

Marpを使用した開発研修用ドキュメントリポジトリです。

## セットアップ

```bash
# 依存関係のインストール
npm install
```

## 使用方法

### スライドのビルド

```bash
# HTMLファイルとして出力
npm run build

# PDFファイルとして出力
npm run build:pdf

# PowerPointファイルとして出力
npm run build:pptx
```

### プレビュー

```bash
# ライブプレビューモードで起動
npm run preview
```

ブラウザで http://localhost:8080 にアクセスしてプレビューできます。

### ファイル管理

```bash
# 出力ファイルの削除
npm run clean
```

## ディレクトリ構造

```
dev_training_docs/
├── slides/           # Markdownスライドファイル
│   ├── sample.md     # サンプルスライド
│   └── dist/         # 出力ファイル（自動生成）
├── package.json      # プロジェクト設定
├── .marprc.yml       # Marp設定ファイル
└── README.md         # このファイル
```

## スライドの作成方法

1. `slides/` ディレクトリに `.md` ファイルを作成
2. 最初にFront Matterを設定:
   ```yaml
   ---
   marp: true
   theme: default
   class: lead
   paginate: true
   ---
   ```
3. `---` でスライドを区切りながらMarkdownで記述
4. `npm run build` でHTMLファイルを生成

## Marpの機能

- Markdown記法でスライド作成
- テーマのカスタマイズ
- 画像や図表の挿入
- コードブロックのシンタックスハイライト
- PDF/PowerPoint出力
- ライブプレビュー機能