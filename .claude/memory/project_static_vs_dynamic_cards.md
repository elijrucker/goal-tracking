---
name: static-vs-dynamic-cards
description: Distinction between static (completed) and dynamic (in-progress) cards governing subtask retention behavior
metadata: 
  node_type: memory
  type: project
  originSessionId: 558ce6b1-c27a-4c9b-8c8b-97fe00429512
---

## Convention

**Static cards** (status: Complete) — full subtask trees are retained as a permanent record. Precedent: 3♣️.

**Dynamic cards** (status: In Progress) — closed chapters within the card are pruned once their parent subtask closes, to reduce file noise. Precedent: joker-1 English LinkedIn profile section; 10-hearts Spring 26 semester block.

For dynamic cards, the two-commit pattern is preferred: first commit closes/marks the subtasks complete, second commit prunes the completed children. Git history preserves the full record; the working file stays clean.

**Why:** joker-1 is a long-lived card with many subtask groups that will open and close over time. Retaining all completed children indefinitely would accumulate noise in a document that needs to remain navigable.

**How to apply:** When a parent subtask on an in-progress card closes, expect a follow-up pruning commit. Do not flag pruning of completed children on dynamic cards as inconsistent with the 3♣️ precedent — that precedent applies to completed cards only.

**Exception — pending external dependency:** A completed subtask series may be intentionally retained on a dynamic card when it is awaiting an external action (e.g., third-party review). In this case the series stays open as a reminder until the dependency resolves, at which point it is pruned on the normal schedule. Precedent: joker-1 "Develop resume suite" retained pending third-party review of both resume versions (2026-06-25).
