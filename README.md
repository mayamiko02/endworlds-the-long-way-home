# ENDWORLDS: THE LONG WAY HOME

An original 2D adventure platformer about identity, loss, discovery, parallel universes and finding a new meaning of home.

**Engine:** Godot 4 · **Stage:** Pre-production (repository scaffolding) · **Owner:** @mayamiko02

---

## About this repository

This repository began as a reference brain for AI agents working on the project and is now the **central source of truth** for ENDWORLDS: THE LONG WAY HOME. Documentation, asset manifests, design canon and — in later phases — the Godot project itself all live here. If a fact about the project is not written down in this repository, treat it as unconfirmed.

**Current state (2026-11-11):** the repository contains project documentation and an empty, ready-to-use directory scaffold. **No Godot project, no game code and no imported art assets exist yet.** Nothing in this repository claims otherwise. See [ROADMAP.md](ROADMAP.md) for what happens next.

## Start here

| If you are… | Read first |
|---|---|
| New to the project | This file, then [AGENTS.md](AGENTS.md), then [PROJECT_BIBLE.md](PROJECT_BIBLE.md) |
| An AI agent of any kind | [AGENTS.md](AGENTS.md) — the master instructions are binding |
| An artist | [ART_BIBLE.md](ART_BIBLE.md) + [docs/roles/ARTIST_GUIDE.md](docs/roles/ARTIST_GUIDE.md) |
| A character designer | [docs/roles/CHARACTER_DESIGN_GUIDE.md](docs/roles/CHARACTER_DESIGN_GUIDE.md) |
| An environment designer | [docs/roles/ENVIRONMENT_DESIGN_GUIDE.md](docs/roles/ENVIRONMENT_DESIGN_GUIDE.md) |
| A gameplay programmer | [TECHNICAL_ARCHITECTURE.md](TECHNICAL_ARCHITECTURE.md) + [docs/roles/GAMEPLAY_PROGRAMMER_GUIDE.md](docs/roles/GAMEPLAY_PROGRAMMER_GUIDE.md) |
| A QA agent | [docs/roles/QA_GUIDE.md](docs/roles/QA_GUIDE.md) |
| Submitting an asset | [assets/ASSET_SUBMISSION_GUIDE.md](assets/ASSET_SUBMISSION_GUIDE.md) |
| Opening a pull request | [CONTRIBUTING.md](CONTRIBUTING.md) + [.github/PULL_REQUEST_TEMPLATE.md](.github/PULL_REQUEST_TEMPLATE.md) |

## Core documentation (repository root)

| Document | Purpose |
|---|---|
| [AGENTS.md](AGENTS.md) | Master AI agent instructions — binding rules for every contributor |
| [PROJECT_BIBLE.md](PROJECT_BIBLE.md) | Story, characters, worlds and canon definition |
| [GAME_DESIGN_DOCUMENT.md](GAME_DESIGN_DOCUMENT.md) | Gameplay systems, mechanics and progression design |
| [ART_BIBLE.md](ART_BIBLE.md) | Visual direction, art specifications and quality bar |
| [TECHNICAL_ARCHITECTURE.md](TECHNICAL_ARCHITECTURE.md) | Engine, code architecture and technical standards |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Branch, pull request, review and merge guidelines |
| [ROADMAP.md](ROADMAP.md) | Phased plan and current milestone status |
| [CHANGELOG.md](CHANGELOG.md) | Dated record of notable repository changes |

## Repository map

```
endworlds-the-long-way-home/
├── .github/          PR template and code ownership
├── assets/           All artwork, audio and fonts + the central ASSET_MANIFEST.json
│   ├── concept-art/      Non-production concept work (painterly exploration)
│   ├── production/       Game-ready sprites, animations, tilesets and UI
│   ├── audio/            Music and sound effects
│   ├── fonts/            Typefaces
│   └── reference/        Reference material supplied by the project owner
├── docs/             Role-specific agent instructions and extended guides
├── game/             The Godot 4 project (planned — no engine files yet)
├── qa/               Test plans and bug reports
├── tools/            Automation and pipeline scripts (planned)
└── <root docs>       The core documentation listed above
```

Every directory contains its own `README.md` explaining its purpose, contents, naming conventions, contribution instructions and dependencies.

## Asset management at a glance

Every asset gets a unique ID (`ELWH-<CATEGORY>-<NNNN>`), a descriptive filename, a folder by category and an entry in [assets/ASSET_MANIFEST.json](assets/ASSET_MANIFEST.json) with an approval status. Approved master assets are never overwritten without explicit owner authorisation. Full details: [assets/README.md](assets/README.md).

## Contributing

All work happens on dedicated branches and lands on `main` through reviewed pull requests only. Nobody — human or agent — pushes unreviewed changes to `main` or silently overwrites another contributor's work. Full workflow: [CONTRIBUTING.md](CONTRIBUTING.md).

## Licence

Not yet decided (tracked in [ROADMAP.md](ROADMAP.md) outstanding issues). Until a licence is added, all content is © the project owner, all rights reserved.
