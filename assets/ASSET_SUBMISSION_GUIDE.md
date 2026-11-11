# ASSET SUBMISSION GUIDE
### How an asset goes from your hands into the project

This is the shared pipeline for all art roles; role guides ([../docs/roles/](../docs/roles/README.md)) tell you *what* to make — this tells you *how to submit it*.

---

## Approval statuses

| Status | Meaning | Who sets it |
|---|---|---|
| `proposed` | Submitted; awaiting review. Not usable in production. | Submitter |
| `in-review` | Being actively reviewed. | Reviewer |
| `changes-requested` | Revisions required; resubmit moves back to `in-review`. | Reviewer |
| `approved` | Accepted for use. New versions remain possible. | Owner (or delegate) |
| `approved-master` | Locked master — **never overwrite without explicit owner authorisation** (rule 6). | Owner only |
| `rejected` | Not accepted; kept on record only if owner requests. | Owner |
| `deprecated` | Superseded by a newer asset ID. | Owner |

## Submission steps

1. **Check first** (rule 1): search [ASSET_INDEX.md](ASSET_INDEX.md), the manifest JSON and folders for existing or in-review work on the same subject. Extend or version — never duplicate or silently replace.
2. **Branch**: `art/<short-description>` from up-to-date `main` ([../CONTRIBUTING.md](../CONTRIBUTING.md)).
3. **Place** the file in the correct folder (concept vs production matters — rule 6):
   - exploration/pitch → `assets/concept-art/…`
   - validated, game-ready → `assets/production/…`
   - music/SFX masters → `assets/audio/…` · typefaces → `assets/fonts/…` · owner reference → `assets/reference/…`
4. **Name** it per [NAMING_CONVENTIONS.md](NAMING_CONVENTIONS.md) and claim the next free ID in its category.
5. **Preserve the original** source file (PSD/KRA/Aseprite/WAV) alongside the export (rule 6).
6. **Manifest**: append an entry to `ASSET_MANIFEST.json` → `assets` array, following `entry_schema`, status `proposed`, honest `author_or_source` and tool disclosure, plus `ASSET_INDEX.md` row **in the same PR** (rule 9).
7. **PR** using the template: include the artwork inline, say what is final vs exploratory, and record validation performed (dimensions, alpha, pivots) or plainly state "not validated".
8. **Review**: the owner (art director) applies the status lifecycle. `approved-master` is the owner's call alone.
9. **Revisions**: new file version (`_vNN`), manifest `notes` updated; superseded approved assets move to `deprecated`. Never edit an `approved-master` file in place.

## Production-readiness checklist (required before status `approved` on production assets)
- [ ] Matches the approved character reference / palette scripts where applicable
- [ ] Meets ART_BIBLE.md §5 working specs (format, alpha, dimensions, pivots, scale)
- [ ] Engine validation performed and described — or the asset honestly stays in `proposed`/`concept`
- [ ] No generic-AI look, no plastic 3D, no inconsistent anatomy (rule 2)

## Common mistakes
- Committing to the wrong folder (concept work in `production/`).
- Editing the manifest without the index (or vice versa) — they change together.
- Marking your own work `approved` — submitters never approve their own assets.
- Hand-flattening texture atlases or exporting straight into `game/` — assets are imported by the engine from `assets/production/` during engine phases.
