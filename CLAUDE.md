# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repo Is

A 52-card deck goal tracking system. Each card is a markdown file representing a personal learning or development goal. This is a **content-only repo** — no build system, no tests, no code to run. All work is reading and editing `.md` files.

## Repo Layout

- `cards/` — The 54 card files organized by suit subdirectories (`clubs/`, `diamonds/`, `hearts/`, `spades/`) plus two joker files at the cards root
- `CARD_TEMPLATE.md` — Canonical template; all card files must follow this structure
- `DECK_OVERVIEW.md` — Quick-reference table of all 52 goals
- `PROGRESS.md` — Completion counts, suit/tier breakdowns, milestones checklist
- `CHANGELOG.md` — Chronological log of all updates (keep-a-changelog style with Added/Changed/Completed/Removed/Notes sections)
- `BACKLOG.md` / `RESOURCES.md` / `GOALS_TLDR.md` — Supporting reference docs
- `WORKFLOW.md` — Describes the deck's relationship to the external daily to-do list (deck = macro/strategic, list = micro/daily-resolution); the list itself is not tracked in this repo

## Card File Conventions

Card filenames: `{value}-{suit}.md` (e.g., `02-spades.md`, `king-hearts.md`, `ace-diamonds.md`). Face cards use full names (`jack`, `queen`, `king`, `ace`).

Every card has these sections in order: **Card Details → Status → Goal Description → Resources → Prerequisites → Subtasks → Progress Notes → Completion Notes → Reflection & Lessons Learned → Unlocks**. Do not add, remove, or reorder sections.

### Key Fields

- **Current Status**: One of `Not Started`, `Preparing`, `Deferred`, `In Progress`, `Complete`
  - `Deferred` = intentionally postponed; card was previously active or preparing but deliberately paused pending better timing, prerequisites, or circumstances
- **Color Tier / Difficulty**: Determined by card value — 2-4 = 🟢 Green/Foundational, 5-7 = 🔵 Blue/Moderate, 8-9 = 🟡 Yellow/Substantial, 10-J = 🟠 Orange/Advanced, Q-K-A = 🔴 Red/Elite
- **Subtasks**: Use `- [x]` / `- [ ]` / `- [/]` / `- [-]` checkboxes (`[x]` = complete, `[ ]` = not started, `[/]` = in progress, `[-]` = skipped)
- **Prerequisites**: Reference other cards that must be completed first
- **Unlocks**: Cards that become available after this one is completed

### Subtask Tree Retention

- **Static cards** (status `Complete`) retain their full subtask tree permanently, as a record of how the goal was completed.
- **Dynamic cards** — cards with open-ended, recurring subtask groups rather than a fixed linear curriculum (e.g., joker-1, 10-hearts) — prune closed subtask entries from the tree once they've been logged in CHANGELOG.md, to keep the file navigable. Course/book cards with a bounded curriculum are not dynamic in this sense and retain their full checklist regardless of status.
- Because dynamic cards don't hold a full history in-file, PROGRESS.md's On the Board table may track them by a different signal than a raw subtask fraction (e.g., joker-1 tracks Prerequisite completion instead — see its Prerequisites section).

### Suit Domains

- ♦️ Diamonds = Tools, Platforms & Certifications
- ♣️ Clubs = Applied Practice & Programming
- ♠️ Spades = Theory, Fundamentals & Mathematics
- ♥️ Hearts = Personal Development

## When Updating Cards

1. Always update the card file itself with the relevant changes (status, subtasks, progress notes, etc.)
2. Add a dated entry to `CHANGELOG.md` under the current date header (create one if it doesn't exist for today)
3. When a card's status changes to `Complete`, also update `PROGRESS.md` counts and milestone checkboxes
4. Progress Notes entries should be prefixed with a bracketed date (e.g., `- [2026-02-17] Completed Chapter 3`)
5. If a card has a subdirectory (e.g., `05-hearts/`), supplementary materials like matrices or trackers live there alongside the card file

## Changelog Conventions

**Entry header order** — When a single day's header covers multiple events, list them in descending order of significance: major milestones and status transitions first, routine progress updates last. Example: `Post-Semester Retro; Status Transitions; joker-2 apparel closed`.

**Annotation update entries** — Use the format `- [card] — [subtask] annotation updated (current annotation)`. The parenthetical reflects the annotation's current state after the update, not a before/after diff. Example: `- [joker-1] — [Optimize Github profile] annotation updated (pinned repositories, repository descriptions)`.

**Subsection order** — Within a single entry, `###` subsections (`Added`/`Changed`/`Completed`/`Removed`/`Notes`/`Process`) are ordered chronologically by when the changes occurred during the session — earliest change at the top, most recent at the bottom — not by a fixed Added→Changed→Completed sequence. This mirrors the entry-header convention at the file level: entries themselves run reverse-chronological (newest date first), but the content within a single entry runs chronological (oldest action first).

## Standing Decisions

Cross-cutting decisions that apply across cards and sessions, not tied to any single card's progress.

- **[2026-06-14] LinkedIn content strategy** — Personal/lifestyle milestones (e.g., weight loss progress) are excluded from individual LinkedIn posts. Reserved for a future cumulative progress-arc reflection post.
- **[2026-06-16] Subtask count in changelog** — Do not log subtask count deltas (e.g., `17/51 → 17/54`) in CHANGELOG.md. The count is represented in the card itself; logging it in the changelog is redundant. Omit the `#### Process` section entirely if it has nothing else to say.
