# D-Day Canonical Rule Specification v0.30 WORKING

STATUS: WORKING_SCENARIO_INDEPENDENCE_BOUNDARY_REFACTOR
DATE: 2026-09-10
ROLE: A1 — COMMON_RULE_CANONICAL_SOURCE
BASELINE: D-Day_Rulebook_Development_Baseline_v0.7_APPROVED
SOURCE_REFERENCE: D-Day_Canonical_Rule_Specification_v0.18_WORKING
SOURCE_TRIAGE: D-Day_Canonical_v0.18_Architecture_Minimality_Forensic_Triage_v0.1
SOURCE_POLICY: D-Day_Rulebook_Development_Baseline_v0.7_APPROVED.md
PARENT_A1: `D-Day_Canonical_Rule_Specification_v0.29_WORKING.md`
CHANGE_SPEC: `D-Day_A1_B1_Scenario_Independence_Boundary_Refactor_Change_Spec_v0.1_APPROVED_SCOPE_FROZEN.md`
SCENARIO_CANONICAL: D-Day_Scenario_Canonical_Source_v0.11_WORKING.md
SOURCE_GATE_HISTORY: D-Day_Full_Campaign_Rule_Data_Calibration_Entry_Gate_APPROVED_v0.1
SOURCE_BOUNDARY_TRIAGE: D-Day_A1_v0.20_Core_Rule_Scenario_Boundary_Triage_v0.1
SOURCE_HUMAN_UAT: D-Day_A2_A3_v0.1_User_Audit_FAIL_2026-09-10

PURPOSE:
Define reusable common game-rule meaning for the D-Day Rulebook System.
This document is normative for common rule meaning used by A2/A3 and referenced by B1/B2/B3.
It is not a Machine Implementation Specification and it does not own D-Day-specific scenario data.

BOUNDARY:
- Player-visible common legality, timing, state, outcome, resource-use, and generic victory semantics belong here.
- Reusable player-visible Game Setup, pre-game commitment sequencing, and special-operation procedures belong here; D-Day-specific Player Role names/order, setup-role assignment, Initial Invasion planning choice, setup/OOB values, chronology, scenario parameters, victory settings, map assignments, and calibration data belong in B1.
- B1 may instantiate parameters or select options that A1 explicitly permits, but B1 may not silently redefine an A1 common rule.
- If A1 and B1 require incompatible meanings, the conflict remains BLOCKED/UNRESOLVED until normal change control resolves it.
- Historical facts and real geography are design evidence/reference; maps and scenarios represent them schematically at the chosen game scale.
- Internal flags, cached sets, storage models, object schemas, and software bookkeeping do not belong here unless they are themselves part of play.
- UNRESOLVED common-rule meaning remains explicit.

---

# 1. SYSTEM FRAME

## 1.1 Core System Frame

A1-FOUND-01
A Game Turn is the common operational time unit.
The active Scenario/Campaign MUST define the calendar duration represented by one Game Turn.
Rules expressed in Game Turns retain the same common-rule meaning regardless of the Scenario-defined calendar duration unless a rule explicitly depends on elapsed calendar time.

A1-FOUND-02
Each Game Turn consists of one Player Turn for each of the two opposing player roles.
The active Scenario/Campaign defines the order in which those two Player Turns occur.
After both Player Turns are complete, play proceeds to the next numbered Turn unless the active Scenario/Campaign has ended.

A1-FOUND-03
Play uses hex-based operational geography.
The active Scenario/Campaign MUST define the nominal physical distance represented by one hex, or explicitly define an equivalent non-literal operational scale if a fixed distance is not used.
Scenario maps are schematic representations of operational relationships; exact real-world distance or coordinate placement is not itself a rule requirement.

A1-FOUND-04
The active Scenario/Campaign MUST define its primary maneuver-formation scale and identify which formation classes are normally represented as directly maneuvered ground units.
Higher organizational formations and smaller independently represented formations may coexist when authorized by Scenario/unit data.

A1-FOUND-05
The design uses bounded, visible combat uncertainty.
Hidden probability modifiers are not permitted.

## 1.2 Player Roles

A1-PLAYER-01
The base game is a competitive two-player game with exactly two opposing player roles.
The active Scenario/Campaign defines the names of those two player roles.
Each role is a victory-bearing decision actor for its side.

A1-PLAYER-02
Either player role may be controlled by a human or by an AI player.
A player role has the same legal actions, player-visible information rights, obligations, and victory accountability regardless of whether its controller is human or AI.

A1-PLAYER-03
Automation, rules enforcement, calculation, presentation, or referee functions are not themselves a third player role.
An AI performs player decisions only when it is assigned to one of the two active player roles.

A1-PLAYER-04
The base common rules do not define a one-player-versus-system mode.
Any future solo mode or cooperative variant requires separate explicit authorization and must not silently alter the two-player competitive baseline.

## 1.3 Core Game Terms

A1-TERM-01
A ground maneuver unit is a map unit allowed to occupy map hexes and perform ground movement.

A1-TERM-02
A hex is occupied when it contains one or more ground maneuver units of one side.
Opposing ground maneuver units may not occupy the same hex.

A1-TERM-03
A controlled hex is a hex whose territorial control belongs to one side.

