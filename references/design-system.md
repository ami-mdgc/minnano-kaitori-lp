# デザインシステム（固定）

## 0. 基本方針
- ターゲット: 法人・業者向け（toB）
- トーン: 信頼感・高級感・プロフェッショナル
- 禁止事項: 影の使用禁止 / グラデーション禁止 / 過剰な装飾禁止

## 1. カラーパレット
| トークン名 | カラーコード | 用途 |
|-----------|------------|------|
| --color-bg-primary | #0a0a0a | メイン背景 |
| --color-bg-secondary | #141414 | セクション背景 |
| --color-bg-card | #1a1a1a | カード背景 |
| --color-accent | #c9a84c | ゴールド：CTA・強調・見出しアクセント |
| --color-accent-light | #e8c97a | ゴールドホバー時 |
| --color-text-primary | #ffffff | メインテキスト |
| --color-text-secondary | #a0a0a0 | サブテキスト・補足 |
| --color-border | #2a2a2a | ボーダー・区切り線 |

## 2. タイポグラフィ

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

## 3. スペーシング（余白体系）
| トークン名 | 値 | 主な用途 |
|-----------|----|----|
| --space-xs | 8px | 要素内の小余白 |
| --space-sm | 16px | 要素間の小余白 |
| --space-md | 32px | コンポーネント間 |
| --space-lg | 64px | セクション内余白 |
| --space-xl | 96px | セクション間余白 |
| --space-xxl | 128px | ページトップ余白 |

## 4. ボタン

### メインCTA
- 背景: --color-accent (#c9a84c)
- テキスト: #0a0a0a（ダーク）
- padding: 16px 40px
- font-weight: 700
- border-radius: 4px
- ホバー: --color-accent-light

### セカンダリボタン（ゴースト型）
- 背景: transparent
- border: 1px solid --color-accent
- テキスト: --color-accent
- ホバー: 背景を--color-accentに、テキストを#0a0a0aに

## 5. カードコンポーネント
- 背景: --color-bg-card (#1a1a1a)
- border: 1px solid --color-border
- border-radius: 8px
- padding: 32px
- ホバー: border-color を --color-accent に変化

## 6. コンテンツ幅・レイアウト
- 最大幅: 1200px
- 左右padding（PC）: 40px
- 左右padding（SP）: 20px
- ブレークポイント: 768px（PC/SP切り替え）

## 7. アニメーション・インタラクション
- トランジション: all 0.3s ease
- スクロールアニメーション: fadeInUp（opacity 0→1 / translateY 20px→0）
- 対象: セクション見出し・カード・ボタン

## 8. 角丸の統一ルール
| 要素 | border-radius |
|------|--------------|
| ボタン | 0px |
| カード | 0px |
| 入力フィールド | 0px |
| バッジ・タグ | 0px |

## 9. フォーム入力フィールド
- 背景: #1a1a1a
- border: 1px solid --color-border
- テキスト: --color-text-primary
- placeholder: --color-text-secondary
- focus: border-color を --color-accent に

## 10. 禁止事項
- box-shadow の使用禁止
- グラデーション（linear-gradient等）の使用禁止
- 白背景セクションの使用禁止
- 未定義のカラーコードの使用禁止
