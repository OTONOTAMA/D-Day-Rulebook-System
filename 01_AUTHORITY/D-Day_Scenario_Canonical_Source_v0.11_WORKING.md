# D-Day Scenario Canonical Source v0.11 WORKING

STATUS: WORKING_SCENARIO_INDEPENDENCE_BOUNDARY_REFACTOR
DATE: 2026-09-10  
ROLE: B1 — D_DAY_SCENARIO_CANONICAL_SOURCE  
BASELINE: `D-Day_Rulebook_Development_Baseline_v0.7_APPROVED.md`  
COMMON_RULE_CANONICAL: `D-Day_Canonical_Rule_Specification_v0.30_WORKING.md`
PARENT_B1: `D-Day_Scenario_Canonical_Source_v0.10_WORKING.md`
CHANGE_SPEC: `D-Day_A1_B1_Scenario_Independence_Boundary_Refactor_Change_Spec_v0.1_APPROVED_SCOPE_FROZEN.md`

PURPOSE:
Define normative D-Day/Normandy Scenario rules, settings, parameters, setup/OOB requirements, victory/end conditions, derivation requirements, and unresolved calibration data.
B1 is the semantic source for B2 and B3. B2 and B3 must not use each other as semantic source.

ACTIVE_B1_SCOPE: D-Day / Normandy Campaign
ACTIVE_START_DATE: 6 June 1944
ACTIVE_END_DATE: NOT_PREDETERMINED
ACTIVE_TURN_LENGTH: exactly 3 calendar days
ACTIVE_TOTAL_GAME_TURNS: NOT_PREDETERMINED
ACTIVE_GAME_END_POLICY: DECISIVE_VICTORY_OR_CONCESSION_OR_MUTUAL_DRAW
ACTIVE_PLAYER_MODEL: TWO_PLAYER_COMPETITIVE
ACTIVE_PLAYER_ROLES: ALLIED_PLAYER__GERMAN_PLAYER
ACTIVE_PLAYER_TURN_ORDER: ALLIED_THEN_GERMAN
ACTIVE_NOMINAL_MAP_SCALE: approximately 10 km per hex
ACTIVE_PRIMARY_MANEUVER_SCALE: regiment/brigade-centered
ACTIVE_DIVISION_ROLE: higher formation / organizational grouping
ACTIVE_BATTALION_POLICY: selective separate representation only when independently operationally meaningful
ACTIVE_SETUP_MODEL: GERMAN_FIRST_CONSTRAINED_FREE_DEPLOYMENT_THEN_ALLIED_INVASION_PLANNING
ACTIVE_D_DAY_NORMANDY_VICTORY_ARCHITECTURE: MULTIPLE_OBJECTIVE_HEX_SIMULTANEOUS_CONTROL
ACTIVE_D_DAY_NORMANDY_DECISIVE_CONDITIONS: STRUCTURE_RESOLVED_OBJECTIVE_SETS_AND_THRESHOLDS_UNRESOLVED
ACTIVE_D_DAY_NORMANDY_VICTORY_CHECK_TIMING: ALLIED_END_OF_GERMAN_PLAYER_TURN__GERMAN_END_OF_ALLIED_PLAYER_TURN
ACTIVE_D_DAY_NORMANDY_VICTORY_PARAMETERS: UNRESOLVED
LEGACY_FULL_CAMPAIGN_SCOPE: NON_ACTIVE
LEGACY_FULL_CAMPAIGN_VICTORY: NON_ACTIVE

AUTHORITY BOUNDARY:
- A1 owns reusable common-rule meaning.
- B1 owns D-Day/Normandy-specific normative scenario meaning and data.
- B1 may instantiate values and select scenario options explicitly permitted by A1.
- B1 may not silently redefine an A1 common rule.
- Any incompatible A1/B1 meaning is BLOCKED/UNRESOLVED until normal change control resolves it.
- Historical sources, external games, maps, and prior-art scenarios are Design Evidence / Reference, not Rule Authority.
- Unresolved numeric or content values remain explicit and must not be synthesized merely to complete this document.

