---
system: family-tutor-kit
version: 0.1.0
audience: parent
last_updated: 2026-06-14
---

# Start Here

This kit helps you use ChatGPT, Claude, or another AI as a tutoring coach while you remain the tutor.

The child does not need unrestricted access to the AI. You ask the AI what to teach, how to teach it, and how to record what happened.

## One-Time Setup

1. Copy `learners/_template-learner/` and rename the copy for your child.
2. Use a stable private folder name, such as `learners/ava-2017/`.
3. Open the copied `00-profile.md`.
4. Fill in only what you know.
5. Leave unknown fields as `unknown`, not blank.
6. Keep this folder local, or store it in a private GitHub repository if you want backup and version history.

If using GitHub, read `PRIVATE-GITHUB-REPO.md` first.

## First AI Message

Attach or paste these files into your preferred AI:

1. `skills/assess-current-level.md`
2. `skills/update-memory.md`
3. the learner's `00-profile.md`
4. the learner's `01-learning-map.md`
5. the learner's `02-evidence-log.md`
6. the learner's `03-review-queue.md`
7. the learner's `04-goals.md`

Then say:

```text
I have 30 minutes to tutor my child. Use the attached Family Tutor Kit files. Start by helping me choose a suitable objective and a short assessment activity.
```

## Normal Session Flow

1. Parent asks for a session plan.
2. AI reads learner memory and proposes one objective.
3. Parent teaches using the AI's coaching.
4. Child completes a controlled activity or explains reasoning aloud.
5. Parent reports what happened.
6. AI writes a structured evidence entry.
7. Parent adds the entry to the learner files.
8. AI recommends what to review next.

## What Not To Do

- Do not ask the AI to invent progress without evidence.
- Do not let old chat history replace the learner memory files.
- Do not store private learner records in public repositories.
- Do not require curriculum codes before recording useful evidence.
- Do not treat the AI as the child's unsupervised tutor.

## The Smallest Useful Routine

If you are short on time, do only this:

1. Ask the AI: "What should we work on for 20 minutes?"
2. Teach the suggested activity.
3. Tell the AI what the child did independently, what required prompting, and what was confusing.
4. Add the AI's evidence entry to `02-evidence-log.md`.
5. Update `03-review-queue.md`.
