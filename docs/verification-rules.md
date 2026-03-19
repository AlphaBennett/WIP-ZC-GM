# Verification Rules

## Status definitions

### verified

Use only when the relevant detail is directly supported by the source with high confidence.

### partially_verified

Use when some elements are directly supported but one or more details remain inferred.

### best_effort_unverified

Use when the structure is a reasoned approximation but cannot be confirmed from the available source.

## Required behavior

- Never present inferred geometry as confirmed fact.
- Prefer a useful approximation over omission when the approximation is clearly labeled.
- Preserve unknowns for later revision instead of hiding them.
- When a higher-resolution render becomes available, re-check prior assumptions before carrying them forward.

## Comparison against prior solutions

When a previous extraction path exists:

1. compare topology
2. compare tile arrangement
3. compare zone counts
4. compare object placement
5. keep the stronger method
6. document meaningful differences

## Disagreement handling

If sources or methods disagree:
- keep the most defensible structure as primary
- record the alternate interpretation in notes
- mark unresolved details as uncertain
