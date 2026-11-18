# Totem Timers — human/AI collaboration and provenance

Follow [the documentation standard](DOCUMENTATION.md) for first-person author voice throughout project documentation, factual changelogs, and naming the AI tool and verified model for each contribution.

## Reading the totems at a glance

For my Shaman, I wanted one native-looking display for the four elements, with shield and weapon icons, red missing-state warnings, and controls to move or lock the display. The first public revision already identifies itself as 1.3.7.

The source does not record every earlier private discussion, alternate UI sketch, uncommitted version or which AI—if any—generated an earlier Lua function. The visible version was already **1.3.7** at first commit; it would be inaccurate to invent versions 1.0–1.3.6 as separately documented releases.

The Sept 18 rename was a recorded technical operation with consequences for users' saved state. The migration script is credited as committed project work; the October editorial assistant does not claim to have implemented it.

## Documented assistant contribution — October 27, 2026

The assistant:
- Confirmed **TotemTimers** as repository **#22** of the current numbered portfolio audit, explicitly skipping #21 GroupBuffToggle.
- Examined the 600-line `TotemTimers.lua`, manifest, existing documentation, PowerShell saved-data tool and fixture, and the two substantive September Git commits.
- Verified public **v1.3.7 release metadata** including ZIP and checksum links.
- Distinguished native `GetTotemInfo` reads from **cast-attempt-based timer prediction** and documented possible failed-cast drift and global wrapper behavior.
- Mapped 23 fallback totems, 4 element ordering, three shield names, four weapon enchant names, commands and SavedVariables.
- Authored/revised 11 Markdown files and checked them against the current source without editing any executable code.

This is **research, technical interpretation and documentation**, not a claim of original conception, 2026 gameplay testing, a fix for timer accuracy, creative approval of any new feature, or verification of binary releases.

## Future work must preserve the collaboration

For each material future change, record:
1. **User direction:** desired player experience, reason and restrictions.
2. **AI suggestion/implementation:** actual alternatives and code/document contributions.
3. **Creative iteration:** mistakes, competing approaches, tests, rejected solutions.
4. **Creative decision:** explicit accepted/rejected/deferred outcome.
5. **Implementation:** exact source, documentation and commit identifiers.
6. **Verification:** actual game client, test setup, screenshots, observed results and unknowns.

Public portfolio entries should be **narrative summaries**, not raw private conversations or client credentials/account data. Do not imply feature proposals in ROADMAP are authorized decisions.

No Lua, TOC, saved-data utility or regression fixture was changed by this October 27 documentation audit.

## 18 November 2026 — Collaboration record review

At my request, Codex (GPT-6) revised this record for first-person voice and checked the attribution against the available repository documentation. Where an earlier AI tool or model is missing from the record, its identity remains unconfirmed.
