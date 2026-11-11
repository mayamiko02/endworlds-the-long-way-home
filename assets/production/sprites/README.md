# assets/production/sprites/ — game-ready sprites

## Purpose
Validated, engine-usable sprite textures. Every file must satisfy ART_BIBLE.md §5: PNG with clean alpha, consistent dimensions per asset class, consistent pivots across a character's full set.

## Contents
| Subdirectory | Holds | Manifest category |
|---|---|---|
| [characters/](characters/README.md) | Protagonist, alternates, NPCs | CHR |
| [creatures/](creatures/README.md) | Creatures and enemies | CRE |
| [items/](items/README.md) | Equipment, crafting materials, interactables | ITM |

All currently empty — no assets registered.

## Naming & frames
`<subject>_<descriptor>.png`; animated clips live as frame sequences under `../animations/`, not here. Full rules: [../../NAMING_CONVENTIONS.md](../../NAMING_CONVENTIONS.md).

## Contributing
Only after the underlying concept/reference is approved. Submission: [../../ASSET_SUBMISSION_GUIDE.md](../../ASSET_SUBMISSION_GUIDE.md).

## Dependencies
Imported by `game/` (Godot) once the engine project exists; no other dependency.
