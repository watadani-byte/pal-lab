# Asset Status Policy

## 定義

Asset Status とは、各 PAL・プロトコル・ノート・宣言ファイルが
現在どの運用状態にあるかを示すラベルである。

Status は各ファイルの冒頭に明記する。
Status が明記されていないファイルは draft として扱う。

-----

## Status の種類

| Status | 意味 | 運用上の扱い |
|---|---|---|
| `active` | 現在有効。本番運用に使用する | 唯一の正式参照先 |
| `draft` | 作成中または未検証 | 本番運用に使わない |
| `experimental` | 試験的に運用中。検証前 | 結果を記録し、昇格か棄却を判断する |
| `deprecated` | 旧版。後継ファイルが存在する | 参照のみ可。新規運用に使わない |
| `rejected` | 不採用。使用禁止 | 原因記録のためのみ保管する |

-----

## 昇格・降格のルール

### draft → active

以下をすべて満たした場合に昇格する：

- 内容が実運用で検証された
- 関連する上位 PAL と矛盾しない
- 担当者が明示的に active と宣言した

### active → deprecated

以下のいずれかが発生した場合に降格する：

- 後継ファイルが active になった
- 内容が現在の運用と一致しなくなった
- 上位 PAL との矛盾が解消できなくなった

### active / draft → rejected

以下のいずれかが発生した場合：

- 内容が drift を誘発することが確認された
- ガバナンス原則と矛盾することが確認された
- 採用できない理由が明確になった

rejected ファイルは削除せず、
理由を記録した上で保管する。

-----

## ファイル冒頭への記載形式

各ファイルの冒頭に以下を記載する：

    Status: active
    Version: v0.1.0
    Last updated: YYYY-MM-DD

-----

## 運用上の注意

- active ファイルは同時に1つだけを原則とする
- experimental は本番と混在させない
- deprecated ファイルは別ディレクトリへ移動するか
  ファイル名に `_deprecated` を付けて区別する
- Status の変更は必ず change log に記録する

*Status 変更の記録方法は
`governance/change_log_policy.md` を参照。*
