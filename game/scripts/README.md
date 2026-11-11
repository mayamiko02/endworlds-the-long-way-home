# game/scripts/ — GDScript source (PLANNED)

## Purpose
Will hold all GDScript source, mirroring `scenes/` organisation plus `systems/` for autoloaded services. Empty until Phase 2 (see [ROADMAP.md](../../ROADMAP.md)); no engine project exists yet.

## Planned systems (see TECHNICAL_ARCHITECTURE.md §4)
`world_state_store.gd` (persist worlds regardless of beacons — canon), `jump_service.gd` (Random Jump / Beacon Travel / Dimensional Recall / Home Signal), `save_system.gd`, `journal_service.gd`, `sanctuary_state.gd`.

## Conventions (proposal — ratify at Phase 2)
- Static typing everywhere; `snake_case.gd` files; `PascalCase` classes.
- Docstring on every public class and function; comments explain *why*.
- One system per PR; docs updated in the same PR (AGENTS.md rule 9).

## Contributing
[docs/roles/GAMEPLAY_PROGRAMMER_GUIDE.md](../../docs/roles/GAMEPLAY_PROGRAMMER_GUIDE.md).

## Dependencies
Godot 4 project (not yet initialised).
