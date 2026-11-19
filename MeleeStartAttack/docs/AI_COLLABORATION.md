# MeleeStartAttack — attribution and collaboration record

Follow [the documentation standard](DOCUMENTATION.md) for first-person author voice throughout project documentation, factual changelogs, and naming the AI tool and verified model for each contribution.

## From Warrior to three classes

After my Warrior experiment, I wanted selected actions to start ordinary auto-attacks for Paladins and Shamans too. The commits show the move from a single hook to three entry points, a cached Attack action, and class-specific start and stop behavior.

They do **not** by themselves establish which lines were originally produced by a human, which were authored with an AI, why every change was discussed or whether any proposal was approved outside recorded changes. Do not attribute the creative's initial idea to AI or fabricate missing conversation.

## AI assistance in this documentation session (2026-10-26)

An assistant:
- Fetched the live GitHub tree, full `MeleeStartAttack.lua` and TOC, existing README, earlier docs and dated August/September Git diffs.
- Identified the **7 Paladin, 20 Warrior, 5 Shaman** default icon entries and one Warrior stop icon.
- Explained the three global wrappers, icon-based spellbook localization, player-intent triggering, cached Attack slot vs combat-flag fallback, per-class persistence, legacy migration, and precise command behavior.
- Flagged unverified edge cases: shared-icon start/stop priority, capturing presses that also trigger actions, session-only on/off, same-class cross-character storage, macro learning failure and interaction with other global hooks.
- Rebuilt 11 Markdown docs including the narrative development history, roadmap and agent rules.

This is **editorial, research and technical analysis work**, not a claim that the assistant conceived the project, changed combat code or tested the client. The current documentation commit is **Markdown-only**.

## Method for future changes

Every substantial discussion/implementation should preserve:
1. **User direction:** What I wanted and why, including limits.
2. **AI interpretation/proposal:** Alternatives, tradeoffs, and what the assistant actually contributed.
3. **Creative iteration:** Misunderstandings, mistakes, rejected ideas and refinements.
4. **Creative decisions:** What was explicitly accepted, rejected or postponed.
5. **Implementation:** Changed paths, commit/PR reference and migration implications.
6. **Verification:** Test environment, commands, actual outcomes and what remains unverified.

Create publishable summaries rather than raw private transcripts. Keep credentials, unrelated private details, and other players' private communications out of the portfolio. Respect the creative's choice of a code license; there is **no LICENSE** committed as of this pass.

## 18 November 2026 — Collaboration record review

At my request, Codex (GPT-6) revised this record for first-person voice and checked the attribution against the available repository documentation. Where an earlier AI tool or model is missing from the record, its identity remains unconfirmed.
