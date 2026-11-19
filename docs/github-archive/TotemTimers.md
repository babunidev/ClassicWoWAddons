# GitHub record — TotemTimers

Issues, pull requests and releases of the former repository `babunidev/TotemTimers`, exported on 2026-11-19 before it was deleted. Its code and full Git history are in [`TotemTimers/`](../../TotemTimers/README.md); release zips are in [`downloads/`](../../downloads/).

## Releases

- **TotemTimers 1.3.7** (`v1.3.7`), published 2026-09-18

### Release notes — v1.3.7

Provider-neutral release of TotemTimers. Add-on, UI, saved-variable, command and installation names are consistent; client compatibility and gameplay behavior are preserved.

Download TotemTimers.zip and extract the TotemTimers folder into Interface/AddOns.

If upgrading from a previous add-on folder name, fully close the game and follow the README upgrade instructions before playing. The included Upgrade-SavedData.ps1 helper copies existing settings and records, keeps originals and backups, and refuses to overwrite existing destination data. Disable the previous add-on after migration.

Validation: source and packaged Lua syntax, TOC file references and branding scan passed. Saved-data migration tests passed for values, Unicode, originals, backups, overwrite protection and invalid paths. Existing applicable regression tests passed. Live in-game verification remains recommended.

## Pull requests

### Pull request #1 — Improve README navigation

*open; opened 2026-11-10 by babunidev.*

*Not merged. Its changes are kept on the branch `archive/TotemTimers-pr1` of this repository.*
