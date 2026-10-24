# D-Day Rulebook System

A bilingual (Japanese / English) rulebook document family for an operational-scale World War II wargame centered on the D-Day landings and the subsequent Normandy Campaign.

**Status: `RULEBOOK_TEMPLATE_BASELINE = COMPLETE` — `PLAYABLE_DDAY_GAME = NOT COMPLETE`.**

This repository is a completed *document template baseline*: the canonical rule/scenario sources, the full bilingual set of six player-facing books, and a cross-document audit (87/87 PASS) verifying that the books are mutually consistent with the canonical sources. Baseline date: 2026-09-12.

It does **not** contain a playable game. Maps, order of battle (OOB), initial placement, unit values, supply values, reinforcements, air, landings, airborne, victory conditions, runtime, and playtest are not yet defined. As they are defined, the canonical sources (A1/B1) and all derived documents are expected to be revised repeatedly. The purpose of this baseline is a document system that can absorb those revisions.

## Document family

| Code | Path | Language | Role |
|------|------|----------|------|
| **A1** | `01_AUTHORITY/D-Day_Canonical_Rule_Specification_v0.30_WORKING.md` | EN | **Canonical source** — common rule semantics. Authority for A2–A5. |
| **B1** | `01_AUTHORITY/D-Day_Scenario_Canonical_Source_v0.11_WORKING.md` | EN | **Canonical source** — D-Day scenario semantics. Authority for B2/B3. |
| A2 | `02_JAPANESE_USER_FACING/D-Day_Japanese_Player_Rulebook_v1.4_WORKING.md` | JA | Player rulebook — the formal manual for "how do I actually handle this?" (turn / movement / combat / supply / reinforcement / air / airborne / landing / victory checks, quick reference). Human Reader UAT: PASS. |
| A3 | `03_ENGLISH_USER_FACING/D-Day_English_Player_Rulebook_v0.2_WORKING.md` | EN | Player rulebook (A2-equivalent). Machine qualified; Human Reader PASS not claimed. |
| A4 | `02_JAPANESE_USER_FACING/D-Day_Japanese_Rules_Companion_v0.5_WORKING.md` | JA | Rules companion — the textbook for "why is the rule this way, and what do I think about on the map?" (scale & abstraction, time & state, movement, combat, retreat, supply, air, landings, coastal strongpoints, victory conditions, integrated examples, judgment training). Human Reader UAT: PASS. |
| A5 | `03_ENGLISH_USER_FACING/D-Day_English_Rules_Companion_v0.4_WORKING.md` | EN | Rules companion (A4-equivalent). Machine qualified; Human Reader PASS not claimed. |
| B2 | `02_JAPANESE_USER_FACING/D-Day_Japanese_D-Day_Scenario_Book_v0.12_WORKING.md` | JA | D-Day scenario book — Normandy Campaign history (Overlord / Neptune through Falaise) plus what to look for in this scenario, the scenario framework, and a player guide. Human Reader UAT: PASS. |
| B3 | `03_ENGLISH_USER_FACING/D-Day_English_D-Day_Scenario_Book_v0.3_WORKING.md` | EN | D-Day scenario book (B2-equivalent). Machine qualified; Human Reader PASS not claimed. |

Supporting documents: `04_GUIDE_AND_AUDIT/` (documentation map + 6-book cross-document audit), `00_README.md` (Japanese overview of the set), `MANIFEST_SHA256.json` (per-file integrity manifest).

## Authority rules

- A2–A5 may not change A1; A1 is the authority for common rule semantics.
- B2/B3 may not change B1; B1 is the authority for scenario semantics.
- The English books (A3/A5/B3) are **not literal translations** of the Japanese books. They were written directly in English from the same canonical sources, matching the product role and reader value of the approved Japanese books.
- Files named `*_WORKING.md` are working baselines: complete for their stated purpose, expected to be revised as the playable game takes shape.

## Which book do I read?

| If you need… | Read (JA) | Read (EN) |
|---|---|---|
| "How do I actually handle this?" (procedure) | A2 | A3 |
| "Why is the rule this way? What do I think about on the map?" | A4 | A5 |
| "What is the D-Day scenario / Normandy Campaign about?" | B2 | B3 |

## Repository layout

```
.
├── README.md
├── LICENSE
├── MANIFEST_SHA256.json
├── 00_README.md
├── 01_AUTHORITY/
├── 02_JAPANESE_USER_FACING/
├── 03_ENGLISH_USER_FACING/
└── 04_GUIDE_AND_AUDIT/
```

## Integrity check

`MANIFEST_SHA256.json` records the size and SHA-256 of each document. Example (PowerShell 5.1+):

