---
name: v2-promotion-workflow
description: "Rules for promoting backlog items into the active deck as V2 goals, established 2026-06-22"
metadata: 
  node_type: memory
  type: project
  originSessionId: a563bc34-c6cb-411b-8ed3-bf30d773cc9b
---

## Convention

The backlog represents Deck V2 — a second pass at the deck after V1 goals are complete. Backlog items are not swapped into V1 card slots freely; they enter only via vacancy-gating.

**Vacancy-gated promotion**: A V2 goal may enter the active deck only when a V1 card completes AND that slot has no queued V1 successor. Completed V1 cards create the opening; V2 fills it only when V1 has nothing queued for that slot.

**Tier integrity**: A goal's tier value is intrinsic to the goal — it is never adjusted up or down to fit a vacant slot. A Green vacancy is filled by a Green-tier V2 goal. Completing a prerequisite does not make an unlocked goal easier or lower-tier.

**File naming**: V2 card files use `{value}-{suit}-v2.md` (e.g., `03-spades-v2.md`), created alongside the completed V1 file. The V1 file is preserved as a historical record and is never overwritten.

**DECK_OVERVIEW**: Update the slot's goal name to reflect the V2 goal, with a parenthetical noting V1 completion (e.g., `The Mythical Man-Month (V2; CS Distilled complete)`).

**BACKLOG**: Mark the promoted item `[x]` with the promotion date and slot; update the Review Log table.

**Precedent**: First V2 promotion — The Mythical Man-Month → 3♠️ V2 (2026-06-22), filling the vacancy created by CS Distilled completing.

**Version parity rule**: No V3 goal may be marked In Progress while any V1 card remains incomplete. Jokers are excluded from this rule. This extends naturally to future versions — no V(n+2) goal may activate while any V(n) card is incomplete.

**Why:** Waiting for full V1 completion before introducing V2 is impractical given the project's longevity. Vacancy-gating ties V2 growth to V1 progress, preventing V2 goals from crowding out V1 focus. The version parity rule provides a harder safeguard against stagnation — earlier versions must close out before a new generation can open.

**How to apply:** When a V1 card completes, check whether its unlocked successors are already active. If no V1 successor is queued for that slot, a V2 item of matching suit and tier may be promoted. Flag tier mismatches rather than bending the tier to fit.
