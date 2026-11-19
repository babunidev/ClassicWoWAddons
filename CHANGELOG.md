# Changelog — Classic WoW Addons

## 2026-11-19 — The Great Iceflow Relay returns to its own repository

- Removed `TheGreatIceflowRelay/` and its install zip. A WoW Forever edition was planned for it the same evening, so by the collection's rule it keeps its own repository again: [babunidev/TheGreatIceflowRelay](https://github.com/babunidev/TheGreatIceflowRelay), recreated from the full local history. Its unmerged readability pull request moved there as the branch `archive/readability-pr1`. Its former pull requests stay recorded in [`docs/github-archive/TheGreatIceflowRelay.md`](docs/github-archive/TheGreatIceflowRelay.md). The collection now holds 20 projects.
- Claude Code (Claude Opus 5.5).

## 2026-11-19 — GitHub records of the former repositories

- Added `docs/github-archive/<Addon>.md` for all 21 former repositories: 31 pull requests with descriptions and comments, and the notes of 14 releases. The former repositories had no issues and no wiki pages.
- Kept the 22 pull requests that were still open as branches `archive/<Addon>-pr<number>`, unmerged.
- Links in the addon documents to the former repositories now lead to the matching folder, commit or `downloads/` in this repository.
- Claude Code (Claude Opus 5.5).

## 2026-11-19 — Collection created

- Merged 21 repositories with their full Git history, one folder each: ActionEmotes-1, ActionEmotes-2, StealthEmotes, BattleEmotesLegacy, BattleEmotes, MultiActionEmotes, RoarGuildAddon, RoarGuildAddonWrath, RoarSoundEffects, TotemTimers, GroupBuffToggle, LootFeed, BattleReport, WorkThatGodBod, TheGreatIceflowRelay, MeleeStartAttack, WarriorStartAttack, ResistInsight, LevelUpAnnouncer, GuildChatBridge and EnchantVisuals. No addon code changed.
- Added `downloads/` with one install zip per addon: the latest GitHub release for EnchantVisuals, TotemTimers, GroupBuffToggle, LootFeed and BattleReport (checksums verified), the earlier LootFeed and BattleReport releases in `downloads/older/`, and zips built from the runtime files for the other 16. `downloads/SHA256SUMS.txt` lists all checksums.
- Added the collection README with an install guide and addon table, AGENTS.md, LICENSE, this changelog, `docs/DEVLOG.md` (including Babuni's 1 November 2026 retrospective of the expressive addon family), `docs/DECISIONS.md` and the shared `docs/DOCUMENTATION.md`.
- Claude Code (Claude Opus 5.5). Install zips were checked against each `.toc` file list; they were not tested in a game client.
