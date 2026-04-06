# pal-lab

## Overview

PAL-based continuity framework for recalling the same person
across changing conditions while controlling drift,
sequence meaning, and adoption decisions.

-----

## Repository Structure

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
      aster_control_persona_pal.md  — 複数媒体をまたぐ制御人格 PAL
      chatbot_persona_pal.md        — 対話 AI の人格固定層
      agent_persona_pal.md          — 複数媒体・工程の主語統一層
      governance_pal.md             — 継続性を実運用で統治する最上位層

    protocols/
      operational_protocol.md            — 確認・遷移・停止・採用・圧縮の手順
      prompt_protocol.md                 — プロンプト設計原則、記述順、長文 / 最適化 / 圧縮の基本仕様
      modes_character_lock_vs_quality.md — キャラ固定優先 / 品質優先の記述モード

    notes/
      motion_notes.md               — 静止画に時間感を与える演出規則
      drift_cases.md                — 実例 drift の記録と工程別危険点
      adoption_and_purge_policy.md  — 採用 / 不採用 / パージの判断基準

-----

## Priority Order

1. Character PAL
2. Sequence PAL
3. Costume PAL
4. Background PAL
5. Style PAL

-----

## Governance

`declarations/pal_declaration.md` — 原則・宣言・適用範囲

`persona/governance_pal.md` — 実運用での統治層
（continuity の権威化防止・停止権・rollback・採否管理）

-----

## Quick Start

1. `declarations/pal_declaration.md` を読む
2. `pal/character_pal.md` と `pal/anti_drift.md` を読む
3. `protocols/operational_protocol.md` の標準手順で生成を開始する