A1-TERM-04
Zone of Control (ZOC) is the operational influence projected by an eligible ground maneuver unit into adjacent hexes.

A1-TERM-05
A ground maneuver unit is IN_CONTACT when the hex it occupies is inside one or more enemy ZOCs.

A1-TERM-06
A stack is two or more friendly ground maneuver units occupying the same hex.

A1-TERM-07
Occupation, territorial control, ZOC, and IN_CONTACT are distinct rule concepts.

## 1.4 Game Setup and Pre-Game Commitment

A1-SETUP-01
Game Setup is completed before Game Turn 1 begins.
Game Setup is not a Player Turn and does not by itself count as either player role's Player Turn for any Player-Turn timing, victory check, resource cycle, or end-of-Player-Turn effect unless an explicit rule states otherwise.

A1-SETUP-02
The active Scenario/Campaign defines all exact initial on-map setup, off-map/staging states, legal setup areas, fixed-location requirements, exclusions, initial resources, and other Scenario-owned information required to begin play.
Those exact identities, locations, quantities, and values are Scenario/unit/map data rather than fixed common-rule values.

A1-SETUP-03
A Scenario/Campaign may designate an observed sequential setup procedure.
When it does, the Scenario/Campaign identifies one player role as the Setup Player and the opposing player role as the Planning Player for that procedure.

A1-SETUP-04
Under an observed sequential setup procedure, the Setup Player completes the Scenario-authorized initial deployment before the Planning Player commits the Scenario-defined pre-game plan or decision.
After the Setup Player's deployment is complete, the resulting player-visible setup is available to the Planning Player before that commitment.
This procedure is not simultaneous secret deployment.

A1-SETUP-05
After observing the completed player-visible setup, the Planning Player selects and commits only the pre-game choices authorized by the active Scenario/Campaign.
The Scenario/Campaign defines the type of plan or decision being committed and all concrete choices, eligibility, locations, staging, capacities, and other data required for that commitment.

A1-SETUP-06
When an observed sequential setup procedure is used, Game Turn 1 begins only after the required pre-game setup and Planning Player commitment are complete.
The pre-game setup and commitment do not create additional Player Turns.
Any committed plan or operation is executed at the timing defined by the applicable common rule and active Scenario/Campaign.

---

# 2. UNITS, STEPS, STACKING, CONTROL, AND ZOC

## 2.1 Standard two-step ground-unit model

A1-UNIT-01
A ground maneuver unit using the standard two-step ground-unit model has two combat steps:
- FULL
- REDUCED
A second step loss eliminates it.
Scenario/unit data identifies which formations use this standard model.

A1-UNIT-02
A step loss changes:
FULL -> REDUCED -> ELIMINATED.

A1-UNIT-03
An eliminated unit is removed from the map immediately and ceases to occupy a hex or project ZOC.
Territorial control of its former hex does not change merely because the unit was removed.

A1-UNIT-04
Each unit using the standard two-step ground-unit model has separate FULL and REDUCED attack and defense factors.
Its REDUCED state must have lower combat capability than its FULL state.
Exact factors are campaign/unit data and remain UNRESOLVED.

A1-UNIT-05
A change from FULL to REDUCED does not by itself change the unit's Regular Movement Allowance unless Scenario/unit data or a later approved rule explicitly says otherwise.

## 2.2 Stacking

A1-STACK-01
Each ground maneuver unit has a Stack Demand defined by Scenario/unit data.
The active Scenario/Campaign defines the normal Stack Capacity of a hex.
A stack is legal only when the total Stack Demand of units ending in the hex does not exceed that capacity.

A1-STACK-02
A unit's FULL or REDUCED step state does not by itself change its Stack Demand unless Scenario/unit data or an explicit rule says otherwise.
Any force-count equivalence used by a Scenario/Campaign is separate Scenario/unit data and must not be inferred from Stack Demand.

A1-STACK-03
A unit may move through a friendly-occupied hex even if stopping there would exceed the stacking limit, but its final hex after movement must be legal.

A1-STACK-04
Stack Demand values for each represented formation class are Scenario/unit data and remain UNRESOLVED unless the active Scenario/Campaign resolves them.

## 2.3 Occupation and control

A1-CONTROL-01
Opposing ground maneuver units may not occupy the same hex.

A1-CONTROL-02
Occupation, territorial control, and ZOC are distinct concepts.

A1-CONTROL-03
Entering an unoccupied enemy-controlled hex changes control to the entering side.

A1-CONTROL-04
Control persists after a unit leaves until another rule changes it.

A1-CONTROL-05
ZOC alone does not change territorial control.

## 2.4 Zone of Control

A1-ZOC-01
Every on-map ground maneuver unit projects ZOC into all six adjacent hexes unless an explicit rule says that unit does not project ZOC.

A1-ZOC-02
Entering enemy ZOC during Regular Movement ends that unit's movement.

A1-ZOC-03
A unit that begins movement in enemy ZOC may leave if the move is otherwise legal.

A1-ZOC-04
Movement directly from one enemy-ZOC hex to another is allowed if otherwise legal, but movement ends on entry.

A1-ZOC-05
ZOC does not create mandatory combat.

