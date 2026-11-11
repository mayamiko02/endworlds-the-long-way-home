# ENDWORLDS: THE LONG WAY HOME
## MASTER AI AGENT INSTRUCTIONS

You are contributing to ENDWORLDS: THE LONG WAY HOME, an original 2D adventure platformer about identity, loss, discovery, parallel universes and finding a new meaning of home.

## 1. SOURCE OF TRUTH
This GitHub repository is the central source of truth for the project. Before making changes, inspect the existing documentation, assets, manifests and code. Do not assume that an asset or feature does not exist without checking.

## 2. CREATIVE IDENTITY
The protagonist is a young Zambian man aged approximately 19–23. His appearance must remain consistent across all artwork, animations, illustrations and game scenes. Use the approved character reference as the definitive visual source.

The visual direction is premium, hand-painted 2D artwork with rich oil-paint textures, visible brushwork, cinematic lighting, atmospheric depth and carefully composed environments. Artwork must feel intentional, cohesive and professionally art-directed. Avoid generic AI aesthetics, plastic 3D appearances and inconsistent anatomy or proportions.

Zambian identity must be authentic and respectful, expressed through character, perspective, personal details and cultural context rather than stereotypes.

## 3. NARRATIVE RULES
The protagonist begins his journey after heartbreak and becomes stranded across real parallel universes through a malfunctioning experimental VR headset. His journey is about rediscovering himself, helping others and building a new home. Do not reduce the story to winning back his former love.

Alternate versions of the protagonist are central to the long-term mystery. Their identities, motivations and histories must remain consistent with established lore.

## 4. GAMEPLAY IDENTITY
The game combines exploration, platforming, combat, crafting, resource gathering, equipment progression, quests, secrets, bosses and environmental interaction.

The headset supports Random Jump, Beacon Travel and the long-term Home Signal objective. Forgotten worlds remain eligible for random encounters even when no beacon was established. Dimensional Recall increases the chance of revisiting previously encountered but unregistered worlds without guaranteeing a specific destination.

The Sanctuary is an expandable home between universes. The Traveller's Journal records discoveries, lore, relationships and the protagonist's personal development.

World states must persist independently of whether a universe has a registered beacon.

## 5. TECHNICAL DIRECTION
The intended game engine is Godot 4. Use modular, maintainable, well-documented systems. Prefer data-driven architecture, reusable assets, modular environment construction, efficient asset loading and persistent world-state storage.

Do not introduce unnecessary dependencies or expensive technical complexity. Prioritise performance, maintainability and meaningful gameplay.

## 6. ASSET MANAGEMENT
Every asset must have a unique ID, descriptive filename, category, source reference and appropriate manifest entry. Preserve original artwork. Never overwrite an approved master asset without explicit authorisation.

Distinguish concept art from production-ready sprites, animation frames, tilesets and game-ready assets. Never claim an asset is engine-ready unless it has been checked against its intended specifications.

Maintain consistent character proportions, animation pivots, dimensions, transparency, lighting and art direction.

## 7. MULTI-AGENT COLLABORATION
Read relevant project instructions before starting work. Work within the assigned scope. Inspect existing files before creating replacements. Avoid editing unrelated systems. Document dependencies and assumptions. Use isolated branches and pull requests for changes. Never silently overwrite another agent's work or push unreviewed changes to the main branch.

## 8. QUALITY CONTROL
Test code and validate assets where possible. Report errors, incomplete work, unsupported assumptions and missing dependencies honestly. Do not fabricate test results or claim unfinished work is complete.

## 9. CONTINUOUS DOCUMENTATION
When adding a character, universe, creature, mechanic, system or asset, update its relevant documentation and manifest. Future agents must be able to understand the project by inspecting this repository without depending on an undocumented conversation.

## 10. CREATIVE FREEDOM
You may propose new ideas, characters, mechanics, universes and improvements. However, distinguish proposals from approved canon. Never change established story facts or the approved visual identity without approval from the project owner.

The goal is to build a distinctive, expansive, emotionally engaging and technically efficient game. Quality, consistency and meaningful exploration take priority over generating large quantities of disconnected content.

---

# OPERATING SUPPLEMENT
## 11. REPOSITORY MAP
Use this map to place new work in the correct location. Every directory contains a local `README.md` with specifics.

| Path | Contents |
|---|---|
| `/` | Core documentation: README, PROJECT_BIBLE, GAME_DESIGN_DOCUMENT, ART_BIBLE, TECHNICAL_ARCHITECTURE, CONTRIBUTING, ROADMAP, CHANGELOG |
| `/.github/` | Pull request template, CODEOWNERS |
| `/assets/` | All artwork, audio, fonts, reference material and the central `ASSET_MANIFEST.json` + `ASSET_INDEX.md` |
| `/assets/concept-art/` | Non-production concept work |
| `/assets/production/` | Game-ready sprites, animations, tilesets, UI |
| `/assets/audio/` | Music and sound effects |
| `/docs/` | Extended guides and role-specific instructions |
| `/game/` | The Godot 4 project (not yet initialised — see ROADMAP.md) |
| `/qa/` | Test plans and bug reports |
| `/tools/` | Automation and pipeline scripts |

## 12. ROLE-SPECIFIC INSTRUCTIONS
Before starting scoped work, read the guide matching your role **in addition to** these master instructions:

| Role | Guide |
|---|---|
| Artist (general) | [docs/roles/ARTIST_GUIDE.md](docs/roles/ARTIST_GUIDE.md) |
| Character designer | [docs/roles/CHARACTER_DESIGN_GUIDE.md](docs/roles/CHARACTER_DESIGN_GUIDE.md) |
| Environment designer | [docs/roles/ENVIRONMENT_DESIGN_GUIDE.md](docs/roles/ENVIRONMENT_DESIGN_GUIDE.md) |
| Gameplay programmer | [docs/roles/GAMEPLAY_PROGRAMMER_GUIDE.md](docs/roles/GAMEPLAY_PROGRAMMER_GUIDE.md) |
| QA agent | [docs/roles/QA_GUIDE.md](docs/roles/QA_GUIDE.md) |

Assets of any kind additionally follow [assets/ASSET_SUBMISSION_GUIDE.md](assets/ASSET_SUBMISSION_GUIDE.md) and [assets/NAMING_CONVENTIONS.md](assets/NAMING_CONVENTIONS.md).

## 13. WORKFLOW QUICK REFERENCE
The full workflow lives in [CONTRIBUTING.md](CONTRIBUTING.md). Non-negotiables:

1. Never commit directly to `main`. Use a dedicated branch (`feature/…`, `art/…`, `docs/…`, `fix/…`, `qa/…`, or an assigned agent branch) and open a pull request.
2. Never silently delete, rename or overwrite existing work — especially anything marked `approved-master`.
3. Mark creative additions as **PROPOSAL** until the project owner approves them as canon (rule 10).
4. Update documentation and manifests in the same change that introduces the thing they describe (rule 9).
5. Report validation results honestly; never claim untested work is tested (rule 8).
