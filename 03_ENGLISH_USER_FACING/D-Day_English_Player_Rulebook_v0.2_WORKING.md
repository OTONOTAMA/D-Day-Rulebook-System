# Operational Wargame Player Rulebook

**Working Draft v0.2**

This rulebook explains the reusable common rules for this operational wargame system. The active Scenario tells you the specific campaign, player-role names, start date, duration of a Game Turn, map scale, setup, unit values, resources, and victory conditions.

The rules below describe what players may do, when actions occur, and how the visible game state changes. Scenario-specific values come from the Scenario and its map and unit data rather than from assumptions in this rulebook.

---

# 1. Game Overview

This chapter explains the common game framework. The active Scenario supplies the campaign-specific names, scale, and timing values.

**Abbreviations used in this chapter:** Artificial Intelligence (AI); Zone of Control (ZOC).

## 1.1 Core Game Framework

A Game Turn is the common operational time unit.
The active Scenario or Campaign states the calendar duration represented by one Game Turn.
Rules expressed in Game Turns retain the same common-rule meaning regardless of the Scenario-defined calendar duration unless a rule explicitly depends on elapsed calendar time.

Each Game Turn consists of one Player Turn for each of the two opposing player roles.
The active Scenario or Campaign defines the order in which those two Player Turns occur.
After both Player Turns are complete, play proceeds to the next numbered Turn unless the active Scenario or Campaign has ended.

Play uses hex-based operational geography.
The active Scenario or Campaign states the nominal physical distance represented by one hex, or provides an equivalent operational scale if a fixed distance is not used.
Scenario maps are schematic representations of operational relationships; exact real-world distance or coordinate placement is not itself a rule requirement.

The active Scenario or Campaign states its primary maneuver-formation scale and identifies which formation classes are normally represented as directly maneuvered ground units.
Higher organizational formations and smaller independently represented formations may coexist when authorized by Scenario or unit data.

The design uses bounded, visible combat uncertainty.
Hidden probability modifiers are not permitted.

## 1.2 Player Roles

The base game is a competitive two-player game with exactly two opposing player roles.
The active Scenario or Campaign defines the names of those two player roles.
Each role makes decisions for one side and is responsible for that side's victory conditions.

Either player role may be controlled by a human or by an AI player.
A player role has the same legal actions, player-visible information rights, obligations, and victory accountability regardless of whether its controller is human or AI.

Automation, rules enforcement, calculation, presentation, or referee functions are not themselves a third player role.
An AI performs player decisions only when it is assigned to one of the two active player roles.

The base common rules do not define a one-player-versus-system mode.
A solo or cooperative variant applies only when the Scenario explicitly provides one; otherwise, use the two-player competitive rules.

## 1.3 Core Terms

A ground maneuver unit is a map unit allowed to occupy map hexes and perform ground movement.

A hex is occupied when it contains one or more ground maneuver units of one side.
Opposing ground maneuver units may not occupy the same hex.

A controlled hex is a hex whose territorial control belongs to one side.

Zone of Control (ZOC) is the operational influence projected by an eligible ground maneuver unit into adjacent hexes.

A ground maneuver unit is in contact when the hex it occupies is inside one or more enemy ZOCs.

A stack is two or more friendly ground maneuver units occupying the same hex.

Occupation, territorial control, ZOC, and in contact are distinct rule concepts.

---

## 1.4 How to Use This Rulebook During Play

Use this Rulebook as the formal table-side reference.

When a question arises, follow this order:

1. Identify the current Step in Chapter 3.
2. Open the chapter for the action you want to perform.
3. Check legality and required conditions.
4. Resolve the procedure in the listed order.
5. If a value is not defined here, check the active Scenario or its map / unit data.
6. If you want deeper explanation of why the system works that way, use the Rules Companion.

Distinguish these kinds of rule text:

- **permission** — whether an action may be performed;
- **cost** — what must be spent;
- **timing** — when the action or check occurs;
- **state** — what status is currently in effect;
- **Scenario-defined data** — values intentionally not fixed by common rules.

Do not invent a missing Scenario value.

## 1.5 Four Questions to Ask Before Resolving an Action

For most procedures, first identify:

- **When?** Is this the correct Step?
- **What?** Which unit, hex, resource, or state is affected?
- **Conditions?** Are supply, control, contact, capacity, or other requirements met?
- **Result?** What state changes after the procedure is completed?

These four questions help locate the exact rule without turning this manual into a strategy guide.

# 2. Game Setup

Before Game Turn 1, prepare the game using the active Scenario. Some scenarios also use a pre-game planning procedure after one side completes its setup.

## 2.1 Setup and Pre-Game Planning

Game Setup is completed before Game Turn 1 begins.
Game Setup is not a Player Turn and does not by itself count as either player role's Player Turn for any Player-Turn timing, victory check, resource cycle, or end-of-Player-Turn effect unless an explicit rule states otherwise.

The active Scenario or Campaign defines all exact initial on-map setup, off-map or staging states, legal setup areas, fixed-location requirements, exclusions, initial resources, and other Scenario-specific information required to begin play.
Those exact identities, locations, quantities, and values are Scenario, unit, or map data rather than fixed common-rule values.

A Scenario or Campaign may designate an observed sequential setup procedure.
When it does, the Scenario or Campaign identifies one player role as the Setup Player and the opposing player role as the Planning Player for that procedure.

Under an observed sequential setup procedure, the Setup Player completes the Scenario-authorized initial deployment before the Planning Player commits the Scenario-defined pre-game plan or decision.
After the Setup Player's deployment is complete, the resulting player-visible setup is available to the Planning Player before that commitment.
This procedure is not simultaneous secret deployment.

After observing the completed player-visible setup, the Planning Player selects and commits only the pre-game choices authorized by the active Scenario or Campaign.
The Scenario or Campaign defines the type of plan or decision being committed and all concrete choices, eligibility, locations, staging, capacities, and other data required for that commitment.

When an observed sequential setup procedure is used, Game Turn 1 begins only after the required pre-game setup and Planning Player commitment are complete.
The pre-game setup and commitment do not create additional Player Turns.
Any committed plan or operation is executed at the timing defined by the applicable common rule and active Scenario or Campaign.

## 2.2 Scenario-Specific Systems

No generic rail movement mode, rail-point pool, or rail-capacity accounting system is part of the core rules.
Rail features may exist as map or Scenario data.

There is no general random weather system in the common rules.
Scenario data may express seasonal or historical constraints through resource, readiness, expiry, or event rules.

A Scenario should add a special local rule only when an important operational condition cannot be represented cleanly by the common rules or Scenario data and the added rule creates a meaningful player decision.

