# assets/audio/ — music & sound effects

## Purpose
All audio for the game. Audio production is scheduled later in the roadmap (Phase 6+, [ROADMAP.md](../../ROADMAP.md)) — proposals welcome earlier.

## Contents
| Subdirectory | Holds | Manifest category |
|---|---|---|
| [music/](music/README.md) | Soundtrack themes, ambient beds, stingers | MUS |
| [sfx/](sfx/README.md) | Interface, movement, combat, world ambience one-shots | SFX |

Both currently empty.

## Working standards (to be ratified with audio lead)
- Masters: WAV 48 kHz / 24-bit, preserved alongside deliverables (rule 6).
- Deliverables: OGG Vorbis for loops in-game; seamless loop points verified and declared in manifest `notes`.
- Loudness target: TBD; one target, uniformly applied.

## Naming & contributing
`<scope>_<title>.<ext>` (e.g. `sanctuary_theme_main.ogg`, `ui_confirm.ogg`) · manifest categories MUS/SFX · see [../NAMING_CONVENTIONS.md](../NAMING_CONVENTIONS.md) and [../ASSET_SUBMISSION_GUIDE.md](../ASSET_SUBMISSION_GUIDE.md). External libraries require licence proof in the manifest entry.

## Dependencies
None at rest; imported by Godot when the engine project exists.
