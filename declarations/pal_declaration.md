# PAL Declaration

## 定義

PAL とは、同じ人物・同じ場面・同じ意図を条件変化の中でも
継続的に呼び戻し、運用するための continuity layer であり、
その継続性は常に人間判断と統治の下に置かれるべきものである。

PAL は、画像生成における同一性を、
単発の成功から継続的な管理対象へ変えるための方法論である。

-----

## 目的

PAL の目的は、同じ存在を偶然ではなく運用可能なものにすることである。

-----

## 適用範囲

本稿では主として画像 continuity を扱う。

以下は PAL の拡張先として別途扱う：

- チャットボット人格の固定
- 制御人格の固定
- エージェント人格の固定
- ガバナンス固定

-----

## 原則

### Continuity は authority ではない

- continuity は authority ではない
- persistence は trust ではない
- stable reconstruction は correctness ではない

PAL が継続性を与えるとしても、
それ自体が正しさや正当性を保証するわけではない。

### 人間判断の優位

PAL は、人間の判断を置き換えるものではない。

現在の人間の判断、停止、修正、採否決定は常に上位にある。
persistent material は continuity を支えうるが、
現在の人間指示に優越してはならない。

### ガバナンスの要件

PAL は無制限に運用されるべきではない。

以下の管理が必要である：

- revocation
- rollback
- versioning
- adoption / rejection の管理

継続性はガバナンスの下でのみ許容される。