---

# 1. Identity, Scope, and Migration Traceability

B1-SCOPE-01
The active B1 product is the D-Day / Normandy Campaign Scenario Canonical Source.

B1-SCOPE-02
The active Scenario begins with the Allied invasion on 6 June 1944.

B1-SCOPE-03
The active Scenario uses exactly 3 calendar days per Game Turn.
The active Scenario has no predetermined fixed end date and no predetermined maximum total Game Turn count.
Play continues until an authorized active Game End Condition is satisfied.

B1-SCOPE-04
The former Western Front full-campaign scope extending through no later than 7 May 1945 and at most 48 Game Turns is not active B1 product scope. It is preserved in Section 11 solely as Legacy/Historical state.

The following legacy A1 scenario identifiers were migrated during the prior A/B authority split:

| Legacy parent ID | Initial B1 migration ID | Current v0.2 disposition |
|---|---|---|
| A1-CAMP-01 | B1-CAMP-01 | ACTIVE |
| A1-CAMP-02 | B1-CAMP-02 | LEGACY_NON_ACTIVE |
| A1-CAMP-03 | B1-CAMP-03 | LEGACY_NON_ACTIVE |
| A1-CAMP-04 | B1-CAMP-04 | ACTIVE |
| A1-CAMP-05 | B1-CAMP-05 | ACTIVE |
| A1-FCV-01 | B1-VICT-01 | LEGACY_NON_ACTIVE |
| A1-FCV-02 | B1-VICT-02 | LEGACY_NON_ACTIVE |
| A1-FCV-03 | B1-VICT-03 | LEGACY_NON_ACTIVE |
| A1-FCV-04 | B1-VICT-04 | LEGACY_NON_ACTIVE |
| A1-FCV-05 | B1-VICT-05 | LEGACY_NON_ACTIVE |
| A1-FCV-06 | B1-VICT-06 | LEGACY_NON_ACTIVE |
| A1-FCV-07 | B1-VICT-07 | LEGACY_NON_ACTIVE |
| A1-FCV-08 | B1-VICT-08 | LEGACY_NON_ACTIVE |

Legacy IDs remain recoverable for traceability but are not active B1 rule IDs unless explicitly marked ACTIVE above.

---

# 2. Active D-Day / Normandy Scenario Rules Currently Resolved

B1-CAMP-01
The active D-Day / Normandy Campaign begins on 6 June 1944.

B1-CAMP-04
The active D-Day / Normandy Campaign's first Allied Player Turn includes the Initial Invasion during the Special Operations Step before the first Allied Supply Checkpoint.

B1-CAMP-05
For the active D-Day / Normandy Campaign's initial Allied airborne operation, scenario data may use the designated initial airborne-reference exception under A1-AIRB-07.

No exact end date, turn count, map extent, OOB, setup, reinforcement schedule, calibration value, or active victory method is resolved merely by these rules.

B1-TIME-01
For the active D-Day / Normandy Campaign, one Game Turn represents exactly 3 calendar days.

B1-TIME-02
Turn 1 begins on 6 June 1944. Each successive Game Turn advances the Scenario calendar by three calendar days.
No final Game Turn number or active Scenario end date is predetermined.

B1-TIME-03
The final calendar date is derived from the Game Turn in which the active Game End Condition ends play, using the three-calendar-day Scenario mapping.
The final date is therefore an outcome of play rather than a fixed Scenario deadline.

B1-SCALE-01
The active D-Day / Normandy Campaign uses hex-based operational geography at a nominal scale of approximately 10 km per hex.
The final Scenario map extent, coastline geometry, individual hex assignments, and terrain/feature mapping remain UNRESOLVED until separately authorized.

B1-SCALE-02
Regiments and brigades are the primary maneuver formations for the active D-Day / Normandy Campaign.
Scenario/OOB data determines the exact represented formation class for each historical formation.

