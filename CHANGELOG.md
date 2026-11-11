# CHANGELOG
### ENDWORLDS: THE LONG WAY HOME

All notable changes to this repository are documented here. Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) conventions (Changed / Added / Fixed / Removed), dated `YYYY-MM-DD`. Versioning per release will follow Semantic Versioning once the game has a build.

---

## [Unreleased]

### Added — 2026-11-11 — Repository initialisation & documentation scaffold

- **Core documentation at root:** rewritten `README.md` (repository overview, doc index, map); expanded `AGENTS.md` (original master instructions preserved verbatim, plus operating supplement §§11–13: repository map, role guides, workflow quick reference); new `PROJECT_BIBLE.md`, `GAME_DESIGN_DOCUMENT.md`, `ART_BIBLE.md`, `TECHNICAL_ARCHITECTURE.md`, `CONTRIBUTING.md` (branch/PR/review/merge guidelines), `ROADMAP.md`, and this `CHANGELOG.md`.
- **Directory scaffold with READMEs everywhere:** `assets/` (concept-art, production/{sprites,animations,tilesets,ui}, audio/{music,sfx}, fonts, reference), `docs/roles/`, `game/` (empty planned engine scaffold — no `project.godot` created), `qa/` (test-plans, bug-reports), `tools/`, `.github/`.
- **Asset pipeline:** empty `assets/ASSET_MANIFEST.json` (self-describing schema, zero entries — no assets imported yet), human-readable `assets/ASSET_INDEX.md`, `assets/NAMING_CONVENTIONS.md`, `assets/ASSET_SUBMISSION_GUIDE.md` with the approval-status lifecycle.
- **Role-specific agent instructions:** artist, character designer, environment designer, gameplay programmer and QA guides under `docs/roles/`.
- **Collaboration infrastructure:** `.github/PULL_REQUEST_TEMPLATE.md`, `.github/CODEOWNERS` (project owner as default reviewer).
- **Enhanced `.gitignore`:** preserved existing Godot rules; added export artifacts, OS/editor noise and tooling caches, each documented inline.

### Existing work preserved

- `a0599cb` — "Add master AI agent instructions" (the original `AGENTS.md`, `README.md`, `.gitignore`). Master instructions copied into the new `AGENTS.md` unchanged; original README description folded into the new README's "About this repository"; all original `.gitignore` entries retained.

---

*Recording rule (AGENTS.md §9): when you add a character, universe, creature, mechanic, system or asset, add a dated entry here in the same PR.*
