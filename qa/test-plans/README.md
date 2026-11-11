# qa/test-plans/ — test plans & checklists

## Purpose
Executable, step-by-step verification for project features — written so anyone (human or agent) can reproduce results identically.

## Contents
Currently empty. Suggested first plans:
- `repository_integrity.md` — manifest validity, link checks, naming conformance (executable today)
- `greybox_movement.md` — Phase 2 player controller smoke checklist (once the engine project exists)

## Format
One file per feature area: `YYYY-MM-DD_area.md` for dated passes, or `area.md` for living checklists. Include: scope, prerequisites, exact steps, expected results, pass/fail evidence, environment (Godot version/OS once relevant).

## Canon-derived test cases worth planning early
- World state persists when the universe has **no** registered beacon (AGENTS.md rule 4).
- Dimensional Recall raises revisit chance but can **never** force a destination.
- Travel table always includes forgotten worlds.

## Contributing
[docs/roles/QA_GUIDE.md](../../docs/roles/QA_GUIDE.md). Update the register in [../README.md](../README.md) in the same PR.

## Dependencies
The feature being tested; otherwise none.
