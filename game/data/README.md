# game/data/ — authored content tables (PLANNED)

## Purpose
Will hold human-authored, machine-read content: jump weight tables, crafting recipes, journal entry text, dialogue. Empty until Phase 2+ (see [ROADMAP.md](../../ROADMAP.md)); no engine project exists yet.

## Planned files (proposal)
| File | Contents |
|---|---|
| `jump_tables.json` | Random Jump/Recall weights per universe (implements canon travel rules) |
| `recipes.json` | Crafting inputs/outputs |
| `journal_entries.json` | Journal text keyed by entry id |

## Conventions
- JSON, UTF-8, 2-space indent, stable key order — diff-friendly.
- Every table has a documented schema (in this README or the consuming system) before content lands.

## Contributing
Text/narrative content is canon-sensitive: mark PROPOSAL and get owner approval per [PROJECT_BIBLE.md](../../PROJECT_BIBLE.md) §7.

## Dependencies
Consumed by systems in `game/scripts/systems/` once those exist.
