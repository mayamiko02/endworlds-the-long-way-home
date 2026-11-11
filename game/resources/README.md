# game/resources/ — custom Godot resources (PLANNED)

## Purpose
Will hold custom `.tres`/`.gd` resource types that make the game data-driven (AGENTS.md rule 5): world definitions, item/equipment data, quest data, boss data. Empty until Phase 2 (see [ROADMAP.md](../../ROADMAP.md)); no engine project exists yet.

## Planned types (proposal)
| Resource | Fields (sketch) |
|---|---|
| `WorldDefinition` | universe_id, display_name, scenes, palette ref, travel weight, boss ref |
| `ItemDefinition` | item_id, sprite ref (from assets/production), crafting recipe, equip effects |
| `QuestDefinition` | quest_id, steps, journal entry refs, rewards |
| `BossDefinition` | boss_id, world ref, phases, unlocks |

## Conventions
- Content lives in resources/data, not hard-coded in scenes.
- Resource schemas get documented here when created (rule 9).

## Contributing
[TECHNICAL_ARCHITECTURE.md](../../TECHNICAL_ARCHITECTURE.md). Schema changes are reviewable PRs like code.

## Dependencies
Godot 4 project (not yet initialised); validated `assets/production/` entries for any visual refs.
