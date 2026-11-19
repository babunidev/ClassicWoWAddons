# GuildChatBridge — changelog

Implemented repository changes are recorded here; ideas and unverified behavior belong in the roadmap or journal.

## 2026-11-19 — documentation moved into `docs/`

- Moved `CONCEPT.md` and `ROADMAP.md` into `docs/`. The root keeps only `README.md`, `AGENTS.md`, `LICENSE` and `CHANGELOG.md`; links to the moved files and the documentation rules in `AGENTS.md` were updated. No code changed. Claude Code (Claude Opus 5.5).

## 2025-08-20 — original source recorded

- [Initial Lua upload](https://github.com/babunidev/ClassicWoWAddons/commit/bd6afe4ab9b9c306ea234525aeef2f67a1617e0d): Event handlers for guild messages and roster updates, storage and a manual guild-chat send command.
- [Manifest addition](https://github.com/babunidev/ClassicWoWAddons/commit/244f60387b01cc14188b029fb3bc2b7d67f46216): `GuildChatAI.toc` added with interface `11200`.

These are repository history dates, not evidence of an in-game release.

## 2026-10-26 — documentation baseline

- Expanded the repository with concept, design, architecture, decisions, development journal and development instructions from inspected source and available history.
- Documentation only; no runtime tests.

## 2026-10-31 — repository renamed and documented

- At my direction, the GitHub project became [GuildChatBridge](https://github.com/babunidev/ClassicWoWAddons/tree/main/GuildChatBridge), previously `GuildChatAI`.
- AI assistance updated eleven Markdown documentation files to reflect the name and authorship convention, while preserving original addon identifiers. See [354d73f](https://github.com/babunidev/ClassicWoWAddons/commit/354d73f1173c646eeaa087b52cfc4e69e052afe1).

## 2026-10-31 — creative history and limitations clarified

- At my request, AI assistance reviewed all current documentation and the two addon source files.
- Rewrote the active documentation to explain the independent-character roleplaying idea, why the experiment was paused, and the distinction between chat-send APIs and an absent real-time local-AI bridge.
- Clarified that potential assisted or autonomous roleplay variants are unapproved possibilities, not delivered functionality.
- Preserved the historical README, Lua, TOC and license unchanged. No live-client test was performed.
