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

## Card File Conventions

Card filenames: `{value}-{suit}.md` (e.g., `02-spades.md`, `king-hearts.md`, `ace-diamonds.md`). Face cards use full names (`jack`, `queen`, `king`, `ace`).

Every card has these sections in order: **Card Details → Status → Goal Description → Resources → Prerequisites → Subtasks → Progress Notes → Completion Notes → Unlocks**. Do not add, remove, or reorder sections.

### Key Fields

- **Current Status**: One of `Not Started`, `Preparing`, `In Progress`, `Complete`
- **Color Tier / Difficulty**: Determined by card value — 2-4 = 🟢 Green/Foundational, 5-7 = 🔵 Blue/Moderate, 8-9 = 🟡 Yellow/Substantial, 10-J = 🟠 Orange/Advanced, Q-K-A = 🔴 Red/Elite
- **Subtasks**: Use `- [x]` / `- [ ]` / `- [/]` checkboxes (`[x]` = complete, `[ ]` = not started, `[/]` = in progress)
- **Prerequisites**: Reference other cards that must be completed first
- **Unlocks**: Cards that become available after this one is completed

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
