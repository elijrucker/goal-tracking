---
name: Changelog Entry Pattern
description: Standardized syntax for all CHANGELOG.md card data entries, established 2026-04-01
type: project
originSessionId: 498da4f9-a162-460b-8422-60f05e73174d
---
## Pattern

```
- [card-name] — action (date)              ← card-scoped
- [card-name] — [subtask] action (date)    ← subtask-scoped
```

`[subtask]` is only included when the action is scoped to a specific subtask. Inline dates in parentheses are only added when the action occurred on a **different date than the entry header** — same-day dates are redundant and omitted.

## Card-level actions

| Action | Usage |
|---|---|
| `transitioned: X → Y` | Card status changed |
| `added [thing]` | New subtask, resource, or field added to the card |
| `refactored [description]` | Structural or naming change at the card level |
| `[Field] set to [value]` | Field updated from blank to a value |
| `[Field] updated: X → Y` | Field updated from one value to another |

## Subtask-level actions

| Action | Usage |
|---|---|
| `promoted backlog → worklog` | Subtask moved to active worklog |
| `marked [state]` | Subtask state changed within the worklog (e.g., `marked in progress`, `marked skipped`) |
| `marked in progress (annotation content)` | Shorthand for simultaneous state change + initial annotation — use when a subtask is started and annotated in the same entry. Avoids redundant `added annotation` line. |
| `closed` | Subtask completed |
| `deferred to [period]` | Subtask pushed to a later period |
| `added` | New item added within an existing subtask tree |
| `refactored [description]` | Structural or naming change at the subtask level |

## Annotations

| Form | Usage |
|---|---|
| `added annotation (content)` | New annotation added to a subtask |
| `updated annotation (content)` | Annotation replaced; old value not worth logging |
| `updated annotation: 'old' → 'new'` | Annotation changed; delta is meaningful |
| `updated annotation: last touched (date)` | Date-tracking annotation on an in-progress subtask; completion date annotations do not need a changelog entry — the `closed` action already captures the temporal event |

## Cascade closures

When a child subtask's completion closes the parent, log each as a separate `Completed` entry — child first, parent second. Do not combine them on one line or reference the child in the parent entry. Prefer verbosity over compression here; two lines are easier to follow at a glance than a semicolon-joined collapse.

```
- [card-name] — [parent > child] closed
- [card-name] — [parent] closed
```

This applies to subtask-to-subtask cascades. A child-subtask close that also completes the *card itself* is a distinct scenario: the card status transition belongs in `Changed`, and the child close can include a milestone callout if warranted.

## Ranges

When an action applies to a consecutive range of subtasks, use an en dash (`–`) between the first and last item: `[parent > wk13–wk16] added`. Legibility over ease of input — `...` is not used.

## Entry header order

When a single day's header covers multiple events, list them in descending order of significance: major milestones and status transitions first, routine progress updates last. Example: `Post-Semester Retro; Status Transitions; joker-2 apparel closed`.

## Subsection order (established 2026-07-03)

Within a single entry, `###` subsections (`Added`/`Changed`/`Completed`/`Removed`/`Notes`/`Process`) are ordered chronologically by when the changes happened during the session — earliest at the top, most recent at the bottom. Not a fixed Added→Changed→Completed sequence.

This mirrors the file-level convention at a smaller scale: entries themselves run reverse-chronological (newest date first), but the content inside a single entry runs chronological (oldest action first). Documented in CLAUDE.md's Changelog Conventions section.

## Sections

Valid sections per CLAUDE.md: `Added`, `Changed`, `Completed`, `Removed`, `Notes`, and `Process`.

### Process

`Process` covers meta-system housekeeping that is distinct from card-file content changes:
- PROGRESS.md count updates and corrections (e.g., `[PROGRESS] — 2♠️ subtask count updated: 1/12 → 5/23`)
- Workflow, tooling, or convention decisions established in the session
- BACKLOG additions that are a downstream consequence of restructuring a card (items deferred out of a card)

### BACKLOG placement rule

- Standalone new ideas added to the backlog → `Added`
- BACKLOG entries that are a side-effect of restructuring or deferring from an active card → `Process`

## Free-form exception

Prose notes that don't map to a fixed verb stay as plain text after the em dash — no action keyword required.

**Why:** Established to replace ad-hoc changelog phrasing with a consistent, scannable format.
**How to apply:** Use this pattern for all new CHANGELOG.md entries. Existing entries are not backfilled.
