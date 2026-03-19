# Zombicide Project

Repository scaffold for maintaining a durable, version-controlled working set for ChatGPT-assisted Zombicide extraction, verification, and bundle generation.

## Purpose

This repo is meant to become the persistent source of truth for:

- master operating instructions
- extraction and verification workflow
- mission / tile / map data
- helper scripts and utilities
- changelog and task tracking

## Recommended workflow

1. Keep `prompts/master-instructions.md` as the primary behavioral guide.
2. Keep `prompts/session-state.md` updated with current progress, assumptions, and next actions.
3. Store structured outputs under `data/`.
4. Store repeatable utilities under `tools/helpers/`.
5. Record important process changes in `changelog/CHANGELOG.md`.

## Current state

This scaffold is designed around an iterative Zombicide map / mission extraction workflow, including exact verification when possible and best-effort estimated geometry when exact verification is not possible.

## Folder layout

```text
zombicide-project/
  README.md
  docs/
    workflow.md
    extraction-method.md
    verification-rules.md
    repo-conventions.md
  data/
    maps/
      README.md
    missions/
      README.md
    tiles/
      README.md
  tools/
    helpers/
      README.md
  prompts/
    master-instructions.md
    session-state.md
  changelog/
    CHANGELOG.md
```

## Git setup suggestion

```bash
git init
git add .
git commit -m "Initial Zombicide project scaffold"
```

## Suggested next commits

1. Add current cumulative master bundle content into `prompts/` and `docs/`.
2. Add extracted mission artifacts under `data/missions/`.
3. Add map / tile geometry outputs under `data/maps/` and `data/tiles/`.
4. Add helper utilities under `tools/helpers/`.
