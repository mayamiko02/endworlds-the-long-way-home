# NAMING CONVENTIONS
### ENDWORLDS: THE LONG WAY HOME — assets, folders and IDs

Consistency here is what lets a multi-agent team work without collisions. When in doubt, look at existing registered assets in [ASSET_MANIFEST.json](ASSET_MANIFEST.json) / [ASSET_INDEX.md](ASSET_INDEX.md) and match them.

---

## 1. Asset IDs

```
ELWH-<CATEGORY>-<NNNN>
```

- `ELWH` — project prefix.
- `<CATEGORY>` — one of the manifest category codes: `CON` concept, `CHR` character sprite, `CRE` creature, `ENV` environment, `TIL` tileset, `ITM` item, `UI` interface, `ANM` animation, `MUS` music, `SFX` sound, `FNT` font, `REF` reference.
- `<NNNN>` — zero-padded serial, 4 digits, assigned in order **per category** (`ELWH-CHR-0001`, `ELWH-CHR-0002`…).
- IDs are **unique and never reused**, even for rejected or deprecated assets. Claim the next free number in your PR; if two PRs collide, later-merged PR renumbers.

## 2. Directories

- `lowercase-with-hyphens`, plural only when natural: `concept-art/`, `test-plans/`, `sprites/`.
- Place files by *kind and status*, not by artist or date: concept work under `concept-art/`, game-ready work under `production/`.

## 3. Filenames

```
<subject>_<descriptor>[_vNN].<ext>
```

- All lowercase `snake_case`, no spaces, no capitals, no dates in names.
- `<subject>` — the thing: `protagonist`, `sanctuary_hub`, `world01_overgrowth`.
- `<descriptor>` — the variant or state: `turnaround`, `idle`, `run_f0001`, `palette_script`.
- `_vNN` — revision number for **work-in-progress iterations** (`_v01`, `_v02`). Once approved, the file is stable; revisions become new versions with new IDs if meaningfully different.
- Extensions lowercase: `.png`, `.psd`, `.kra`, `.aseprite`, `.wav`, `.ogg`, `.ttf`.

### Examples (illustrative — these files do not exist yet)
| File | Would-be ID |
|---|---|
| `concept-art/characters/protagonist_turnaround_v01.png` | ELWH-CON-0001 |
| `concept-art/environments/world01_mood_key_v01.png` | ELWH-CON-0002 |
| `production/sprites/characters/protagonist_idle.png` | ELWH-CHR-0001 |
| `production/animations/protagonist_run/protagonist_run_f0001.png` | ELWH-ANM-0001 |
| `production/tilesets/world01_terrain.png` | ELWH-TIL-0001 |

## 4. Animation frames

One folder per clip: `production/animations/<subject>_<clip>/` containing `…_f0001.png`, `…_f0002.png`… (4-digit frame numbers). The **pivot must be identical across all frames of all clips** for a character (rule 6) — record it in the manifest `notes`.

## 5. Source files

Keep originals beside or near exports with the same base name where practical: `protagonist_idle.aseprite` → `protagonist_idle.png`. List them in the manifest `source_files` array.

## 6. Documentation files

`UPPER_SNAKE_CASE.md` for project-level docs (`ART_BIBLE.md`), `README.md` exactly cased for directory guides. GitHub renders both natively.

## 7. Branches & commits

- Branches: `art/<short-description>` (see [../CONTRIBUTING.md](../CONTRIBUTING.md)).
- Commit messages reference IDs: `Add ELWH-CON-0001 protagonist turnaround concept`.