A1-ZOC-06
Multiple enemy ZOCs do not create an additional movement effect unless an explicit rule says otherwise.

---

# 3. TERRAIN AND MOVEMENT

## 3.1 Terrain classes

A1-TERRAIN-01
Each named terrain type has one movement class:
- NORMAL: 1 MP to enter
- DIFFICULT: 2 MP to enter
- PROHIBITED: no normal ground entry

A1-TERRAIN-02
Crossing a Major River hexside adds 1 MP unless an explicit rule removes that surcharge.

A1-TERRAIN-03
Exact named-terrain mapping remains campaign/map data and is UNRESOLVED.

## 3.2 Regular Movement

A1-MOVE-01
Each unit has a Regular Movement Allowance defined by unit data.

A1-MOVE-02
Regular Movement proceeds one adjacent hex at a time.
Entry cost equals destination-terrain cost plus any applicable crossed-hexside cost.

A1-MOVE-03
A unit may not enter a hex if the required cost exceeds its remaining MP.
There is no automatic minimum-move exception.

A1-MOVE-04
Unused MP cannot be saved or transferred.

A1-MOVE-05
A unit may not enter an enemy-occupied hex during Regular Movement.

A1-MOVE-06
Units move sequentially in the owning player's chosen order.

A1-MOVE-07
During one Ground Movement Step, a unit may perform at most one movement action:
- Regular Movement;
- Operational Movement, if eligible; or
- no movement.

## 3.3 Operational Movement

A1-OPMOVE-01
Operational Movement is an optional high-speed movement mode.

A1-OPMOVE-02
A unit may use Operational Movement only if:
- its unit data says it is eligible;
- it is SUPPLIED;
- it was not IN_CONTACT at the start of movement; and
- it has not already moved that turn.

A1-OPMOVE-03
Operational Movement Allowance is twice the unit's Regular Movement Allowance.

A1-OPMOVE-04
Operational Movement replaces Regular Movement for that turn and otherwise uses normal terrain/hexside costs unless explicitly modified.

A1-OPMOVE-05
Entering enemy ZOC ends Operational Movement.

A1-OPMOVE-06
A unit that uses Operational Movement may not attack that turn.

A1-OPMOVE-07
An INTERDICTED unit may not use Operational Movement.

## 3.4 Roads, rivers, bridges, and rail

A1-ROAD-01
Moving along a connected Major Road into DIFFICULT terrain reduces that destination terrain cost to 1 MP.

A1-ROAD-02
Major Roads do not reduce NORMAL terrain below 1 MP, do not permit entry into PROHIBITED terrain, and do not by themselves remove a Major River surcharge.

A1-ROAD-03
Major Road effects apply to both Regular and Operational Movement.

A1-RIVER-01
A Major River gives a -1 Combat Band shift only if every participating attacker attacks the target across a Major River hexside.

A1-RIVER-02
If at least one attacker attacks the target without crossing a Major River, no Major River combat shift applies.

A1-RIVER-03
A retreat may cross a Major River if the destination is otherwise legal.
It costs no MP and causes no automatic additional step loss.

A1-BRIDGE-01
An INTACT bridge across a Major River removes that river's +1 MP crossing surcharge.

A1-BRIDGE-02
A DESTROYED bridge does not remove the surcharge.

A1-BRIDGE-03
An intact bridge does not remove the Major River combat shift.

A1-BRIDGE-04
No generic bridge-demolition or engineer-repair subsystem is currently part of the core rules.
Bridge-state changes require explicit scenario/event rules.

A1-RAIL-01
No generic rail movement mode, rail-point pool, or rail-capacity accounting system is part of the core rules.
Rail features may exist as map/scenario data.

---

# 4. COMBAT

## 4.1 Combat participation and order

A1-COMBAT-01
Combat is voluntary unless an explicit rule says otherwise.
Being IN_CONTACT does not itself require an attack.

A1-COMBAT-02
One combat targets exactly one enemy-occupied hex.
All defending ground units in that target hex defend together as one group.

A1-COMBAT-03
Eligible adjacent units may participate as attackers.
One unit may not split its attack strength among multiple combats.

A1-COMBAT-04
A unit may attack at most once during its own Combat Step.

A1-COMBAT-05
A defending unit may defend in at most one combat during one enemy Combat Step.

A1-COMBAT-06
The attacking player chooses and resolves combats one at a time.
A combat is completed, including losses, retreat, advance, control changes, and other immediate effects, before the next combat is chosen.

A1-COMBAT-07
The attacker is not required to predeclare all combats.
Results from earlier combats may change the legality or value of later combats.

A1-COMBAT-08
If a hex contains any defending unit that has already defended during the current enemy Combat Step, that hex may not be selected as a new target during that Combat Step.

A1-COMBAT-09
A fresh defending unit sharing such a hex does not create an exception to A1-COMBAT-08.
This preserves both the rule that all defenders in a target hex defend together and the rule that one unit may defend at most once in the same enemy Combat Step.

## 4.2 Combat strength and Combat Bands

A1-CPOWER-01
Use the participating units' current FULL or REDUCED attack/defense factors.

A1-CPOWER-02
For a SUPPLIED unit, use its current attack and defense factors normally.

