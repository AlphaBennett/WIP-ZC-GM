# Zombicide GM System (WIP)

Repository: https://github.com/AlphaBennett/WIP-ZC-GM

## Purpose
This repository is the single source of truth for the Zombicide Game Master system.

It contains:
- Structured mission and map data
- Extraction and verification workflows
- Helper tooling and prompts
- Iterative refinements to process and outputs

All substantial work performed in ChatGPT should resolve into updates for this repository.

---

## Core Principles

1. **Repository is authoritative**
   - This repo is the canonical working location
   - External bundles are delivery mechanisms, not the final source of truth

2. **Deterministic structure**
   - Data should be organized, modular, and reusable
   - Prefer structured files over ad hoc notes

3. **Verification-aware data**
   - Extracted or inferred data must distinguish between:
     - `verified`
     - `unverified (best-effort)`

4. **Continuous refinement**
   - Workflows, prompts, and helper methods should improve over time
   - Process updates should be captured in `/docs` and `/prompts`

5. **Modified-files-only delivery**
   - ChatGPT update bundles should include only files that changed
   - Changed files should be delivered as full file replacements

---

## Standard ChatGPT Update Workflow

1. Extract, interpret, or refine data
2. Validate where possible
3. Mark uncertainty clearly where exact verification is not possible
4. Integrate changes into the repo structure
5. Deliver a modified-files-only update bundle
6. Commit and push to the repository

---

## Update Bundle Standard

Each ChatGPT repo update should include:

- A concise list of modified files
- Full replacement contents for each changed file
- A suggested commit message
- The required git commands:
  - `git add`
  - `git commit`
  - `git push`

Unchanged files should not be resent unless explicitly requested.

---

## Current Focus

- A47 map extraction and zone-level geometry
- Improving high-resolution interpretation workflow
- Reducing ambiguity in tile interpretation
- Standardizing helper tooling and repo conventions

---

## Folder Overview

- `/docs` → methodology, rules, and repo conventions
- `/data` → extracted structured content
- `/tools` → scripts and helpers
- `/prompts` → ChatGPT instruction/state files
- `/changelog` → change history

---

## Status

Work in progress.  
Primary development occurs through ChatGPT-assisted iteration, with this repository serving as the canonical destination for accepted changes.
