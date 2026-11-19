# GitHub record — LootFeed

Issues, pull requests and releases of the former repository `babunidev/LootFeed`, exported on 2026-11-19 before it was deleted. Its code and full Git history are in [`LootFeed/`](../../LootFeed/README.md); release zips are in [`downloads/`](../../downloads/).

## Releases

- **LootFeed 0.2.2** (`v0.2.2`), published 2026-09-18
- **Loot Feed 0.2.1 - Group roll timing fix** (`v0.2.1`), published 2026-09-11
- **Loot Feed 0.2.0 - Group rolls** (`v0.2.0`), published 2026-09-11
- **Loot Feed 0.1.5** (`v0.1.5`), published 2026-09-08

### Release notes — v0.2.2

Provider-neutral release of LootFeed. Add-on, UI, saved-variable, command and installation names are consistent; client compatibility and gameplay behavior are preserved.

Download LootFeed.zip and extract the LootFeed folder into Interface/AddOns.

If upgrading from a previous add-on folder name, fully close the game and follow the README upgrade instructions before playing. The included Upgrade-SavedData.ps1 helper copies existing settings and records, keeps originals and backups, and refuses to overwrite existing destination data. Disable the previous add-on after migration.

Validation: source and packaged Lua syntax, TOC file references and branding scan passed. Saved-data migration tests passed for values, Unicode, originals, backups, overwrite protection and invalid paths. Existing applicable regression tests passed. Live in-game verification remains recommended.

### Release notes — v0.2.1

Fixes premature group-roll termination when the local roll prompt closes before other players finish. Closing the prompt no longer triggers the three-second result cutoff. Tracking continues to the original deadline, late results can recover provisional timeouts, and roll numbers arriving after the winner are retained.

Regression tests cover early prompt closure, delayed votes/results, timeout recovery, and restoring a result after its row has faded. Existing loot and group-roll tests pass. The original screenshot's event sequence was not recorded, so confirmation in a live group is still needed.

Replace the LootFeed folder with the ZIP contents and reload the UI.


Packaging update: names and documentation have been made provider-neutral; the historical gameplay implementation and version are retained. If changing installation folder names, use the included saved-data upgrade helper before playing. Historical Git tags retain their original source snapshots. The ready-to-install ZIP contains the neutral names.

### Release notes — v0.2.0

Group-roll notifications now stay visible while rolling. Hover the dice to see player choices, reported roll numbers, and the winner; completed results stay for 15 seconds and pause while hovered. The winner is shown beside the dice. Use the normal game buttons to choose Need, Greed, or Pass.

Use /lfeed testroll for a preview. The client loot-detail setting is enabled to receive roll messages. Identical simultaneous item links are flagged as ambiguous instead of guessing which copy a result belongs to.

Validated with automated Vanilla-format event tests covering self/group choices, numeric rolls, winners, all-pass, cancellation, timeout, hover retention, overflow, positional translations, currency, and quest labels. Live group testing is still needed.

Extract LootFeed.zip into Interface\AddOns, replacing the existing LootFeed folder, then reload the UI.


Packaging update: names and documentation have been made provider-neutral; the historical gameplay implementation and version are retained. If changing installation folder names, use the included saved-data upgrade helper before playing. Historical Git tags retain their original source snapshots. The ready-to-install ZIP contains the neutral names.

### Release notes — v0.1.5

Compact animated loot feed for World of Warcraft 1.12.

Download LootFeed.zip below, extract the LootFeed folder into Interface\AddOns, and restart WoW. Use /lfeed unlock to position the feed and /lfeed test to preview it.


Packaging update: names and documentation have been made provider-neutral; the historical gameplay implementation and version are retained. If changing installation folder names, use the included saved-data upgrade helper before playing. Historical Git tags retain their original source snapshots. The ready-to-install ZIP contains the neutral names.

## Pull requests

### Pull request #1 — Improve project documentation readability

*open; opened 2026-11-10 by babunidev.*

*Not merged. Its changes are kept on the branch `archive/LootFeed-pr1` of this repository.*

Editorial changes to headings, attribution, spacing, or reader navigation. Existing technical and historical claims are preserved.
