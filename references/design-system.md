# デザインシステム（固定）

## 0. コミュニケーション・プロトコル
- 使用言語: 日本語
- ターゲット: 法人・業者向け（toB）
- トーン: 信頼感・高級感・プロフェッショナル
- 推奨表現: 数値・実績・具体的なベネフィットを優先する
- 文体: です・ます調（敬体）
- 禁止事項: 影の使用禁止 / グラデーション禁止 / 過剰な装飾禁止
- ロゴ：`assets/logo.svg` を必ず参照すること


## 1. デザイナーとしての役割と使命
- 役割: このデザインシステムを忠実に実装するエンジニア兼デザイナーとして振る舞うこと
- 使命: みんなの買取のブランド価値を視覚的に最大化し、toBターゲットに信頼と安心を与えるLPを生成すること
- 優先順位:
  1. デザインシステムの仕様を遵守する
  2. LP構造（lp-structure.md）のセクション順を守る
  3. コンテンツ原稿（content-source.md）のテキストを一字一句変えない
- 品質基準:
  - 余白・フォントサイズ・カラーはすべてCSS変数で管理すること
  - レスポンシブ対応（768px以下）を必ず実装すること
  - アクセシビリティ（コントラスト比・alt属性）を確保すること
- 禁止事項: 独自判断でデザインを改変しない・未定義のカラーを使用しない

## 2. カラーパレット
- `references/tokens.json` を参照すること
- Figmaのバリアブルから書き出したJSONがそのまま入っている
- `Primitive` 配下の値は直接使用禁止
- `Semantic` 配下のトークン名をCSS変数名として実装に使うこと
- tokens.jsonにないカラーコードは使用禁止

## 3. タイポグラフィ

### フォントファミリー
- 見出し: 'LINESeedJP_OTF', 'Noto Sans JP', sans-serif
- 本文: 'Noto Sans JP', sans-serif

### フォントサイズ規定
| 要素 | PC | SP |
|------|----|----|
| h1（FVメインコピー） | 56px | 32px |
| h2（セクション見出し） | 40px | 28px |
| h3（カード見出し） | 24px | 20px |
| 本文 | 16px | 15px |
| 補足・キャプション | 14px | 13px |

### font-weight
- 見出し: 700
- 強調: 600
- 本文: 400

### 行間・字間
- 見出し: line-height 1.3 / letter-spacing 0.05em
- 本文: line-height 1.8 / letter-spacing 0.02em

## 4. スペーシング（余白体系）
| トークン名 | 値 | 主な用途 |
|-----------|----|----|
| --space-xs | 8px | 要素内の小余白 |
| --space-sm | 16px | 要素間の小余白 |
| --space-md | 32px | コンポーネント間 |
| --space-lg | 64px | セクション内余白 |
| --space-xl | 96px | セクション間余白 |
| --space-xxl | 128px | ページトップ余白 |

## 5. ボタン

### メインCTA
- 背景: Semantic.UI.Accent.CTA の値を使用
- テキスト: Semantic.UI.Text.on-dark の値を使用
- padding: 16px 40px
- font-weight: 700
- border-radius: 0px
- ホバー: Semantic.UI.Accent.CTAHover の値を使用

### セカンダリボタン（ゴースト型）
- 背景: transparent
- border: 1px solid Semantic.UI.Accent.CTA
- テキスト: Semantic.UI.Accent.CTA
- ホバー: 背景をSemantic.UI.Accent.CTAに、テキストをSemantic.UI.Text.on-darkに

## 6. カードコンポーネント
- 背景: Semantic.UI.Background.Dark の値を使用
- border: 1px solid Semantic.UI.Border の値を使用
- border-radius: 0px
- padding: 32px
- ホバー: border-color を Semantic.UI.Accent.CTA に変化

## 7. コンテンツ幅・レイアウト
- 最大幅: 1200px
- 左右padding（PC）: 40px
- 左右padding（SP）: 20px
- ブレークポイント: 768px（PC/SP切り替え）

## 8. ヒーローセクションの絶対ルール
- 背景色: Semantic.UI.Background.Dark
- 高さ: min-height 100vh（画面全体を必ず埋めること）
- レイアウト: 左コピー・CTA / 右ビジュアル（2カラム）/ SP時は縦積み
- メインCTA: Semantic.UI.Accent.CTAのbtn-primaryを必ず左側に配置
- テキスト色: 見出し Semantic.UI.Text.on-dark / サブコピー Semantic.UI.Text.secondary

## 9. ビジュアル規定
### イラストスタイル
### 写真トーン

## 10. アニメーション・インタラクション
- トランジション: all 0.3s ease
- スクロールアニメーション: fadeInUp（opacity 0→1 / translateY 20px→0）
- 対象: セクション見出し・カード・ボタン

## 11. ヘッダー・フッター規定
### ヘッダー
- ロゴ：左端に配置ロゴを配置　/ 高さはPC：24px　SP：20px
- 背景色：Semantic.UI.Background.Dark / スクロール時も同色を維持
- PC時：高さ108px　/ 左ロゴ / 中央ナビメニュー（4項目）/ 右CTAボタン・高さ72px
- SP時：高さ58px　/　左ロゴ / 右ハンバーガーメニューアイコン（ナビは非表示）

### フッター
- 背景色：Semantic.UI.Background.Dark
- 文字色：Semantic.UI.Text.secondary
- ロゴ：左端に配置・ヘッダーと同じロゴ
- PC時：左ロゴ / 右に規約リンク群を横並び
- SP時：上ロゴ（中央揃え）/ 下に規約リンク群（中央揃え・縦積み）
- コピーライト：© 2025 みんなの買取 All Rights Reserved. / 中央揃え・最下部

## 12. 角丸の統一ルール
| 要素 | border-radius |
|------|--------------|
| ボタン | 0px |
| カード | 0px |
| 入力フィールド | 0px |
| バッジ・タグ | 0px |

## 13. フォーム入力フィールド
- 背景: Semantic.UI.Background.Dark
- border: 1px solid Semantic.UI.Border
- テキスト: Semantic.UI.Text.on-dark
- placeholder: Semantic.UI.Text.secondary
- focus: border-color を Semantic.UI.Accent.CTA に

## 14. 禁止事項
- box-shadow の使用禁止
- グラデーション（linear-gradient等）の使用禁止
- 白背景セクションの使用禁止
- 未定義のカラーコードの使用禁止
- Primitiveトークンの直接使用禁止（必ずSemantic経由で参照すること）
