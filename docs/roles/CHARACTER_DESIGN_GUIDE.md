# CHARACTER DESIGN GUIDE
### Role instructions for character designers and character art agents

Read first: [AGENTS.md](../../AGENTS.md) → [PROJECT_BIBLE.md](../../PROJECT_BIBLE.md) (canon facts) → [ART_BIBLE.md](../../ART_BIBLE.md) (specs) → [assets/ASSET_SUBMISSION_GUIDE.md](../../assets/ASSET_SUBMISSION_GUIDE.md). Then return here.

---

## Mission
Define and protect the visual identity of the protagonist, alternate protagonists and supporting characters — **consistency is the job**.

## The protagonist (CANON)
- Young Zambian man, ~19–23. Appearance fixed across **all** artwork, animations, illustrations and scenes.
- The **approved character reference is the definitive visual source.** No such reference exists in the manifest yet — the first approved one becomes it, and everything after answers to it.
- Present Zambian identity with authenticity and respect; details (style, grooming, clothing, manner) grounded and personal, never costume-like (rule 2).

## Alternate protagonists (CANON)
Alternate versions are central to the long-term mystery. Their designs must be visually traceable to the same person while reading as distinct lives. **Their identities, motivations and histories must stay consistent with established lore** (rule 3) — coordinate every alternate design with PROJECT_BIBLE.md, and treat unrevealed lore as owner-gated.

## Deliverables for a complete character
| Piece | Folder | Notes |
|---|---|---|
| Turnaround (front / side / back / ¾) | `assets/concept-art/characters/` | Candidate for `approved-master` once ratified |
| Expression sheet | `assets/concept-art/characters/` | Range honest to the character, not stock emoji |
| Proportion & pivot sheet | `assets/concept-art/characters/` | Heights in heads, limb ratios, joint pivot points for animators |
| Palette swatches | `assets/concept-art/characters/` | Skin, hair, clothing in light/shadow — sRGB values noted |
| (Later) Production sprite set | `assets/production/sprites/characters/` | Only after the reference is `approved-master` and engine specs exist |

## Rules when designing
1. **Check the index first** — a character may already exist or be in review. Extend, never duplicate (rule 1).
2. Proportions, pivots, dimensions, transparency and lighting must stay consistent across every piece of the same character (rule 6).
3. Production sprites only after owner approval of the reference; never mark your own work engine-ready (rule 6) — validation is recorded in review.
4. New characters are **PROPOSAL** until the owner approves; keep the label visible in the file notes and manifest entry.
5. Never overwrite `approved-master` files; version up (`_v02`) and set the old entry per the status lifecycle.

## Definition of done (character PR)
- [ ] All deliverable pieces present or explicitly deferred with reason
- [ ] Pivot/proportion sheet lets an animator work without guessing
- [ ] Manifest entries complete; branch is `art/…`; PR template checklist complete
- [ ] Lore-sensitive elements cross-checked against PROJECT_BIBLE.md
