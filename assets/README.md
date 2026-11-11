# assets/ — all project artwork, audio and fonts

## Purpose
Every image, animation, sound and typeface for ENDWORLDS: THE LONG WAY HOME lives here, tracked in one central manifest. Two file-level companions define the pipeline:

| File | Purpose |
|---|---|
| [ASSET_MANIFEST.json](ASSET_MANIFEST.json) | Machine-readable registry of every asset (currently empty — no assets imported yet) |
| [ASSET_INDEX.md](ASSET_INDEX.md) | Human-readable view of the same data |
| [NAMING_CONVENTIONS.md](NAMING_CONVENTIONS.md) | Folder, filename and asset-ID rules |
| [ASSET_SUBMISSION_GUIDE.md](ASSET_SUBMISSION_GUIDE.md) | Step-by-step submission and approval process |

## Directory contents
| Directory | Holds | Production status |
|---|---|---|
| [concept-art/](concept-art/README.md) | Exploratory/pitch artwork: characters, environments, UI | NOT game-ready |
| [production/](production/README.md) | Game-ready sprites, animation frames, tilesets, UI | Game-ready once validated |
| [audio/](audio/README.md) | Music and sound effects | Game-ready once validated |
| [fonts/](fonts/README.md) | Typefaces with licence proof | Game-ready once validated |
| [reference/](reference/README.md) | Owner-supplied reference material | Never ships |

## The four rules that matter most (AGENTS.md rule 6)
1. Every asset has a **unique ID**, descriptive filename, category, source reference and manifest entry.
2. **Preserve original artwork** — source files (PSD/KRA/Aseprite/WAV) are committed alongside exports.
3. **Never overwrite an `approved-master` asset** without explicit owner authorisation — version up instead.
4. Never claim an asset is engine-ready until validated against its specs; validation is recorded in the manifest.

## Contributing
Submissions follow [ASSET_SUBMISSION_GUIDE.md](ASSET_SUBMISSION_GUIDE.md): branch `art/…` → correct folder → manifest entry (`status: "proposed"`) → PR → owner review → status moves to `approved`/`approved-master`.

## Dependencies
None at rest. Future `tools/` validators will parse `ASSET_MANIFEST.json` — keep it valid JSON (no comments, no trailing commas).
