---
name: feedback-commit-push-cadence
description: User lets commits accumulate locally through the day on personal projects rather than pushing after each one
metadata: 
  node_type: memory
  type: feedback
  originSessionId: ffb71084-0957-4036-9906-36ccfdc7aa62
---

Don't push after every individual commit on personal projects — let commits accumulate locally over a day's work, then push in a batch.

**Why:** Stated preference: "I usually allow them to accumulate over a day's work for personal projects." This is a personal repo (the deck goal-tracker), not a shared/collaborative one, so there's no urgency to sync each commit to the remote.

**How to apply:** After committing, don't proactively offer or run `git push` unless the user asks for it or it's clear they're wrapping up for the day. Committing still requires confirmation per global CLAUDE.md instructions, but push is a separate, rarer action on this kind of repo.
