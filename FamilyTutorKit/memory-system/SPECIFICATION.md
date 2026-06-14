---
system: family-tutor-kit
version: 0.1.0
component: memory-specification
last_updated: 2026-06-14
---

# Lifetime Learner Memory Specification

This specification defines an all-Markdown memory system for a student's lifetime learning record.

The memory is agent-first: files are structured enough for an AI to parse reliably. It is still parent-readable and editable.

## Storage Model

One family vault can hold many learners.

```text
learners/
  child-folder/
    00-profile.md
    01-learning-map.md
    02-evidence-log.md
    03-review-queue.md
    04-goals.md
    05-session-reports.md
    06-curriculum-links.md
    archive/
```

The child folder name should not expose unnecessary private information if the vault may ever be synced.

Recommended folder names:

- `ava-2017`
- `learner-a`
- `child-001`

Avoid:

- full legal names
- school names
- medical details

## File Rules

Every memory file must:

- be Markdown
- start with YAML frontmatter
- use ISO dates such as `2026-06-14`
- keep unknown values as `unknown`
- keep headings stable
- preserve append-only logs unless correcting a factual mistake

## Required Frontmatter

Each learner memory file uses this minimum frontmatter:

```yaml
---
memory_file: 00-profile
learner_id: learner-a
learner_display_name: unknown
version: 0.1.0
last_updated: 2026-06-14
privacy: private
---
```

## Stable IDs

Use stable IDs so models and tools can connect evidence across files.

| ID Type | Format | Example |
| --- | --- | --- |
| Learner | short stable slug | `learner-a` |
| Skill | subject-domain-sequence | `maths-fractions-001` |
| Evidence | date plus short sequence | `2026-06-14-001` |
| Session | date plus short sequence | `session-2026-06-14-001` |
| Goal | year plus sequence | `goal-2026-001` |

Do not rename IDs after evidence has been recorded.

## Skill State Vocabulary

Use these states in `01-learning-map.md`.

| State | Meaning |
| --- | --- |
| `new` | Introduced but not enough evidence yet. |
| `developing` | Some success, but still needs support or review. |
| `secure` | Reliable independent performance across more than one context. |
| `review` | Previously learned and due for retrieval practice. |
| `stale` | Not checked recently enough to trust. |
| `regressed` | Recent evidence shows loss of reliability. |

## Assistance Vocabulary

Use these levels in evidence and review records.

| Level | Meaning |
| --- | --- |
| `independent` | No instructional prompt was needed. |
| `prompted` | A hint, question, or reminder was needed. |
| `modeled` | The method had to be demonstrated. |
| `not-yet` | The learner could not complete it with available support. |

## Confidence Vocabulary

Use confidence to separate fact from interpretation.

| Confidence | Meaning |
| --- | --- |
| `observed` | Direct evidence from parent, teacher, assessment, or activity result. |
| `inferred` | Reasonable interpretation from observed evidence. |
| `unverified` | Useful note that must be checked before relying on it. |

## Evidence-First Rule

Update the learning map only from evidence.

Valid evidence includes:

- parent observation
- child explanation
- completed activity result
- worksheet or quiz outcome
- school report information
- teacher feedback

Invalid evidence includes:

- "the AI thinks so" without observed support
- a single lucky answer
- parent confidence without a concrete example
- old chat history with no dated record

## Lifetime Summary Rule

The lifetime memory should not become a giant unreadable transcript.

Use this pattern:

- `02-evidence-log.md` stores the detailed timeline.
- `01-learning-map.md` stores the current concise state.
- `05-session-reports.md` stores parent-readable summaries.
- `archive/` stores older yearly snapshots.

At the end of each term or year, summarize durable patterns into `01-learning-map.md` and keep the detailed evidence in the log or archive.

## Privacy Classification

Use one of these values in file frontmatter and sensitive notes:

| Value | Meaning |
| --- | --- |
| `private` | Normal learner data. Do not publish. |
| `sensitive` | Health, diagnosis, school conflict, family circumstances, or identity details. |
| `shareable-redacted` | Safe to paste into an AI chat after removing names and private details. |

The default is `private`.

## Curriculum Mapping

The core memory is evidence-first. Curriculum links are optional and belong in `06-curriculum-links.md`.

This keeps the learner record portable if the family changes:

- country
- state
- school
- curriculum
- AI model
- tutoring provider

