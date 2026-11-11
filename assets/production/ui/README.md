# assets/production/ui/ — production UI art

## Purpose
Game-ready interface art: HUD, menus, headset travel interface, Traveller's Journal and Sanctuary screens — hand-painted to match ART_BIBLE.md while staying legible at target resolutions.

## Prerequisites
Approved UI concept from `assets/concept-art/ui/` and ratified UI metrics (resolution targets, icon scale — currently TBD).

## Contents
Currently empty. Earliest need: basic HUD during Phase 4 playable slice (see [ROADMAP.md](../../../ROADMAP.md)).

## Standards
- PNG with alpha; 9-patch-friendly margins for panels; states (normal/hover/pressed/disabled) in one submission.
- Text-safe areas respected; no baked text (fonts handle text rendering).

## Naming & contributing
`<screen>_<element>_<state>.png` where applicable (e.g. `journal_button_normal.png`) · manifest category `UI` · see [assets/NAMING_CONVENTIONS.md](../../NAMING_CONVENTIONS.md) and [assets/ASSET_SUBMISSION_GUIDE.md](../../ASSET_SUBMISSION_GUIDE.md).

## Dependencies
UI concepts approved; fonts from `assets/fonts/` for any text shown in mockups.