B1-SCALE-03
Divisions remain higher formations and organizational groupings for the active D-Day / Normandy Campaign rather than being universally indivisible primary maneuver units.
The later representation of divisional command, support, parent-formation relationships, or formation-level effects remains UNRESOLVED unless separately authorized.

B1-SCALE-04
Battalions are represented as separate maneuver units only when independently operationally meaningful and explicitly identified by Scenario/OOB data.
Ordinary organic battalions are not automatically represented as separate maneuver units merely because software can manage them.
All scale-sensitive numeric values remain UNRESOLVED unless separately authorized, including Stack Demand/Capacity, Supply Demand/Reach, Entry Demand, Replacement Cost, Airborne Lift Demand/Reference Distance, Amphibious Lift Demand, and movement/unit calibration.

---

B1-PLAYER-01
The active D-Day / Normandy Campaign is a two-player competitive Scenario:
- one Allied Player;
- one German Player.

B1-PLAYER-02
Either active player role may be controlled by a human or an AI player.
The active Scenario does not grant an AI player additional rule authority, legal actions, or player-visible information merely because the controller is AI.

B1-PLAYER-03
The active D-Day / Normandy Scenario defines the Player Turn order for each Game Turn as:
1. Allied Player Turn;
2. German Player Turn.
This instantiates the Scenario-defined Player Turn order required by A1-FOUND-02.

---

# 3. Scenario Content Contract

B1-CONTENT-01
A formally qualified B1 Scenario must resolve or explicitly mark UNRESOLVED each of the following content categories. Omission must not be treated as implicit default data.

## 3.1 Scenario Identity / Product Scope

Required: Scenario identity, product scope, relationship to any other B-family Scenario/Campaign, and active/non-active status.

Current state: D-Day / Normandy Campaign is ACTIVE. Broader Western Front full-campaign content is LEGACY_NON_ACTIVE.

## 3.2 Temporal Scope / Turn Structure

Required: start date/time, end condition or end date, total turn structure, and any Scenario-specific temporal exceptions.

Current state: start = 6 June 1944; one Game Turn = exactly 3 calendar days; each Game Turn proceeds Allied Player Turn then German Player Turn; Turn 1 begins on 6 June 1944. No fixed end date or maximum total Game Turn count is used. The exact active Game End Conditions remain UNRESOLVED, and the final calendar date will be derived from the ending Game Turn.

## 3.3 Map / Playable Area

Required: playable geographic extent, map/area identity, legal off-map/staging areas, and Scenario-owned terrain/feature assignments where applicable.

Current state: nominal map scale = approximately 10 km/hex; exact map extent, coastline/hex geometry, and feature assignments = UNRESOLVED.

## 3.4 Common Rule Dependencies

Required: explicit references to A1 common-rule systems used by the Scenario and any A1 extension point instantiated by B1.

Current state: defined generally in Section 8; detailed dependency coverage remains ongoing.

## 3.5 Scenario-specific Rules / Modules

Required: D-Day/Normandy-only rules or modules that are not universal A1 common rules.

Current state: Initial Invasion timing and initial airborne-reference interface are resolved; other Scenario-specific modules remain subject to evidence-based design.

## 3.6 Initial Setup / OOB / Staging

Required: complete initial on-map units, off-map/staging state, ownership/control state, and any pre-game availability state.

Current state: German-first constrained free deployment followed by Allied invasion planning is resolved as the active setup architecture. Primary maneuver scale is regiment/brigade-centered; divisions are higher formations; battalions are selective when independently operationally meaningful. Exact OOB, represented formations, setup zones/constraints, Allied invasion choices, and staging values = UNRESOLVED.

## 3.7 Reinforcements / Replacements / Entry

Required: reinforcement schedules, replacement schedules, entry sources, entry capacities, activation conditions, and Scenario-owned entry data.

Current state: UNRESOLVED.

## 3.8 Supply / Logistics / Ports / Beachheads

Required: Scenario-owned supply-source capacities, anchors, logistics resources, port conditions, beachhead values, persistence, activation, and repair data where used.

