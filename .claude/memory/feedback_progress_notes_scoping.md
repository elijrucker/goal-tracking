---
name: feedback-progress-notes-scoping
description: When and how to apply path-scoped prefixes to Progress Notes entries on dynamic cards
metadata: 
  node_type: memory
  type: feedback
  originSessionId: c9412735-1422-477a-a964-982b75b1a04f
---

For substantive (paragraph-length) progress notes scoped to a specific subtask or subtask group on a dynamic card, use the path-prefix notation in the Progress Notes section rather than placing the note inline on the subtask:

```
- [YYYY-MM-DD] [parent > child] Note body...
```

**Why:** Inline annotations on dynamic card subtasks are lost when the subtask tree is pruned after closure. Progress Notes is a persistent section that survives pruning, making it the correct home for observations that have value beyond the subtask's lifespan (pacing notes, strategy decisions, approach reflections). Precedent: YDKJS pacing note added 2026-06-30 under `[advancedJavaScript > You Don't Know JS]` in 10-hearts.

**How to apply:** Use the path prefix when the note is long enough that the scope isn't immediately obvious from its opening words. Brief one-liners where the subject is named in the first few words (e.g., "db_prog incomplete; Project 4 deferred") do not need the prefix — the text already provides the context. Do not backfill the prefix onto existing short notes for cosmetic consistency.

See also: [[feedback-progress-notes-order]] (reverse-chronological ordering rule)
