# Character PAL

## 定義

Character PAL とは、同じ人物を、条件変化の中でも同じ人物として
再び呼び出すために、不変の芯・年齢レイヤー・禁止 drift・
優先順位を固定する継続層である。

Character PAL は、単なる外見メモではない。
参照画像そのものでもない。
Character PAL は、人物の同一性を構成する以下を固定するための記述層である。

- 不変の芯
- 許容される変化
- 禁止される drift
- 再呼び出し時の優先順位

-----

## 目的

Character PAL の目的は、キャラクター画像を一度再現することではない。
目的は、条件が変わっても以下の状態を維持することである。

- 同じ人として読める
- 類型ジャンプしない
- 欧米人化しない
- 理想化で別人化しない
- 年齢変化でも本人性を失わない

Character PAL は、似ている画像を出すためではなく、
同じ存在を継続させるために用いられる。

-----

## Character PAL が固定するもの

### 1. Identity Core

Identity Core は、その人物の不変の芯である。
衣装や背景が変わっても、これが残っていれば同じ人として読める。

Identity Core には主に次の要素が含まれる：

- 日本人女性として自然な骨格
- 顔の重心
- 目元の温度
- 鼻梁の強さの上限
- 口元の静けさ
- 穏やかで親しみやすい知性
- 冷たくなりすぎない落ち着き
- 類型化されすぎない本人性

Identity Core は最優先で保護される。

### 2. Presentation Defaults

> Visual defaults such as hair, eye color, glasses,
> and baseline body reading are handled in
> [pal/character_base_appearance.md](character_base_appearance.md).
> Presentation Defaults in Character PAL refer to
> the most stable default presentation conditions
> for recall, including expression, stance, and
> standard calling posture.

Presentation Defaults は、その人物を最も安定して呼び出せる
標準的な見た目である。

例：

- 標準髪型
- 眼鏡の有無と形状
- 髪色
- 瞳の色
- 基本表情
- 標準的な立ち姿

Presentation Defaults は Identity Core ではないが、
再呼び出し時の成功率を高めるための標準アンカーとして機能する。

### 3. Age Layers

Age Layers は、同じ人物の中で年齢ごとに安定しやすい再構成点である。

年齢は独立した別人ではなく、同じ人物の別安定点として扱われる。

詳細は `pal/age_layer.md` を参照。

### 4. Forbidden Drift

Forbidden Drift は、その人物を別類型へ崩す再解釈である。
Character PAL はこれを明示的に抑止する。

Forbidden Drift の例：

- 欧米人化
- 鼻筋強化
- 眼窩深化
- 顎先や頬骨の鋭化
- generic glamorous woman 化
- office-worker archetype 化
- 幼児化
- kawaii 化しすぎること
- 年齢上昇に伴う人格変質
- 花嫁類型への吸着による別人化

drift の分類と詳細は `pal/anti_drift.md` を参照。

-----

## 運用原則

### 1. まずベース呼び出しを確認する

Character PAL は、最初に参照画像またはベース呼び出しで
再現確認を行う。一致しない場合は続行しない。

### 2. アンカー以外は遷移で記述する

Character PAL は、最初のアンカー以外をすべて
前の画像からの遷移として記述する。
変えない要素は維持と明記し、変える要素は差分だけを書く。

### 3. Character PAL は最優先

背景、衣装、シーケンス、スタイルと競合する場合、
Character PAL を最優先する。

優先順位：

1. Character PAL
1. Sequence PAL
1. Costume PAL
1. Background PAL
1. Style PAL

### 4. 採用画像のみを資産化する

Character PAL に反映する画像は採用済み画像に限る。
drift や不一致がある画像は、ログには残せてもアンカー資産にはしない。

-----

## 意義

Character PAL の意義は、キャラクターを「その都度作る対象」から、
継続的に運用できる存在へ変えることにある。

これにより以下が、再設計ではなく再接続として扱いやすくなる：

- 同じ人を別衣装で呼ぶ
- 同じ人を別背景で呼ぶ
- 同じ人を年齢違いで呼ぶ
- 同じ人を sequence の中で変化させる

Character PAL は、画像生成における人物の同一性を、
偶然ではなく運用可能なものへ変えるための基盤である。