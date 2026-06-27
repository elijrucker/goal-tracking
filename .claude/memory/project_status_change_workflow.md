---
name: project-status-change-workflow
description: "All card file, PROGRESS.md, and CHANGELOG.md changes required whenever a card status transitions"
metadata: 
  node_type: memory
  type: project
  originSessionId: 17c52877-6154-40cf-af7a-a97368b84fc6
---

Any card status transition (Preparing → In Progress, In Progress → Deferred, etc.) requires updates across three files. Missing any of the aggregate PROGRESS.md fields is the most common source of drift — they require explicit propagation and don't update automatically when individual rows change.

**Why:** The 3♠️ V2 promotion (2026-06-22) correctly updated the Spades individual suit row but left the Total row and Color Tier table stale for several sessions, requiring a bulk correction on 2026-06-27.

---

## 1. Card file

- `Current Status` field: update to new status
- `Start Date`: set if this is the first transition to In Progress
- `Completion Date` + `Time Invested`: set if transitioning to Complete

---

## 2. PROGRESS.md — all four areas must be updated

**Summary section**
Decrement the old status count, increment the new one. Affected fields: `Cards Completed`, `Cards In Progress`, `Cards Preparing`, `Cards Deferred`.
Also update `Last Completed` and `Current Streak` if completing a card.

**Suit table — individual row**
Decrement the old status column, increment the new one for the card's suit row.

**Suit table — Total row**
Recalculate after updating the individual row. The Total row does not self-update — it must be explicitly verified as the arithmetic sum of all suit rows. This is the field most likely to be missed.

**Color Tier table**
Update `In Progress` and/or `Completed` columns for the card's tier (Green/Blue/Yellow/Orange/Red). Jokers are excluded from this table (they have no tier).

**On the Board table** (per [[feedback-on-the-board]])
- Transitioning TO In Progress or Deferred → add a row; place In Progress rows above Deferred rows
- Transitioning AWAY from In Progress or Deferred → remove the row
- Preparing cards are never listed; their presence is implied by their prerequisite cards

If adding a row, also verify the subtask count is current (per [[feedback-progress-sync]]).

**Completed Cards section**
If completing a card, add the standard entry block (Card Value, Suit, Goal Name, Completed date, Time Invested, Key Takeaway). Check milestone checkboxes if applicable.

---

## 3. CHANGELOG.md

Log the transition under the `Changed` section using the standard verb:

```
- [card-name] — transitioned: X → Y
```

Entry header order: status transitions are significant events — list them before routine progress updates in the same day's header (per CLAUDE.md entry header order convention).

Same-day inline dates are omitted (redundant with the entry header date).

If the status change also triggers other logged events in the same session (e.g., a subtask added, a field set), group them under the same date header with the transition listed first.
