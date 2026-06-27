---
name: feedback-progress-sync
description: "After making any subtask changes to an active card, verify the On the Board count in PROGRESS.md matches"
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 17c52877-6154-40cf-af7a-a97368b84fc6
---

After making any subtask changes to an active card (marking [x], adding or removing items, restructuring), cross-check the corresponding row in the PROGRESS.md "On the Board" table and update the subtask count if it has drifted.

**Why:** Counts in PROGRESS.md are manually maintained and go stale silently — cards get updated in isolation and PROGRESS.md falls behind. Discovered during a bulk audit (2026-06-27) where 2♠️ was off by 1 and 3♦️ had both the numerator and denominator wrong.

**How to apply:** Any time a card file is edited in a session — even for a progress note or status change — glance at its On the Board row and confirm the count still reflects the current [x] (and [/] for complex wildcard goals) tally. Fix it in the same edit if it's off.
