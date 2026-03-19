# Workflow

## Objective

Maintain a reliable, versioned process for extracting and refining Zombicide-related data with a bias toward accuracy, auditability, and incremental improvement.

## Core loop

1. **Ingest source material**
   - rulebooks
   - mission books
   - high-resolution map or tile renders
   - prior extracted data

2. **Extract structured information**
   - mission metadata
   - tile IDs
   - zones
   - doors / objectives / spawn points / special markers
   - line-of-sight and movement-relevant features when available

3. **Verify where possible**
   - confirm from higher-resolution or alternate source views
   - compare against prior successful extraction paths
   - preserve traceability of what is exact vs estimated

4. **Mark uncertainty explicitly**
   - `verified`
   - `partially_verified`
   - `best_effort_unverified`

5. **Integrate into cumulative master set**
   - update instructions if the process improved
   - update state tracking
   - avoid duplicate logic spread across files

6. **Record process improvements**
   - extraction improvements
   - verification improvements
   - naming and schema improvements
   - known limitations and follow-up tasks

## Operating principles

- Prefer exact geometry over inferred geometry.
- When exact verification is not possible, provide best-effort output and label it clearly.
- Preserve intention and accuracy over speed.
- Consolidate repeated instructions into a single authoritative location.
- Keep outputs modular enough for partial replacement.

## Change management

Use small, logical commits.

Suggested commit pattern:

- `docs: refine verification workflow`
- `data: add A47 best-effort geometry`
- `tools: add extraction helper for zone segmentation`
- `prompts: update master bundle instructions`
