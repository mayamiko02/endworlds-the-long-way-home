# tools/ — automation & pipeline scripts (PLANNED)

## Purpose
Repository automation that supports the project but is not game code: validators, generators, batch exporters.

## Contents
Currently empty. Proposed first tools (open PRs to implement):
| Tool | Job |
|---|---|
| `validate_manifest.py` | Check `assets/ASSET_MANIFEST.json`: valid JSON, unique IDs, known categories/statuses, referenced files exist, index in sync |
| `check_links.py` | Verify relative Markdown links resolve |

## Rules
- Language: Python 3 standard library only, unless a dependency is justified in the PR (AGENTS.md rule 5 — no unnecessary dependencies).
- Tools are honest: exit non-zero on failure, print what failed, never silently "fix" tracked files.
- Caches (`__pycache__/`, `.pytest_cache/`) are git-ignored — do not commit them.
- If a tool should run in CI, that's an owner decision recorded in a PR (see [ROADMAP.md](../ROADMAP.md) outstanding issue #4).

## Contributing
Branches `feature/tools-…`, PR per [CONTRIBUTING.md](../CONTRIBUTING.md). Add a row to the table above in the same PR.

## Dependencies
Python 3.10+ (only when tools exist).