There is no generic naval combat system.

---

## 2.3 Setup Checklist

Before Game Turn 1, confirm at least:

- the active Scenario and the two player roles;
- Player-Turn order;
- all initial on-map placements;
- any off-map staging;
- initial port, Beachhead, Supply Source, or other relevant states;
- reinforcement and replacement schedules;
- initial Tactical Air or other Scenario-defined resources;
- any Special Operations available before or during the opening turn;
- Victory Conditions;
- Game End Conditions;
- any Scenario-specific exceptions.

If the Scenario uses sequential visible setup, complete the designated setup side's deployment before the planning side commits its permitted pre-game plan.

## 2.4 Setup Is Not a Player Turn

Pre-game deployment and planning are not automatically part of Game Turn 1.

Unless the Scenario explicitly says otherwise, do not perform ordinary:

- Ground Movement;
- Combat;
- Supply determination;
- Reinforcement Entry;

as part of setup.

Complete all pre-game procedures first, then begin the formal Player-Turn Sequence in Chapter 3.

# 3. Player-Turn Sequence

Each Player Turn follows the same common sequence unless an explicit Scenario rule changes a permitted option or timing.

**Abbreviations used in this chapter:** Tactical Air Points (TAP).

## 3.1 Complete Player-Turn Sequence

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

If the active Scenario or Campaign designates an Initial Invasion, resolve it during the Special Operations Step before that Player Turn's Supply Checkpoint.

Within the Special Operations Step, legal special operations are resolved in the owning player's chosen order unless an explicit rule requires another order.

Scenario setup establishes TAP available for each side's initial air-resource cycle.
From the next own Start / Resource Step onward, unused TAP from the previous cycle expires and the new Scenario-defined TAP amount becomes available.

---

## 3.2 Player-Turn Quick Table

| Order | Step | Main check |
|---:|---|---|
| 1 | Start / Resource | refresh or establish scheduled resources |
| 2 | Reinforcement Entry | enter legally available reinforcements |
| 3 | Special Operations | resolve Airborne / Amphibious or other legal operations |
| 4 | Logistics Support Declaration | assign Logistics Support |
| 5 | Supply Checkpoint | determine supply and isolation states |
| 6 | Replacement | restore eligible reduced formations |
| 7 | Opponent Air Interdiction Window | opponent may interdict eligible units |
| 8 | Ground Movement | Regular or Operational Movement |
| 9 | Combat | resolve attacks one at a time |
| 10 | End | finish the Player Turn |

## 3.3 Do Not Go Back to a Completed Step

A Step with no action is still completed when play moves on.

Unless an explicit rule permits it, once the Player Turn advances to a later Step, do not return to an earlier Step to add an action that was omitted.

## 3.4 Persistent-State Reminder

Some states are determined at a checkpoint and remain in effect after the board changes.

Supply is the main example.

If a road opens after the Supply Checkpoint, do not automatically recalculate supply in the middle of movement or combat.

Use the state established at the last proper check until the next rule-defined check.

## 3.5 Special-Operations Order

If more than one legal Special Operation may be performed in the same Special Operations Step, resolve one completely before beginning the next unless a rule says otherwise.

Any placement, control, stacking, or other board change created by the earlier operation is part of the current board state for the later operation.

# 4. Units, Occupation, Control, and Stacking

Ground units occupy hexes, may lose combat steps, can form stacks, and can establish territorial control.

**Abbreviations used in this chapter:** Zone of Control (ZOC).

## 4.1 Two-Step Ground Units

A ground maneuver unit using the standard two-step ground-unit model has two combat steps:
- Full strength
- Reduced strength
A second step loss eliminates it.
Scenario or unit data identifies which formations use this standard model.

A step loss changes:
Full strength → Reduced strength → eliminated.

An eliminated unit is removed from the map immediately and ceases to occupy a hex or project ZOC.
Territorial control of its former hex does not change merely because the unit was removed.

Each unit using the standard two-step ground-unit model has separate Full strength and Reduced strength attack and defense factors.
Its Reduced strength state must have lower combat capability than its Full strength state.
Exact factors are provided by the Scenario or unit data.

A change from Full strength to Reduced strength does not by itself change the unit's Regular Movement Allowance unless the Scenario, unit data, or another rule says otherwise.

## 4.2 Occupation and Control

Opposing ground maneuver units may not occupy the same hex.

Occupation, territorial control, and ZOC are distinct concepts.

Entering an unoccupied enemy-controlled hex changes control to the entering side.

Control persists after a unit leaves until another rule changes it.

ZOC alone does not change territorial control.

## 4.3 Stacking

Each ground maneuver unit has a Stack Demand defined by Scenario or unit data.
The active Scenario or Campaign defines the normal Stack Capacity of a hex.
A stack is legal only when the total Stack Demand of units ending in the hex does not exceed that capacity.

A unit's Full-strength or Reduced-strength step state does not by itself change its Stack Demand unless Scenario or unit data or an explicit rule says otherwise.
Any force-count equivalence used by a Scenario or Campaign is separate Scenario or unit data and must not be inferred from Stack Demand.

A unit may move through a friendly-occupied hex even if stopping there would exceed the stacking limit, but its final hex after movement must be legal.

The Scenario or unit data provides the Stack Demand values for each represented formation class.

---

## 4.4 Unit-State Check

Before using a ground formation, check only the states relevant to the procedure:

- Full strength or Reduced strength;
- supplied or unsupplied;
- isolated or connected;
- in contact or not in contact;
- already moved this turn or not;
- already attacked / defended in the current Combat Step or not;
- already used in a movement-or-placement Special Operation or not.

Do not assume one state automatically changes another.

## 4.5 Stacking Check

Whenever a unit enters or is placed in a hex:

1. identify all friendly units that will occupy the final hex;
2. total their Stacking Demand;
3. compare the total with the Scenario-defined Stacking Capacity;
4. confirm the final position is legal.

Temporary passage and final occupation are separate questions if the rules allow different treatment.

## 4.6 Reduced Strength Does Not Automatically Change Demand Values

Changing from Full strength to Reduced strength changes the unit's current combat factors.

It does not automatically change:

- Stacking Demand;
- Supply Demand;
- Entry Demand;
- Lift Demand;

unless Scenario or unit data or an explicit rule says otherwise.

# 5. Movement and Zones of Control

Movement uses terrain costs, Movement Points, and the effects of enemy Zones of Control.

**Abbreviations used in this chapter:** Zone of Control (ZOC); Movement Points (MP).

## 5.1 Terrain and Movement Points

