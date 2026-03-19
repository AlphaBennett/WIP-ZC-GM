# Repo Conventions

## Naming

- Mission files: `mission-<id>.json` or `mission-<id>.md`
- Tile files: `tile-<id>.json`
- Map geometry files: `map-<id>-geometry.json`
- Notes files: `mission-<id>-notes.md`

## Content rules

- Keep instructions centralized under `prompts/`.
- Keep process documentation under `docs/`.
- Keep structured extraction outputs under `data/`.
- Keep executable helpers under `tools/helpers/`.

## Schema preference

Prefer stable keys and explicit status fields.

Recommended fields:
- `id`
- `source`
- `source_status`
- `confidence`
- `notes`
- `last_reviewed`

## Versioning

Use append-only notes in the changelog for major workflow changes.

## Commit hygiene

- one logical change per commit
- clear scope in commit subject
- avoid mixing docs, data, and tooling unless tightly related
