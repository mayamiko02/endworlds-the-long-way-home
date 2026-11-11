# assets/production/animations/ — animation frame sequences

## Purpose
Game-ready animation clips as PNG frame sequences, **one folder per clip**:

```
animations/
└── protagonist_run/
    ├── protagonist_run_f0001.png
    ├── protagonist_run_f0002.png
    └── …
```

## Rules (AGENTS.md rule 6)
- The **pivot is identical across every frame of a clip and across every clip of a character** — record the pivot in the manifest `notes`.
- Frame numbering is 4-digit (`_f0001`), timing/fps declared in the manifest entry, dimensions constant within a clip.
- Character clips require the `approved-master` character reference first.

## Contents
Currently empty. First expected set: protagonist idle/run/jump land — Phase 4 (see [ROADMAP.md](../../../ROADMAP.md)).

## Contributing
Manifest category `ANM` — one entry per **clip** with its folder in `file`. Process: [../ASSET_SUBMISSION_GUIDE.md](../../ASSET_SUBMISSION_GUIDE.md).

## Dependencies
Depends on approved production sprites; consumed by Godot `SpriteFrames`/animation import when the engine project exists.
