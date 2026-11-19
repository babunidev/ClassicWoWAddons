# Agent Rules — ClassicWoWAddons

This repository collects Babuni's finished addons for the World of Warcraft 1.12 and 3.3.5 clients and the EnchantVisuals client mod. They are not developed further.

## What this repository is

- Each top-level folder is a former standalone repository, merged with its full Git history on 2026-11-19. Its README, AGENTS.md, CHANGELOG and `docs/` remain the record for that addon and keep their own rules.
- `downloads/` holds the install zips: release zips where a GitHub release existed, otherwise a zip built from the folder's runtime files (`.toc`, `.lua` and media beside it, plus LICENSE) inside a folder named after the `.toc`. Rebuild a zip only when that addon's runtime files change, and update `downloads/SHA256SUMS.txt`.
- Do not change addon code, start new features or "fix" items from the old roadmaps unless Babuni asks for that specific change. Roadmap checklists are historical records, not tasks.

## Human–AI collaboration record

`docs/AI_COLLABORATION.md` is the short record of how Babuni works with AI and who did what, with the same text in all of Babuni's repositories. Do not add dated entries, session notes or per-change attribution to it. Record each contribution in `docs/DEVLOG.md` (what Babuni asked for and what the AI did, naming the tool and model) and in `CHANGELOG.md`. Change `docs/AI_COLLABORATION.md` only to add a row to its "Who did what" table when a new AI tool or model starts contributing to this project, or when Babuni revises the shared text.

## Repository layout

The repository root holds only `README.md`, `AGENTS.md`, `LICENSE` and `CHANGELOG.md`, plus the addon folders and `downloads/`. Collection-wide documentation lives in `docs/`; put new documents there.

## Documentation

Follow [the documentation standard](docs/DOCUMENTATION.md): first-person narrative from Babuni's perspective without opening sentences with "I" or "My", factual changelogs, and naming the AI tool and verified model for each contribution. **Babuni** is the human creative; **babuni.dev** is the website. Preserve third-party credits, the copyright lines in each folder and historical legal notices.

## Sources and privacy

Write only claims supported by the repository, supplied material or checks actually run. Do not publish private chats, credentials or unrelated personal information.
