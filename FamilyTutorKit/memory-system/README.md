---
system: family-tutor-kit
version: 0.1.0
component: memory-system
last_updated: 2026-06-14
---

# Memory System

This folder defines the Markdown lifetime learner memory.

## Design Goals

- Agent-parseable Markdown.
- Parent-readable records.
- Local-first storage.
- Multi-learner family support.
- Evidence-first progress tracking.
- Curriculum mapping as an optional layer.
- Durable records that can survive model changes.

## Read These In Order

1. `SPECIFICATION.md`
2. `OPERATING-RULES.md`
3. `LIFETIME-MAINTENANCE.md`
4. `templates/`

## Memory Files Per Learner

Each learner folder contains:

| File | Purpose |
| --- | --- |
| `00-profile.md` | Durable learner context. |
| `01-learning-map.md` | Current skill state by subject and domain. |
| `02-evidence-log.md` | Append-only evidence from sessions. |
| `03-review-queue.md` | Spaced review and retention checks. |
| `04-goals.md` | Parent, learner, and school goals. |
| `05-session-reports.md` | Parent-readable session summaries. |
| `06-curriculum-links.md` | Optional curriculum mappings. |
