---
name: feedback-hyphens-not-em-dashes
description: "Default to hyphens instead of em dashes in prose within this repo's files"
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 7bc5d578-3c35-44b8-8b4e-276d6a3755fd
---

Use hyphens ("-") instead of em dashes ("—") by default when writing or editing prose in this repo's `.md` files (e.g. card descriptions, annotations, free-text notes).

**Why:** User's explicit stylistic preference (2026-07-14), given while editing 10-hearts.md.

**How to apply:** Applies to prose only. Does NOT apply to structural separators already documented as conventions — e.g. CLAUDE.md's `[card] — [subtask]` annotation format, or CHANGELOG.md's `[date] — description` header format (see [[project_changelog_pattern]]) — the user explicitly scoped this to prose, keeping em dashes in those documented schema separators.
