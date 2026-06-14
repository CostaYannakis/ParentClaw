---
system: family-tutor-kit
version: 0.1.0
component: private-github-storage
last_updated: 2026-06-14
privacy: private
---

# Private GitHub Repository Storage

The default storage model is local files. A private GitHub repository can add backup, version history, and device sync.

Never store learner memory in a public repository.

## Recommended Setup

Use a private repository with a neutral name, such as:

- `family-learning-records`
- `home-tutor-memory`
- `learning-vault-private`

Avoid names that include:

- the child's full name
- school name
- diagnosis
- address or suburb

## What To Store

It is reasonable to store:

- learner memory files
- curriculum mappings
- asset metadata
- session summaries

Be careful with:

- medical or diagnostic notes
- school reports
- teacher emails
- full names
- screenshots or photos

## Safe Working Routine

1. Keep the repository private.
2. Add only trusted parent or guardian accounts.
3. Review changes before syncing.
4. Use short commit messages that do not reveal sensitive details.
5. Keep exported or redacted files separate from private learner memory.

## Commit Message Examples

Use:

- `update maths review queue`
- `add June session evidence`
- `summarise term 2 progress`

Avoid:

- full names
- medical details
- school conflict details
- emotionally sensitive notes

## Sharing With AI

When attaching files to an AI service:

- attach only the files needed for the current tutoring task
- remove sensitive notes when they are not instructionally necessary
- prefer learner ID over full name
- do not attach the full lifetime archive unless the task requires it

## Recovery

If private learner data is accidentally made public:

1. Make the repository private immediately.
2. Remove sensitive files from the current repository state.
3. Rotate any exposed credentials if they were included.
4. Consider the exposed data copied, even after deletion.
5. Create a new private repository if needed.

