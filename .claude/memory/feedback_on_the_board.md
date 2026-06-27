---
name: feedback-on-the-board
description: "What qualifies for inclusion in the PROGRESS.md \"On the Board\" table"
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 69b72ecc-1791-4562-8ebe-b3bce43ef7a6
---

The "On the Board" table in PROGRESS.md should only include cards that are actively being worked on: `In Progress` and `Deferred` cards.

**Why:** `Preparing` status is implied by the prerequisite cards that are already on the board — listing them separately adds noise without actionable signal. Aspirational/distant cards (like joker-2) are similarly excluded.

**How to apply:** When adding or reviewing rows, ask: is this card actively being worked on right now (In Progress or Deferred)? If not — including Preparing cards — omit it. Preparing cards are visible through the In Progress cards that precede them.
