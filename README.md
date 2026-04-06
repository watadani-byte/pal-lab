# PAL LAB

PAL LAB is a public research and governance initiative investigating persistence, identity drift, and reconstruction continuity in AI systems — and developing frameworks for governing what persistent anchor layers may stabilize.

-----

PAL LAB is a public research and governance initiative focused on persistence, drift, and continuity in AI systems.

It began with a narrow operational problem: when a character or persona is established in one AI session, it tends to drift — across sessions, turns, and platforms. Reference images help. Prompt design helps. But neither, by itself, constitutes a governance framework.

PAL (Persistent Anchor Layer) and CIP (Character Identity Protocol) are attempts to describe and govern these conditions. Neither is a finished solution. Both are working frameworks under continued development.

As investigation continued, the problem widened. Persistence mechanisms that stabilize visual identity may also stabilize role, tone, and normative frame — for better or worse. That widening raised governance questions that visual continuity alone does not.

PAL LAB is where those connected questions are investigated together.

-----

**PAL LAB focuses on:**

- Identity drift and continuity failure across AI sessions
- Anchor-bound reconstruction and the PAL hypothesis
- Role drift, normative drift, and culturally bounded reconstruction
- Contamination risk in persistent reference layers
- Governance language and frameworks for AI persistence mechanisms
- The relationship between continuity, stability, and accountability
- Documentation and validation framing for PAL, CIP, and related frameworks

*Full launch text and background: <docs/launch.md>*

-----

## Overview

PAL-based continuity framework for recalling the same person
across changing conditions while controlling drift,
sequence meaning, and adoption decisions.

-----

## Repository Structure

```
declarations/
  pal_declaration.md        — PAL の定義・原則・適用範囲・ガバナンス宣言

pal/
  character_pal.md          — 人物同一性の固定層
  age_layer.md              — 年齢をまたぐ同一性の安定点層
  anti_drift.md             — 禁止 drift の分類・停止条件・管理層
  sequence_pal.md           — 複数枚の意味連続性の固定層
  background_pal.md         — 場面・空間・光の固定層
  costume_pal.md            — 衣装・小物・着用状態の固定層
  style_pal.md              — 描画様式・質感の固定層

persona/
  aster_control_persona_pal.md             — 複数媒体をまたぐ制御人格 PAL
  chatbot_persona_pal.md                   — 対話 AI の人格固定層
  agent_persona_pal.md                     — 複数媒体・工程の主語統一層
  organizational_persona_pal.md            — 組織の立場・権限境界を保つ人格固定層
  institutional_persona_pal.md             — 制度上の主語・説明責任を保つ人格固定層
  international_institutional_persona_pal.md — 国際機関の中立性と権限境界を保つ人格固定層
  governance_pal.md                        — 継続性を実運用で統治する最上位層

protocols/
  operational_protocol.md            — 確認・遷移・停止・採用・圧縮の手順
  prompt_protocol.md                 — プロンプト設計原則、記述順、長文 / 最適化 / 圧縮の基本仕様
  modes_character_lock_vs_quality.md — キャラ固定優先 / 品質優先の記述モード

notes/
  motion_notes.md               — 静止画に時間感を与える演出規則
  drift_cases.md                — 実例 drift の記録と工程別危険点
  adoption_and_purge_policy.md  — 採用 / 不採用 / パージの判断基準

governance/
  asset_status_policy.md  — draft / active / deprecated の条件
  change_log_policy.md    — 変更理由・記録形式・監査証跡
  trust_rank_policy.md    — canonical / working / provisional / rejected

docs/
  launch.md               — Full launch text and background
```

-----

## Priority Order

### PAL Layer

1. Character PAL
1. Sequence PAL
1. Costume PAL
1. Background PAL
1. Style PAL

### Persona Layer

1. Governance PAL（最上位）
1. International Institutional Persona PAL
1. Institutional Persona PAL
1. Organizational Persona PAL
1. Agent Persona PAL / Aster Control Persona PAL
1. Chatbot Persona PAL

上位層が権限・立場・説明責任の境界を定め、
下位層はその枠の内側で機能する。

-----

## Governance

`declarations/pal_declaration.md` — 原則・宣言・適用範囲

`persona/governance_pal.md` — 実運用での統治層
（continuity の権威化防止・停止権・rollback・採否管理）

`governance/asset_status_policy.md` — Status 管理
（draft / active / deprecated / rejected）

`governance/change_log_policy.md` — 変更記録・監査証跡

`governance/trust_rank_policy.md` — 信頼度ランク
（canonical / working / provisional / rejected）

-----

## Quick Start

1. `declarations/pal_declaration.md` を読む
1. `pal/character_pal.md` と `pal/anti_drift.md` を読む
1. `protocols/operational_protocol.md` の標準手順で生成を開始する
1. 各ファイルの Status と Trust Rank を確認する
   （active + canonical 以外は本番運用の基準点にしない）