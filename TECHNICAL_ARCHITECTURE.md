# TECHNICAL ARCHITECTURE
### ENDWORLDS: THE LONG WAY HOME

> **Purpose:** engine choice, project structure, system architecture and coding standards.
> **Honest state (2026-11-11): no Godot project exists yet.** This document describes the intended architecture and the scaffold reserved for it in `game/`. Implementation begins in Phase 2 — see [ROADMAP.md](ROADMAP.md).

---

## 1. Engine & language — CANON

- **Engine:** Godot 4 (latest stable 4.x at project initialisation; pin the version in `game/README.md` when created).
- **Language:** GDScript for gameplay and tooling; consider C# only if a concrete need arises (adds export/build complexity — requires owner sign-off per rule 5).
- **Rendering target:** 2D. No 3D nodes outside editor tooling.

## 2. Architectural principles — CANON (from master instructions rule 5)

1. **Modular, maintainable, well-documented systems.**
2. **Data-driven architecture** — content lives in resources/files, not hard-coded in scenes.
3. **Reusable assets, modular environment construction.**
4. **Efficient asset loading** (load screens stream; worlds unload cleanly).
5. **Persistent world-state storage** — world states persist independently of beacon registration (rule 4).
6. **No unnecessary dependencies or expensive technical complexity.** Performance, maintainability, meaningful gameplay — in that order of trade-offs.

## 3. Planned repository layout (engine project)

The `game/` directory is reserved for the Godot project. Current status: documentation scaffold only — **no `project.godot` yet.**

```
game/
├── project.godot        (to be created at Phase 2)
├── scenes/              Scene files, organised by feature
├── scripts/             GDScript source, mirroring scenes
├── resources/           Custom .tres resource types & content data
├── data/                JSON/CFG authored content (world definitions, item tables…)
└── addons/              Third-party plugins only if truly needed (default: none)
```

Planned scene/script organisation (PROPOSAL — refine at initialisation):

| Area | Contents |
|---|---|
| `scenes/player/` | Player controller, headset UI hooks |
| `scenes/worlds/` | One folder per universe; shared world base scene with per-world overrides |
| `scenes/sanctuary/` | Sanctuary hub and expansion modules |
| `scripts/systems/` | Autoloaded services (see §4) |
| `resources/definitions/` | World, item, quest, boss definitions as custom resources |

## 4. Planned core systems (PROPOSAL, ordered by roadmap)

| System | Responsibility | Notes |
|---|---|---|
| `WorldStateStore` | Persist per-universe state regardless of beacon status (CANON rule) | JSON-serialised records keyed by universe ID; save-slot aware |
| `JumpService` | Random Jump, Beacon Travel, Dimensional Recall weighting, Home Signal progress | Implements the travel table incl. forgotten-world eligibility |
| `SaveSystem` | Slot management, migrations, integrity checks | |
| `JournalService` | Journal entries, discoveries, relationships | Data-driven entries referenced by content |
| `SanctuaryState` | Hub expansion state, stations, residents | Feeds off quest outcomes |
| `InputMap` conventions | Rebindable actions, keyboard + gamepad | Bindings TBD (GDD §10) |

Autoloads are introduced one at a time, each with its own PR and documentation.

## 5. Coding standards — PROPOSAL (ratify at Phase 2)

- GDScript with **static typing** everywhere (`var x: int`, typed signatures).
- `snake_case` files/functions/variables; `PascalCase` classes; `CONSTANT_CASE` constants.
- One responsibility per script; compose scenes from small nodes; prefer signals over hard references.
- Every public class/function carries a docstring comment; non-obvious logic gets a `## why` comment (rule: well-documented systems).
- Follow the official Godot GDScript style guide and export-order conventions.

## 6. Performance budgets — WORKING DEFAULTS

- 60 FPS on modest hardware; texture budget per world ≤ 512 MB VRAM (proposal).
- Loading between universes must not hitch mid-gameplay — stream during jump transitions.
- Profile before optimising; document any optimisation in the PR.

## 7. Generated files

Never commit Godot-generated or build artifacts — the canonical list lives in [CONTRIBUTING.md](CONTRIBUTING.md) §7 and is enforced by [.gitignore](.gitignore).

## 8. Dependencies & tooling

- Default: **zero external addons.** Any addition needs justification in its PR (rule 5).
- Pipeline automation (e.g. manifest validation) belongs in `tools/` — see `tools/README.md`.
