# QA GUIDE
### Role instructions for QA agents and testers

Read first: [AGENTS.md](../../AGENTS.md) → [CONTRIBUTING.md](../../CONTRIBUTING.md). Then return here.

---

## Mission
Keep the project honest. Verify claims, find what breaks, and make sure nothing undocumented masquerades as done (rule 8: report errors, incomplete work and unsupported assumptions honestly; never fabricate results).

## What can be tested right now (2026-11-11)
There is no build yet. Meaningful QA today is **repository QA**:
- Documentation consistency: do docs contradict each other or the master instructions?
- Manifest validity: `assets/ASSET_MANIFEST.json` is valid JSON; entries match the schema; IDs unique; statuses from the defined lifecycle; referenced files exist on disk.
- Link integrity: relative links in Markdown resolve.
- `.gitignore` coverage: no generated/binary export files tracked.

A script for manifest validation belongs in `tools/` (propose it via PR; do not silently wire CI).

## When the engine exists (Phase 2+)
- Smoke checklist per PR touching gameplay (launch, move, jump, save, reload).
- Canon rule checks: e.g. *world state persists without a beacon*; *Dimensional Recall never guarantees a destination* — these are testable canon, not vibes.
- Environment matrix: record Godot version, OS, hardware in every test report.

## Where work goes
| Artifact | Location | Notes |
|---|---|---|
| Test plans / checklists | `qa/test-plans/` | One file per feature area; keep executable steps |
| Bug reports | `qa/bug-reports/` | One file per issue, template below |
| Automated validators (proposal) | `tools/` | Requires owner sign-off if wired into CI |

## Bug report template
Save as `qa/bug-reports/YYYY-MM-DD_short-title.md`:

```
# Bug: <short title>
- Date: YYYY-MM-DD
- Found by: <name/agent>
- Area: docs | manifest | engine:system | art-pipeline
- Severity: blocker | major | minor | polish
- Status: open
## Environment
- Godot version / OS: (or N/A pre-engine)
## Steps to reproduce
1. …
## Expected
## Actual
## Evidence
- (logs, screenshots, file links)
## Notes / suspected cause
- (label speculation as speculation)
```

## Definition of done (QA PR)
- [ ] Findings reproducible from the written steps alone
- [ ] Honest status: what was verified vs. assumed vs. not run
- [ ] Files in the right folders; index table in `qa/README.md` updated
- [ ] No retconning: failed stays failed until a fix PR passes it
