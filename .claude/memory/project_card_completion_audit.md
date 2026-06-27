---
name: project-card-completion-audit
description: Full codebase audit triggered on every card completion to catch stale data and unsynced changes
metadata: 
  node_type: memory
  type: project
  originSessionId: 17c52877-6154-40cf-af7a-a97368b84fc6
---

Every card completion is a trigger for a full codebase audit. Card completions represent a natural checkpoint — enough change has accumulated between them to make the review worthwhile, and the completion workflow already touches PROGRESS.md and CHANGELOG.md, making it a natural extension.

**Why:** Stale counts and unsynced changes accumulate silently across sessions. Without a consistent trigger, drift compounds between reviews and requires larger manual corrections. Card completions are frequent enough to keep the system honest but infrequent enough that the audit doesn't become noise.

**How to apply:** After completing a card's standard completion workflow (card file, PROGRESS.md counts, CHANGELOG.md entry), run the following audit before closing the session:

1. **PROGRESS.md Summary** — verify Cards Completed, In Progress, Preparing, Deferred, and Not Started counts are correct
2. **Suit table individual rows** — for each suit, verify Completed/In Progress/Preparing/Deferred/Not Started add up to the correct total and match actual card file statuses
3. **Suit table Total row** — verify it is the correct arithmetic sum of all suit rows
4. **Color Tier table** — verify In Progress and Completed counts match actual card files by tier
5. **On the Board table** — verify only In Progress and Deferred cards are listed, subtask counts match card files, and rows are ordered (In Progress first, Deferred last)
6. **DECK_OVERVIEW.md** — spot-check status column for recently changed cards
7. **Recently modified card files** — confirm progress notes are reverse-chronological, subtask states are consistent, and no section ordering has drifted

8. **Convention review** — for each issue found in steps 1–7, assess whether a new memory convention or an amendment to an existing one would prevent recurrence. If yes, write or update the convention before closing the session. Issues that surface once may be one-offs; issues that required manual correction despite an existing convention suggest the convention needs sharpening or a new one is warranted.

**Precedent:** First formal audit run 2026-06-27. Found Total row arithmetic errors in the suit table (In Progress off by 1, Not Started off by 1) and Color Tier table distribution errors (Green In Progress understated, Yellow In Progress overstated) — all traceable to the 3♠️ V2 promotion not propagating to aggregate rows. Convention review from that session produced [[project-status-change-workflow]] and [[feedback-progress-sync]].