A1-CPOWER-03
For an UNSUPPLIED unit:
- attack strength is halved, rounding fractions up;
- defense strength is unchanged.

A1-CPOWER-04
Add all participating attacker strengths and all defender strengths, then form attacker strength divided by defender strength.

A1-CPOWER-05
The ratio maps to the following base Combat Band:

| Ratio | Base Combat Band |
|---|---:|
| less than 1:2 | -3 |
| 1:2 to less than 2:3 | -2 |
| 2:3 to less than 1:1 | -1 |
| 1:1 to less than 3:2 | 0 |
| 3:2 to less than 2:1 | +1 |
| 2:1 to less than 3:1 | +2 |
| 3:1 or greater | +3 |

A1-CPOWER-06
Apply all approved Combat Band shifts, then clamp the final modifier to the range -3 through +3.

A1-CPOWER-07
A combat must include at least one attacker and must have positive total attack and defense strength.
Exact factor values are unit data.

## 4.3 Roll and result

A1-RESOLVE-01
Roll two ordinary fair six-sided dice and add them.
Add the final Combat Band modifier.

A1-RESOLVE-02
Use the modified total:

| Modified total | Result |
|---|---|
| 4 or less | Attacker loses 1 step |
| 5-6 | No effect |
| 7-8 | Defender retreats 1 hex |
| 9-10 | Defender loses 1 step |
| 11 or more | Defender loses 1 step, then surviving defenders retreat 1 hex |

A1-RESOLVE-03
When the attacker must take a step loss, the attacking player chooses one participating attacker to take it.

A1-RESOLVE-04
When the defender must take a step loss, the defending player chooses one participating defender to take it.

A1-RESOLVE-05
For the combined defender loss + retreat result, apply the loss first.
If defenders survive, resolve their retreat.

A1-RESOLVE-06
No hidden probability modifier may alter the approved combat-resolution procedure.

## 4.4 Retreat

A1-RETREAT-01
Standard retreat distance is one hex.

A1-RETREAT-02
The defending player chooses one legal adjacent destination for the surviving defending group.

A1-RETREAT-03
The destination must:
- contain no enemy ground unit;
- not be PROHIBITED terrain;
- satisfy stacking;
- be outside enemy ZOC unless friendly occupied.

A1-RETREAT-04
All surviving defenders retreat to the same destination unless an explicit rule says otherwise.

A1-RETREAT-05
If no legal retreat destination exists, the retreating group does not move and suffers one additional step loss, assigned by the defending player to one surviving unit.

A1-RETREAT-06
Retreat does not spend MP.

## 4.5 Post-combat advance

A1-ADV-01
If combat causes the target hex to become vacant, surviving on-map participating attackers may advance into it.

A1-ADV-02
Maximum post-combat advance is one hex, into the vacated target hex only.

A1-ADV-03
Post-combat advance costs no MP, may enter enemy ZOC, and must satisfy stacking.

A1-ADV-04
No further movement follows a post-combat advance.

## 4.6 Fortifications

A1-FORT-01
Fortifications use the normal combat system; there is no separate siege CRT or siege subsystem.

A1-FORT-02
If the defending side is eligible to use at least one active fortification in the target hex, apply one -1 Combat Band shift.

A1-FORT-03
Multiple fortification features in the same target hex do not stack beyond that single -1 shift.

A1-FORT-04
Territorial control alone does not make a captured fortification usable.
Map/scenario data must state which side can use each fortification and whether it is active.

---

# 5. LOGISTICS

## 5.1 Supply sources and paths

A1-SUPPLY-01
A Supply Source is a location authorized to provide supply.
Each source has a side, a source type, a Supply Capacity, and a Base Reach.

A1-SUPPLY-02
A normal land supply path is a contiguous path of adjacent land hexes from the unit to a usable friendly Supply Source.

A1-SUPPLY-03
Every path hex must be friendly-controlled and free of enemy ground units.

A1-SUPPLY-04
A path may pass through an enemy-ZOC hex only if that hex is friendly occupied.

A1-SUPPLY-05
PROHIBITED terrain blocks normal land supply unless an explicit rule says otherwise.

A1-SUPPLY-06
Path length is counted in hex transitions.

## 5.2 Capacity and Logistics Support

A1-SUPPLY-07
Each ground maneuver unit has a Supply Demand defined by Scenario/unit data.
A change between FULL and REDUCED state does not by itself change Supply Demand unless Scenario/unit data or an explicit rule says otherwise.

A1-SUPPLY-08
A normally supplied unit must be assigned to one usable Supply Source with a legal path, sufficient reach, and available capacity.

A1-SUPPLY-09
The total Supply Demand assigned to one source may not exceed that source's Supply Capacity.

A1-SUPPLY-10
The owning player chooses among legal source assignments.
A unit without a valid normal assignment is UNSUPPLIED unless an explicit special-supply rule applies.

A1-SUPPLY-11
Each Supply Source uses the Base Reach defined by Scenario/source data.
Base Reach is measured in hex transitions under A1-SUPPLY-06.

A1-SUPPLY-12
Each Logistics Support resource assigned to a source adds the Scenario-defined Logistics Reach Increment to that source's Base Reach.
A maximum of two Logistics Support resources may be assigned to one source unless a separately approved common rule changes that limit.
The resulting reach is Base Reach plus zero, one, or two Logistics Reach Increments.