Current state: UNRESOLVED.

## 3.9 Air / Naval / Artillery / Other Support

Required: Scenario availability, timing, capacity, restrictions, and Scenario-specific parameters for common A1 support systems.

Current state: UNRESOLVED unless a specific A1/B1 rule separately resolves an interface.

## 3.10 Airborne / Amphibious / Other Special Operations

Required: Scenario-specific availability, staging, timing, capacities, eligible areas, and other values needed to instantiate A1 special-operation frameworks.

Current state: Initial Invasion occurs in the first Allied Player Turn; initial airborne-reference exception may be used under A1-AIRB-07. Remaining data = UNRESOLVED.

## 3.11 Weather / Scenario Environment

Required: Scenario weather/environment state, schedules, probabilities, constraints, or explicit declaration that no Scenario-owned weather data is used.

Current state: UNRESOLVED.

## 3.12 Victory Conditions / End Conditions

Required: active victory method, required thresholds/areas/durations where applicable, tie/end handling, and any immediate victory/end conditions.

Current state: active decisive victory uses separate multiple Allied/German Victory Objective Hex groups and Scenario-defined simultaneous-control thresholds. Allied victory is checked at the end of the German Player Turn; German victory is checked at the end of the Allied Player Turn. Exact Objective Hex identities, group sizes, required control counts, and any side-to-side symmetry/asymmetry remain UNRESOLVED. Concession and mutual draw remain player-driven end mechanisms. No automatic fallback termination is active. Legacy full-campaign victory is NON_ACTIVE and appears only in Section 11.

## 3.13 Scenario Parameters / Calibration

Required: every Scenario-owned numeric or categorical parameter needed to instantiate A1 rules or B1-specific rules.

Current state: unresolved items are maintained in Section 7.

## 3.14 Unresolved Data Register

Required: explicit fail-closed register of missing authoritative Scenario data.

Current state: Section 7 is authoritative for current unresolved Scenario-data classes.

## 3.15 Historical Rationale / Design Rationale

Required: sufficient evidence/rationale traceability for consequential Scenario-specific choices without converting historical or prior-art sources into Rule Authority.

Current state: design-method boundary is resolved; detailed rationale records grow with later Scenario decisions.

## 3.16 B2/B3 Derivation Requirements

Required: semantic derivation rules for Japanese and English Scenario Books.

Current state: defined in Section 9.

## 3.17 Traceability / Validation Coverage

Required: mapping between B1 decisions, A1 dependencies, evidence, unresolved state, and cross-scenario independence checks.

Current state: Sections 6, 8, 10, and 11 provide the foundation; coverage expands with later B1 content.

---

# 4. Setup, OOB, and Scenario Entry State

B1-SETUP-01
The active D-Day / Normandy Scenario must define the complete initial on-map unit setup and all required off-map/staging states before formal Scenario qualification.

B1-SETUP-02
Until the exact setup/OOB values are authorized, they remain UNRESOLVED and must not be inferred from memory, later derivatives, or external games.

B1-SETUP-03
Reinforcement schedules, entry capacities, replacement schedules, map assignments, and other Scenario-owned values are normative only when explicitly resolved in B1.

B1-SETUP-04
The active D-Day / Normandy Scenario instantiates the observed sequential setup procedure defined by A1-SETUP-03 through A1-SETUP-06 as follows:
- Setup Player = German Player;
- Planning Player = Allied Player;
- Scenario-defined pre-game plan = Initial Invasion plan.
The Scenario defines the authorized German initial OOB and all legal setup areas, fixed-location requirements, exclusions, and other setup constraints required to instantiate that procedure.
Exact German setup identities, areas, hexes, and values remain Scenario-owned data.

B1-SETUP-05
After the German Player completes the Scenario-authorized initial deployment, the resulting player-visible German setup is available to the Allied Player before the Allied Player commits the Initial Invasion plan.
This instantiates A1-SETUP-04 and A1-SETUP-05.
The active Scenario does not use simultaneous secret initial deployment.

