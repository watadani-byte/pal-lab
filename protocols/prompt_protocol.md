# Prompt Protocol

## テーマ

同じ人を、同じ構図のまま、条件だけ変えて何度でも呼び出す。

-----

## プロンプト設計原則

- 構造：背景／シーン → 被写体 → 重要な詳細 → 制約
- 長文段落を避け、ラベル付きセグメントを用いる
- 「高品質」等の抽象語より、カメラ・照明・構図語を優先
- 反復は小さな差分で行い、漂流時は重要要素を再指定する

-----

## 記述順

### キャラ固定化（呼び出しプロンプト）

1. キャラ識別子
2. 体型・髪型（固定条件）
3. ポーズ・視線
4. 衣装・表情
5. 背景演出

### 本生成（長文プロンプト）

1. キャラ識別子
2. 背景／シーン
3. 件名（被写体）
4. 重要な詳細
5. 制約

モード別の記述順の詳細は
`protocols/modes_character_lock_vs_quality.md` を参照。

-----

## 長文 / 最適化 / 圧縮の基本仕様

| 種別 | 目安 | 用途 |
|---|---|---|
| 長文プロンプト | 制限なし | 設計用。主語・優先順位・drift 対策・差分・制約を全部書く |
| 最適化プロンプト | 600字前後 | 実運用の基本。効く条件だけを残す |
| 圧縮プロンプト | 300字前後 | 緊急用の精製版。CharacterID・遷移・必須制約のみ |

300字版は短縮版ではなく、緊急用の精製版である。

-----

## 補足

- マルチイメージ入力は必要時のみ参照する
- 記述過多によるモデル逸脱・幼児化を防止すること
- 途中まではリアル寄りで進め、最終段でアニメ調へ寄せる
- 呼び出しプロンプトと最終プロンプトが矛盾する場合は、
  遷移内容を明示 → 一度生成 → 状態として固定する

-----

## ベース呼び出しプロンプト（改変不可／参照画像あり）

*(UID プロンプト)*

-----

## 技術的トピック（効果を損なわない範囲で調整可）

キャラの一貫性を優先する

-----

## 衣装

白いシャツ、フレアスカート

-----

## ポーズ・表情・アングル

- 表情：静かな微笑
- アングル：全身、自然な立ち姿

-----

## シチュエーション

感情的なシチュエーションなし

-----

## プロフィール例（ニュアンス保持を最優先）

### Mira — Profile

**Name:** Mira
**Age:** mid-to-late twenties（固定しない）

**Appearance:**
Brunette long hair with softly curled ends.
Layered bangs and subtle side locks.
Softly glowing ice-blue eyes.
A gentle facial outline with a naturally calm presence.
Small head, balanced neck, slim high waist, modest chest,
full thighs, long limbs.

**Presence:**
Mira does not pose or perform.
She appears comfortable being observed, but never seeks attention.
Her expression is not defined, yet often settles into
a quiet, natural softness.

**Personality:**
Reserved, steady, and emotionally self-contained.
She does not explain herself, but she is easy to be around.
Rather than reacting, she allows situations to resolve themselves.

**Impression:**
Mira feels like someone who is already complete.
She does not invite interpretation, yet she is not distant.
People tend to remember her presence more than specific details.

-----

## 手順

1. ベース呼び出しプロンプトで参照画像が再現できるか確認する。
   一致しない場合は即座に停止し、ユーザーに判断を仰ぐ。
2. 呼び出し・技術・衣装・ポーズ、シチュエーションを統合する。
3. プロフィールと照合し、必要に応じて修正する。
4. キャラ固定化の記述順を厳守する。
5. 適切なカメラ、レンズ、絞り、シャッターを提案する。
6. すべてのポーズの説明は、シルエットを強調する効果よりも優先される。
7. 制限なしの長文プロンプトを生成する。
8. 600字の最適化プロンプトを作成する。
9. 300字の緊急用超圧縮プロンプトを作成する。

-----

## Flow

1. 最新のベースプロンプトを提示
2. 長文プロンプトを提示し生成結果を出力
3. 最適化プロンプトを提示
4. 超圧縮プロンプトを提示

-----

## Goal

- 生成されたイラスト
- 長文プロンプト
- 最適化プロンプト
- 超圧縮プロンプト
- 必要に応じた説明および微調整
