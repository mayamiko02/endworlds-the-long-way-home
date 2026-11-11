# qa/ — quality assurance

## Purpose
Test plans, checklists and bug reports for ENDWORLDS. Operates under [docs/roles/QA_GUIDE.md](../docs/roles/QA_GUIDE.md); the golden rule is AGENTS.md rule 8 — report honestly, never fabricate results.

## Contents
| Subdirectory | Holds |
|---|---|
| [test-plans/](test-plans/README.md) | Executable checklists per feature area |
| [bug-reports/](bug-reports/README.md) | One Markdown file per bug, from the guide's template |

## Current testable surface (2026-11-11)
No build exists. Active QA areas: documentation consistency, manifest JSON validity, ID uniqueness, link integrity, `.gitignore` coverage — see the QA guide.

## Test & bug registers
| Plan / Report | Area | Status |
|---|---|---|
| — | *none filed yet* | |

(Keep this register updated in the same PR as the plan/report it lists.)

## Contributing
Branches `qa/…`, PR per [CONTRIBUTING.md](../CONTRIBUTING.md).

## Dependencies
None today; engine builds become a dependency from Phase 2 onward.
