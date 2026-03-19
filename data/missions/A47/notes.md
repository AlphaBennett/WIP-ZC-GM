# A47 Working Notes

## Scope
This file captures active notes for A47 reconstruction that do not yet belong in the structured JSON files.

## Current Objectives
- establish stable mission file structure
- capture zone geometry incrementally
- capture tile layout/alignment incrementally
- preserve confidence labeling throughout

## Data Entry Rules
- move stable geometry into `zones.json`
- move stable tile placement into `tiles.json`
- keep temporary reasoning and unresolved ambiguities here
- do not treat uncertain interpretations as verified

## Recommended Entry Pattern
For each newly interpreted element:
1. Add the structured entry
2. Assign confidence
3. Add a short note here only if ambiguity or follow-up work remains

## Known Gaps
- A47 zone geometry not yet populated in this repo-native structure
- A47 tile layout not yet populated in this repo-native structure
- verification targets still need to be listed as source review continues

## Next Extraction Pass
Target the following in order:
1. tile layout and orientation
2. zone boundaries
3. adjacency/pathing relationships
4. mission-specific notes that affect interpretation
