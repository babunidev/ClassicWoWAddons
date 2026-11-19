# GitHub record — RoarGuildAddon

Issues, pull requests and releases of the former repository `babunidev/RoarGuildAddon`, exported on 2026-11-19 before it was deleted. Its code and full Git history are in [`RoarGuildAddon/`](../../RoarGuildAddon/README.md); release zips are in [`downloads/`](../../downloads/).

## Pull requests

### Pull request #1 — Align addon version string with release metadata

*merged, merged 2026-01-30; opened 2026-01-30 by babunidev.*

### Motivation
- Ensure the file header and `ADDON_VERSION` constant match the release metadata (`1.32`) so version information is consistent across the addon.

### Description
- Updated the header comment and bumped the `ADDON_VERSION` constant in `roarguild.lua` from `"1.3"` to `"1.32"`.

### Testing
- No automated tests were run.

------
[Codex Task](https://chatgpt.com/codex/tasks/task_e_697d3f88852c8327a9099fc2a704df82)

### Pull request #2 — Add `/rogu fallback chance` and `/rogu fallback timer` commands

*merged, merged 2026-01-30; opened 2026-01-30 by babunidev.*

### Motivation

- Provide user-configurable fallback behavior so players can customize the fallback chance and cooldown and have those values persist in the profile database.

### Description

- Add a new subcommand handler for `FALLBACK` implementing ` /rogu fallback chance <0-1000>` to set `fb.chancePermille` and ` /rogu fallback timer <sec>` to set `fb.cd`, creating the `ROGU.fallback` table and applying defaults when missing via `ROGU_EnsureFallbackDefaultsOn`.
- Update the interactive help line shown by `/rogu` to document the new `fallback chance` and `fallback timer` commands.
- Validate numeric ranges for chance (`0..1000`) and timer (`>=0`) and emit usage messages on invalid input.

### Testing

- No automated tests were run for this change.

------
[Codex Task](https://chatgpt.com/codex/tasks/task_e_697d41ce05088327a0693002478bb9fd)

### Pull request #3 — Add clearer section commentary in roarguild.lua

*open; opened 2026-01-30 by babunidev.*

*Not merged. Its changes are kept on the branch `archive/RoarGuildAddon-pr3` of this repository.*

### Motivation
- Improve readability and navigation within `roarguild.lua` by making the file structure explicit and adding short intent notes for major blocks.
- Make profile/DB helpers, emote selection, feature behaviors, and slash command groups easier to understand at a glance.

### Description
- Add a top-level structure guide and expand section headers across `roarguild.lua` to label constants, utilities, core state, data pools, profile/DB helpers, features, stats, hooks, slash commands, and init/save wiring.
- Add brief intent comments for chat/emote wrappers (`roarChat`, `performEmote`), profile helpers (`ROGU_EnsureDB`, `ROGU_EnsureProfile`, migration), emote ID sanitization/selection (`ROGU_SanitizeEmoteIDs`, `ROGU_PickEmoteForCfg`), load/sync (`ROGU_LoadOnce`, `ROGU_SyncToProfile`), features (invite, fallback, reminders), and stats windowing.
- Clarify slash-command groupings under `/rogu` (core, social, utility, debug, instance config, emote DB, instance emote selection, maintenance) and add short notes explaining each group's purpose.
- These are documentation/comment changes only and do not alter runtime logic.

### Testing
- No automated tests were run because this change is comment- and formatting-only for `roarguild.lua`.

------
[Codex Task](https://chatgpt.com/codex/tasks/task_e_697d41ffe62c832787a9a02d998923d7)

### Pull request #4 — Use explicit `ROAR` emote for `/rogu ROAR` command

*merged, merged 2026-03-28; opened 2026-03-28 by babunidev.*

### Motivation
- Ensure the manual `ROAR` slash command always emits the literal `ROAR` emote instead of selecting an emote from the configured slots, avoiding config-dependent or nil token issues.

### Description
- Replace the dynamic pick `ROGU_PickEmoteForCfg(...)` and `performEmote(token)` with a direct `performEmote("ROAR")` call in the `ROAR` handler while preserving the stats recording and `ROGU.lastRoar` update.

### Testing
- No automated tests were added or run for this trivial change.

------
[Codex Task](https://chatgpt.com/codex/tasks/task_e_69c72d9118c88327958fe1673983d1ac)

### Pull request #5 — Add Roarboard guild message board

*merged, merged 2026-08-18; opened 2026-08-17 by babunidev.*

## What changed

- Added Roarboard: a shared, channel-synchronized guild message board with a quest-log-style two-panel UI.
- Added posting, reactions, activity ordering, seven-day expiry, and `/roarboard sync`.
- Reworked the guild invite-message pool and updated the addon version and documentation.

## Why

Guild members need a lightweight, in-game place to leave and react to shared messages without external services.

## Impact

Players can post with `/roarboard <message>`, open the board with `/roarboard`, and react with **Roar**.

## Validation

- Checked the staged diff for whitespace errors.
- Fixed the Vanilla UI incompatibility caused by `SetWordWrap`; final in-game verification remains recommended.

### Pull request #6 — Improve project documentation readability

*open; opened 2026-11-10 by babunidev.*

*Not merged. Its changes are kept on the branch `archive/RoarGuildAddon-pr6` of this repository.*

Editorial changes to headings, attribution, spacing, or reader navigation. Existing technical and historical claims are preserved.
