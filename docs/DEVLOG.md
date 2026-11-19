# Development journal — Classic WoW Addons

This journal covers the collection as a whole. Each addon's own development journal stays in its folder (`<addon>/docs/DEVLOG.md`) with its original dates and wording.

## 2026-11-19 — One home for the finished addons

Most of my old World of Warcraft addons were small projects for the 1.12 and 3.3.5 clients, each in its own repository and each with its own tile on babuni.dev. Together they cluttered both GitHub and the website, and I am not going to develop them further. I decided to put all of them into one repository, each folder keeping its documentation, and to offer ready install zips for download. Addons with real plans for further development were to keep their own repositories.

Claude Code (Claude Opus 5.5) checked the roadmaps first. Apart from RoarSoundEffects and ResistInsight, which say they are finished, they contained only verification checklists and unapproved ideas written during the October documentation audits, no features I had decided to build, so I chose to include all 21. The WoW Forever addons stay separate because they are active and publish to CurseForge. AI merged each repository with its complete history into its own folder, built install zips from the runtime files where no release existed and copied the existing release zips after verifying their checksums. The old repositories are deleted once this collection is published; GitHub keeps them restorable for 90 days.

## 2026-11-19 — The Great Iceflow Relay goes its own way again

The same evening I decided that The Great Iceflow Relay should get a WoW Forever edition. That is further development, so it no longer belongs here. Claude Code (Claude Opus 5.5) had already deleted its repository; at my choice it recreated it from the complete local history and took the folder out of this collection.

## Retrospective — the expressive addon family (August 2025 to October 2026)

*Compiled by Babuni on 1 November 2026 in FlourishForever's `docs/EMOTE_FAMILY_HISTORY.md` and reproduced here; links now point to the folders in this collection.*

