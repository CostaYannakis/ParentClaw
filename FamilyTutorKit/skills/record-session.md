---
skill: record-session
version: 0.1.0
last_updated: 2026-06-14
mode: parent-led
---

# Skill: Record Session

You are turning a parent's session notes into structured learner evidence.

## Required Inputs

Use:

- the parent's report of what happened
- the session plan, if supplied
- current `01-learning-map.md`
- current `02-evidence-log.md`
- current `03-review-queue.md`

## Task

Produce a clean evidence entry that the parent can paste into `02-evidence-log.md`.

## Evidence Rules

- Separate observed evidence from interpretation.
- Use exact learner wording when available.
- Label uncertainty.
- Use only the approved assistance vocabulary.
- Use only the approved confidence vocabulary.
- Do not update skill state unless evidence supports it.

## Output Format

Return these sections:

## Evidence Entry For `02-evidence-log.md`

Provide a complete Markdown entry:

```markdown
### Evidence YYYY-MM-DD-001

| Field | Value |
| --- | --- |
| Date | YYYY-MM-DD |
| Session ID | session-YYYY-MM-DD-001 |
| Subject | subject |
| Domain | domain |
| Skill ID | skill-id |
| Activity | activity |
| Time spent | duration |
| Result | result |
| Assistance level | independent/prompted/modeled/not-yet |
| Confidence | observed/inferred/unverified |
| Next review | YYYY-MM-DD or unknown |

#### Observed Evidence

...

#### Learner Explanation Or Exact Words

...

#### Errors Or Misconceptions

...

#### Parent Notes

...

#### AI Interpretation

...

#### Correction Notes

none
```

## Memory Impact

List recommended changes to:

- `01-learning-map.md`
- `03-review-queue.md`
- `05-session-reports.md`

Do not silently rewrite files. Show the exact rows or entries to add or change.

## Questions If Evidence Is Insufficient

Ask only necessary follow-up questions.

