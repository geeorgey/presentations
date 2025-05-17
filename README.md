# 吉田丈治プレゼンテーションリポジトリ

このリポジトリは、吉田丈治が対外的に利用するプレゼンテーションをまとめるためのものです。各プレゼン資料はWebブラウザで閲覧できるHTMLファイルとして公開することを想定しています。

## フォルダ構成例

```
.
├── README.md          # このファイル
├── slides/            # プレゼンのMarkdownソースを格納
│   └── sample/        # プレゼンごとにディレクトリを作成
│       └── slides.md  # Markdown形式のスライド
└── docs/              # 生成されたHTMLを配置（GitHub Pages用）
```

- `slides/` 以下に各プレゼン用ディレクトリを作り、その中に `slides.md`（もしくは任意の名前のMarkdownファイル）を置きます。
- `docs/` ディレクトリには、Markdownから生成したHTMLファイルを配置します。GitHub Pages の公開ディレクトリとして設定すると、ブラウザから直接閲覧できます。

## プレゼンファイルの作成手順（Marp CLI利用例）

1. Node.js をインストールしておきます。
2. Marp CLI をグローバルインストールします。
   ```bash
   npm install -g @marp-team/marp-cli
   ```
3. `slides/<プレゼン名>/slides.md` に Markdown でスライドを記述します。例として `slides/sample/slides.md` を配置しています。
4. HTML を生成します。
   ```bash
   marp slides/<プレゼン名>/slides.md --html --output docs/<プレゼン名>.html
   ```
   これで `docs/` 以下に HTML ファイルが作成されます。
5. `marp -s slides/<プレゼン名>/slides.md` を実行すると、ローカルサーバーでプレビューしながら編集できます。

`docs/` フォルダを GitHub Pages の公開対象に設定することで、生成したHTMLをWeb上で簡単に共有できます。
