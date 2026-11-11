# ART BIBLE
### ENDWORLDS: THE LONG WAY HOME

> **Purpose:** the visual direction and quality bar for every image, animation and scene in the game.
> Canon visual rules come from [AGENTS.md](AGENTS.md) rule 2 and rule 6; everything else here is working guidance or **PROPOSAL** until the owner ratifies it.

---

## 1. North star — CANON

**Premium, hand-painted 2D artwork.** Rich oil-paint textures, visible brushwork, cinematic lighting, atmospheric depth, carefully composed environments. Every asset must feel intentional, cohesive and professionally art-directed.

### Never acceptable — CANON
- Generic "AI look" output (smoothed, weightless, texture-free rendering).
- Plastic or pseudo-3D appearance.
- Inconsistent anatomy, proportions or lighting between pieces of the same subject.
- Stereotyped depiction of Zambian identity.

## 2. The protagonist — CANON

- Young Zambian man, approximately 19–23.
- His appearance is **locked** across artwork, animations, illustrations and game scenes.
- The **approved character reference is the definitive visual source**. Until such a reference exists in `assets/` and is marked `approved-master` in the manifest, no production character art may be approved — concept exploration only.
- Required reference set (submission target, see [docs/roles/CHARACTER_DESIGN_GUIDE.md](docs/roles/CHARACTER_DESIGN_GUIDE.md)): turnaround, expression sheet, proportion/pivot sheet, palette swatches.

## 3. Environments — CANON (direction) + PROPOSAL (application)

- CANON: composed, atmospheric, painterly; depth through layered value and light, not noise.
- PROPOSAL: each universe gets a distinct but related painterly identity (palette script + brush language); parallax layer plans defined per world; environments built modularly for tileset production — see [docs/roles/ENVIRONMENT_DESIGN_GUIDE.md](docs/roles/ENVIRONMENT_DESIGN_GUIDE.md).

## 4. Palettes & lighting — PROPOSAL

- Master palette: TBD once concept phase produces approved keys.
- Rule of intent: light carries emotion — the Sanctuary warm and safe; unknown worlds colder/harder until understood.
- Per-world palette scripts must be registered as concept assets before production tilesets begin.

## 5. Technical art specifications — WORKING DEFAULTS (to be ratified with the engine project)

| Spec | Default | Notes |
|---|---|---|
| Format | PNG (lossless, alpha) for sprites/tiles; source PSD/KRA/Aseprite preserved alongside | Master rule 6: preserve original artwork |
| Colour | sRGB, 8-bit RGBA | |
| Sprite dimensions | Powers-of-two friendly, consistent per asset class; exact grid TBD with first tileset | |
| Animation pivots | **Consistent across every frame of a clip and across clips of a character** (rule 6) — document pivot in the manifest `notes` | |
| Transparency | Clean alpha edges; no baked drop shadows on sprites unless intentional and consistent | |
| Scale | Fixed pixels-per-unit across all production art (value TBD with engine setup — proposal: 100 PPU) | |
| Export | Textures ≤ 4096²; atlases assembled at import, not hand-flattened | |

**Never claim an asset is engine-ready until it has been validated against this table** (rule 6) — that validation happens in review and is recorded in the manifest entry.

## 6. Concept vs production — CANON distinction

- **Concept art** (`assets/concept-art/`): exploration, pitch, reference. May be loose. Clearly labelled; never ships in-game.
- **Production assets** (`assets/production/`): game-ready sprites, animation frames, tilesets, UI. Held to §5 and the character consistency rule.
- The manifest `category` encodes this distinction; statuses track the approval journey (see [assets/ASSET_SUBMISSION_GUIDE.md](assets/ASSET_SUBMISSION_GUIDE.md)).

## 7. Review & approval

Art approvals follow the manifest status lifecycle (`proposed → in-review → changes-requested → approved → approved-master`). The owner is the final art director. `approved-master` files are immutable without explicit authorisation.
