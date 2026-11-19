# GitHub record — BattleReport

Issues, pull requests and releases of the former repository `babunidev/BattleReport`, exported on 2026-11-19 before it was deleted. Its code and full Git history are in [`BattleReport/`](../../BattleReport/README.md); release zips are in [`downloads/`](../../downloads/).

## Releases

- **BattleReport 1.6.5** (`v1.6.5`), published 2026-09-18
- **Battle Report 1.6.4** (`v1.6.4`), published 2026-09-11
- **Battle Report 1.6.3** (`v1.6.3`), published 2026-09-09
- **Battle Report 1.6.1** (`v1.6.1`), published 2026-09-08
- **Battle Report 1.5.1** (`v1.5.1`), published 2026-09-07
- **Battle Report 1.3.1** (`v1.3.1`), published 2026-09-07

### Release notes — v1.6.5

Provider-neutral release of BattleReport. Add-on, UI, saved-variable, command and installation names are consistent; client compatibility and gameplay behavior are preserved.

Download BattleReport.zip and extract the BattleReport folder into Interface/AddOns.

If upgrading from a previous add-on folder name, fully close the game and follow the README upgrade instructions before playing. The included Upgrade-SavedData.ps1 helper copies existing settings and records, keeps originals and backups, and refuses to overwrite existing destination data. Disable the previous add-on after migration.

Validation: source and packaged Lua syntax, TOC file references and branding scan passed. Saved-data migration tests passed for values, Unicode, originals, backups, overwrite protection and invalid paths. Existing applicable regression tests passed. Live in-game verification remains recommended.

### Release notes — v1.6.4

Battle reports now start only when the player enters combat and close immediately when combat ends. Out-of-combat falling damage, healing, casts and resource changes no longer create or enter reports. Opening actions reported before combat begins are excluded.

Updated regression coverage and documentation. Full automated suite passes; in-game verification remains pending.

Extract BattleReport.zip into Interface/AddOns and reload the UI.


Packaging update: names and documentation have been made provider-neutral; the historical gameplay implementation and version are retained. If changing installation folder names, use the included saved-data upgrade helper before playing. Historical Git tags retain their original source snapshots. The ready-to-install ZIP contains the neutral names.

### Release notes — v1.6.3

Drag the Battle Report button while the quick report is visible to save its position per character. The timer pauses while dragging and restarts on release.

Also fixes missed confirmed casts after rejected retries and incorrect spell names for resource gains from other players.

Includes regression tests; the full automated suite passes. Extract BattleReport.zip into Interface/AddOns, then reload the game UI.


Packaging update: names and documentation have been made provider-neutral; the historical gameplay implementation and version are retained. If changing installation folder names, use the included saved-data upgrade helper before playing. Historical Git tags retain their original source snapshots. The ready-to-install ZIP contains the neutral names.

### Release notes — v1.6.1

Adds signed, colored comparisons with the pre-fight average to Damage Dealt, Damage Taken, Healing Done, and quick-report facts. Baselines stay attached to completed reports; ambiguous comparisons remain neutral.

Also reduces combat-start baseline calculation work and restores launcher state when quick-report fades are interrupted, hidden, or dismissed by combat.

Regression tests include average calculations, fade cleanup, and the actual Melee Start Attack hooks in a mocked WoW environment. These tests pass; the previously reported intermittent in-game action-bar problem has not been reproduced, so this release does not claim its cause is confirmed or resolved.

Download **BattleReport.zip**, replace the addon folder's files under **Interface\AddOns**, and type `/reload`. Restart the game for a first installation.


Packaging update: names and documentation have been made provider-neutral; the historical gameplay implementation and version are retained. If changing installation folder names, use the included saved-data upgrade helper before playing. Historical Git tags retain their original source snapshots. The ready-to-install ZIP contains the neutral names.

### Release notes — v1.5.1

Adds an optional post-fight quick report with three random fight facts.

- The launcher fades out, moves to the upper part of the screen, and fades in with a compact translucent facts panel.
- Remains visible for 12 seconds, then fades back to its saved position.
- Click to open that fight immediately while the launcher returns.
- Toggle **Quick report** at the top right of the main window. The setting is saved per character; disabling it dismisses the prompt without stopping fight recording.
- README now explains the checkbox and post-fight behavior.

Download **BattleReport.zip**, extract into **Interface\AddOns**, and reload the UI if upgrading. Restart WoW for a first installation.

Regression tests cover animation transitions, timeout, saved position, checkbox persistence, and continued recording when disabled.


Packaging update: names and documentation have been made provider-neutral; the historical gameplay implementation and version are retained. If changing installation folder names, use the included saved-data upgrade helper before playing. Historical Git tags retain their original source snapshots. The ready-to-install ZIP contains the neutral names.

### Release notes — v1.3.1

Personal combat reports for the original WoW 1.12 client.

Download **BattleReport.zip** below, extract it into your game's **Interface\AddOns** folder, restart WoW, and enable **Battle Report**. Open it with `/battlereport`.

- Live and saved fight reports, with up to 100 fights per character.
- Damage, defense, healing, casts, effects, and recovery views.
- Resources used and recovered side by side.
- Per-fight averages and a reset for starting a new measurement period.
- Beginner-friendly README and three in-game screenshots.

ShaguDPS is not required. Nampower is optional for improved cast tracking and item identification. Resource/recovery values are observed changes; see the included guide for capture limits.

Use the **BattleReport.zip** asset for the ready-to-install folder layout.


Packaging update: names and documentation have been made provider-neutral; the historical gameplay implementation and version are retained. If changing installation folder names, use the included saved-data upgrade helper before playing. Historical Git tags retain their original source snapshots. The ready-to-install ZIP contains the neutral names.

## Pull requests

### Pull request #1 — Improve project documentation readability

*open; opened 2026-11-10 by babunidev.*

*Not merged. Its changes are kept on the branch `archive/BattleReport-pr1` of this repository.*

Editorial changes to headings, attribution, spacing, or reader navigation. Existing technical and historical claims are preserved.
