# Trust Rank Policy

## 定義

Trust Rank とは、PAL・アンカー画像・参照資料・プロトコル・
ノートなどの参照資産が、現在どの程度の信頼度で
運用に使用できるかを示すランクである。

Status（draft / active / deprecated / rejected）が
ファイルの運用状態を示すのに対し、
Trust Rank は参照資産の内容の信頼度を示す。
両者は独立して管理する。

-----

## Trust Rank の種類

| Rank | 意味 | 運用上の扱い |
|---|---|---|
| `canonical` | 検証済み。最も信頼度が高い | 本番運用の基準点として使用する |
| `working` | 運用中だが完全には検証されていない | 本番運用に使用できるが canonical への昇格を目指す |
| `provisional` | 仮採用。検証中または条件付き | 限定的な運用のみ許可。単独で基準点にしない |
| `rejected` | 不採用。使用禁止 | 原因記録のためのみ保管する |

-----

## 各資産種別への適用

### アンカー画像

| Rank | 条件 |
|---|---|
| `canonical` | 再現確認済み。人物同一性・drift なし・採用済み |
| `working` | 運用中だが再現確認が不完全 |
| `provisional` | 仮アンカー。特定工程のみ使用 |
| `rejected` | drift あり・不採用・汚染確認済み |

### PAL ファイル

| Rank | 条件 |
|---|---|
| `canonical` | 実運用で検証済み。安定して再現できる |
| `working` | 運用中だが一部未検証の要素がある |
| `provisional` | 新規作成・試験的運用中 |
| `rejected` | drift を誘発することが確認された |

### 参照資料・プロトコル

| Rank | 条件 |
|---|---|
| `canonical` | 正式採用。運用の基準として確定済み |
| `working` | 運用中だが改訂の可能性がある |
| `provisional` | 草案・試用中 |
| `rejected` | 廃止・使用禁止 |

-----

## Trust Rank と Status の関係

Trust Rank と Status は独立しているが、
組み合わせによって運用上の扱いが決まる。

| Status | Trust Rank | 運用上の扱い |
|---|---|---|
| `active` | `canonical` | 本番運用の基準点。最も安全 |
| `active` | `working` | 本番運用可。canonical 昇格を目指す |
| `active` | `provisional` | 限定運用のみ。単独基準点にしない |
| `deprecated` | 任意 | 参照のみ。新規運用に使わない |
| `rejected` | `rejected` | 保管のみ。運用に使わない |

-----

## 昇格・降格のルール

### provisional → working

以下を満たした場合に昇格する：

- 実運用で問題なく使用できることが確認された
- 関連する上位 PAL と矛盾しない
- 担当者が明示的に working と宣言した

### working → canonical

以下を満たした場合に昇格する：

- 複数回の運用で安定した再現性が確認された
- drift・不一致・汚染が確認されていない
- 担当者が明示的に canonical と宣言した

### canonical / working → rejected

以下のいずれかが確認された場合：

- drift を誘発することが確認された
- 汚染が確認された
- 上位 PAL・ガバナンス原則と矛盾することが確認された

rejected への降格は即時とする。
降格理由は必ず記録する。

-----

## 記載形式

各ファイル・資産の管理記録に以下を記載する：

    trust_rank: canonical
    rank_updated: YYYY-MM-DD
    rank_reason: 複数回の運用で再現性確認済み

-----

## 運用上の注意

- provisional は単独で基準点・アンカーとして使わない
- rejected は削除せず、降格理由とともに保管する
- Trust Rank の変更は必ず change log に記録する
- working のまま長期間放置しない
  （検証を進めて canonical か rejected に移行する）

*Trust Rank の変更記録は
`governance/change_log_policy.md` に従う。*
*Status 管理は
`governance/asset_status_policy.md` に従う。*
