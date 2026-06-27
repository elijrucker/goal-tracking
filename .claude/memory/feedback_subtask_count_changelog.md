---
name: feedback-subtask-count-changelog
description: Do not log subtask count updates in CHANGELOG.md Process section — count is visible in the card itself
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 4c759f2e-bd8b-44ca-a921-290f77628746
---

Do not add `[PROGRESS] — 🃏X subtask count: A/B → C/D` entries to CHANGELOG.md under `#### Process`.

**Why:** The subtask count is already represented directly in the card file. Logging it in the changelog is redundant overhead.

**How to apply:** When updating a card's subtasks (adding, removing, completing, pruning), update the card and PROGRESS.md as needed, but omit the subtask count line from the changelog Process section entirely. If there's nothing else in the Process section, omit the section.
