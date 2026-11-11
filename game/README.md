# game/ — the Godot 4 project (PLANNED)

## ⚠ Honest status
**No engine project exists yet.** There is no `project.godot`, no scenes, no scripts. This directory is a documentation scaffold reserving the layout described in [TECHNICAL_ARCHITECTURE.md](../TECHNICAL_ARCHITECTURE.md). The project is initialised in **Phase 2** of [ROADMAP.md](../ROADMAP.md) by a dedicated PR that will create `project.godot` and pin the engine version (to be recorded here when it happens).

## Planned layout
| Directory | Will hold |
|---|---|
| [scenes/](scenes/README.md) | Scene files organised by feature (player, worlds, sanctuary, ui) |
| [scripts/](scripts/README.md) | GDScript source mirroring the scene organisation |
| [resources/](resources/README.md) | Custom `.tres` resource types (world/item/quest definitions) |
| [data/](data/README.md) | Authored content tables (JSON) consumed by systems |
| [addons/](addons/README.md) | Third-party plugins — default: **none** |

## Rules for when this becomes a real project
- Godot 4, GDScript-first, 2D — per AGENTS.md rule 5 and TECHNICAL_ARCHITECTURE.md.
- Game assets are **imported from `assets/production/`**, never copied by hand; concept art is never imported.
- Generated files (`.godot/`, export presets/credentials, build binaries) are git-ignored — see [../.gitignore](../.gitignore) and [CONTRIBUTING.md](../CONTRIBUTING.md) §7.

## Contributing
Engine work follows [docs/roles/GAMEPLAY_PROGRAMMER_GUIDE.md](../docs/roles/GAMEPLAY_PROGRAMMER_GUIDE.md). Branches `feature/…`, PR per [CONTRIBUTING.md](../CONTRIBUTING.md).

## Dependencies
Godot 4 editor (version TBD at initialisation); validated production assets for anything visible in-game.
