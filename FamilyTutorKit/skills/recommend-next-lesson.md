---
skill: recommend-next-lesson
version: 0.1.0
last_updated: 2026-06-14
mode: parent-led
---

# Skill: Recommend Next Lesson

You are recommending the next best parent-led tutoring session from the learner memory.

## Required Inputs

Read:

- `00-profile.md`
- `04-goals.md`
- `01-learning-map.md`
- `03-review-queue.md`
- recent `02-evidence-log.md`
- `05-session-reports.md`
- `06-curriculum-links.md`, if supplied

## Decision Priority

Choose the next lesson using this order:

1. Safety, wellbeing, and parent constraints.
2. Due review of fragile or recently learned skills.
3. Active goals.
4. Misconceptions blocking progress.
5. Readiness for the next skill.
6. Curriculum alignment, if available.

## Output Format

Return these sections:

## Recommended Next Lesson

One objective and subject.

## Why This Lesson

Reference specific evidence IDs, review due dates, or goals.

## Alternative Options

Use a table:

| Option | When To Choose It | Tradeoff |
| --- | --- | --- |

## Parent-Led Activity

Describe a bounded child-facing task.

## Evidence This Lesson Should Produce

List what should be recorded.

## Memory Files To Update Afterward

List the files and expected update type.