A1-SUPPLY-13
Each Logistics Support resource may support only one source at a time.
The total number assigned may not exceed the side's available Logistics Support resources.

A1-SUPPLY-14
Logistics Support is assigned during the Logistics Support Declaration step and cannot be reassigned again during that Supply Checkpoint.
It is not consumed by being assigned.

## 5.3 Ports and beachheads

A1-PORT-01
A port has operational state CLOSED, DAMAGED, or ACTIVE and sea access CLOSED or OPEN.

A1-PORT-02
A port can function as a normal Supply Source only when:
- it is friendly-controlled;
- its port state is ACTIVE; and
- sea access is OPEN.

A1-PORT-03
Control alone does not activate a port.

A1-PORT-04
Capturing, repairing, or opening a port after a Supply Checkpoint does not change that already-completed supply determination.

A1-PORT-05
Capturing a port does not automatically make it usable.

A1-PORT-06
Campaign/scenario data for each relevant port must define:
- its operational state after capture;
- the condition or delay by which a DAMAGED port becomes ACTIVE;
- its sea-access condition.

A1-PORT-07
Port repair is not a generic player-managed engineer/resource subsystem in the core rules.
Port-specific recovery is represented by the explicit campaign/scenario condition or delay for that port.

A1-PORT-08
Sea access is independent of physical port condition.
A port may be ACTIVE but unusable as a Supply Source or Entry Source while its sea-access condition is not satisfied.

A1-PORT-09
A port that becomes usable after the current Supply Checkpoint does not retroactively change that completed supply determination.

A1-PORT-10
Exact port-by-port repair delays, activation conditions, sea-access conditions, and capacities remain campaign/scenario data and are UNRESOLVED.

A1-PORT-11
Beachheads are distinct from ports even when both exist in the same hex.

## 5.4 Supply effects and timing

A1-SUPPLY-15
Each side checks supply once during its own Player Turn, before Ground Movement.

A1-SUPPLY-16
The supply result is based on the board and source situation at that Supply Checkpoint and remains in effect until that side's next Supply Checkpoint.
Do not recalculate supply continuously during movement or combat.

A1-SUPPLY-17
An UNSUPPLIED unit:
- halves attack strength, rounding up;
- halves Regular Movement Allowance, rounding up;
- keeps normal defense strength;
- may not use Operational Movement.

## 5.5 Isolation

A1-ISO-01
Isolation is separate from ordinary supply status.

A1-ISO-02
At each own Supply Checkpoint, determine whether a unit has a legal physical land connection to a friendly Supply Anchor.
For this connection test, ignore source capacity, source reach, and source activation; use the normal supply-path restrictions.

A1-ISO-03
A unit with physical connection is CONNECTED.

A1-ISO-04
A unit without physical connection is ISOLATED.

A1-ISO-05
On the first consecutive Supply Checkpoint at which the unit is isolated, it suffers no isolation step loss.
At each later consecutive own Supply Checkpoint while it remains isolated, it suffers one step loss after supply determination.

A1-ISO-06
An ISOLATED unit cannot receive normal source supply, but an explicit special-supply rule may temporarily supply it.

A1-ISO-07
Exact Supply Anchor locations are campaign/map data and remain UNRESOLVED.

---

# 6. REINFORCEMENTS AND REPLACEMENTS

## 6.1 Reinforcement availability

A1-REINF-01
A reinforcement is:
- SCHEDULED before its availability condition is met;
- AVAILABLE when it may enter;
- ENTERED after it has been legally placed on the map.

A1-REINF-02
Normal reinforcement availability is checked during the Start/Resource Step.

A1-REINF-03
An AVAILABLE reinforcement remains available if it cannot or does not enter that turn.

A1-REINF-04
Each reinforcement has an entry state of FULL or REDUCED.
If it later survives an off-map staging state with losses, those losses are retained; simply entering later does not restore it.

A1-REINF-05
Every scenario identifies which side each reinforcement belongs to, which formation it is, when it becomes available, and how it may enter.

A1-REINF-06
An ELIMINATED formation may not return merely because it is or once was an available reinforcement.
It can return only through an explicit reconstitution rule followed by legal entry.

## 6.2 Normal entry

A1-ENTRY-01
An Entry Source is an authorized reinforcement-introduction location.

A1-ENTRY-02
A port used as an Entry Source must be friendly-controlled, ACTIVE, OPEN to sea access, and explicitly authorized for entry.

A1-ENTRY-03
Each Entry Source has an Entry Capacity for that Player Turn.
Entry Capacity and Supply Capacity are separate.

A1-ENTRY-04
Each reinforcement formation has an Entry Demand defined by Scenario/unit data.
A change between FULL and REDUCED state does not by itself change Entry Demand unless Scenario/unit data or an explicit rule says otherwise.

A1-ENTRY-05
The total Entry Demand entering through a source in one Reinforcement Entry Step may not exceed that source's Entry Capacity.
Unused Entry Capacity does not carry forward.

A1-ENTRY-06
An entry hex must be:
- friendly-controlled;
- free of enemy ground units;
- outside enemy ZOC;
- stacking-legal.