```powershell
$m = Get-Content .\MANIFEST_SHA256.json -Raw | ConvertFrom-Json
foreach ($a in $m.artifacts) {
  $h = (Get-FileHash -Algorithm SHA256 $a.path).Hash.ToLower()
  if ($h -ne $a.sha256) { Write-Warning ($a.path + ' MISMATCH') }
}
```

## License

MIT — see [LICENSE](LICENSE).

---

# 日本語（Japanese）

## 概要

D-Day（ノルマンディー上陸作戦）およびその後のノルマンディー戦役を題材とする、作戦級規模のワールドウォーIIウォーゲームのためのルールブック文書ファミリー（日本語 / 英語バイリンガル）。

**ステータス: `RULEBOOK_TEMPLATE_BASELINE = COMPLETE` — `PLAYABLE_DDAY_GAME = NOT COMPLETE`**

本リポジトリには完成した**文書ひな型（開発ベースライン）**が入っています。共通ルール正本（A1）・シナリオ正本（B1）、日英 6 冊のプレイヤー向け書群、およびそれらの相互整合を検証した横断監査（87/87 PASS）です。ベースライン日付: 2026-09-12。

**プレイ可能なゲーム本体は含まれていません。** マップ・OOB（兵力表）・初期配置・ユニット数値・補給値・増援・航空・上陸・空挺・勝利条件・実ランタイム・プレイテストは未具体化です。これらが具体化すれば A1/B1 正本および全派生文書は何度も改訂される前提で、このベースラインの目的は「その改訂を受け止められる文書体系の完成」です。

## 文書ファミリーと役割

| 記号 | 役割 |
|------|------|
| **A1**（英語・正本） | 共通ルール意味論の正本。A2〜A5 の権威ソース。 |
| **B1**（英語・正本） | D-Day シナリオ意味論の正本。B2/B3 の権威ソース。 |
| A2（日本語） | Player Rulebook。「実際どう処理する？」の正式マニュアル（Player Turn / 移動 / 戦闘 / 補給・孤立 / 増援・補充 / 航空 / 空挺 / 上陸 / 勝利・ゲーム終了 / クイック参照）。Human Reader UAT: PASS。 |
| A3（英語） | Player Rulebook（A2 相当）。Machine Qualified / Human Reader PASS 未主張。 |
| A4（日本語） | Rules Companion。「なぜこのルールなのか」「盤面で何を考えるのか」の教科書（作戦級スケールと抽象化 / 時間と状態 / 移動 / 戦闘 / 退却 / 補給 / 増援 / 航空 / 空挺 / 上陸 / 海岸堡 / 勝利条件 / 統合例 / 判断トレーニング）。Human Reader UAT: PASS。 |
| A5（英語） | Rules Companion（A4 相当）。Machine Qualified / Human Reader PASS 未主張。 |
| B2（日本語） | D-Day Scenario Book。ノルマンディー戦役の歴史解説（Overlord / Neptune から Falaise まで）+ このシナリオで何を見るべきか・シナリオフレームワーク・プレイヤーガイド。Human Reader UAT: PASS。 |
| B3（英語） | D-Day Scenario Book（B2 相当）。Machine Qualified / Human Reader PASS 未主張。 |

補助文書: `04_GUIDE_AND_AUDIT/`（文書マップ + 6 冊横断監査）、`00_README.md`（日本語のセット概要）、`MANIFEST_SHA256.json`（ファイル毎の整合性 manifest）。

## 権威規則

- A2〜A5 は A1 を変更できない。共通ルール意味論の権威は A1。
- B2/B3 は B1 を変更できない。シナリオ意味論の権威は B1。
- 英語版（A3/A5/B3）は日本語版の逐語訳ではありません。同じ権威ソースを基準に、承認済み日本語版の製品役割・読者価値を踏まえて英語として直接作成されています。
- `*_WORKING.md` 名ファイルは作業ベースラインです。目的に対しては完成していますが、実ゲームの具体化に伴う改訂が前提です。

## 使い分け

| 知りたいこと | 日本語 | 英語 |
|---|---|---|
| 「実際どう処理する？」（手順） | A2 | A3 |
| 「なぜこのルール？盤面で何を考える？」 | A4 | A5 |
| 「D-Day シナリオ / ノルマンディー戦役とは？」 | B2 | B3 |

## 整合性確認

`MANIFEST_SHA256.json` は各文書のサイズと SHA-256 を記録しています。確認例（PowerShell 5.1 以上）は英語セクション「Integrity check」を参照してください。

## ライセンス

MIT — [LICENSE](LICENSE) を参照。