Each named terrain type has one movement class:
- Normal: 1 MP to enter
- Difficult: 2 MP to enter
- Prohibited: no normal ground entry

Crossing a Major River hexside adds 1 MP unless an explicit rule removes that surcharge.

The Scenario or map provides the exact named-terrain mapping.

Each unit has a Regular Movement Allowance defined by unit data.

Regular Movement proceeds one adjacent hex at a time.
Entry cost equals destination-terrain cost plus any applicable crossed-hexside cost.

A unit may not enter a hex if the required cost exceeds its remaining MP.
There is no automatic minimum-move exception.

Unused MP cannot be saved or transferred.

A unit may not enter an enemy-occupied hex during Regular Movement.

Units move sequentially in the owning player's chosen order.

During one Ground Movement Step, a unit may perform at most one movement action:
- Regular Movement;
- Operational Movement, if eligible; or
- no movement.

## 5.2 Zones of Control

Every on-map ground maneuver unit projects ZOC into all six adjacent hexes unless an explicit rule says that unit does not project ZOC.

Entering enemy ZOC during Regular Movement ends that unit's movement.

A unit that begins movement in enemy ZOC may leave if the move is otherwise legal.

Movement directly from one enemy-ZOC hex to another is allowed if otherwise legal, but movement ends on entry.

ZOC does not create mandatory combat.

Multiple enemy ZOCs do not create an additional movement effect unless an explicit rule says otherwise.

## 5.3 Operational Movement

Operational Movement is an optional high-speed movement mode.

A unit may use Operational Movement only if:
- its unit data says it is eligible;
- it is supplied;
- it was not in contact at the start of movement; and
- it has not already moved that turn.

Operational Movement Allowance is twice the unit's Regular Movement Allowance.

Operational Movement replaces Regular Movement for that turn and otherwise uses normal terrain and hexside costs unless explicitly modified.

Entering enemy ZOC ends Operational Movement.

A unit that uses Operational Movement may not attack that turn.

An interdicted unit may not use Operational Movement.

## 5.4 Major Roads

Moving along a connected Major Road into Difficult terrain reduces that destination terrain cost to 1 MP.

Major Roads do not reduce Normal terrain below 1 MP, do not permit entry into Prohibited terrain, and do not by themselves remove a Major River surcharge.

Major Road effects apply to both Regular and Operational Movement.

## 5.5 Major Rivers and Bridges

A Major River gives a -1 Combat Band shift only if every participating attacker attacks the target across a Major River hexside.

If at least one attacker attacks the target without crossing a Major River, no Major River combat shift applies.

A retreat may cross a Major River if the destination is otherwise legal.
It costs no MP and causes no automatic additional step loss.

An intact bridge across a Major River removes that river's +1 MP crossing surcharge.

A destroyed bridge does not remove the surcharge.

An intact bridge does not remove the Major River combat shift.

There is no general bridge-demolition or engineer-repair system in the common rules.
Bridge-state changes require explicit Scenario or event rules.

---

## 5.6 Movement Checklist

Before moving a unit:

1. Confirm the Ground Movement Step is active.
2. Confirm the unit has not already used its movement action this turn.
3. Choose Regular Movement, Operational Movement, or no movement.
4. If using Operational Movement, verify all eligibility conditions first.
5. For each hex entered, pay the correct terrain / hexside cost.
6. Do not enter a hex occupied by an enemy ground unit.
7. If Regular Movement enters enemy Zone of Control, stop there.
8. Confirm final stacking legality.

## 5.7 Movement-Cost Example

Suppose a unit enters Difficult terrain across a Major River.

If no usable bridge removes the crossing cost, pay:

- 2 Movement Points for entering Difficult terrain; plus
- 1 additional Movement Point for the Major River crossing.

Total: 3 Movement Points.

If a usable bridge removes the extra crossing cost, the movement total changes, but combat effects for attacking across the Major River are checked separately under Chapter 6.

## 5.8 Zone-of-Control Example

A unit begins the Ground Movement Step inside an enemy Zone of Control.

If a legal adjacent hex is available, it may leave.

If the destination is also in an enemy Zone of Control, the unit stops immediately upon entry even if Movement Points remain.

## 5.9 Operational Movement Checklist

Before declaring Operational Movement, confirm:

- the unit is eligible to use it;
- it is supplied;
- it does not begin in contact;
- it has not already moved;
- it is not prohibited by Operational Interdiction or another rule.

A unit that uses Operational Movement may not attack in that turn's Combat Step.

## 5.10 Cost and Permission Are Separate

Having enough Movement Points does not make every move legal.

Also check:

- enemy occupation;
- prohibited terrain;
- Zone-of-Control stopping rules;
- final stacking legality;
- any mode-specific restriction.

# 6. Combat

Combat is voluntary unless a rule says otherwise. Resolve one combat completely before choosing the next.

**Abbreviations used in this chapter:** Zone of Control (ZOC); Movement Points (MP).

## 6.1 Combat Participation and Order

Combat is voluntary unless an explicit rule says otherwise.
Being in contact does not itself require an attack.

One combat targets exactly one enemy-occupied hex.
All defending ground units in that target hex defend together as one group.

Eligible adjacent units may participate as attackers.
One unit may not split its attack strength among multiple combats.

A unit may attack at most once during its own Combat Step.

A defending unit may defend in at most one combat during one enemy Combat Step.

The attacking player chooses and resolves combats one at a time.
A combat is completed, including losses, retreat, advance, control changes, and other immediate effects, before the next combat is chosen.

The attacker is not required to predeclare all combats.
Results from earlier combats may change the legality or value of later combats.

If a hex contains any defending unit that has already defended during the current enemy Combat Step, that hex may not be selected as a new target during that Combat Step.

A fresh defending unit sharing such a hex does not create an exception to this restriction.
This preserves both the rule that all defenders in a target hex defend together and the rule that one unit may defend at most once in the same enemy Combat Step.

## 6.2 Combat Strength and Combat Bands

Use the participating units' current Full-strength or Reduced-strength attack and defense factors.

For a supplied unit, use its current attack and defense factors normally.

For an unsupplied unit:
- attack strength is halved, rounding fractions up;
- defense strength is unchanged.

Add all participating attacker strengths and all defender strengths, then form attacker strength divided by defender strength.

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

Apply all applicable Combat Band shifts, then clamp the final modifier to the range -3 through +3.

A combat must include at least one attacker and must have positive total attack and defense strength.
Exact factor values are unit data.

## 6.3 Terrain and Fortifications

Fortifications use the normal combat system; there is no separate siege Combat Results Table or siege system.

If the defending side is eligible to use at least one active fortification in the target hex, apply one -1 Combat Band shift.

