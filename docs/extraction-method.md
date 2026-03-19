# Extraction Method

## Goal

Convert source pages or renders into structured, reusable map / mission data.

## Preferred extraction order

1. Mission-level metadata
2. Tile layout
3. Zone boundaries
4. Doors and barricades
5. Objectives / spawn points / tokens
6. Text rules or mission-specific exceptions
7. Validation pass against visual source

## Geometry guidance

### Exact extraction

Use when the source render is sufficiently sharp to support confident boundary placement.

Characteristics:
- clear zone borders
- identifiable room / street segmentation
- distinguishable token placement
- stable alignment with prior known tile geometry

### Best-effort extraction

Use when exact confirmation is not possible but a useful approximation can still be produced.

Requirements:
- preserve likely topology
- avoid false claims of certainty
- annotate uncertain boundaries or object placement
- retain enough structure for later refinement

Suggested status labels:
- `verified`
- `estimated_from_high_res`
- `estimated_from_low_res`
- `unverified_guess`

## Recommended data shape

Use machine-friendly, human-readable formats such as JSON or YAML.

Example:

```json
{
  "mission_id": "A47",
  "source_status": "best_effort_unverified",
  "tiles": [],
  "zones": [],
  "objects": [],
  "notes": []
}
```

## Validation checklist

- Does the zone count match the visible source?
- Are exterior and interior segments logically separated?
- Are doors aligned to zone boundaries?
- Are special markers mapped to plausible zones?
- Are assumptions called out explicitly?
