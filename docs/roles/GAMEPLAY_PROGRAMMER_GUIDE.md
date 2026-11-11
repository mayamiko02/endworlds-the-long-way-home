# GAMEPLAY PROGRAMMER GUIDE
### Role instructions for gameplay programmers and coding agents

Read first: [AGENTS.md](../../AGENTS.md) → [TECHNICAL_ARCHITECTURE.md](../../TECHNICAL_ARCHITECTURE.md) → [GAME_DESIGN_DOCUMENT.md](../../GAME_DESIGN_DOCUMENT.md) → [CONTRIBUTING.md](../../CONTRIBUTING.md). Then return here.

---

## Mission
Build **modular, maintainable, well-documented** Godot 4 systems that express the design: exploration, platforming, combat, crafting, equipment, quests, secrets, bosses, environmental interaction — and the headset travel rules that make ENDWORLDS itself.

## Current reality
**No engine project exists.** `game/` is a documentation scaffold; Phase 2 in [ROADMAP.md](../../ROADMAP.md) initialises it. Until then, programming work means: preparing architecture proposals, `tools/` scripts (e.g. manifest validation), and QA checklists — not inventing game code out of sequence.

## Non-negotiable technical rules (master instructions)
1. Godot 4, GDScript-first, 2D. Data-driven over hard-coded.
2. World states persist **independently of beacon registration** — `WorldStateStore` design must not couple persistence to the beacon system.
3. Travel semantics are canon: Random Jump (uncontrolled, all worlds incl. forgotten stay eligible), Beacon Travel (registered worlds only), Dimensional Recall (raises revisit chance for unregistered worlds, **never** guarantees a destination), Home Signal (long-term objective).
4. No unnecessary dependencies or expensive complexity. Justify every addon in its PR (default: zero).
5. Test where possible; report honestly. Untested code is labelled untested (rule 8). Fabricated test results are the fastest way to lose trust in this project.

## Coding standards (working defaults — TECHNICAL_ARCHITECTURE.md §5)
- Static typing everywhere; `snake_case` funcs/vars, `PascalCase` classes.
- Small scenes, composed nodes, signals over hard references.
- Docstrings on public APIs; explain *why*, not *what*.
- One system per PR; docs updated in the same PR (rule 9).

## Definition of done (code PR)
- [ ] Runs in the pinned engine version (once the project exists) — evidence in PR
- [ ] No `.godot/`, export artifacts or editor files committed ([.gitignore](../../.gitignore))
- [ ] New systems documented in TECHNICAL_ARCHITECTURE.md / GDD as applicable
- [ ] QA-visible changes come with test notes in `qa/test-plans/`
- [ ] Scope discipline: unrelated systems untouched (rule 7)

## Out of scope without owner sign-off
Engine version changes, language switches (C#/C++), new addons, changes to canon travel semantics, and anything touching approved narrative content.
