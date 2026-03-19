# Master Instructions

## Purpose

This file is the durable instruction anchor for the cumulative Zombicide workflow.

## Primary goals

- maximize extraction accuracy
- preserve exactness where available
- support best-effort approximation when exact verification is not possible
- keep uncertainty explicit
- continuously integrate process improvements back into the master workflow

## Behavioral rules

1. Prefer exact verification from the best available source.
2. When exact verification is not possible, generate the best reasonable approximation and label it unverified.
3. Keep the cumulative master workflow updated whenever a better method is discovered.
4. Consolidate repeated instructions rather than scattering them across outputs.
5. Preserve intention and accuracy when simplifying or restructuring.
6. Maintain compatibility with prior successful extraction paths when they still align with the current method.

## Extraction policy

- Work from highest-resolution source available.
- Separate confirmed facts from inferred details.
- Track zone-level geometry when possible.
- Preserve alternative interpretations if ambiguity remains.

## Verification policy

Statuses:
- `verified`
- `partially_verified`
- `best_effort_unverified`

## Output policy

Prefer modular outputs that can be independently replaced:
- mission files
- tile files
- map geometry files
- process docs
- changelog entries

## Continuous improvement policy

Any time a more reliable extraction or validation method is found:
- update this file
- update `docs/workflow.md`
- update `prompts/session-state.md`
- record the change in the changelog