B1-SETUP-06
The active Scenario must define the D-Day-specific Initial Invasion data needed for the Allied Planning Player's pre-game commitment under A1-SETUP-05 and for execution under A1-AMPH-02, including authorized invasion choices and all required eligible-formation, staging, lift/capacity, coastal-hex, and related Scenario parameters.
Exact invasion choices and values remain Scenario-owned data.

B1-SETUP-07
Allied formations designated for the Initial Invasion or initial airborne operations begin in the Scenario-defined off-map/staging states and enter or are placed through the authorized Initial Invasion / Airborne procedures.
No exact Allied initial OOB, staging allocation, invasion area, or landing assignment is resolved by this rule.

B1-SETUP-08
Game Setup and Allied Initial Invasion planning/commitment are completed before Game Turn 1 under A1-SETUP-01 and A1-SETUP-06; neither creates an additional Player Turn.
Game Turn 1 then follows B1-PLAYER-03: Allied Player Turn followed by German Player Turn.
B1-CAMP-04 instantiates A1-AMPH-01 for D-Day: the committed Initial Invasion is resolved during the first Allied Player Turn's Special Operations Step before the first Allied Supply Checkpoint.

---

# 5. Active Victory State

B1-ACTIVE-VICT-01
The active D-Day / Normandy Campaign MUST define one or more positive decisive victory conditions for the Allied Player and one or more positive decisive victory conditions for the German Player.
The exact decisive conditions remain UNRESOLVED until separately authorized.

B1-ACTIVE-VICT-02
Active decisive victory areas, force/logistics conditions, thresholds, required durations, and any quality-of-victory grading remain UNRESOLVED until separately authorized.

B1-ACTIVE-VICT-03
The Legacy full-campaign victory model in Section 11 must not be used as the active D-Day / Normandy victory method without explicit change control and authorization.

---

B1-ACTIVE-VICT-04
The active D-Day / Normandy Campaign does not end merely because a predetermined calendar date or maximum Game Turn number is reached.
Its authorized game-end modes are:
- satisfaction of an active decisive victory condition;
- concession by either player;
- mutual agreement by both players to a draw.

B1-ACTIVE-VICT-05
When an Allied or German decisive victory condition is satisfied at its authorized check timing, play ends and that side wins according to the active decisive-condition rule.
The active D-Day / Normandy decisive-victory check timings are defined by B1-ACTIVE-VICT-12.

B1-ACTIVE-VICT-06
Either player may concede by declaring defeat under A1-VICT-09.
The game ends immediately and the opposing player wins.

B1-ACTIVE-VICT-07
The two players may mutually agree to a draw under A1-VICT-10.
A unilateral draw proposal does not end the game; agreement by both players ends play immediately as a draw.

B1-ACTIVE-VICT-08
The active D-Day / Normandy Campaign has no automatic fallback termination for containment, exhaustion, objective impossibility, operational stalemate, or similar state merely to force the game to end.
If no decisive victory condition has ended play, neither player concedes, and no mutual draw is agreed, play continues.

B1-ACTIVE-VICT-09
A human-controlled or AI-controlled Allied/German player role has the same authority to concede or to propose, accept, or decline a draw.
The AI decision policy for doing so is not B1 rule meaning.

B1-ACTIVE-VICT-10
The active Scenario defines an Allied Victory Objective Hex group and a German Victory Objective Hex group.
Each group contains multiple Scenario-designated Objective Hexes.

B1-ACTIVE-VICT-11
For each side, the active Scenario defines a required simultaneous-control count for that side's Victory Objective Hex group.
At an authorized decisive-victory check, a side satisfies its Objective victory condition when it controls at least its required number of its own designated Victory Objective Hexes simultaneously.

B1-ACTIVE-VICT-12
The Allied Objective victory condition is checked at the end of each German Player Turn.
The German Objective victory condition is checked at the end of each Allied Player Turn.
If the checked side satisfies its active Objective victory condition, play ends immediately and that side wins under B1-ACTIVE-VICT-05.

