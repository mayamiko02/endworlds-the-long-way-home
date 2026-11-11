# assets/fonts/ — typefaces

## Purpose
Fonts used by the game's UI, Traveller's Journal and any in-world text. Type choice must fit the hand-painted identity (ART_BIBLE.md): a distinctive display face for titles/journal + a highly legible face for UI body text (proposal, not canon).

## Licence rule
**Only fonts with verifiable games-embedding licences** (e.g. OFL). Record the licence name and source URL in the manifest entry (`license` field) and drop the licence text file next to the font. No licence → no commit.

## Contents
Currently empty.

## Naming & contributing
`<family>_<weight>.ttf` (e.g. `garamond_regular.ttf`) · manifest category `FNT` · [../ASSET_SUBMISSION_GUIDE.md](../ASSET_SUBMISSION_GUIDE.md).

## Dependencies
Imported by Godot when the engine project exists; referenced by UI production art in `assets/production/ui/`.
