# Classic WoW Addons

**Creative:** Babuni

My finished World of Warcraft addons for the old 1.12 and 3.3.5 clients, together with one client mod, collected in one place. I no longer develop them. Each folder is a complete former repository: source, README, changelog, development journal and decisions, with its full Git history. My current addons for WoW Forever live in their own repositories (see below).

## Install

Download the addon's zip from [`downloads/`](downloads/) and extract it into your client's `Interface/AddOns/` folder. The zip already contains the folder with the name the game expects (column *Installs as*). Restart the game or reload the UI. EnchantVisuals is a client mod rather than an addon; follow the [instructions in its README](EnchantVisuals/README.md).

Earlier releases of LootFeed and BattleReport are kept in [`downloads/older/`](downloads/older/). [`downloads/SHA256SUMS.txt`](downloads/SHA256SUMS.txt) lists the checksums.

## The addons

| Addon | Client | Installs as | What it does | Download |
| --- | --- | --- | --- | --- |
| [ActionEmotes #1](ActionEmotes-1/README.md) | 1.12 | `BuxbrewCharge` | Babuni.dev’s first WoW add-on: action-bar-triggered character emotes, originally BuxbrewCharge. | [ActionEmotes-1.zip](downloads/ActionEmotes-1.zip) |
| [StealthEmotes](StealthEmotes/README.md) | 1.12 | `Amazin` | Action-slot emote addon with rested experience reporting; successful Stealth casts are not detected. | [StealthEmotes.zip](downloads/StealthEmotes.zip) |
| [ActionEmotes #2](ActionEmotes-2/README.md) | 1.12 | `Buxbrew` | Custom roleplay emotes triggered by a watched action-bar slot, with a cooldown and per-character settings. | [ActionEmotes-2.zip](downloads/ActionEmotes-2.zip) |
| [Battle Emotes Legacy](BattleEmotesLegacy/README.md) | 1.12 | `roarr` | Historical action-slot emote addon with configurable chance and cooldown; installed as ROARR. | [BattleEmotesLegacy.zip](downloads/BattleEmotesLegacy.zip) |
| [Battle Emotes](BattleEmotes/README.md) | 1.12 | `roarr` | Action-slot roleplay emotes with chance, cooldown and tutorial controls; distinct from Battle Emotes Legacy. | [BattleEmotes.zip](downloads/BattleEmotes.zip) |
| [MultiActionEmotes](MultiActionEmotes/README.md) | 1.12 | `ROARRunlimited` | Multiple action-slot emote configurations with independent chances and cooldowns. | [MultiActionEmotes.zip](downloads/MultiActionEmotes.zip) |
| [RoarGuild Add-on](RoarGuildAddon/README.md) | 1.12 | `roarguild` | Character-expression addon with configurable action emotes, recruitment messages and Roarboard. | [RoarGuildAddon.zip](downloads/RoarGuildAddon.zip) |
| [Roar Guild Addon Wrath](RoarGuildAddonWrath/README.md) | 3.3.5 | `ROARTrigger` | Wrath 3.3.5 port of the Roar Guild addon, with action-slot emotes and character profiles; Roarboard is not included. | [RoarGuildAddonWrath.zip](downloads/RoarGuildAddonWrath.zip) |
| [RoarSoundEffects](RoarSoundEffects/README.md) | 3.3.5 | `ROAR` | Addon for restoring built-in character roar sounds from recognized emote events; no game audio is bundled. | [RoarSoundEffects.zip](downloads/RoarSoundEffects.zip) |
| [BattleReport](BattleReport/README.md) | 1.12 | `BattleReport` | Personal encounter and combat-statistics reporter. | [BattleReport.zip](downloads/BattleReport.zip) |
| [EnchantVisuals](EnchantVisuals/README.md) | 1.12 (client mod) | `see its README (Install.ps1)` | Native client mod combining weapon enchant and imbue visuals. | [EnchantVisuals.zip](downloads/EnchantVisuals.zip) |
| [GroupBuffToggle](GroupBuffToggle/README.md) | 1.12 | `GroupBuffToggle` | Toggleable party and target unit-frame buffs. | [GroupBuffToggle.zip](downloads/GroupBuffToggle.zip) |
| [GuildChatBridge](GuildChatBridge/README.md) | 1.12 | `GuildChatAI` | Paused WoW roleplaying experiment: guild-chat capture and manual sending; no working AI conversation bridge. | [GuildChatBridge.zip](downloads/GuildChatBridge.zip) |
| [LevelUpAnnouncer](LevelUpAnnouncer/README.md) | 1.12 | `BuxbrewDing` | Guild level-up announcer with 60 roleplay messages, local previews and manual sends; live-client compatibility remains unverified. | [LevelUpAnnouncer.zip](downloads/LevelUpAnnouncer.zip) |
| [LootFeed](LootFeed/README.md) | 1.12 | `LootFeed` | Animated loot and group-roll information display. | [LootFeed.zip](downloads/LootFeed.zip) |
| [MeleeStartAttack](MeleeStartAttack/README.md) | 1.12 | `MeleeStartAttack` | Attack-start helper for several melee classes. | [MeleeStartAttack.zip](downloads/MeleeStartAttack.zip) |
| [ResistInsight](ResistInsight/README.md) | 1.12 | `BuxbrewResist` | On-hold resistance-tooltip addon for WoW 1.12 and predecessor of ResistForever; explains estimated spell resistance and damage reduction. | [ResistInsight.zip](downloads/ResistInsight.zip) |
| [TotemTimers](TotemTimers/README.md) | 1.12 | `TotemTimers` | Shaman totem, shield and weapon-enhancement tracking. | [TotemTimers.zip](downloads/TotemTimers.zip) |
| [WarriorStartAttack](WarriorStartAttack/README.md) | 1.12 | `WarriorStartAttack` | Auto-attack helper for warrior abilities. | [WarriorStartAttack.zip](downloads/WarriorStartAttack.zip) |
| [WorkThatGodBod](WorkThatGodBod/README.md) | 1.12 | `WorkThatGodBod` | In-game posture, movement and hydration reminders. | [WorkThatGodBod.zip](downloads/WorkThatGodBod.zip) |

Battle Emotes and Battle Emotes Legacy both install as `roarr`, so only one of them can be installed at a time. MultiActionEmotes' `.toc` names `roarrunlimited.lua` while the file is `ROARRunlimited.lua`; this works on Windows, which ignores letter case, and is recorded in [its roadmap](MultiActionEmotes/docs/ROADMAP.md).

## How they belong together

Most of these began as ways to give my characters more personality in ordinary play. The [development journal](docs/DEVLOG.md) tells that history across the emote addons, guild tools and sound experiments. The verification checklists and open ideas in each folder's roadmap are kept as a record; they are not plans.

## Current addons, in their own repositories

[FlourishForever](https://github.com/babunidev/FlourishForever) · [RoarForever](https://github.com/babunidev/RoarForever) · [SocialForever](https://github.com/babunidev/SocialForever) · [ResistForever](https://github.com/babunidev/ResistForever) · [ClearViewForever](https://github.com/babunidev/ClearViewForever) · [FavorCraft](https://github.com/babunidev/favorcraft) · [GatherMap](https://github.com/babunidev/GatherMap)

## Former repositories

Each folder was its own GitHub repository until 19 November 2026. Their pull requests and release notes are preserved in [`docs/github-archive/`](docs/github-archive/). Pull requests that were still open (mostly readability rewrites from November 2026, never merged) keep their changes on branches named `archive/<Addon>-pr<number>`; they are records, not merged work.

## License

Each addon keeps its own [MIT](LICENSE) license file and copyright line in its folder; asset and third-party notices stay with the addon they belong to. The collection's own documents are MIT-licensed as well.
