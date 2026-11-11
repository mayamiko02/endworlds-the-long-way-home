# GAME DESIGN DOCUMENT
### ENDWORLDS: THE LONG WAY HOME

> **Purpose:** how the game plays — systems, loops and rules.
> **Scale note:** this is a living design document. Sections state design intent only. **Nothing on this page is implemented** — no Godot project exists yet (see [ROADMAP.md](ROADMAP.md)). Implementation status is tracked in §11.
> Canon definitions of story elements live in [PROJECT_BIBLE.md](PROJECT_BIBLE.md); this document owns their mechanical expression.

---

## 1. Game identity — CANON (from master instructions)

A 2D adventure platformer combining: **exploration, platforming, combat, crafting, resource gathering, equipment progression, quests, secrets, bosses and environmental interaction.**

## 2. Design pillars — PROPOSAL

1. **The journey inward** — mechanics reinforce the emotional arc: journaling, relationships, home-building.
2. **Every world persists** — exploration has durable consequences; revisiting matters.
3. **Mastery through movement** — platforming should feel expressive and improve with player and equipment growth.
4. **Discovery over volume** — fewer, denser, hand-crafted worlds rather than many shallow ones (AGENTS.md closing rule).

## 3. Core loop — PROPOSAL

```
EXPLORE a world → GATHER resources / HELP inhabitants → SURVIVE platforming,
combat and bosses → RETURN via headset (if possible) → BUILD the Sanctuary
and record the JOURNAL → unlocked understanding opens new travel options → repeat
```

## 4. The headset — CANON rules, mechanical form PROPOSAL

| System | Canon rule | Mechanical intent (PROPOSAL) |
|---|---|---|
| **Random Jump** | Uncontrolled travel to real, persistent universes | Primary travel verb early game; destination unknown; risk/reward resource runs |
| **Beacon Travel** | Deliberate return to registered universes | Beacons are established through play (quest/explore/craft — exact cost TBD); beaconed worlds form the player's known map |
| **Home Signal** | Long-term objective | Meta-progression meter advanced by story milestones and Sanctuary/Journal development; gates the endgame |
| **Dimensional Recall** | Raises the chance of revisiting previously encountered but **unregistered** worlds; never guarantees a destination | Upgrade path that biases Random Jump toward forgotten worlds |
| **Forgotten worlds** | Unregistered worlds stay eligible for random encounters | Random Jump table always includes every unregistered world ever visited |
| **World persistence** | State persists **independently of beacon status** | Per-world save records (see [TECHNICAL_ARCHITECTURE.md](TECHNICAL_ARCHITECTURE.md)) |

## 5. The Sanctuary — CANON + PROPOSAL

- **CANON:** an expandable home between universes.
- **PROPOSAL:** hubs for crafting stations, storage, journal/study, cosmetic expansion; sanctuary upgrades tied to helping NPCs who may (proposal) take residence.

## 6. The Traveller's Journal — CANON + PROPOSAL

- **CANON:** records discoveries, lore, relationships and the protagonist's personal development.
- **PROPOSAL:** doubles as codex + quest log + relationship tracker + reflection pages written in the protagonist's own voice (subject to narrative approval).

## 7. Gameplay systems

### 7.1 Platforming — PROPOSAL
Run/jump/climb set tuned for expressive traversal; world layouts reward route mastery. Movement tech grows with equipment (§7.4).

### 7.2 Combat — PROPOSAL
Melee-focused toolkit with equipment-defined options; boss encounters test pattern learning. No combat detail is canon yet.

### 7.3 Crafting & resource gathering — PROPOSAL
Resources harvested per-world (some world-unique to encourage returns); crafting at Sanctuary stations produces equipment, beacons and upgrades.

### 7.4 Equipment progression — PROPOSAL
Equipment modifies traversal and combat capabilities (gating new routes — soft metroidvania structure). Slots and tiers TBD.

### 7.5 Quests & relationships — PROPOSAL
Per-world questlines; helping inhabitants feeds Journal relationship entries and Sanctuary growth; canon rule: the journey is about helping others and self-rediscovery, not reclaiming lost love.

### 7.6 Secrets & bosses — PROPOSAL
Sealed areas tied to equipment and Dimensional Recall revisits; each major world (PROPOSAL) hosts a guardian-style boss protecting something narratively meaningful.

### 7.7 Environmental interaction — PROPOSAL
Readable interactables: switches, physics objects, weather/hazard states that persist per the world-state rule.

## 8. World model

- Each **world** is a self-contained universe: palette, tileset, inhabitants, resources, questlines, boss, secrets. Template TBD in first world production.
- Worlds are authored modularly (tilesets + layered hand-painted backgrounds per [ART_BIBLE.md](ART_BIBLE.md)).
- **Data contract (PROPOSAL):** a world = scenes + a `world_definition` resource + a persistent `world_state` record keyed by universe ID.

## 9. Progression summary

| Axis | Driver |
|---|---|
| Player skill | Platforming/combat mastery |
| Equipment | Crafting, bosses, secrets |
| Travel | Beacons, Dimensional Recall, Home Signal milestones |
| Sanctuary | Expansion through quests and resources |
| Narrative | Journal entries, relationships, alternates mystery (owner-gated canon) |

## 10. Controls — TBD

No bindings are canon. Proposal will be written when the engine project exists; must support keyboard with gamepad as a first-class target.

## 11. Implementation status (updated 2026-11-11)

| System | Status |
|---|---|
| Engine project | ❌ Not created |
| Any gameplay system | ❌ Not implemented |
| Any world | ❌ Not produced |
| Assets | ❌ None imported |

This file describes intent, not reality. When implementation begins, statuses move through: `Design → Prototype → Implemented → Shipped`, recorded here and in [CHANGELOG.md](CHANGELOG.md).