**Still to add:** the chapter before the first standalone addon (WeakAuras in Classic Anniversary and Madaxe Morkahja's Charge) comes from an interview that is not yet part of these documents.

**Creative:** Babuni · **Retrospective compiled:** 1 November 2026  
**Scope:** Related projects and source-grounded milestones, not an assertion that every later repository directly forks the previous one.

Across these experiments, my interest has been in giving characters a little more life during ordinary play. The underlying action stayed with the player; emotes supplied personality, surprise or a shared guild ritual. The surviving repositories trace changes in trigger methods, writing, customization, community features and client targets. AI assisted with implementation and later documentation where recorded, while creative direction remained mine.

### Timeline of the action-emote family

| First visible milestone | Current repository (earlier name) | What changed |
| --- | --- | --- |
| **18 Aug 2025** | [Action Emotes #1](../ActionEmotes-1/README.md) (BuxbrewCharge) | First addon: one watched action slot and randomly selected native emotes; current pool 10, fixed 21-second cooldown. |
| **Aug 2025** | [Stealth Emotes](../StealthEmotes/README.md) (Amazin) | Rogue Stealth-button experiment made for my younger brother: 12 built-in emotes, adjustable chance and cooldown; the source monitors the slot, not Stealth itself. |
| **12 Sep 2025** | [Action Emotes #2](../ActionEmotes-2/README.md) (Buxbrew / MadAxeBuxbrew) | A different expressive branch: 215 authored text emotes sent through chat instead of game-native emote tokens. |
| **22 Nov 2025** | [Battle Emotes Legacy](../BattleEmotesLegacy/README.md) (roar / ROAR) | BuxbrewCharge-derived single-slot system with five fixed native battle emotes and adjustable chance/cooldown. |
| **23 Nov 2025** | [Battle Emotes](../BattleEmotes/README.md) (roarr / ROARR) | Nearly identical gameplay implementation to Legacy; the second repository's tutorial expands to seven steps. |
| **14 Dec 2025** | [Multi Action Emotes](../MultiActionEmotes/README.md) (ROARRunlimited) | Multiple numbered action-slot configurations, each with its own chance/cooldown; four fixed native emote tokens in current code. |
| **10 Jan 2026** | [Roar Guild Addon](../RoarGuildAddon/README.md) (RoarGuild) | Multiple triggers plus a player-extensible native-emote registry, per-character profiles and guild identity; later gained manual recruiting messages and Roarboard (Aug 2026). |
| **27 Apr 2026** | [Roar Guild Addon Wrath](../RoarGuildAddonWrath/README.md) (ROARemoteTrigger → EmoteTrigger; installed as ROARTrigger) | Wrath 3.3.5 port of the guild-addon emote features, including editable emote registry and manual recruiting text; excludes the later Roarboard. |
| **22 Oct 2026** | [Flourish Forever](https://github.com/babunidev/FlourishForever) | WoW Forever addon with a graphical spellbook selector, per-ability native-emote choices and successful-spellcast event triggers rather than action-slot presses. |

These dates are documented **commits or first visible source milestones**, not proof of when every idea was first imagined. The two Battle Emotes repositories are closely related snapshots, not evidence of two separate gameplay engines.

### What “how many emotes?” actually means

**Fixed built-in pools:** Action Emotes #1, Stealth Emotes, Battle Emotes Legacy, Battle Emotes and Multi Action Emotes have lists defined in Lua; **players cannot add to those lists with an in-game command in the current source**. Action Emotes #2 instead holds 215 fixed authored roleplay lines. In particular, the five and four battle tokens are not merely default entries in an unlimited player-editable registry.

**Player-extensible native-emote registry:** Roar Guild Addon and its Wrath port begin with **ROAR** at registry ID 1. `/rogu emote LAUGH` registers another token, `/rogu emote list` lists entries, and `/rogu emote1 <id>` assigns an ID to an instance. There is no small hardcoded registry cap, but a token must be supported by the game client to function, and practical limits apply. This is not the same as creating custom animation assets or writing arbitrary text emotes.

**Player-selectable client emotes:** Flourish Forever presents native emote tokens reported by its target client, selecting a set for each configured spell. A new spell starts with ROAR selected. This is a user-editable **selection** of existing client tokens, not unrestricted creation of arbitrary tokens.

**Trigger semantics:** The earlier addons react to `UseAction` presses, even if a spell fails. Flourish Forever instead responds to the player's `UNIT_SPELLCAST_SUCCEEDED` event, which means a reported completed cast, **not** necessarily a landed hit. Its unsuccessful chance roll does not consume the emote cooldown, unlike the older configured ROAR implementations.

### Related sound-restoration branch

Two other repositories share the goal of expressive character presence, **but are not action-triggered emote generators**:

- [Roar Sound Effects](../RoarSoundEffects/README.md) (originally ROARSounds; source from **19 Apr 2026**) responds to observed text emotes and restores native voice assets, beginning with /roar.
- [Roar Forever](https://github.com/babunidev/RoarForever) (WoW Forever) expands the restoration idea into more voiced emotes, client-specific detection, options, language handling and experimental addon communication/distance behavior.

The distinction matters: an action-emote addon *initiates an emote*; a sound-restoration addon *tries to play an appropriate existing voice for an emote*. Their goals complement one another, but neither guarantees integration with the other.

### Guild history and attribution

ROAR was also my guild, which shaped the identity of the later Roar Guild projects. In those sources, `/rogu invite` **sends a randomized recruitment message to a chat channel when invoked**; it does not send a game API invitation to a named player and is not present in the two early Battle Emotes repositories. Roarboard is specific to the later Vanilla guild-addon revision.

The chronology is a **retrospective synthesis** from source and Git documentation, supplemented by my recollections. It does not establish exact code-copy relationships for every pair, assign unrecorded human–AI design conversations, or claim in-game verification of every current build. No runtime changes are implied by this historical document.

### FlourishForever's place

Flourish Forever is the October 2026 WoW Forever expression of the action-emote idea. Unlike the earlier action-slot hooks, it responds to the player’s **reported successful spellcast** event and lets the player select spellbook abilities and existing client-native emotes in a GUI. Each new ability initially has ROAR selected, but the player may choose other available emote tokens. This is client-token selection rather than creation of arbitrary new emotes, and cast success does not prove a landed hit.
