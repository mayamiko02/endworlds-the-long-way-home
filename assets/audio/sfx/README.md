# assets/audio/sfx/ — sound effects

## Purpose
One-shots and short loops: footsteps, jumps, hits, crafting, UI, headset/jump transitions, ambient world layers.

## Contents
Currently empty — audio phase scheduled for Phase 6+ ([ROADMAP.md](../../../ROADMAP.md)). The headset's jump sound is a signature design element; treat its design as a deliberate creative decision when the time comes.

## Standards (working defaults)
- WAV 48 kHz / 24-bit masters preserved; OGG Vorbis deliverables.
- Named by surface/action for data-driven lookup: `<system>_<action>[_variantNN]` — e.g. `footstep_grass_01.ogg`, `headset_jump_01.ogg`.

## Contributing
Manifest category `SFX` (variants under one ID, listed in `notes`) · [../../ASSET_SUBMISSION_GUIDE.md](../../ASSET_SUBMISSION_GUIDE.md) and [../../NAMING_CONVENTIONS.md](../../NAMING_CONVENTIONS.md). External SFX need licence proof in the manifest.

## Dependencies
None.
