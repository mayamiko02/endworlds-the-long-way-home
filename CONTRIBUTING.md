# Contributing to ENDWORLDS: THE LONG WAY HOME

These guidelines bind every contributor — human and AI agent alike. They restate the collaboration rules in [AGENTS.md](AGENTS.md) as an operational workflow. If anything here conflicts with AGENTS.md, AGENTS.md wins; raise the conflict in a PR so it can be resolved.

---

## 1. Before you start

1. Read [AGENTS.md](AGENTS.md) (master instructions — binding).
2. Read the role guide matching your task in [docs/roles/](docs/roles/README.md).
3. Inspect the existing repository: search before you create. Do not assume a file, asset or feature does not exist without checking.
4. For asset work, also read [assets/ASSET_SUBMISSION_GUIDE.md](assets/ASSET_SUBMISSION_GUIDE.md) and [assets/NAMING_CONVENTIONS.md](assets/NAMING_CONVENTIONS.md).

## 2. Branching

- `main` is protected by convention and by review: **nobody commits directly to it.**
- Create one branch per unit of work, branched from an up-to-date `main`.
- Naming: `type/short-description`, lowercase, hyphenated:

| Prefix | Use |
|---|---|
| `feature/` | New gameplay systems, engine work, tools |
| `art/` | Concept art and production assets |
| `docs/` | Documentation-only changes |
| `fix/` | Bug fixes |
| `qa/` | Test plans and QA artifacts |
| `arena/` | Reserved for Arena agent sessions (already named by the platform) |

Examples: `feature/sanctuary-save-system`, `art/protagonist-concept-v01`, `docs/update-roadmap`.

## 3. Commits

- Imperative, descriptive subjects: `Add protagonist turnaround concept`, not `updates`.
- Group related files; do not bundle unrelated systems in one commit (AGENTS.md rule 7).
- Reference asset IDs (e.g. `ELWH-CON-0001`) in commit messages for asset work.

## 4. Pull requests

- Fill in [.github/PULL_REQUEST_TEMPLATE.md](.github/PULL_REQUEST_TEMPLATE.md) completely; it encodes the project rules as a checklist.
- Keep PRs scoped. A PR that touches unrelated systems should be split.
- **Canon changes** (story facts, protagonist identity, approved visual identity) require explicit approval from the project owner (@mayamiko02) — see CODEOWNERS. Mark unapproved creative additions **PROPOSAL** in the document itself.
- **Asset PRs** must update `assets/ASSET_MANIFEST.json` and `assets/ASSET_INDEX.md` in the same PR (AGENTS.md rule 9).
- Describe validation honestly: state what was tested, how, and what was *not* tested (AGENTS.md rule 8).

## 5. Review

- Every PR needs review before merge. Reviews check:
  - Scope discipline (no unrelated edits, nothing silently overwritten or deleted).
  - Documentation and manifest updates included (rule 9).
  - Canon/proposal separation respected (rule 10).
  - For code: modularity, Godot 4 conventions, no unnecessary dependencies (rule 5).
  - For art: consistency with [ART_BIBLE.md](ART_BIBLE.md), correct folder, naming and manifest status.
- Reviewers comment with specific, actionable feedback. Authors respond to every thread.

## 6. Merge

- Only the project owner merges canon-affecting PRs; routine PRs may be merged by the owner after review approval.
- Default merge method: **merge commit** (preserves context). Squash is acceptable for noisy WIP branches.
- After merge, delete the feature branch if it is no longer needed (except platform-managed `arena/*` branches, which Arena manages).
- Never approve and merge your own PR.

## 7. Files that must NOT be committed

[.gitignore](.gitignore) enforces this; the list below documents *why*:

- **Godot generated data**: `.godot/` (editor cache, imported resources, global script class cache), `.import/` (Godot 3-style import cache), `*.translation` (generated from CSVs), `.mono/`, `data_*/`, `mono_crash.*.json`.
- **Export artifacts**: `export.cfg`, `export_credentials.cfg` (may contain secrets), `*.exe`, `*.pck` releases, `*.apk`, `*.aab`, `*.ipa`, `*.dmg`, `*.zip` builds — builds go in Releases, not Git.
- **OS/editor noise**: `.DS_Store`, `Thumbs.db`, `desktop.ini`, `.vscode/`, `.idea/`, swap files.
- **Tooling caches**: `__pycache__/`, `.pytest_cache/`, `node_modules/`.
- **Anything containing credentials or tokens — ever.** If a secret is committed by accident, treat it as compromised and rotate it immediately.

Source files for assets (PSD, KRA, Aseprite projects, WAV masters) **should** be committed when practical — they are originals the manifest requires us to preserve (rule 6).

## 8. Definition of done

A change is done when: it is on a branch, the PR template checklist is complete, docs and manifests are updated, review is approved, no unrelated files changed, and the honest validation status is recorded in the PR.

## 9. Disagreements and proposals

Creative freedom is welcome (rule 10): open a PR or issue with your idea clearly labelled **PROPOSAL**. The project owner's decision on canon is final.
