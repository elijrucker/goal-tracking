# REFLECTIONS.md

A standing log for insights that don't belong to a single card's lifecycle —
cross-cutting patterns, product/system-level realizations, and reflections
that emerge from working across the deck rather than completing one part of it.

Card-specific reflections still live in each card's own **Reflection & Lessons
Learned** section. This file is for everything else: patterns noticed across
cards, meta-level realizations about the system itself, and reflections tied
to backlog items or initiatives that don't yet have (or may never have) a
dedicated card.

---

## Template for Future Entries

### [YYYY-MM-DD] — Entry Title

**Context:** [What prompted this reflection — session, milestone, or realization]

**What surprised me:**

**What worked well:**

**What this unlocks:**

**Core insight:**

**One thing that worked:**

**One thing harder than expected:**

**Insight for future similar work:**

**Delayed reflection (revisit ~[date, 1-2 weeks out]):**
- [Question 1]
- [Question 2]

---

## Entries

### [2026-08-03] — AWS Track Pivot: Solutions Architect Associate over Developer Associate

**Context:** A mentor advised pursuing AWS Solutions Architect Associate years before this
system existed, but the reasoning behind that advice wasn't understood at the time — it read
as one AWS cert among several plausible options. The Diamonds suit was originally built around
Developer Associate instead. On 2026-08-03, comparing the SAA and DVA exam material directly
surfaced the distinction the mentor's advice had been pointing at, and the track was pivoted
retroactively (see CHANGELOG.md). No dedicated planning session preceded it — the realization
happened inline while reviewing prep resources.

**What surprised me:** That the mentor's advice took years to actually land — not because it
was wrong, but because understanding *why* it was right required doing enough side-by-side
comparison to see the distinction it was built on. Advice can be correct and still inert until
the recipient has the context to recognize what it's naming.

**What worked well:** Catching the mismatch before more Developer-track study time was sunk —
the Phase 0/1 progress under J♦️ didn't carry over and had to reset, cheaper to absorb early
than after finishing the prep course.

**Core insight:** Developer Associate certifies implementation — writing and deploying against
AWS SDKs, Lambda, CI/CD integration, working within a system someone else has already designed.
Solutions Architect Associate certifies the design layer above that: reasoning about compute,
storage, networking, and database choices as a coherent system, exercising independent judgment
over tradeoffs (cost, resilience, security) rather than executing against a spec. This maps
directly onto the architect/builder distinction Brooks draws in *The Mythical Man-Month* —
conceptual integrity and system design as a distinct discipline from the implementation work
that follows it, and a different skill than either. For a backend candidate whose implementation
ability is already carried by a project portfolio, the architecture-reasoning credential fills
the gap the portfolio doesn't otherwise demonstrate — and it's the AWS cert most consistently
recognized across job postings regardless of whether the role is framed as "developer" or
"engineer."

**What this unlocks:** The actual capability of reasoning about a system as a whole — service
selection, tradeoffs, resilience — rather than only implementing pieces of one someone else
designed. Interview conversation is a downstream byproduct of that, not the reason for it. It
also gives a concrete throughline connecting three separate threads that all point the same
direction — the mentor's original advice, the SAA/DVA material comparison, and the Brooks
architect/builder framing encountered independently while reading *Mythical Man-Month*. Three
unrelated sources converging on the same distinction is a stronger signal than any one of them
alone.

**One thing that worked:** Staying open to revisiting old advice instead of treating "already
decided years ago, didn't act on it" as a closed question — the comparison that triggered this
could have just as easily been skipped as redundant.

**One thing harder than expected:** Recognizing that a multi-year gap between receiving advice
and understanding it isn't a failure to act — some advice genuinely requires accumulated context
to parse, and there's no way to compress that except by living through it.

**Insight for future similar work:** When old advice suddenly clicks, that's worth logging as
its own event, not just folding into the resulting decision — the "why now" is often more
instructive than the "what changed."

**Delayed reflection (revisit ~2026-08-17):**
- Did the SAA material actually surface system-design language usable in interviews, or did
  the benefit stay theoretical?
- Does the architect/builder distinction from Brooks keep showing up elsewhere now that it's
  been named once, or was this a one-off connection?

### [2026-08-03] — Engineering Culture Reading Cluster Planning — Session Reflection

**Context:** Began collecting foundational CS literature after reading Pragmatic
Programmer and ordering Programming Pearls, which prompted the question: with
all the material already in hand, what's still missing? Surfaced that CS50 AI
(6♠️) and CS50 Cybersecurity (4♠️) had each been provisioned their own card
slot before their actual scope was weighed against neighboring cards.

**What worked well:** Once the hesitation cleared, comparative-effort
reasoning surfaced cleanly — CS50 AI + CS50 Cybersecurity combined still
likely represent less depth than CS50x given the volume of extra-curricular
deep dives undertaken there, confirming the merge and its Green tier. Merging
the two was a more organic decision once weighed against their combined
assumed effort compared to Discrete Mathematics.

**What this unlocks:** A more substantial foundation in theory, usable to
improve the goal tracking project itself, and reinforcing standing not just
as a developer but as an engineer and architect.

**One thing harder than expected:** Getting past the initial hesitation to
make a larger structural change to the deck (reshuffling card slots, merging
cards) rather than just adding to the backlog.

**Pattern identified:** Tier assignment should be calibrated against
comparative effort/intensity between neighboring cards, not just sequential
position — flagged via the Discrete Math (5♠️) vs. CS50 AI (6♠️) comparison.

**Insight for future similar work:** It's much easier to reformat or
restructure work that hasn't yet begun than work already in progress — scope
creep has less impact when it isn't immediate in nature.

**Delayed reflection (revisit ~2026-08-17):**
- [Question 1]
- [Question 2]
