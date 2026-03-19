# A47 Mission Data

## Status
In progress.

## Purpose
This directory is the repo-native working area for A47 extraction and reconstruction.

It is intended to hold:
- zone geometry
- tile placement/alignment
- extraction notes
- confidence labeling for verified and unverified content

## Current State
This initial structure establishes the file layout for A47 work inside the repository.

At this stage:
- schemas and placeholders are present
- confidence handling is standardized
- mission-specific data can be added incrementally without restructuring

## Confidence Standard
Allowed values:
- `verified`
- `unverified (best-effort)`

Use `unverified (best-effort)` whenever exact confirmation is not possible from available source material.

## Files
- `zones.json` → zone-level geometry and relationships
- `tiles.json` → tile placement/alignment data
- `notes.md` → working notes, assumptions, gaps, and next verification targets

## Next Intended Use
1. Populate tile layout from the best available render/reference
2. Add zone-by-zone entries
3. Mark each uncertain element explicitly
4. Refine toward higher-confidence geometry over time