B1-ACTIVE-VICT-13
Before formal Scenario qualification, the active Scenario's map, German setup constraints, Allied Initial Invasion options, and opening forces must be calibrated so that the Allied Player has a legal Turn 1 opportunity to gain control of enough German Victory Objective Hexes to prevent German decisive victory from being automatic merely because of the initial German setup.
The exact Objective Hexes, counts, geometry, combat probabilities, and other map-dependent calibration values are not resolved by this rule.

B1-ACTIVE-VICT-14
The exact number of Allied Victory Objective Hexes, Allied required simultaneous-control count, number of German Victory Objective Hexes, German required simultaneous-control count, whether the two sides use equal or unequal totals/thresholds, and the exact Objective Hex identities/locations remain UNRESOLVED until later Scenario/map calibration.

---

# 6. Scenario Independence and Cross-Scenario Coverage

B1-INDEP-01
B1/A1 development must maintain a Scenario Reference Portfolio and Cross-Scenario Coverage model so that A1 common rules are not validated only against D-Day.

B1-INDEP-02
External games and scenarios used in this portfolio are Design Evidence / Prior-Art Reference only. They are not Rule Authority and their specific text, tables, or values must not be copied into B1 as authority.

Current reference classes/evidence include:

- Normandy '44 — D-Day/Normandy campaign and shorter-scenario comparison;
- Salerno '43 — alternate amphibious invasion comparison;
- Holland '44 — airborne/bridge/reinforcement-race comparison;
- Ardennes '44 — land breakthrough/counterattack/weather/supply/traffic comparison;
- The Battle for Normandy — multiple Normandy operational phases and Scenario Book information-structure comparison.

Cross-Scenario Coverage dimensions currently include at least:

| Dimension | Primary cross-check purpose |
|---|---|
| Amphibious invasion | prevent D-Day-only amphibious semantics |
| Airborne operation | keep airborne interface separable from amphibious rules |
| Beachhead / entry | test generic entry/supply boundaries |
| Bridge / river / traffic | test general operational terrain/traffic semantics |
| Breakthrough | test common rules outside invasion opening conditions |
| Counterattack | test defending-side operational response |
| Campaign vs short Scenario | separate Scenario scope from common-rule meaning |
| Multi-phase Normandy campaign | test one common system across invasion, attrition, breakout, and related phases |
| Scenario Book structure | support later B1 -> B2/B3 information completeness without making prior art authoritative |

This coverage model is validation/development control. It does not make any external Scenario normative.

---

# 7. Unresolved Data Register

The items below are Scenario/campaign/map/unit data gaps. They are not permission to infer values.

OPEN-DATA-01 Exact Allied/German Victory Objective Hex identities, group sizes, and required simultaneous-control counts. Active check timing is resolved by B1-ACTIVE-VICT-12.
OPEN-DATA-02 Exact Scenario map extent, hex layout, and playable-region definition.
OPEN-DATA-03 Scenario map terrain, river, road, bridge, port, fortification, and other feature assignments.
OPEN-DATA-04 Exact unit FULL/REDUCED combat factors and Regular Movement Allowances.
OPEN-DATA-05 Smaller-formation stacking, supply, and entry values.
OPEN-DATA-06 Number of Logistics Support resources for the active Scenario.
OPEN-DATA-07 Supply Source capacities and Supply Anchor definitions.
OPEN-DATA-08 Beachhead supply/entry values and persistence.
OPEN-DATA-09 Operational Movement eligibility by formation.
OPEN-DATA-10 TAP schedules and initial TAP values.
OPEN-DATA-11 HBR availability/count/timing.
OPEN-DATA-12 Airborne Lift values and any Scenario-defined initial airborne reference hexes.
OPEN-DATA-13 Initial-invasion lift, maximum assault hexes, and Amphibious Combat Band shift where used.
OPEN-DATA-14 Amphibious Reserve ready/expiry window and eligible coast where used.
OPEN-DATA-15 Reinforcement schedules and Entry Capacities.
OPEN-DATA-16 Replacement schedules and any reconstitution rules.
OPEN-DATA-17 Active D-Day/Normandy Objective Hex locations, per-side Objective group sizes, required simultaneous-control thresholds, any side-to-side symmetry/asymmetry, and any later quality-of-victory grading.
OPEN-DATA-18 Port repair delays/activation, sea-access conditions, capacities, and other Scenario-specific port conditions.
OPEN-DATA-19 Weather-specific Scenario constraints or explicit no-Scenario-weather declaration.
OPEN-DATA-20 Exact initial setup/OOB and all off-map/staging states.
OPEN-DATA-21 Scale-sensitive calibration values required by A1 v0.25 interfaces, including Stack Demand/Capacity, Supply Demand/Reach and Logistics Reach Increment, Entry Demand, Replacement Cost, Airborne Lift Demand/Reference Distance, Amphibious Lift Demand, and movement/unit-data calibration.

