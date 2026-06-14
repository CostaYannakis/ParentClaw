---
system: family-tutor-kit
version: 0.1.0
component: learning-asset-protocol
last_updated: 2026-06-14
---

# Learning Asset Protocol

This protocol defines how child-facing activities connect to the learner memory.

Assets can be paper tasks, diagrams, manipulatives, browser activities, videos, simulations, games, or worksheets. The protocol is Markdown-first so assets can be used across AI tools.

## Asset Principles

- The activity is controlled and bounded.
- The parent can observe the child using it.
- The asset returns evidence, not a vague score.
- The evidence links to one or more skill IDs.
- The child does not need unrestricted chatbot access.

## Required Asset Metadata

Each asset should have a Markdown descriptor using this structure:

```yaml
---
asset_id: maths-fractions-bars-001
asset_type: manipulative
title: Fraction Bars
version: 0.1.0
subjects:
  - maths
domains:
  - fractions
skill_ids:
  - maths-fractions-001
recommended_levels:
  - flexible
requires_ai_for_child: false
privacy: shareable-redacted
last_updated: 2026-06-14
---
```

## Required Headings

Every asset descriptor should include:

- `# Asset Title`
- `## Purpose`
- `## Prerequisites`
- `## Parent Setup`
- `## Child Task`
- `## Evidence Produced`
- `## Scoring Or Interpretation`
- `## Memory Update Guidance`

## Evidence Return Format

After using an asset, the parent or AI should be able to produce:

| Field | Meaning |
| --- | --- |
| Asset ID | Stable activity ID. |
| Skill ID | Skill being checked or taught. |
| Attempted items | What the child tried. |
| Correct items | What was correct. |
| Reasoning evidence | What the child said, showed, sorted, moved, drew, or selected. |
| Assistance level | `independent`, `prompted`, `modeled`, or `not-yet`. |
| Misconception evidence | Specific error pattern, if present. |
| Suggested next review | Date or timing suggestion. |

## Interpretation Rule

An asset score is not the same as understanding.

The memory update should consider:

- correctness
- explanation
- transfer to a new example
- assistance needed
- consistency with previous evidence
- whether the task was too easy or too hard

## Asset ID Convention

Use:

```text
subject-domain-shortname-sequence
```

Examples:

- `maths-number-placevalue-001`
- `maths-fractions-bars-001`
- `writing-sentences-expansion-001`
- `reading-comprehension-mainidea-001`

