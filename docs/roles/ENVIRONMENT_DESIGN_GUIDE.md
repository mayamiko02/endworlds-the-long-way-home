# ENVIRONMENT DESIGN GUIDE
### Role instructions for environment designers and environment art agents

Read first: [AGENTS.md](../../AGENTS.md) → [GAME_DESIGN_DOCUMENT.md](../../GAME_DESIGN_DOCUMENT.md) (world model) → [ART_BIBLE.md](../../ART_BIBLE.md) (specs) → [assets/ASSET_SUBMISSION_GUIDE.md](../../assets/ASSET_SUBMISSION_GUIDE.md). Then return here.

---

## Mission
Build the Endworlds: **carefully composed, atmospheric, hand-painted environments** with real depth — places that feel lived-in and emotionally tuned, never procedural backdrops.

## Visual mandate (CANON, ART_BIBLE.md §1/§3)
- Rich oil-paint texture, visible brushwork, cinematic lighting, atmospheric depth.
- Depth through layered value and light — plan foreground/midground/background (parallax layers) from the first sketch.
- Each universe needs a coherent identity: palette script + brush language registered as concept art before production begins.

## From concept to production
1. **Concept phase** (`assets/concept-art/environments/`): mood keys, composition studies, palette scripts. Loose is fine; labelled as concept.
2. **Production phase** (`assets/production/tilesets/`, `assets/production/…`): only after the world's concepts are approved *and* engine specs are ratified (tile grid, PPU — currently TBD in ART_BIBLE.md §5).
3. Modular construction is a core technical value (rule 5): design sets that recombine — tiles, props, layer cards — instead of one-off mega-paintings that can't be reused.

## World-state awareness
Worlds persist and change (GDD §8; canon persistence rule). Design environments so states can differ: intact/destroyed props, weather variants, unlocked routes. Note intended state variants in the concept's manifest `notes` so programmers can plan for them.

## Rules
1. Check the index and manifest before inventing a world or location (rule 1).
2. Consistent lighting direction and scale across all pieces of one world (rule 6).
3. Never claim production tilesets engine-ready until validated against the ratified specs (rule 6).
4. New universes/locations are **PROPOSAL**-labelled until owner-approved; universe canon is tracked in PROJECT_BIBLE.md.
5. Version up, never overwrite `approved-master`.

## Definition of done (environment PR)
- [ ] Concept includes palette script for the location
- [ ] Parallax/mood intent documented in manifest notes
- [ ] For production: tile grid + pivot/origin conventions respected, specs validated and listed in the PR
- [ ] Manifest entries complete; docs updated in the same PR
