# ROADMAP
### ENDWORLDS: THE LONG WAY HOME

> Phased plan from repository scaffold to playable game. Dates are targets, not promises; scope beats schedule. Creative phases require owner approval of canon before production begins (AGENTS.md rule 10).

**Current phase: Phase 0 (completing).**

---

## Phase 0 — Repository foundation ✅ (this scaffolding PR)

**Goal:** source of truth established; every future contributor can navigate the repo alone.
- [x] Directory scaffold with READMEs in every meaningful directory
- [x] Core documentation set (bibles, GDD, architecture, contributing, roadmap, changelog)
- [x] Asset manifest, index, naming conventions, submission guide
- [x] Role-specific instructions (artist / character / environment / programmer / QA)
- [x] Branch/PR/review/merge guidelines and PR template

**Exit criteria:** PR reviewed and merged by owner.

## Phase 1 — Canon & pre-production (next)

**Goal:** ratify the creative foundation so art and code can start without rework.
- [ ] Owner answers PROJECT_BIBLE.md open questions (Q1–Q6) or delegates as proposals
- [ ] Protagonist name/backstory approved
- [ ] First protagonist character reference produced and approved → status `approved-master`
- [ ] Master palette + first universe concept keys approved
- [ ] Control scheme proposal reviewed (GDD §10)
- [ ] Decide licence for repository content

**Exit criteria:** approved character reference + approved first-world concept keys in the manifest.

## Phase 2 — Engine foundation

**Goal:** a Godot 4 project exists and runs a greybox movement prototype.
- [ ] Initialise `game/` (create `project.godot`, pin engine version, folder layout per TECHNICAL_ARCHITECTURE.md)
- [ ] Player controller greybox (run/jump/climb) with programmer-art placeholder — clearly labelled, never confused with real assets
- [ ] Save slot + `WorldStateStore` skeleton
- [ ] First automated smoke checks (QA guide)

**Exit criteria:** prototype build launches; greybox character moves on test platforms; persistence round-trips.

## Phase 3 — Travel prototype

**Goal:** the headset loop is real.
- [ ] `JumpService`: Random Jump over a table of placeholder worlds
- [ ] Beacon registration + Beacon Travel between two test universes
- [ ] World-state persistence verified across jumps without beacons (canon rule)
- [ ] Dimensional Recall weighting implemented per canon (chance ↑, no guarantee)

**Exit criteria:** jump → play → return → state persisted, demonstrated in a recorded test.

## Phase 4 — First playable slice

**Goal:** one hand-painted world, end-to-end.
- [ ] World 01 production art (tileset + layered background) from approved concepts
- [ ] Protagonist production sprite set + core animation set from approved reference
- [ ] One questline, one boss, crafting loop with world resources
- [ ] Journal v1 (discoveries + entries)

**Exit criteria:** 15–30 minute slice playable by the owner; QA pass logged in `qa/`.

## Phase 5 — Home systems

**Goal:** Sanctuary and Home Signal close the loop.
- [ ] Sanctuary hub + expansion + stations
- [ ] Home Signal progression and its narrative milestones (canon-gated)
- [ ] Relationship tracking surfaced in Journal

## Phase 6+ — Expansion

Second and third worlds, alternates mystery content (owner-gated), audio production (music/SFX), accessibility pass, performance pass, platform export decisions.

---

## Outstanding issues (as of 2026-11-11)

| # | Issue | Blocking |
|---|---|---|
| 1 | No licence chosen for the repo | Public release |
| 2 | No approved protagonist reference exists; production art cannot start | Phases 1, 4 |
| 3 | Canon open questions Q1–Q6 unanswered | Phases 1, 5 |
| 4 | No Godot version pinned / engine not installed in CI | Phase 2 |
| 5 | CODEOWNERS assumes owner handle `mayamiko02` — confirm or correct | Reviews |
| 6 | Branch protection for `main` not verified in repo settings | Merge discipline |