A1-ENTRY-07
If no legal entry hex is available, the reinforcement remains AVAILABLE.

A1-ENTRY-08
A reinforcement that enters normally is on-map before that Player Turn's Supply Checkpoint.

## 6.3 Replacements

A1-REPL-01
Each side receives Replacement Points (RP) according to campaign/scenario schedule.
Unused RP carry over.

A1-REPL-02
Each formation eligible for replacement has a Replacement Cost defined by Scenario/unit data.
During the Replacement Step, spending that Replacement Cost restores one eligible REDUCED formation to FULL.

A1-REPL-03
A unit is eligible for replacement only if it is:
- REDUCED;
- SUPPLIED; and
- not IN_CONTACT.

A1-REPL-04
Replacement does not grant movement, change position, clear contact, or otherwise create an additional action.

A1-REPL-05
Generic RP cannot restore an ELIMINATED formation.
Eliminated formations return only through explicit reconstitution plus normal reinforcement entry.

A1-REPL-06
Exact replacement schedules and any reconstitution rules remain UNRESOLVED.

A1-OBJECTIVE-01
There is no generic rule that awards replacement strength merely for capturing an objective.

A1-SEA-01
There is no generic sea-redeployment system.

---

# 7. TACTICAL AIR, INTERDICTION, AND HBR

## 7.1 Tactical Air Points

A1-AIR-01
Tactical Air Points (TAP) represent allocatable tactical air effort.

A1-AIR-02
Campaign/scenario data determines each side's TAP availability.
Unused TAP expire at the end of their defined air-resource cycle.

A1-AIR-03
Approved TAP missions are:
- Offensive Air Support;
- Defensive Air Support;
- Operational Interdiction.

A1-AIR-04
There is no separate generic route/river-interdiction mission.

## 7.2 Combat air support

A1-AIRSUP-01
Offensive Air Support costs 1 TAP and gives +1 Combat Band to one friendly attack.
Maximum: one Offensive Air Support mission per combat.

A1-AIRSUP-02
Defensive Air Support costs 1 TAP and gives -1 Combat Band to one combat against one friendly defending hex.
Maximum: one Defensive Air Support mission per combat.

A1-AIRSUP-03
For each combat, commitments occur in this order:
1. attacker declares eligible HBR;
2. attacker declares Offensive Air Support;
3. defender declares Defensive Air Support;
4. final Combat Band is determined;
5. combat is rolled.

A1-AIRSUP-04
Once a resource is committed in that sequence, it cannot be withdrawn because of a later opposing declaration.

## 7.3 Operational Interdiction

A1-INT-01
Operational Interdiction costs 1 TAP and targets one enemy on-map ground maneuver unit.

A1-INT-02
The target may not use Operational Movement during its next own Ground Movement Step.

A1-INT-03
Interdiction does not by itself reduce Regular Movement or combat strength.

A1-INT-04
Additional interdiction missions on the same already-interdicted unit have no additional effect.

A1-INT-05
Interdiction is declared during the opponent-air-interdiction window immediately before that side's Ground Movement Step.

## 7.4 Heavy Breakthrough Bombardment

A1-HBR-01
Heavy Breakthrough Bombardment (HBR) is a scarce campaign resource.
Campaign/scenario data defines its available uses, first eligible turn, and expiry if any.

A1-HBR-02
An HBR target must:
- be enemy occupied when HBR is declared; and
- be the same hex that had at least one adjacent friendly ground unit at the end of the attacking side's previous Player Turn.

A1-HBR-03
The friendly unit that established that prior adjacency need not still be present when HBR is used.

A1-HBR-04
HBR costs one available use.

A1-HBR-05
For an HBR-supported attack, resolve the normal combat roll twice using the same Combat Band and known modifiers.
Reveal both outcomes; the attacker chooses one and applies only that outcome.

A1-HBR-06
HBR does not itself change the Combat Band and does not create a new result type.

A1-HBR-07
HBR may not support Amphibious Assault.

A1-HBR-08
The exact HBR schedule/count remains UNRESOLVED.

---

# 8. AIRBORNE OPERATIONS

A1-AIRB-01
Only formations identified as airborne-capable may perform an Airborne Operation.

A1-AIRB-02
Campaign/scenario data defines Airborne Lift Capacity for each Player Turn in which airborne operations are permitted.
Each participating formation has an Airborne Lift Demand defined by Scenario/unit data.
Total Airborne Lift Demand may not exceed that turn's capacity; unused lift does not carry over.

A1-AIRB-03
An Airborne Operation requires:
- an airborne-capable unit;
- sufficient lift;
- the unit to be AVAILABLE off-map or at an explicitly authorized airborne staging location;
- the unit not to have moved or entered normally that turn;
- the unit not to have participated in another movement/placement Special Operation that turn.

A1-AIRB-04
A legal airborne drop hex must:
- be land terrain;
- contain no enemy ground unit;
- not be prohibited for airborne landing by map/scenario data;
- satisfy stacking.

A1-AIRB-05
The drop hex may be enemy-controlled or in enemy ZOC.
Landing in an unoccupied enemy-controlled hex changes control normally.

