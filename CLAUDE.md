# みんなの買取 LP制作

## このリポジトリについて
Claude Codeを使ってみんなの買取のLPを制作するためのリポジトリです。

## 読み込み順序（必ず守ること）
LPを生成する前に、以下の順番でファイルを読み込むこと。

1. `references/design-system.md`   ← Layer 1: デザインシステム（固定）
2. `references/lp-structure.md`    ← Layer 2: toB LP構造（固定）
3. `references/content-source.md`  ← Layer 3: コンテンツ原稿（可変）

## 作業ルール
- 3つのファイルをすべて読んでからコードを生成すること
- content-source.md のテキストは一言一句変えずに使うこと
- design-system.md のカラー・フォント指定を必ず遵守すること
- lp-structure.md のセクション順序を変えないこと
- HTML / CSS / JS は index.html の1ファイルにまとめること

## 出力ファイル
- `index.html`（HTML + CSS + JS を1ファイルにまとめる）

## カラートークンの参照ルール
- カラーはすべて `references/tokens.json` を参照すること
- Figmaのバリアブルから書き出したJSONがそのまま入っている
- `Primitive` 配下の値は直接使用禁止
- `Semantic` 配下のトークン名をCSS変数名として実装に使うこと
- tokens.jsonにないカラーコードは使用禁止
