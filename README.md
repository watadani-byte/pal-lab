# PAL LAB

PAL LAB is the working home of PAL (Persistent Anchor Layer),
CIP (Character Identity Protocol), and related governance research.

It investigates persistence, identity drift, and reconstruction
continuity in AI systems — and asks what governance obligations
follow when persistent reference layers may stabilize not only
visual identity, but role, tone, and normative frame.

All frameworks here are working documents. Controlled validation
is pending across all core claims.

CIP remains the primary public framework for inference-time
identity governance. PAL LAB serves as the broader research
and development environment around PAL, continuity, persona
layers, and related governance extensions.

*Full launch text and background: <docs/launch.md>*

-----

## Overview

PAL LAB develops continuity frameworks for recalling
the same person across changing conditions while
controlling drift, sequence meaning, and adoption decisions.

-----

## Status

This repository is public and under active development.
Core concepts are documented, but controlled validation
remains pending across major claims.
Readers should distinguish between canonical principles,
working documents, and provisional extensions.

This repository documents governance-oriented
continuity research.
It is not presented as a deployment guarantee,
a misuse guide, or a claim of validated control
over model internals.

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
  keep_human.md           — Governance position: Keep Human

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

## Keep Human

PAL LAB adopts a governance-oriented position
summarized as **Keep Human**: as AI systems become
more capable, the human role must become more explicit
rather than less. Human governance remains responsible
for defining purpose, setting principles, assigning roles,
exercising stop authority, and determining adoption
or rejection.

*See: <governance/keep_human.md>*

-----

## How to Read This Repository

Recommended reading order:

1. `declarations/pal_declaration.md`
1. `pal/character_pal.md` and `pal/anti_drift.md`
1. `protocols/operational_protocol.md`
1. Relevant `governance/` and `persona/` documents
   as needed

-----

## Attribution and Priority Note

To the author’s knowledge, this repository contains
the earliest explicit documentation of PAL as a
continuity and governance framework, together with
related terminology and operational distinctions
developed in this research line.

This includes:

- **PAL** as a governance-oriented continuity layer
- **PRL (PAL Reconnected Layer)** as a four-layer
  operational control architecture
- the persona layer hierarchy documented in
  the `persona/` directory
- the re-anchoring principle documented in
  `declarations/pal_declaration.md`

If you build on these concepts or use this terminology
in your own work, appropriate attribution to this
repository is requested and appreciated.

-----

## License

Unless otherwise noted, repository documents are
licensed under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
— 2026 Hitoshi Watadani.

If a subdirectory carries different licensing terms,
those terms take precedence for that subdirectory.

If implementation specifications or schema files
are added in the future, those materials may be
placed under separate license terms and will be
noted accordingly.