A1-AIRB-06
Unless an approved Scenario-specific initial-operation exception applies, the drop hex must be within the Scenario-defined Airborne Reference Distance of a friendly SUPPLIED non-airborne ground unit that was on-map at the beginning of that turn.

A1-AIRB-07
Scenario/campaign setup may define designated airborne reference hexes for an initial airborne operation instead of the normal friendly-unit reference.
When used, the drop hex must be within the Scenario-defined Airborne Reference Distance of one such reference hex.

A1-AIRB-08
There is no generic airborne scatter/failure system.
A legal committed Airborne Operation completes its placement.

A1-AIRB-09
A unit conducting an Airborne Operation may not perform Regular or Operational Movement that turn, but may attack if otherwise eligible.

A1-AIRB-10
An airborne unit is treated as SUPPLIED for the remainder of its drop turn without consuming normal source capacity.
At its following own Supply Checkpoint it returns to normal supply rules.

A1-AIRB-11
There is no generic air-extraction system.

---

# 9. AMPHIBIOUS OPERATIONS AND BEACHHEADS

## 9.1 Initial and follow-on invasion framework

A1-AMPH-01
A scenario/campaign may designate an Initial Invasion.
When designated, it is resolved during the specified owning Player Turn's Special Operations Step before that Player Turn's Supply Checkpoint.

A1-AMPH-02
Each amphibious operation must have campaign/scenario data defining:
- eligible coastal hexes;
- eligible assault formations;
- Amphibious Lift Capacity;
- maximum assault hexes;
- beachhead supply and entry values.

A1-AMPH-03
Each participating assault formation has an Amphibious Lift Demand defined by Scenario/unit data.
Total Amphibious Lift Demand assigned to the operation may not exceed its lift capacity; unused lift does not carry over.

A1-AMPH-04
Before resolving landings, the player conducting the amphibious operation assigns each participating assault unit to exactly one selected assault hex.
Assignments are fixed before any assault is resolved.

A1-AMPH-05
After assignments are fixed, the player conducting the amphibious operation chooses the order in which assault hexes are resolved.
Resolve one assault hex completely before the next; its results immediately affect the board.

## 9.2 Unopposed landing

A1-AMPH-06
If a selected coastal hex contains no enemy ground unit, assigned assault units may enter up to the stacking limit.

A1-AMPH-07
A surviving assigned unit that cannot legally enter remains off-map in amphibious staging under the same post-assault staging rules.

## 9.3 Opposed Amphibious Assault

A1-AMPH-08
If the target coastal hex contains enemy ground units, resolve an Amphibious Assault.

A1-AMPH-09
For the beach assault only, off-map assaulting units use their current FULL/REDUCED attack factors directly.
They are not treated as normally SUPPLIED or UNSUPPLIED solely for that off-map combat, and the assault consumes no normal Supply Source capacity.

A1-AMPH-10
Amphibious Assault uses the normal ratio, Combat Band, dice, result, loss, and retreat system with these changes:
- apply the scenario-defined Amphibious Combat Band shift once;
- apply target-hex terrain shift normally;
- apply an eligible fortification shift normally;
- Offensive and Defensive Air Support may be used normally;
- HBR may not be used;
- Major River shift does not apply merely because the attackers approach from sea staging.

A1-AMPH-11
If defenders vacate or are eliminated, surviving assault units may occupy the target hex up to stacking limits.

A1-AMPH-12
A surviving assault unit that does not enter the target hex returns to off-map amphibious staging with any losses retained.

A1-AMPH-13
A unit in amphibious staging may take no further movement, attack, reinforcement entry, or other entry action during the rest of that Player Turn.
At the beginning of the next owning Start/Resource Step it becomes AVAILABLE again.

A1-AMPH-14
A failed assault does not restore spent amphibious capability.
Any later amphibious attempt requires a separate currently legal amphibious capability.

## 9.4 Actions after landing

A1-AMPH-15
Participation in an amphibious operation consumes that unit's ground-movement action for the turn.
A landed amphibious unit may not use Regular or Operational Movement later that turn.

A1-AMPH-16
A unit that lands unopposed may attack during the later normal Combat Step if otherwise eligible.

A1-AMPH-17
A unit that participated as an attacker in an opposed Amphibious Assault may not attack again in the later normal Combat Step that turn.

A1-AMPH-18
A surviving unit that defended against an opposed Amphibious Assault may not be attacked again in the later normal Combat Step of that same Player Turn.

A1-AMPH-19
A unit may participate in at most one movement/placement Special Operation during one own Player Turn.

A1-AMPH-20
No generic post-landing defense penalty exists.

## 9.5 Beachheads

A1-BEACH-01
A coastal hex successfully occupied through the Initial Invasion or a legal follow-on invasion becomes a Beachhead.

A1-BEACH-02
Beginning with the first owning-side Supply Checkpoint after its creation, a Beachhead may function as a temporary Supply Source and Entry Source using campaign/scenario values.

A1-BEACH-03
Beachhead data must define:
- Base Reach;
- Supply Capacity;
- Entry Capacity;
- entry hexes;
- persistence.

A1-BEACH-04
A Beachhead does not require a port to be ACTIVE and remains distinct from any port in the same hex.

A1-BEACH-05
When Beachhead persistence ends, its temporary supply/entry functions end unless an explicit rule replaces them.

