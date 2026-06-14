---
title: Dungeon Mechanics
type: system
domain: Systems
status: canonical
visibility: mixed
aliases: [Dungeon Mechanics, Stretches, Fast-Combat, Encounter Types, Milestone Leveling, Retreating]
tags: [embers, system, dungeon-mode, roguelike]
source: ["campaign bible v0.4 §10"]
created: 2026-06-14
---

# Dungeon Mechanics

Up: [[Game Systems]]

**Dungeon Mode is a resource-attrition roguelike run on 10-minute Stretches. The dungeon limits how far you go through HP, slots, hit dice, and consumables — not a global timer.** Player-facing rules: [[Dungeoneering Rules]]. See also [[The Two Modes of Play]] and [[Floor Reset and the Intelligence Gradient]].

## Stretches

Per the [[Dungeoneering Rules]]: 10-minute increments. Each Stretch, each PC chooses one Activity. **Wandering-monster rolls happen at end of Stretch.**

## Encounter Density (default calibration)

- **Frequency:** Medium (d6 every 3 Stretches)
- **Likelihood:** Possible (5–6 triggers an encounter)
- **Difficulty:** tuned to drain resources without being deadly on average
- Adjust per-floor as the design fits.

## Resource Attrition Is the Limit

- The **wandering-monster table is the primary pressure dial.**
- Short rests cost a Stretch and trigger a wandering roll — don't house-rule this away.
- Some monsters drain non-combat resources (eat torches, break tools, ruin rations).
- Some rooms penalize lingering (poison gas, psychic hum, flooded-chamber Con saves).
- "Take Your Time" still works but with penalty (the dungeon reacts to patience — see [[The Dungeon]]).

## Encounter-Type Discipline (5 types)

Daily reset means PCs re-encounter the "same" room. To avoid tedium, every encounter is one of five types with defined reset behavior — **no generic encounters exist.**

| Type | Behavior | Frequency |
|---|---|---|
| **Wandering** | Rolled per Stretch off the floor table; different each time | High |
| **Triggered** | Spawned by puzzle failure / trap / wrong door / broken seal; bypassable with floor knowledge | Medium |
| **Sigil** | [[Wesley's Sigils|Wesley's sigils]]; persistent until cleared; reset does NOT clear them | Low, high-stakes |
| **Guardian** | Pre-set, fixed location, gated to a discoverable reward; repeats on reset | 1–2/floor |
| **Boss** | Pre-set set-piece; one-time only across the campaign; does NOT repeat | 1/floor max |

**Strategic implication:** an experienced party plans routes to avoid known guardians, bypass triggers, and only fight wandering monsters that find them — picking which fixed encounters to engage per delve by resource budget and reward.

## Fast-Combat (2d10)

For repeat encounters the DM *may* offer fast-combat: skip the table, lock in a probabilistic resource cost. **Only offered** when the encounter was previously cleared **at the party's current level** AND is type Triggered or Guardian (never wandering, sigil, or boss). Above-level clears from a lower level don't qualify. Each PC rolls 2d10:

| 2d10 | Outcome |
|---|---|
| 2 | Lose 2/3 max HP, AND (2 spell slots OR 3–4 hit dice — player's choice; non-casters take hit dice) |
| 3–4 | Lose 1/2 max HP, AND (1 slot OR 2 hit dice — non-casters take hit dice) |
| 5–7 | Lose 1/3 max HP and 1 hit die |
| 8–11 | Lose 1/4 current HP |
| 12–14 | Lose 1d6 HP |
| 15–17 | Untouched |
| 18–19 | Untouched + small benefit (regain a hit die / extra ration / advantage next Stretch's first roll) |
| 20 | Untouched + small benefit + useful loot drop |

Distribution: ~21% painful (2–7), ~58% light (8–14), ~21% untouched-or-better. **The 2 result keeps real danger** — a low-HP PC can still drop into ember-intervention. Fast-combat is not a safety net.

## Level-Disparity Flee Rule

Once the party is **2+ levels above** a wandering monster's typical CR, that monster **flees by default**. Exceptions (DM call): mindless creatures (oozes, basic constructs) engage; pack-driven groups may engage; pre-committed guardians engage; cornered creatures fight desperately. By Levels 4–5 the lower-floor tables visibly empty out — Floor 1 becomes the party's territory. Chasing a fleeing monster costs a Stretch and a wandering roll.

## Milestone Leveling (stairs-found)

Tied to descent — and granted when the down-stairs are **found**, not when the party descends.

| PC Level | Trigger |
|---|---|
| 2 | Stairs to Floor 2 found |
| 3 | Stairs to Floor 3 found |
| 4 | Stairs to Floor 4 found |
| 5 | Stairs to Floor 5 found |

So Level 3 is granted while still on Floor 2, the moment the down-stairs are discovered. Plot pacing aligns (Level 2 by mid-July, Level 5 by equinox); aggressive delvers may outrun the calendar — tune to actual level. Levels 6+ tie to Tier-2 milestones (defer to Act 2).

## Speedrunning

PCs *may* push to Floor 5 fast and ignore the town — a valid strategic choice the campaign supports. Floor design must **not** make it easy (keystones protected, down-stairs need real exploration without the compass — see [[The Keystone Tablet]]). **The cost is topside:** every delve commits the whole day (see [[Time Points]]); aggressive delving starves investigations and relationships, NPCs go unsaved, [[The Bizarro Plot|the bizarro plot]] proceeds unchecked, the town gets worse. The DM makes the cost visible, not railroady.

## Retreating

Location-based, not timer-based. Returning to the entrance is the way out.

- **Soft Retreat:** travel back through cleared floors; Stretches and wandering rolls happen normally. The deeper you went, the longer the trip.
- **Surfacing Ritual (panic button):** any PC, as their Stretch Activity, makes a **DC 15 ability check (Wisdom or Charisma — player picks flavor)**. Entity-flavored escape — your [[The Embers|ember]] pulls you out (*the warmth in your chest catches and surges, and the dungeon releases you*). **Success:** whole party wakes at home, each gains 1 level of exhaustion. **Failure:** next wandering roll is automatic and uses the harder end of the table.
- **Wesley's Sigil** is the anti-ember-exclusive mirror of Surfacing (dungeon-flavored, costs persistent monsters) — not available to PCs. See [[Wesley's Sigils]].

## Source
Campaign Bible v0.4, §10 (Dungeon Mechanics). Player-facing complement: [[Dungeoneering Rules]].
