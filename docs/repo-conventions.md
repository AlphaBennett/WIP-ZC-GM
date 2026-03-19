# Repository Conventions

## Purpose
This document defines how the Zombicide GM repository should be organized and updated.

The repository is the canonical source of truth. ChatGPT outputs are working artifacts that should resolve into repo updates.

---

## General Rules

- Prefer modular, clearly named files
- Avoid duplicate data across files unless intentional and documented
- Keep instructions, workflow notes, and structured data separate
- Prefer structured formats when stability or automation matters
- Prefer concise explanatory notes over long freeform commentary

---

## Verification Standard

All extracted, inferred, or reconstructed data should clearly indicate confidence.

### Allowed labels
- `verified`
- `unverified (best-effort)`

### Usage
Use `verified` when the information has been directly confirmed from a reliable source or clearly observable reference.

Use `unverified (best-effort)` when:
- exact confirmation is not possible
- image quality prevents certainty
- geometry or content must be estimated from available evidence

Best-effort approximations are allowed when necessary, but they must be labeled clearly.

---

## File Update Standard

All ChatGPT-generated repo updates should be delivered as a structured update bundle containing only modified files.

### Required method
Use full file replacement for any changed file.

### Required format
Each changed file should be presented as:

```text
FILE: <path>
ACTION: replace
```

followed by the complete updated file contents.

### Scope rule
Do not resend unchanged files unless explicitly requested.

---

## GitHub Integration Model

This repository is manually updated based on outputs generated in ChatGPT.

### Update method
Changes are applied via:
- full file replacement for changed files
- modular additions for new data
- deletions only when clearly intentional

### Commit guidelines
Use structured commit prefixes where practical:

- `feat:` new data or capability
- `fix:` corrected data or logic
- `refactor:` structural improvements
- `docs:` documentation or instruction updates

Example:

```text
feat: add A47 zone geometry (partial, unverified)
```

### Source attribution
When useful, note:
- extraction method used
- confidence level
- whether approximation was required

---

## ChatGPT Delivery Expectations

Every repo update bundle should include:

1. A short header identifying the repo
2. A list of modified files
3. Full replacement contents for each changed file
4. A suggested commit message
5. The required git commands:
   - `git add`
   - `git commit`
   - `git push`

### Git command standard
Each bundle should include commands in this form:

```bash
git add <modified files>
git commit -m "<type>: <summary>"
git push
```

---

## Data Organization Guidance

### Docs
Store workflow, methodology, and conventions in `/docs`.

### Prompts
Store durable ChatGPT operating instructions and current working state in `/prompts`.

### Data
Store extracted mission, map, tile, and structured outputs in `/data`.

### Tools
Store helper scripts and utilities in `/tools`.

### Changelog
Store notable repository evolution in `/changelog`.

---

## Decision Rule for Ambiguity

When perfect certainty is unavailable:
- preserve intent
- prefer consistency
- record best-effort output
- label uncertainty explicitly

Do not block progress solely because exact verification is unavailable.
