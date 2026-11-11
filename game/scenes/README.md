# game/scenes/ — Godot scene files (PLANNED)

## Purpose
Will hold `.tscn` scene files organised by feature. Empty until Phase 2 (see [ROADMAP.md](../../ROADMAP.md)); no engine project exists yet.

## Planned sub-organisation
| Folder | Scenes |
|---|---|
| `player/` | Player controller, camera rig |
| `worlds/` | Shared world base scene + one folder per universe |
| `sanctuary/` | Sanctuary hub and expansion modules |
| `ui/` | HUD, menus, journal, headset interface |

## Conventions (proposal — ratify at Phase 2)
- Scene files `snake_case.tscn`; one root node named after the scene.
- Small composed scenes over monoliths; shared behaviour via base scenes/inheritance, not copy-paste.
- Each universe folder contains only that universe's overrides on the world base scene.

## Contributing
[TECHNICAL_ARCHITECTURE.md](../../TECHNICAL_ARCHITECTURE.md) + [docs/roles/GAMEPLAY_PROGRAMMER_GUIDE.md](../../docs/roles/GAMEPLAY_PROGRAMMER_GUIDE.md).

## Dependencies
Godot 4 project (not yet initialised).