Multiple fortification features in the same target hex do not stack beyond that single -1 shift.

Territorial control alone does not make a captured fortification usable.
Map or Scenario data must state which side can use each fortification and whether it is active.

Each named hex terrain has:
- movement class Normal / Difficult / Prohibited;
- defensive terrain shift 0 or -1.

Only the target hex's defensive terrain shift applies as the inherent hex-terrain combat effect.
Multiple terrain labels do not stack multiple inherent terrain shifts.

## 6.4 Dice Roll and Results

Roll two ordinary fair six-sided dice and add them.
Add the final Combat Band modifier.

Use the modified total:

| Modified total | Result |
|---|---|
| 4 or less | Attacker loses 1 step |
| 5-6 | No effect |
| 7-8 | Defender retreats 1 hex |
| 9-10 | Defender loses 1 step |
| 11 or more | Defender loses 1 step, then surviving defenders retreat 1 hex |

When the attacker must take a step loss, the attacking player chooses one participating attacker to take it.

When the defender must take a step loss, the defending player chooses one participating defender to take it.

For the combined defender loss + retreat result, apply the loss first.
If defenders survive, resolve their retreat.

No hidden probability modifier may alter this combat-resolution procedure.

## 6.5 Retreat

Standard retreat distance is one hex.

The defending player chooses one legal adjacent destination for the surviving defending group.

The destination must:
- contain no enemy ground unit;
- not be Prohibited terrain;
- satisfy stacking;
- be outside enemy ZOC unless friendly occupied.

All surviving defenders retreat to the same destination unless an explicit rule says otherwise.

If no legal retreat destination exists, the retreating group does not move and suffers one additional step loss, assigned by the defending player to one surviving unit.

Retreat does not spend MP.

## 6.6 Post-Combat Advance

If combat causes the target hex to become vacant, surviving on-map participating attackers may advance into it.

Maximum post-combat advance is one hex, into the vacated target hex only.

Post-combat advance costs no MP, may enter enemy ZOC, and must satisfy stacking.

No further movement follows a post-combat advance.

---

## 6.7 Combat Resolution Checklist

Resolve one combat completely in this order:

1. Select one target hex.
2. Select all participating attackers.
3. Confirm every attacker is eligible.
4. Total current attack strength.
5. Total current defense strength.
6. Determine the base Combat Band from the ratio.
7. Apply terrain, fortification, river, air, and other legal shifts.
8. Clamp the final modifier to -3 through +3.
9. Roll 2D6.
10. Apply the result.
11. Apply Step losses.
12. Resolve retreat if required.
13. Resolve Post-Combat Advance if permitted.
14. Complete resulting control or state changes.
15. Only then select the next combat.

## 6.8 Attacker Eligibility Check

Before adding a formation to an attack, confirm:

- it is adjacent to the target hex;
- it has not already attacked in this Combat Step;
- it is not prohibited from attacking by Operational Movement or another rule;
- its current attack strength is greater than zero.

If the unit is unsupplied, halve its attack strength, rounding fractions up, before totaling the attack.

## 6.9 Combat-Shift Example

Example:

- base Combat Band: +2;
- target terrain: -1;
- Offensive Air Support: +1;
- Defensive Air Support: -1.

Final modifier:

+2 -1 +1 -1 = +1.

If the final total would exceed +3 or -3, clamp it to that limit.

## 6.10 Major-River Example

If every attacking unit attacks across a Major River, apply the Major River shift.

If at least one participating attacker does not attack across the Major River, do not apply that shift.

Check the attack directions of all participating attackers.

## 6.11 Retreat Checklist

A retreat hex must satisfy all applicable retreat rules.

Check:

- no enemy ground unit;
- not prohibited terrain;
- final stacking legality;
- normally outside enemy Zone of Control;
- if inside enemy Zone of Control, any required friendly occupation condition.

If no legal retreat hex exists, apply the rule for failure to retreat.

## 6.12 Post-Combat Advance Checklist

A surviving attacking unit may advance only when the combat result permits it.

Check:

- the defending hex is vacant;
- the advancing unit participated in that combat;
- the unit survived;
- the target hex is stacking-legal.

Post-Combat Advance uses no Movement Points.

Entering enemy Zone of Control does not by itself prevent the advance.

## 6.13 Combat Is Not Finished at the Dice Result

Do not begin another combat until all required loss, retreat, advance, and immediate state-change procedures from the current combat are complete.

Later combats use the board state created by earlier combats.

# 7. Supply and Isolation

Supply is checked once during each side’s own Player Turn and then remains fixed until that side’s next Supply Checkpoint.

**Abbreviations used in this chapter:** Zone of Control (ZOC).

## 7.1 Supply Sources and Paths

A Supply Source is a location authorized to provide supply.
Each source has a side, a source type, a Supply Capacity, and a Base Reach.

A normal land supply path is a contiguous path of adjacent land hexes from the unit to a usable friendly Supply Source.

Every path hex must be friendly-controlled and free of enemy ground units.

A path may pass through an enemy-ZOC hex only if that hex is friendly occupied.

Prohibited terrain blocks normal land supply unless an explicit rule says otherwise.

Path length is counted in hex transitions.

Each ground maneuver unit has a Supply Demand defined by Scenario or unit data.
A change between Full-strength and Reduced-strength state does not by itself change Supply Demand unless Scenario or unit data or an explicit rule says otherwise.

A normally supplied unit must be assigned to one usable Supply Source with a legal path, sufficient reach, and available capacity.

The total Supply Demand assigned to one source may not exceed that source's Supply Capacity.

The owning player chooses among legal source assignments.
A unit without a valid normal assignment is unsupplied unless an explicit special-supply rule applies.

Each Supply Source uses the Base Reach defined by Scenario or source data.
Base Reach is measured in hex transitions.

Each Logistics Support resource assigned to a source adds the Scenario-defined Logistics Reach Increment to that source's Base Reach.
A maximum of two Logistics Support resources may be assigned to one source unless another common rule changes that limit.
The resulting reach is Base Reach plus zero, one, or two Logistics Reach Increments.

Each Logistics Support resource may support only one source at a time.
The total number assigned may not exceed the side's available Logistics Support resources.

Logistics Support is assigned during the Logistics Support Declaration step and cannot be reassigned again during that Supply Checkpoint.
It is not consumed by being assigned.

Each side checks supply once during its own Player Turn, before Ground Movement.

The supply result is based on the board and source situation at that Supply Checkpoint and remains in effect until that side's next Supply Checkpoint.
Do not recalculate supply continuously during movement or combat.

