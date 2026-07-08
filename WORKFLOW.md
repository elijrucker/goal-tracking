# Workflow

Describes how this deck relates to day-to-day task selection. The deck is not a daily planner — it is deliberately too coarse-grained to answer "what do I work on today" without incurring more decision overhead than it's worth. That resolution is handled by a separate, external daily to-do list, not tracked in this repo.

---

## The Two Layers

- **Deck (macro/strategic)** — this repo. Cards define goals, prerequisites, tiers, and unlocks. Answers "what's the shape of the plan" and "what depends on what."
- **Daily to-do list (micro/daily-resolution)** — external, not tracked here. A short list drawn from currently active cards. Answers "what do I work on today."

Card completions and status changes in the deck can trigger promotions/demotions in the daily list (see Tier 3 triggers below), but the daily list's own internal shuffling (rollover, pinning, day-to-day reprioritization) is not deck business and isn't logged here. Structural changes to the daily list's tier system are worth a brief `[System]`-tagged note in CHANGELOG.md, same as any other cross-cutting process change.

## Daily List Structure

Three tiers, as of 2026-07-07:

### Tier 1 — School + Active Focus

Deadline-driven items take priority over everything else. Reserved for:
- MATC coursework with hard deadlines
- Whatever is designated the current active daily focus
- Joker 1 subtasks, pinned here while actively in progress

German portfolio items pin to the top of Tier 1 when active, overriding all other ordering.

### Tier 2 — Rotating Goals (slot-based)

Four named resource slots, each holding one active goal. Slots cap how many goals can compete for attention at once by matching the context/effort the item actually requires:

| Slot | Requires | Current occupant |
|---|---|---|
| Terminal | Active computer/dev environment | Python Crash Course |
| Screen | Passive consumption, laptop or tablet | CS50x |
| Reading | Location-independent, no device | The Mythical Man-Month |
| Daily Review | Low-effort, consistent cadence | LeetCode (pinned to bottom permanently) |

Berlin vacation pins to the top of Tier 2 when active, overriding slot order.

### Tier 3 — Backlog

Unstructured holding bin for low-priority, gated, or on-hold items. No internal organization — overhead risk outweighs benefit. Physical pre-relocation tasks, deferred learning goals, and housekeeping items live here alongside gated items.

Standing promotion triggers:
- Claude Academy → Tier 2 Terminal, on Python Crash Course completion
- Berlin outreach items → Tier 1, on German portfolio completion

## Ordering Rules

- Tier 1 uses a rollover pattern: updating an item's date annotation sends it to the bottom; undated items float to the top.
- German portfolio and job application items override rollover and pin to the top of their respective tier.
- Tier 2's Daily Review slot is permanently pinned to the bottom, regardless of activity.
- Tier 3 is unordered by design.

## Note on Terminology

"Tier 2" / "Tier 3" here refer to the daily list's structure and are unrelated to any similarly-numbered tiers inside individual cards (e.g., joker-1's Tier 2/Tier 3 market segmentation for Berlin job search).
