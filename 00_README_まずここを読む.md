# D-Day Rulebook Template Baseline v0.1

**STATUS: RULEBOOK / SCENARIO-BOOK TEMPLATE BASELINE COMPLETE**  
**DATE: 2026-09-12**

## この成果物セットの位置づけ

これは、D-Dayゲームそのものの最終完成版ではありません。

当初の目的だった、

> **D-Dayゲームを成立させられるルールブック＋シナリオ仕様のひな型を完成させる**

ための成果物セットです。

現時点で、

- 共通ルール正本
- D-Dayシナリオ正本
- 日本語Player Rulebook
- 英語Player Rulebook
- 日本語Rules Companion
- 英語Rules Companion
- 日本語D-Day Scenario Book
- 英語D-Day Scenario Book

の文書体系が揃っています。

今後、実際のマップ、OOB、Game Data、システム実装、プレイテストが進めば、これらは何度も改訂されます。

したがってこれは、

**Final Productではなく、今後の実ゲーム開発を始めるための完成した文書ひな型／開発ベースライン**

です。

---

# 1. 権威ソース

## A1
`D-Day_Canonical_Rule_Specification_v0.30_WORKING.md`

共通ルール意味論の正本。

## B1
`D-Day_Scenario_Canonical_Source_v0.11_WORKING.md`

D-Dayシナリオ意味論の正本。

A2～A5はA1を勝手に変更できません。

B2/B3はB1を勝手に変更できません。

---

# 2. 日本語ユーザー向け3冊

## A2 日本語 Player Rulebook

`D-Day_Japanese_Player_Rulebook_v1.4_WORKING.md`

役割：

**「実際どう処理する？」を確認する正式マニュアル。**

主な特徴：
- Player Turn確認
- 移動チェック
- 戦闘解決チェック
- 補給／孤立チェック
- 増援／補充
- 航空
- 空挺
- 上陸
- 勝利／ゲーム終了
- クイック参照

Human Reader UAT：**PASS**

---

## A4 日本語 Rules Companion

`D-Day_Japanese_Rules_Companion_v0.5_WORKING.md`

役割：

**「なぜこのルールなのか」「盤面で何を考えるのか」を理解する教科書。**

主な特徴：
- 作戦級スケールと抽象化
- 時間と状態
- 移動
- 戦闘
- 退却
- 補給
- 増援
- 航空
- 空挺
- 上陸
- 海岸堡
- 勝利条件
- 統合例
- 判断トレーニング

Human Reader UAT：**PASS**

---

## B2 日本語 D-Day Scenario Book

`D-Day_Japanese_D-Day_Scenario_Book_v0.12_WORKING.md`

役割：

**ノルマンディー戦役を理解し、このD-Dayシナリオで何を見るべきかを知る本。**

主な特徴：
- Normandy Campaignの歴史解説
- Overlord / Neptune
- Bodyguard / Fortitude
- Perch / Villers-Bocage
- Epsom
- Windsor
- Charnwood
- Goodwood
- Atlantic
- Spring
- Cobra
- Bluecoat
- Mortain / Lüttich
- Totalize
- Tractable
- Falaise
- Red Ball Express
- Scenario framework
- Player Guide
- 未解決Game Data

Human Reader UAT：**PASS**

---

# 3. 英語ユーザー向け3冊

英語版は日本語版の逐語訳ではありません。

同じ権威ソースと、承認済み日本語版の製品役割・読者価値を基準に、英語として直接作成しています。

## A3
`D-Day_English_Player_Rulebook_v0.2_WORKING.md`

A2相当。  
Machine Qualified / Human Reader PASS未主張。

## A5
`D-Day_English_Rules_Companion_v0.4_WORKING.md`

A4相当。  
Machine Qualified / Human Reader PASS未主張。

## B3
`D-Day_English_D-Day_Scenario_Book_v0.3_WORKING.md`

B2相当。  
Machine Qualified / Human Reader PASS未主張。

---

# 4. 一番簡単な使い分け

**処理に困った → A2**

**意味が分からない → A4**

**D-Day戦役・シナリオ固有を知りたい → B2**

英語ではそれぞれ A3 / A5 / B3。

---

# 5. 横断監査

6冊横断監査：

**87 / 87 PASS**

確認内容：
- A1/B1との権威整合
- 役割分担
- 用語
- 共通ルール整合
- Scenario意味論整合
- 日英reader-value parity
- 未解決Game Data境界
- 不要な長文重複
- 文書間ナビゲーション

この結果は、

> **現時点のA1/B1と設計に対して、6冊が矛盾なく揃っている**

ことを意味します。

最終製品完成を意味しません。

---

# 6. 今後の前提

今後、

- マップ
- OOB
- 初期配置
- ユニット数値
- 補給値
- 増援
- 航空
- 上陸
- 空挺
- 勝利条件
- 実ランタイム
- プレイテスト

が具体化すると、A1/B1および派生文書は何度も修正される前提です。

この成果物セットの目的は、

**その修正を受け止められる文書体系のひな型を完成させること**

です。

---

# 7. 今回の成果

**RULEBOOK_TEMPLATE_BASELINE = COMPLETE**

ただし、

**PLAYABLE_DDAY_GAME = NOT_COMPLETE**

です。
