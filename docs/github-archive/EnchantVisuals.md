# GitHub record — EnchantVisuals

Issues, pull requests and releases of the former repository `babunidev/EnchantVisuals`, exported on 2026-11-19 before it was deleted. Its code and full Git history are in [`EnchantVisuals/`](../../EnchantVisuals/README.md); release zips are in [`downloads/`](../../downloads/).

## Releases

- **EnchantVisuals 1.0.1** (`v1.0.1`), published 2026-09-18
- **Enchant Visuals 1.0 (superseded)** (`v1.0.0`), published 2026-09-11

### Release notes — v1.0.1

Provider-neutral build of Enchant Visuals for the exact supported 32-bit World of Warcraft 1.12.1 (5875) executable.

The library, configuration, log and installer names are updated. The installer preserves existing configuration and unrelated loader entries, recognizes previous builds by checksum and creates backups. Executable and runtime signature checks remain unchanged.

Download EnchantVisuals-1.0.1.zip. This is a native client mod, not an Interface/AddOns add-on.

Validation: x86 build and visual-selection tests passed; installer upgrade, backup, configuration, repeat-install, removal and checksum-rejection tests passed. The rebuilt binary has not yet been revalidated in game. See the README for exact compatibility, installation and remaining in-game checks.

### Release notes — v1.0.0

Historical release, superseded by [Enchant Visuals 1.0.1](https://github.com/Morkahja/EnchantVisuals/releases/tag/v1.0.1).

The original implementation was tested in game. Its previous download used retired names, so the downloadable package is now provided by the current release. Version 1.0.1 rebuilds the same visual implementation with neutral configuration and log names, preserves installer checks and adds upgrade handling. Its offline build and installer tests pass; the rebuilt binary still needs an in-game check.

This historical tag remains unchanged. Use the current release ZIP for installation rather than the automatic source archive.

## Pull requests

### Pull request #1 — Improve project documentation readability

*open; opened 2026-11-10 by babunidev.*

*Not merged. Its changes are kept on the branch `archive/EnchantVisuals-pr1` of this repository.*

Editorial changes to headings, attribution, spacing, or reader navigation. Existing technical and historical claims are preserved.
