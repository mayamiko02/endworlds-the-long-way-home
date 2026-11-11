# assets/production/ — game-ready assets

## Purpose
The **only** asset tree the engine imports from. Everything here must be validated against [ART_BIBLE.md](../../ART_BIBLE.md) §5 specs (format, dimensions, alpha, pivots, scale) and carry manifest status `approved` or `approved-master` before use in the build.

> Currently empty — no production assets exist. Production begins after Phase 1 approvals ([ROADMAP.md](../../ROADMAP.md)).

## Contents
| Subdirectory | Holds | Manifest categories |
|---|---|---|
| [sprites/](sprites/README.md) | Game-ready character, creature and item sprites | CHR, CRE, ITM |
| [animations/](animations/README.md) | Animation frame sequences, one folder per clip | ANM |
| [tilesets/](tilesets/README.md) | Modular terrain/environment tilesets | TIL |
| [ui/](ui/README.md) | Production UI art | UI |

(Production environment background art also belongs here as category `ENV` — add `backgrounds/` when the first world is produced.)

## Rules
- Concept work never lives here — it stays in `assets/concept-art/`.
- Never claim engine-readiness without validation; record validation in the manifest entry (rule 6).
- `approved-master` files are immutable without owner authorisation.

## Contributing & dependencies
[../ASSET_SUBMISSION_GUIDE.md](../ASSET_SUBMISSION_GUIDE.md). No engine dependency at rest; the Godot project will reference this tree at import time.