Named historical-operation inclusion, exact geographic fidelity, map count, and future commercial packaging are not automatically Core Rule questions.

---

# 8. A1 Dependency Interface

B1-REF-01
B1 uses the common legality, timing, movement, combat, supply, reinforcement, air, airborne, amphibious, turn-sequence, and generic victory frameworks defined by A1.

B1-REF-02
A B1 parameter or Scenario-specific rule is valid only if it instantiates or selects behavior permitted by A1, or if a separately approved A1 change creates the required extension point.

B1-REF-03
A conflict between active A1 and B1 meaning is not resolved by precedence. It is BLOCKED/UNRESOLVED until change control produces compatible authoritative text.

B1-REF-04
Scenario-specific data must not be moved into A1 merely because the D-Day Scenario needs it. A1 ownership requires reusable common-rule meaning.

---

# 9. B2/B3 Derivation Requirements

B1-DERIVE-01
B2 Japanese D-Day Scenario Book and B3 English D-Day Scenario Book must derive Scenario semantics directly from B1 plus referenced A1 common rules.

B1-DERIVE-02
B2 and B3 must not use each other as semantic source.

B1-DERIVE-03
`User-Facing_Artifact_Design_Guide_v0.1_STABLE` is REFERENCE_ONLY for B2/B3 design and may not change B1/A1 rule meaning.

B1-DERIVE-04
Prior-art Rulebooks, Playbooks, and Scenario Books may inform human-facing structure as Design Evidence but may not become semantic authority for B2/B3.

---

# 10. Traceability and Validation Foundation

B1-TRACE-01
Each later consequential B1 Scenario decision should retain enough traceability to identify its governing Basic Policy, A1 dependency where applicable, Scenario evidence/rationale, and unresolved dependencies.

B1-TRACE-02
Scenario independence must be checked by coverage dimension rather than by assuming one external game is a universal template.

B1-TRACE-03
A B1 content category is not considered resolved merely because a Player-facing derivative contains plausible prose or values.

B1-TRACE-04
B1 qualification must fail closed when mandatory Scenario content remains unresolved for the target playable product state.

---

B1-TRACE-05
The active 3-calendar-day Game Turn instantiates the Scenario-defined temporal-duration interface in A1-FOUND-01. B1-PLAYER-03 separately instantiates the Scenario-defined Player Turn order interface in A1-FOUND-02 as Allied Player Turn -> German Player Turn.

B1-TRACE-06
The active approximately-10-km map scale and regiment/brigade-centered maneuver scale instantiate the Scenario-defined spatial and formation interfaces in A1-FOUND-03 and A1-FOUND-04.
B1 does not infer scale-sensitive stacking, supply, entry, replacement, airborne/amphibious lift, or movement calibration values from the nominal scale alone.

---

# 11. Legacy / Historical State — NON_ACTIVE

This section preserves content migrated from the former A1 Western Front full-campaign profile. It is not active D-Day / Normandy Scenario authority.