An unsupplied unit:
- halves attack strength, rounding up;
- halves Regular Movement Allowance, rounding up;
- keeps normal defense strength;
- may not use Operational Movement.

## 7.2 Ports and Beachheads

A port has operational state closed, damaged, or active and sea access closed or open.

A port can function as a normal Supply Source only when:
- it is friendly-controlled;
- its port state is active; and
- sea access is open.

Control alone does not activate a port.

Capturing, repairing, or opening a port after a Supply Checkpoint does not change that already-completed supply determination.

Capturing a port does not automatically make it usable.

For each relevant port, the Scenario defines:
- its operational state after capture;
- the condition or delay by which a damaged port becomes active;
- its sea-access condition.

Port repair is not handled through a general player-managed engineer or resource system in the common rules.
Port-specific recovery is represented by the explicit Scenario condition or delay for that port.

Sea access is independent of physical port condition.
A port may be active but unusable as a Supply Source or Entry Source while its sea-access condition is not satisfied.

A port that becomes usable after the current Supply Checkpoint does not retroactively change that completed supply determination.

The Scenario provides the exact port-by-port repair delays, activation conditions, sea-access conditions, and capacities.

Beachheads are distinct from ports even when both exist in the same hex.

## 7.3 Isolation

Isolation is separate from ordinary supply status.

At each own Supply Checkpoint, determine whether a unit has a legal physical land connection to a friendly Supply Anchor.
For this connection test, ignore source capacity, source reach, and source activation; use the normal supply-path restrictions.

A unit with physical connection is connected.

A unit without physical connection is isolated.

On the first consecutive Supply Checkpoint at which the unit is isolated, it suffers no isolation step loss.
At each later consecutive own Supply Checkpoint while it remains isolated, it suffers one step loss after supply determination.

An isolated unit cannot receive normal source supply, but an explicit special-supply rule may temporarily supply it.

The Scenario or map identifies the exact Supply Anchor locations.

---

## 7.4 Supply Determination Checklist

For each unit that needs normal supply:

1. Identify usable friendly Supply Sources.
2. Find a legal supply path.
3. Confirm the path is within the source's current Reach.
4. Confirm the source has sufficient remaining Supply Capacity.
5. Assign the unit to one legal source.
6. If no legal normal assignment exists, apply any explicit special-supply rule if available.
7. Otherwise mark the unit unsupplied.
8. Determine isolation separately.

Supply and isolation are separate checks.

## 7.5 Supply-Path Example

Suppose formation A is within normal reach of Supply Source S.

Every path hex is friendly-controlled and free of enemy ground units, but one path hex lies in enemy Zone of Control and is not friendly occupied.

That path is not legal.

The player must find another legal path or use another legal source.

## 7.6 Multiple Sources

If a unit can legally draw supply from more than one source, the owning player chooses the assignment.

This matters because each source has separate capacity.

Do not count one unit's Supply Demand against multiple sources.

## 7.7 Logistics-Support Check

During Logistics Support Declaration:

1. choose the Supply Source receiving the support;
2. observe the maximum number that may support one source;
3. do not assign the same resource to more than one source;
4. keep that assignment fixed for the current Supply Checkpoint.

## 7.8 Port Supply Checklist

Before using a port as a normal Supply Source, confirm:

- friendly control;
- active port state;
- open sea access.

Control alone is not enough.

## 7.9 Isolation Checklist

For isolation, ignore ordinary Supply Capacity, Reach, and source activation.

Instead ask whether the unit has a legal physical land connection to a friendly Supply Anchor under the isolation rules.

Connected and supplied are not the same state.

## 7.10 Example — Unsupplied but Not Isolated

Formation A is too far from a usable Supply Source to receive normal supply.

It still has a legal physical land connection to a friendly Supply Anchor.

A is unsupplied, but not isolated.

## 7.11 Persistent-State Reminder

After the Supply Checkpoint, later movement, combat, port activation, or road opening does not retroactively rewrite the completed supply determination.

Recheck at the next proper Supply Checkpoint.

# 8. Reinforcements and Replacements

Reinforcements enter through authorized Entry Sources. Replacements restore eligible reduced-strength formations according to Scenario data.

**Abbreviations used in this chapter:** Zone of Control (ZOC); Replacement Points (RP).

## 8.1 Reinforcement Availability

A reinforcement is:
- scheduled before its availability condition is met;
- available when it may enter;
- entered after it has been legally placed on the map.

Normal reinforcement availability is checked during the Start / Resource Step.

An available reinforcement remains available if it cannot or does not enter that turn.

Each reinforcement has an entry state of Full strength or Reduced strength.
If it later survives an off-map staging state with losses, those losses are retained; simply entering later does not restore it.

Every scenario identifies which side each reinforcement belongs to, which formation it is, when it becomes available, and how it may enter.

An eliminated formation may not return merely because it is or once was an available reinforcement.
It can return only through an explicit reconstitution rule followed by legal entry.

## 8.2 Normal Entry

An Entry Source is an authorized reinforcement-introduction location.

A port used as an Entry Source must be friendly-controlled, active, open to sea access, and explicitly authorized for entry.

Each Entry Source has an Entry Capacity for that Player Turn.
Entry Capacity and Supply Capacity are separate.

Each reinforcement formation has an Entry Demand defined by Scenario or unit data.
A change between Full-strength and Reduced-strength state does not by itself change Entry Demand unless Scenario or unit data or an explicit rule says otherwise.

The total Entry Demand entering through a source in one Reinforcement Entry Step may not exceed that source's Entry Capacity.
Unused Entry Capacity does not carry forward.

An entry hex must be:
- friendly-controlled;
- free of enemy ground units;
- outside enemy ZOC;
- stacking-legal.

If no legal entry hex is available, the reinforcement remains available.

A reinforcement that enters normally is on-map before that Player Turn's Supply Checkpoint.

## 8.3 Replacement Points and Replacements

Each side receives Replacement Points (RP) according to Scenario schedule.
Unused RP carry over.

Each formation eligible for replacement has a Replacement Cost defined by Scenario or unit data.
During the Replacement Step, spending that Replacement Cost restores one eligible Reduced strength formation to Full strength.

A unit is eligible for replacement only if it is:
- Reduced strength;
- supplied; and
- not in contact.

Replacement does not grant movement, change position, clear contact, or otherwise create an additional action.

Generic RP cannot restore an eliminated formation.
Eliminated formations return only through explicit reconstitution plus normal reinforcement entry.

The Scenario provides exact replacement schedules and any reconstitution rules.

## 8.4 Other Common Limits

There is no generic rule that awards replacement strength merely for capturing an objective.

There is no generic sea-redeployment system.

---