## 9.6 Amphibious Reserve

A1-ARES-01
The campaign may include one one-use Amphibious Reserve authorizing one follow-on invasion.

A1-ARES-02
Campaign/scenario data defines its ready turn, expiry turn, lift, eligible coast, and maximum assault hexes.

A1-ARES-03
It may be used once during its inclusive ready-to-expiry window.
If unused by the end of its owning side's Special Operations Step on the expiry turn, it expires.

A1-ARES-04
A follow-on invasion uses the normal approved amphibious rules unless an explicit scenario rule states a permitted difference.

---

# 10. COMPLETE PLAYER-TURN SEQUENCE

A1-TURN-01
Each Player Turn proceeds in this order:

1. Start / Resource Step
2. Reinforcement Entry Step
3. Special Operations Step
4. Logistics Support Declaration
5. Supply Checkpoint
6. Replacement Step
7. Opponent Air Interdiction Window
8. Ground Movement Step
9. Combat Step
10. End Step

A1-TURN-02
If the active scenario/campaign designates an Initial Invasion, resolve it during the Special Operations Step as specified by A1-AMPH-01.

A1-TURN-03
Within the Special Operations Step, legal special operations are resolved in the owning player's chosen order unless an explicit rule requires another order.

A1-TURN-04
Scenario/campaign setup establishes TAP available for each side's initial air-resource cycle.
From the next own Start/Resource Step onward, unused TAP from the previous cycle expires and the new scenario-defined TAP amount becomes available.

---

# 11. TERRAIN COMBAT, WEATHER, AND SPECIAL-SYSTEM POLICY

A1-TCOM-01
Each named hex terrain has:
- movement class NORMAL / DIFFICULT / PROHIBITED;
- defensive terrain shift 0 or -1.

A1-TCOM-02
Only the target hex's defensive terrain shift applies as the inherent hex-terrain combat effect.
Multiple terrain labels do not stack multiple inherent terrain shifts.

A1-WEATHER-01
There is no generic random weather subsystem.
Scenario/campaign data may express seasonal or historical constraints through already-approved resource, readiness, expiry, or event rules.

A1-SPECIAL-01
Create a special local rule only when an important operational condition cannot be represented by existing core rules or cleanly by map/scenario data and when it creates a meaningful player decision.

A1-NAVAL-01
There is no generic naval combat system.

---

# 12. VICTORY

## 12.1 Core Victory Framework

A1-VICT-01
Each scenario/campaign must define its victory conditions and the timing at which they are checked.

A1-VICT-02
Victory conditions may use any already-defined game state, including:
- unit survival or position;
- territorial control;
- supply state;
- objective or area conditions;
- elapsed turns;
- scenario-defined points or thresholds.

A1-VICT-03
A scenario-specific victory method is not automatically a universal rule for other scenarios.

A1-VICT-04
Game End Conditions are distinct from Victory Conditions.
A Game End Condition defines when play stops.
Victory Conditions define the outcome awarded when or because the relevant Game End Condition is satisfied.

A1-VICT-05
A scenario/campaign may use condition-driven ending and is not required to define a fixed calendar end date or a fixed maximum Game Turn count.
A fixed time limit is valid only when the scenario/campaign explicitly defines one.

A1-VICT-06
Every scenario/campaign must define complete termination handling.
It must state the Game End Conditions and the outcome mapping needed to determine what happens when play ends.
Termination handling may not remain implicit in a formally playable scenario.

A1-VICT-07
If a scenario maps Game Turns to calendar time, its final calendar state or reported final date may be derived from the Game Turn in which a Game End Condition is satisfied, according to that scenario's temporal mapping.

A1-VICT-08
No automatic draw, tie, stalemate, exhaustion, or automatic time-limit outcome exists by default.
Player concession and mutual draw agreement are common two-player game-end mechanisms under A1-VICT-09 and A1-VICT-10.
A scenario/campaign may define additional end conditions explicitly, but they are not implied merely to force closure.

A1-VICT-09
A player may concede the game by declaring defeat.
When a player concedes, play ends immediately and the opposing player wins.

A1-VICT-10
The two players may mutually agree to end the game as a draw.
A draw proposal by one player does not end play unless the other player agrees.
When both players agree, play ends immediately as a draw.

A1-VICT-11
A human-controlled or AI-controlled player role has the same authority to concede, propose a draw, accept a draw, or decline a draw.
The canonical rules do not define the controller policy or algorithm used to make those decisions.

# 13. EXPLICITLY DEFERRED IMPLEMENTATION MATTERS

The following are NOT A1 rule questions unless future implementation reveals a player-visible ambiguity:

- internal Boolean flags for whether a unit has attacked/defended;
- cached prior-turn hex sets for HBR eligibility;
- internal source-activation predicates/functions;
- remaining-balance variable names for TAP/HBR/RP/Entry Capacity;
- internal state-machine initialization routines;
- serialization or object identity;
- PRNG algorithm, seed, library, or random-service implementation;
- internal validation schemas;
- caching/snapshot representation.

Future implementation work must preserve the rule meaning in this A1, but may choose its own internal representation.

---

END_OF_CANONICAL_v0.29_WORKING
