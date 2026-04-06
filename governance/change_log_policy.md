# Change Log Policy

## 定義

Change Log とは、PAL・プロトコル・ノート・宣言ファイルに
加えた変更を、何をいつなぜ変えたかを記録するための層である。

Change Log は rollback の根拠であり、
運用判断の監査証跡である。

-----

## 記録が必要なタイミング

以下のいずれかが発生した時に記録する：

- ファイルの内容を変更した
- Status を変更した（draft → active など）
- ファイルを新規作成した
- ファイルを deprecated または rejected にした
- アンカー画像を差し替えた
- 採用 / 不採用の判定を行った

-----

## 最小記録項目

Change Log の1エントリには最低限以下を含む：

| 項目 | 内容 |
|---|---|
| 日付 | YYYY-MM-DD |
| 対象ファイル | 変更したファイルのパス |
| 変更種別 | 新規 / 更新 / Status変更 / 削除 |
| 変更内容 | 何を変えたか（一行） |
| 変更理由 | なぜ変えたか（一行） |
| 変更者 | 担当者名または識別子 |

-----

## 記録形式

各ファイルの末尾に以下の形式で記載する：

    ## Change Log

    | Date | Version | Type | Summary | Reason |
    |---|---|---|---|---|
    | YYYY-MM-DD | v0.1.0 | 新規 | 初版作成 | pal-lab 初期構築 |
    | YYYY-MM-DD | v0.2.0 | 更新 | ○○を修正 | drift 再発のため |

-----

## 監査ログとして最低限残すべき項目

生成運用における監査ログには
以下を最低限記録する：

- 生成日時
- 使用した PAL のバージョン
- 採用 / 不採用の判定
- 判定理由（一行）
- drift の種別（あれば）
- 参照したアンカー画像の識別子

これらは `notes/adoption_and_purge_policy.md` の
運用と連動する。

-----

## Rollback の手順

Change Log を使った rollback は以下の手順で行う：

1. Change Log で直前の active バージョンを確認する
2. 該当バージョンのファイルを復元する
3. 現バージョンを deprecated に変更する
4. rollback の理由を Change Log に記録する

-----

## 運用上の注意

- Change Log は削除しない
- 理由のない変更は記録しない
  （理由が書けない変更は行わない）
- rollback 後も元の変更記録は残す
- change reason は一行でよいが、
  必ず書く

*Status の定義と昇格・降格ルールは
`governance/asset_status_policy.md` を参照。*