## 8.5 Reinforcement Entry Checklist

To enter a reinforcement:

1. Confirm it is available.
2. Identify an authorized Entry Source.
3. Confirm sufficient Entry Capacity remains.
4. Confirm the reinforcement's Entry Demand.
5. Choose a legal entry hex.
6. Confirm friendly control, no enemy unit, no enemy Zone of Control, and legal stacking.
7. Place the reinforcement and update remaining Entry Capacity.

If no legal entry is possible, the reinforcement remains available.

## 8.6 Port Entry Checklist

A port used as an Entry Source must be:

- friendly-controlled;
- active;
- open to sea access;
- explicitly authorized for reinforcement entry.

A port's ability to provide supply does not automatically mean it is an authorized Entry Source.

## 8.7 Entry-Capacity Example

If Entry Source E has less remaining Entry Capacity than formation R's Entry Demand, R cannot enter through E this turn.

Unused capacity does not carry forward.

If no other legal Entry Source exists, R remains available off-map.

## 8.8 Replacement Checklist

Before spending Replacement Points, confirm the unit is:

- Reduced strength;
- supplied;
- not in contact.

Then pay the Scenario-defined Replacement Cost and restore the unit to Full strength.

Replacement does not itself move the unit, clear contact, or grant an additional action.

## 8.9 Availability and Entry Are Different States

A reinforcement can be available without being on-map.

Do not treat availability as automatic placement.

Entry still requires a legal Entry Source, sufficient capacity, and a legal entry hex.

# 9. Tactical Air Power

Tactical air resources may support combat or interdict enemy movement. Heavy Breakthrough Bombardment is a separate scarce campaign resource.

**Abbreviations used in this chapter:** Tactical Air Points (TAP); Heavy Breakthrough Bombardment (HBR).

## 9.1 Tactical Air Points

Tactical Air Points (TAP) represent allocatable tactical air effort.

Scenario data determines each side's TAP availability.
Unused TAP expire at the end of their defined air-resource cycle.

TAP may be spent on three missions:
- Offensive Air Support;
- Defensive Air Support;
- Operational Interdiction.

There is no separate generic route or river-interdiction mission.

## 9.2 Combat Air Support

Offensive Air Support costs 1 TAP and gives +1 Combat Band to one friendly attack.
Maximum: one Offensive Air Support mission per combat.

Defensive Air Support costs 1 TAP and gives -1 Combat Band to one combat against one friendly defending hex.
Maximum: one Defensive Air Support mission per combat.

For each combat, commitments occur in this order:
1. attacker declares eligible HBR;
2. attacker declares Offensive Air Support;
3. defender declares Defensive Air Support;
4. final Combat Band is determined;
5. combat is rolled.

Once a resource is committed in that sequence, it cannot be withdrawn because of a later opposing declaration.

## 9.3 Operational Interdiction

Operational Interdiction costs 1 TAP and targets one enemy on-map ground maneuver unit.

The target may not use Operational Movement during its next own Ground Movement Step.

Interdiction does not by itself reduce Regular Movement or combat strength.

Additional interdiction missions on the same already-interdicted unit have no additional effect.

Interdiction is declared during the opponent-air-interdiction window immediately before that side's Ground Movement Step.

## 9.4 Heavy Breakthrough Bombardment

Heavy Breakthrough Bombardment (HBR) is a scarce campaign resource.
Scenario data defines its available uses, first eligible turn, and expiry if any.

An HBR target must:
- be enemy occupied when HBR is declared; and
- be the same hex that had at least one adjacent friendly ground unit at the end of the attacking side's previous Player Turn.

The friendly unit that established that prior adjacency need not still be present when HBR is used.

HBR costs one available use.

For an HBR-supported attack, resolve the normal combat roll twice using the same Combat Band and known modifiers.
Reveal both outcomes; the attacker chooses one and applies only that outcome.

HBR does not itself change the Combat Band and does not create a new result type.

HBR may not support Amphibious Assault.

The Scenario provides the exact Heavy Breakthrough Bombardment schedule and number of uses.

---

## 9.5 Air-Resource Checklist

Before spending Tactical Air or Heavy Breakthrough Bombardment:

1. confirm the resource is currently available;
2. confirm the mission or use is legal;
3. confirm the target is legal;
4. observe any per-combat, per-cycle, or timing limit;
5. declare resources in the required order;
6. deduct or record the spent resource.

## 9.6 Combat Air-Support Reminder

For each combat, the declaration order is:

1. attacker declares eligible Heavy Breakthrough Bombardment;
2. attacker declares Offensive Air Support;
3. defender declares Defensive Air Support;
4. determine the final Combat Band;
5. roll combat.

Once declared, a resource is not withdrawn because of a later opposing declaration.

## 9.7 Operational-Interdiction Reminder

Operational Interdiction prevents the targeted unit from using Operational Movement during its next own Ground Movement Step.

It does not by itself change:

- Regular Movement Allowance;
- attack strength;
- defense strength.

## 9.8 Heavy Breakthrough Bombardment Check

Before declaring Heavy Breakthrough Bombardment, confirm:

- the target hex is currently enemy occupied;
- the prior-adjacency condition is satisfied;
- a use remains available;
- the timing is within the Scenario-defined availability window;
- the combat is not an Amphibious Assault.

# 10. Airborne Operations

Airborne Operations place eligible airborne formations using Scenario-defined lift and reference-distance limits.

**Abbreviations used in this chapter:** Zone of Control (ZOC).

## 10.1 Airborne Operations

Only formations identified as airborne-capable may perform an Airborne Operation.

Scenario data defines Airborne Lift Capacity for each Player Turn in which airborne operations are permitted.
Each participating formation has an Airborne Lift Demand defined by Scenario or unit data.
Total Airborne Lift Demand may not exceed that turn's capacity; unused lift does not carry over.

An Airborne Operation requires:
- an airborne-capable unit;
- sufficient lift;
- the unit to be available off-map or at an explicitly authorized airborne staging location;
- the unit not to have moved or entered normally that turn;
- the unit not to have participated in another movement-or-placement Special Operation that turn.

A legal airborne drop hex must:
- be land terrain;
- contain no enemy ground unit;
- not be prohibited for airborne landing by map or Scenario data;
- satisfy stacking.

The drop hex may be enemy-controlled or in enemy ZOC.
Landing in an unoccupied enemy-controlled hex changes control normally.

Unless a Scenario-specific initial-operation exception applies, the drop hex must be within the Scenario-defined Airborne Reference Distance of a friendly supplied non-airborne ground unit that was on-map at the beginning of that turn.

