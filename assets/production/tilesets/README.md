# assets/production/tilesets/ — environment tilesets

## Purpose
Modular, reusable tilesets for building worlds (AGENTS.md rule 5: modular environment construction). Each universe gets its own tileset family derived from its approved environment concept.

## Prerequisites
- Approved environment concept + palette script for the world (Phase 1).
- Ratified tile grid and PPU in ART_BIBLE.md §5 (currently TBD — do not produce tilesets before these are pinned).

## Contents
Currently empty.

## Standards
- PNG, one atlas per tile theme; grid size stated in the manifest `notes` and uniform within a set.
- Designed to recombine: transitions, corners and variants included as a coherent kit.
- Texture size ≤ 4096² (ART_BIBLE.md §5).

## Naming & contributing
`<world>_<theme>.png` (e.g. `world01_terrain.png`) · manifest category `TIL` · see [assets/NAMING_CONVENTIONS.md](../../NAMING_CONVENTIONS.md) and [assets/ASSET_SUBMISSION_GUIDE.md](../../ASSET_SUBMISSION_GUIDE.md).

## Dependencies
Environment concepts in `assets/concept-art/environments/`; imported by Godot `TileSet` resources when the engine project exists.
