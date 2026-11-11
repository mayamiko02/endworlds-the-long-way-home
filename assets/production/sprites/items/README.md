# assets/production/sprites/items/ — item & equipment sprites

## Purpose
Game-ready sprites for equipment, crafting materials, collectibles and world interactables (GDD §7.3–7.4). Includes both world pickups and their inventory/journal icons — keep both in the same submission so they match.

## Contents
Currently empty. Item production starts no earlier than Phase 3–4 (see [ROADMAP.md](../../../../ROADMAP.md)).

## Standards
- PNG, sRGB, clean alpha; one consistent icon scale across the whole inventory (value TBD with UI spec).
- World-object versions share palette/lighting conventions with their home world.

## Naming & contributing
`<item>_<descriptor>.png` (e.g. `beacon_crystal_icon.png`, `beacon_crystal_world.png`) · manifest category `ITM` · see [assets/NAMING_CONVENTIONS.md](../../../NAMING_CONVENTIONS.md) and [assets/ASSET_SUBMISSION_GUIDE.md](../../../ASSET_SUBMISSION_GUIDE.md).

## Dependencies
Crafting/item definitions will live in `game/data/`; icons must not ship before their data definition exists.
