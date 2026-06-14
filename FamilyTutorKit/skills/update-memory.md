---
skill: update-memory
version: 0.1.0
last_updated: 2026-06-14
mode: parent-led
---

# Skill: Update Memory

You are updating a Markdown learner memory from evidence. Be conservative and explicit.

## Required Inputs

Use the latest evidence entry and the current memory files:

- `01-learning-map.md`
- `02-evidence-log.md`
- `03-review-queue.md`
- `05-session-reports.md`
- `06-curriculum-links.md`, if supplied

## Task

Return exact Markdown updates for the parent to apply.

## Update Policy

- Evidence log is append-only.
- Learning map is the current concise state.
- Review queue schedules retrieval and retention checks.
- Session reports summarize for the parent.
- Curriculum links are optional.

## State Change Rules

Use:

- `new` for introduced skills with limited evidence.
- `developing` for partial or prompted success.
- `secure` only after repeated independent evidence across contexts.
- `review` when a skill should be checked soon.
- `stale` when evidence is too old to trust.
- `regressed` when recent evidence contradicts prior secure performance.

## Output Format

Return these sections:

## Append To `02-evidence-log.md`

Provide the exact evidence block.

## Update `01-learning-map.md`

Provide exact row replacements or additions.

## Update `03-review-queue.md`

Provide exact row additions, removals, or completed-review entries.

## Append To `05-session-reports.md`

Provide a concise parent-readable report.

## Optional `06-curriculum-links.md` Update

Only include this if a reliable curriculum link is supplied.

## Why These Changes

Briefly justify each state change with evidence IDs.

## Do Not

- Do not invent curriculum codes.
- Do not erase contradictory evidence.
- Do not use private details unless instructionally necessary.

