# assets/production/sprites/characters/ — character sprites

## Purpose
Game-ready character sprites for the protagonist, alternate protagonists and NPCs.

## Prerequisites (non-negotiable)
The relevant **approved character reference** must exist with status `approved-master` before production sprites of that character are made (AGENTS.md rules 2/6). Until then this folder stays empty.

## Contents
Currently empty.

## Standards
- PNG, sRGB, clean alpha (ART_BIBLE.md §5).
- Proportions, pivots, lighting and dimensions identical to the approved reference and to every other sprite of the same character.
- Sprite animation frames go in `assets/production/animations/<subject>_<clip>/`, not here.

## Naming & contributing
`<character>_<pose_or_state>.png` · branch `art/…` · manifest category `CHR` · see [assets/NAMING_CONVENTIONS.md](../../../NAMING_CONVENTIONS.md) and [assets/ASSET_SUBMISSION_GUIDE.md](../../../ASSET_SUBMISSION_GUIDE.md).

## Dependencies
Requires approved reference in `assets/concept-art/characters/`. Consumed by the Godot project at import time.