Scenario setup may define designated airborne reference hexes for an initial airborne operation instead of the normal friendly-unit reference.
When used, the drop hex must be within the Scenario-defined Airborne Reference Distance of one such reference hex.

There is no generic airborne scatter or failure system.
A legal committed Airborne Operation completes its placement.

A unit conducting an Airborne Operation may not perform Regular or Operational Movement that turn, but may attack if otherwise eligible.

An airborne unit is treated as supplied for the remainder of its drop turn without consuming normal source capacity.
At its following own Supply Checkpoint it returns to normal supply rules.

There is no generic air-extraction system.

---

## 10.2 Airborne Operation Checklist

Resolve an Airborne Operation by checking:

1. the unit is airborne-capable;
2. the operation is permitted this turn;
3. sufficient Airborne Lift Capacity exists;
4. the unit is in an authorized off-map or staging state;
5. the unit has not already moved, entered normally, or used another movement-or-placement Special Operation;
6. the drop hex is legal;
7. the reference-distance rule is satisfied;
8. final stacking is legal;
9. apply the special supply treatment for the remainder of the drop turn.

## 10.3 Drop-Hex Checklist

A legal drop hex must:

- be land terrain;
- contain no enemy ground unit;
- not be prohibited for airborne landing;
- satisfy stacking.

Enemy control or enemy Zone of Control does not by itself prohibit the drop.

## 10.4 Initial Reference-Hex Reminder

If the Scenario authorizes designated initial airborne reference hexes, use them only under that Scenario-defined initial-operation exception.

Otherwise use the normal friendly supplied non-airborne ground-unit reference rule.

## 10.5 After the Drop

An airborne unit that conducted the operation:

- may not use Regular Movement that turn;
- may not use Operational Movement that turn;
- may attack later if otherwise eligible;
- is treated as supplied for the remainder of the drop turn under the common Airborne rule.

# 11. Amphibious Operations

Amphibious Operations place assault formations from off-map staging onto eligible coastal hexes and can create temporary Beachheads.

**Abbreviations used in this chapter:** Heavy Breakthrough Bombardment (HBR).

## 11.1 Initial and Follow-On Invasions

A Scenario or Campaign may designate an Initial Invasion.
When designated, it is resolved during the specified owning Player Turn's Special Operations Step before that Player Turn's Supply Checkpoint.

Each amphibious operation must have Scenario data defining:
- eligible coastal hexes;
- eligible assault formations;
- Amphibious Lift Capacity;
- maximum assault hexes;
- beachhead supply and entry values.

Each participating assault formation has an Amphibious Lift Demand defined by Scenario or unit data.
Total Amphibious Lift Demand assigned to the operation may not exceed its lift capacity; unused lift does not carry over.

Before resolving landings, the player conducting the amphibious operation assigns each participating assault unit to exactly one selected assault hex.
Assignments are fixed before any assault is resolved.

After assignments are fixed, the player conducting the amphibious operation chooses the order in which assault hexes are resolved.
Resolve one assault hex completely before the next; its results immediately affect the board.

If a selected coastal hex contains no enemy ground unit, assigned assault units may enter up to the stacking limit.

A surviving assigned unit that cannot legally enter remains off-map in amphibious staging under the same post-assault staging rules.

If the target coastal hex contains enemy ground units, resolve an Amphibious Assault.

For the beach assault only, off-map assaulting units use their current Full-strength or Reduced-strength attack factors directly.
They are not treated as normally supplied or unsupplied solely for that off-map combat, and the assault consumes no normal Supply Source capacity.

Amphibious Assault uses the normal ratio, Combat Band, dice, result, loss, and retreat system with these changes:
- apply the Scenario-defined Amphibious Combat Band shift once;
- apply target-hex terrain shift normally;
- apply an eligible fortification shift normally;
- Offensive and Defensive Air Support may be used normally;
- HBR may not be used;
- Major River shift does not apply merely because the attackers approach from sea staging.

If defenders vacate or are eliminated, surviving assault units may occupy the target hex up to stacking limits.

A surviving assault unit that does not enter the target hex returns to off-map amphibious staging with any losses retained.

A unit in amphibious staging may take no further movement, attack, reinforcement entry, or other entry action during the rest of that Player Turn.
At the beginning of the next owning Start / Resource Step it becomes available again.

A failed assault does not restore spent amphibious capability.
Any later amphibious attempt requires a separate currently legal amphibious capability.

Participation in an amphibious operation consumes that unit's ground-movement action for the turn.
A landed amphibious unit may not use Regular or Operational Movement later that turn.

A unit that lands unopposed may attack during the later normal Combat Step if otherwise eligible.

A unit that participated as an attacker in an opposed Amphibious Assault may not attack again in the later normal Combat Step that turn.

A surviving unit that defended against an opposed Amphibious Assault may not be attacked again in the later normal Combat Step of that same Player Turn.

A unit may participate in at most one movement-or-placement Special Operation during one own Player Turn.

No generic post-landing defense penalty exists.

## 11.2 Beachheads

A coastal hex successfully occupied through the Initial Invasion or a legal follow-on invasion becomes a Beachhead.

Beginning with the first owning-side Supply Checkpoint after its creation, a Beachhead may function as a temporary Supply Source and Entry Source using Scenario values.

The Scenario provides the following Beachhead data:
- Base Reach;
- Supply Capacity;
- Entry Capacity;
- entry hexes;
- persistence.

A Beachhead does not require a port to be active and remains distinct from any port in the same hex.

When Beachhead persistence ends, its temporary supply and entry functions end unless an explicit rule replaces them.

## 11.3 Amphibious Reserve

The campaign may include one one-use Amphibious Reserve authorizing one follow-on invasion.

Scenario data defines its ready turn, expiry turn, lift, eligible coast, and maximum assault hexes.

It may be used once during its inclusive ready-to-expiry window.
If unused by the end of its owning side's Special Operations Step on the expiry turn, it expires.

A follow-on invasion uses the normal amphibious rules unless an explicit Scenario rule states a permitted difference.

---

## 11.4 Amphibious Operation Checklist

Use this order:

1. Confirm the operation is currently authorized.
2. Confirm Amphibious Lift Capacity.
3. Confirm participating formations and their Lift Demand.
4. Confirm eligible coastal hexes and maximum assault hexes.
5. Assign every participating formation to an assault hex.
6. Fix all assignments before resolving any assault.
7. Choose the order of assault-hex resolution.
8. Resolve one hex completely.
9. Update on-map / staging states.
10. Continue to the next assault hex.
11. Create a Beachhead if the rules and Scenario conditions permit.

## 11.5 Assignment Lock

Do not wait for the result of the first assault before changing assignments to another assault hex.