LEGACY_SCOPE_STATUS: LEGACY_NON_ACTIVE
LEGACY_FULL_CAMPAIGN_VICTORY: NON_ACTIVE

## 11.1 Legacy Full-Campaign Scope

LEGACY-B1-CAMP-02 (former active ID B1-CAMP-02)
The current full campaign represents the Western Front through no later than 7 May 1945.

LEGACY-B1-CAMP-03 (former active ID B1-CAMP-03)
The current full campaign lasts at most 48 Game Turns.

The wording above is preserved for historical traceability. The phrase "current full campaign" reflects the former source state and has no current active authority in B1 v0.2.

## 11.2 Legacy Full-Campaign Victory

LEGACY-B1-VICT-01 (former active ID B1-VICT-01)
Current full-campaign Allied victory is based on sustained SUPPLIED penetration into a decisive area, not a generic victory-point total.

LEGACY-B1-VICT-02 (former active ID B1-VICT-02)
Current full-campaign data must define:
- Decisive Penetration Area;
- required number of Allied standard division-equivalents;
- required number of consecutive Allied Supply Checkpoints.

LEGACY-B1-VICT-03 (former active ID B1-VICT-03)
At each Allied Supply Checkpoint, after supply and isolation effects are resolved, count surviving SUPPLIED Allied standard division-equivalents in the Decisive Penetration Area.

LEGACY-B1-VICT-04 (former active ID B1-VICT-04)
If the required threshold is met for the required number of consecutive Allied Supply Checkpoints, the Allied player wins immediately.

LEGACY-B1-VICT-05 (former active ID B1-VICT-05)
If no Allied victory has occurred by the end of the German Player Turn of Turn 48, the German player wins.

LEGACY-B1-VICT-06 (former active ID B1-VICT-06)
Germany also wins immediately at the end of a German Player Turn if all are true:
- no Allied ground maneuver unit remains on-map;
- no Allied continental Entry Source is currently capable of introducing at least one standard division-equivalent on the next Allied entry opportunity;
- no unused Amphibious Reserve remains available.

LEGACY-B1-VICT-07 (former active ID B1-VICT-07)
For B1-VICT-06, a continental Entry Source counts as currently usable only if its activation requirements are satisfied, it will have positive Entry Capacity for the next Allied entry opportunity, and it has at least one legal entry hex at the time of the German victory check.

LEGACY-B1-VICT-08 (former active ID B1-VICT-08)
The current full campaign uses no generic victory-point total.
Other scenarios may define their own victory methods explicitly.

The wording above is preserved as Legacy/Historical evidence only. None of LEGACY-B1-VICT-01 through LEGACY-B1-VICT-08 defines active D-Day / Normandy victory in v0.2.

---

# 12. Current Status

- Active B1 scope = D-Day / Normandy Campaign.
- Active start = 6 June 1944.
- Active turn length = exactly 3 calendar days.
- Active end policy = CONDITION_DRIVEN; no fixed end date and no fixed maximum total Game Turn count.
- Final calendar date = derived from the Game Turn in which an active Game End Condition ends play.
- Base player model = two-player competitive, Allied Player vs German Player; either role may be human- or AI-controlled.
- Active victory architecture = positive decisive victory conditions for both sides + concession + mutual draw; exact decisive conditions/parameters = UNRESOLVED.
- No automatic containment/exhaustion/stalemate fallback termination is active.
- Legacy Western Front full-campaign scope and victory are preserved but NON_ACTIVE.
- Scenario Content Contract is defined.
- Scenario Reference Portfolio / Cross-Scenario Coverage foundation is bound as Design Evidence, not Rule Authority.
- Exact OOB/setup/map/reinforcement/calibration data remain UNRESOLVED.
- A1 v0.28 provides the common two-player concession/draw framework; B1 v0.7 instantiates positive decisive victory for both sides with concession/mutual-draw end modes and no automatic fallback.
- B2/B3 have not yet been generated.