All participating formations are assigned before the first landing is resolved.

## 11.6 Unopposed Landing Check

If the coastal hex contains no enemy ground unit:

- confirm the hex is eligible;
- confirm final stacking;
- place as many assigned units as can legally enter.

Any surviving assigned unit that cannot legally enter follows the off-map staging rule.

## 11.7 Opposed Amphibious Assault Check

Use the normal combat system with the listed Amphibious changes.

Confirm:

- Scenario-defined Amphibious Combat Band shift;
- target terrain;
- eligible fortification;
- Offensive / Defensive Air Support if used;
- no Heavy Breakthrough Bombardment;
- no Major River shift merely because attackers came from sea staging.

## 11.8 Example — Not Every Survivor Can Enter

Suppose the defense is removed and several assaulting units survive.

If placing all survivors would exceed Stacking Capacity, place only the legal amount.

Other surviving assigned units return to amphibious staging with their current losses retained.

## 11.9 Post-Landing Action Check

After participation in an Amphibious Operation:

- the unit's ground-movement action for that turn is spent;
- it may not use Regular or Operational Movement later that turn;
- an unopposed landing unit may attack later if otherwise eligible;
- an attacker in an opposed Amphibious Assault may not attack again in the normal Combat Step;
- a surviving defender from an opposed Amphibious Assault may not be attacked again in the later normal Combat Step of that same Player Turn.

## 11.10 Beachhead Record

When a Beachhead is created, record the Scenario-defined:

- Base Reach;
- Supply Capacity;
- Entry Capacity;
- entry hexes;
- persistence.

Beginning with the first owning-side Supply Checkpoint after creation, the Beachhead may function according to those values.

Keep Beachhead state separate from any port in the same hex.

## 11.11 Amphibious Reserve Check

Before using an Amphibious Reserve, confirm:

- ready turn;
- expiry turn;
- Lift Capacity;
- eligible coast;
- maximum assault hexes.

It is one-use.

If not used by the specified expiry point, it expires.

# 12. Victory and Game End

Every Scenario defines how victory is achieved and when the game ends. Common rules also allow concession and a mutually agreed draw.

**Abbreviations used in this chapter:** Artificial Intelligence (AI).

## 12.1 Victory and Game-End Framework

Each Scenario or Campaign states its victory conditions and when they are checked.

Victory conditions may use any already-defined game state, including:
- unit survival or position;
- territorial control;
- supply state;
- objective or area conditions;
- elapsed turns;
- Scenario-defined points or thresholds.

A scenario-specific victory method is not automatically a universal rule for other scenarios.

Game End Conditions are distinct from Victory Conditions.
A Game End Condition defines when play stops.
Victory Conditions define the outcome awarded when or because the relevant Game End Condition is satisfied.

A Scenario or Campaign may use condition-driven ending and is not required to define a fixed calendar end date or a fixed maximum Game Turn count.
A fixed time limit is valid only when the Scenario or Campaign explicitly defines one.

Every Scenario or Campaign must clearly state the Game End Conditions and the result produced by each way the game can end.

If a scenario maps Game Turns to calendar time, its final calendar state or reported final date may be derived from the Game Turn in which a Game End Condition is satisfied, according to that scenario's temporal mapping.

No automatic draw, tie, stalemate, exhaustion, or automatic time-limit outcome exists by default.
Player concession and mutual draw agreement are common two-player game-end mechanisms described below.
A Scenario or Campaign may define additional end conditions explicitly, but they are not implied merely to force closure.

A player may concede the game by declaring defeat.
When a player concedes, play ends immediately and the opposing player wins.

The two players may mutually agree to end the game as a draw.
A draw proposal by one player does not end play unless the other player agrees.
When both players agree, play ends immediately as a draw.

A human-controlled or AI-controlled player role has the same authority to concede, propose a draw, accept a draw, or decline a draw.
These rules do not prescribe how a human or AI controller decides whether to concede or respond to a draw proposal.

---

## 12.2 Victory Check Checklist

Before declaring a Scenario victory, confirm:

1. which game state the Victory Condition uses;
2. the exact timing of the check;
3. whether satisfaction ends the game immediately;
4. whether the Scenario instead checks outcome after a separate Game End Condition;
5. whether any fixed final turn or calendar mapping exists.

Meeting a condition temporarily is not enough unless it is true at the official check time.

## 12.3 Game-End Checklist

Before ending play, identify the legal end path:

- a Scenario-defined Game End Condition;
- concession;
- mutually agreed draw.

Do not create an automatic end merely because:

- the front is quiet;
- the position appears stalemated;
- both sides are exhausted;
- many turns have passed;

unless the active Scenario explicitly defines such an end condition.

## 12.4 Example — Objective Captured, Check Not Yet Reached

Suppose a side controls every required Objective during its own Player Turn.

If the Scenario checks victory only after the opponent's Player Turn, play continues.

The opponent may still change the required game state before the formal check.

## 12.5 Concession and Draw

Concession ends the game immediately and awards the win to the opposing player.

A draw proposal does not end play until the other player accepts it.

Human-controlled and artificial-intelligence-controlled player roles have the same authority for these player decisions.

## 12.6 Scenario Priority

This chapter defines the common framework.

The active Scenario defines:

- the actual Victory Conditions;
- check timing;
- Game End Conditions;
- any fixed time limit;
- any Scenario-specific result structure.

Do not copy the victory architecture of one Scenario into another unless the new Scenario explicitly defines it.


---

# Appendix A. Quick Reference

This appendix adds no new rules. It points to the main procedure chapters.

| Need | Start here |
|---|---|
| Confirm current Step | Chapter 3 |
| Move a unit | Chapter 5 |
| Resolve an attack | Chapter 6 |
| Check retreat legality | 6.11 |
| Resolve Post-Combat Advance | 6.12 |
| Check supply | Chapter 7 |
| Check isolation | 7.9 |
| Enter reinforcements | Chapter 8 |
| Spend Replacement Points | 8.8 |
| Use Tactical Air / Heavy Breakthrough Bombardment | Chapter 9 |
| Conduct an Airborne Operation | Chapter 10 |
| Conduct an Amphibious Operation | Chapter 11 |
| Check victory or game end | Chapter 12 |

## A.1 If You Are Unsure What to Do Next

1. Confirm the current Step.
2. Confirm the unit / hex / resource state.
3. Check action legality.
4. Check cost, capacity, or resource requirements.
5. Resolve the procedure completely.
6. Record the resulting state.
7. If a required value is Scenario-defined, use the active Scenario.

When this appendix conflicts with detailed chapter text, the detailed chapter text controls.
