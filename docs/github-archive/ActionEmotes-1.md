# GitHub record — ActionEmotes-1

Issues, pull requests and releases of the former repository `babunidev/ActionEmotes-1`, exported on 2026-11-19 before it was deleted. Its code and full Git history are in [`ActionEmotes-1/`](../../ActionEmotes-1/README.md); release zips are in [`downloads/`](../../downloads/).

## Pull requests

### Pull request #1 — docs: align Action Emotes #1 with the babuni.dev creative-first writing rules

*merged, merged 2026-10-31; opened 2026-10-31 by babunidev.*

## Purpose
Revise the existing project documentation to match the approved babuni.dev writing perspective. This is a documentation-only review.

## Changes
- Preserve Babuni's first-person creative perspective without opening sentences with “I” or “My”.
- Standardize the role label **Creative** and distinguish human direction and hands-on work from ChatGPT's code suggestions and later editorial assistance.
- Condense the development journal while preserving its retrospective nature and uncertainties.
- Clarify Git-confirmed historical changes: the 2025-11-01 emote-pool revision and the 2026-01-10 parser change.
- Correct content grammar and note the unchanged packaging discrepancy.

## Verification
- Compared branch against `main`: only 11 Markdown files changed.
- Audited all 11 files for forbidden sentence openings: zero.
- Checked 11 relative Markdown links: no broken targets.
- No Lua, TOC or license changes.
- No in-game or runtime test performed.

**Comment by chatgpt-codex-connector (2026-10-31):**

<!-- codex-pull-request-review-summary -->
<!-- codex-review-state:v1 {"code_review":{"commit_sha":"42213d2e9204e842877ff4223e2c204d4be4d48e","has_any_findings":false,"has_unresolved_findings":false,"status":"completed"},"security_review":{"commit_sha":null,"has_any_findings":null,"has_unresolved_findings":null,"status":null}} -->

## Codex Review Summary

This comment shows the latest Codex review activity on this pull request.

| Review | Status | Commit | Review trigger |
| --- | --- | --- | --- |
| 📝 **Code Review** | ✅ **Completed** <relative-time datetime="2026-10-31T21:08:37.313017Z">2026-10-31T21:08:37.313017Z</relative-time> | `42213d2` | PR opened |



<details> <summary>ℹ️ About Codex in GitHub</summary>
<br/>

[Your team has set up Codex to review pull requests in this repo](https://chatgpt.com/codex/cloud/settings/general). Reviews are triggered when you
- Open a pull request for review
- Mark a draft as ready
- Comment "@codex review" or "@codex security review".

Codex reacts with 👀 while any review is running, comments if it has suggestions, and reacts with 👍 once all reviews finish with no findings.

</details>

### Pull request #2 — fix: make BuxbrewCharge directly installable from repository

*merged, merged 2026-10-31; opened 2026-10-31 by babunidev.*

## Scope
Fix the historical manifest typo and establish a self-contained installable `BuxbrewCharge/` folder. Preserve the Lua runtime exactly and keep the project's historical addon identity.

## File changes
- Move `BuxbrewCharge.lua` unchanged into `BuxbrewCharge/BuxbrewCharge.lua`.
- Rename `BuxbreCharge.toc` to `BuxbrewCharge/BuxbrewCharge.toc` without changing the manifest content.
- Update README with explicit steps to copy the inner addon directory, not the GitHub repository wrapper.
- Update roadmap, technical documentation, decisions, changelog, AI instructions and short first-person journal entry.
- Add standard-library packaging tests and a GitHub Actions workflow to check the folder and TOC layout on future changes.

## Verification
- Git tree inspection confirms exactly one installable Lua/TOC pair and no old root duplicates.
- Manifest lists `BuxbrewCharge.lua`, sets interface `11200` and preserves `BuxbrewChargeDB`.
- Both moved Git blobs have their original SHA; no Lua or TOC contents changed.
- **Not verified:** loading or behavior in a live WoW 1.12 client. Those earlier runtime concerns remain out of scope.

**Comment by chatgpt-codex-connector (2026-10-31):**

<!-- codex-pull-request-review-summary -->
<!-- codex-review-state:v1 {"code_review":{"commit_sha":"911cd01174e5ac887d37480be989c35b67f76908","has_any_findings":false,"has_unresolved_findings":false,"status":"completed"},"security_review":{"commit_sha":null,"has_any_findings":null,"has_unresolved_findings":null,"status":null}} -->

## Codex Review Summary

This comment shows the latest Codex review activity on this pull request.

| Review | Status | Commit | Review trigger |
| --- | --- | --- | --- |
| 📝 **Code Review** | ✅ **Completed** <relative-time datetime="2026-10-31T21:39:49.333844Z">2026-10-31T21:39:49.333844Z</relative-time> | `911cd01` | PR opened |



<details> <summary>ℹ️ About Codex in GitHub</summary>
<br/>

[Your team has set up Codex to review pull requests in this repo](https://chatgpt.com/codex/cloud/settings/general). Reviews are triggered when you
- Open a pull request for review
- Mark a draft as ready
- Comment "@codex review" or "@codex security review".

Codex reacts with 👀 while any review is running, comments if it has suggestions, and reacts with 👍 once all reviews finish with no findings.

</details>

### Pull request #3 — fix: restore WoW 1.12 event handling and remove unnecessary RNG seeding

*merged, merged 2026-10-31; opened 2026-10-31 by babunidev.*

## Why
Vanilla WoW 1.12 supplies `event` as an implicit global in `OnEvent` callbacks, unlike the newer `(self, event)` signature. The previous local parameter shadowed the real event. The login branch also called `math.randomseed`, which WoW documentation identifies as unavailable; the client seeds its generator itself.

## Changes
- Switch the callback to `function()` and read the implicit `event` global.
- Remove the now-unneeded `PLAYER_LOGIN` registration and `math.randomseed` call.
- Preserve the original action hook, ten-emote pool, cooldown, commands, saved variable and packaging.
- Add a mocked Lua legacy-event test and static contract tests; extend CI to run both.
- Update README, roadmap, architecture, decisions, changelog and a concise journal entry.

## Verification limits
Simulated Lua and static tests check event handling, action forwarding and saved-slot behavior without a WoW client. A real WoW 1.12 client test remains pending. No launcher-specific behavior is asserted.

**Comment by chatgpt-codex-connector (2026-10-31):**

<!-- codex-pull-request-review-summary -->
<!-- codex-review-state:v1 {"code_review":{"commit_sha":"c277943fad039885449f0623bb3062c3d329cb42","has_any_findings":false,"has_unresolved_findings":false,"status":"completed"},"security_review":{"commit_sha":null,"has_any_findings":null,"has_unresolved_findings":null,"status":null}} -->

## Codex Review Summary

This comment shows the latest Codex review activity on this pull request.

| Review | Status | Commit | Review trigger |
| --- | --- | --- | --- |
| 📝 **Code Review** | ✅ **Completed** <relative-time datetime="2026-10-31T21:48:04.063898Z">2026-10-31T21:48:04.063898Z</relative-time> | `c277943` | PR opened |



<details> <summary>ℹ️ About Codex in GitHub</summary>
<br/>

[Your team has set up Codex to review pull requests in this repo](https://chatgpt.com/codex/cloud/settings/general). Reviews are triggered when you
- Open a pull request for review
- Mark a draft as ready
- Comment "@codex review" or "@codex security review".

Codex reacts with 👀 while any review is running, comments if it has suggestions, and reacts with 👍 once all reviews finish with no findings.

</details>

### Pull request #4 — fix: correct emote token, validate action slots, allow first emote immediately

*merged, merged 2026-10-31; opened 2026-10-31 by babunidev.*

## Purpose
Improve the historical Action Emotes #1 addon for Turtle WoW / Octo WoW's modified 1.12 clients, without changing its single-slot trigger, 10-emote pool size, or the 21-second interval.

## Changes
- Correct the `/attacktarget` `DoEmote` token to `ATTACKMYTARGET` following Turtle WoW's emote token reference.
- Accept only whole-number action slots 1–120; reject out-of-range/decimal/non-numeric inputs without overwriting the configured slot.
- Initialize the last-emote timestamp as unset, allowing an emote on the first eligible press even when `GetTime()` is 0. Keep the 21-second cooldown thereafter and make `/bbc timer` report 0 seconds before the first emote.
- Extend CI's simulated Lua tests for the token, initial timer, cooldown boundaries, valid and invalid input, and original action forwarding.
- Update the docs, changelog and brief first-person development journal.

## Verification limitations
Automated tests simulate relevant 1.12 APIs using Lua 5.1. Turtle WoW and Octo WoW actual client testing is still necessary. No folder/TOC/launcher packaging or licensing changes in this PR.

**Comment by chatgpt-codex-connector (2026-10-31):**

<!-- codex-pull-request-review-summary -->
<!-- codex-review-state:v1 {"code_review":{"commit_sha":"d928164bd297be9f75785639604cacbf17720eec","has_any_findings":false,"has_unresolved_findings":false,"status":"completed"},"security_review":{"commit_sha":null,"has_any_findings":null,"has_unresolved_findings":null,"status":null}} -->

## Codex Review Summary

This comment shows the latest Codex review activity on this pull request.

| Review | Status | Commit | Review trigger |
| --- | --- | --- | --- |
| 📝 **Code Review** | ✅ **Completed** <relative-time datetime="2026-10-31T21:56:06.248477Z">2026-10-31T21:56:06.248477Z</relative-time> | `d928164` | PR opened |



<details> <summary>ℹ️ About Codex in GitHub</summary>
<br/>

[Your team has set up Codex to review pull requests in this repo](https://chatgpt.com/codex/cloud/settings/general). Reviews are triggered when you
- Open a pull request for review
- Mark a draft as ready
- Comment "@codex review" or "@codex security review".

Codex reacts with 👀 while any review is running, comments if it has suggestions, and reacts with 👍 once all reviews finish with no findings.

</details>

### Pull request #5 — docs: invite community testing and feedback

*merged, merged 2026-10-31; opened 2026-10-31 by babunidev.*

## Why
The creative no longer plays on the servers for which this addon was made and will not personally verify the updated code in-game. Community members remain welcome to try it and report feedback at babunigaming@gmail.com.

## Changes
- Add a clear community-testing invitation and contact address to the README.
- Distinguish outstanding live-client verification from scheduled personal work in the roadmap and architecture docs.
- Record the decision in the first-person development journal and decisions log; update the changelog and AI instructions.

## Verification
Documentation-only. All public narrative edits follow the first-person rule without sentences beginning in 'I' or 'My'. No Lua, TOC, tests or license were changed. No in-game validation is claimed.

**Comment by chatgpt-codex-connector (2026-10-31):**

<!-- codex-pull-request-review-summary -->
<!-- codex-review-state:v1 {"code_review":{"commit_sha":"a9f516f9c08809910518baaa579b46762f6ebba3","has_any_findings":false,"has_unresolved_findings":false,"status":"completed"},"security_review":{"commit_sha":null,"has_any_findings":null,"has_unresolved_findings":null,"status":null}} -->

## Codex Review Summary

This comment shows the latest Codex review activity on this pull request.

| Review | Status | Commit | Review trigger |
| --- | --- | --- | --- |
| 📝 **Code Review** | ✅ **Completed** <relative-time datetime="2026-10-31T22:30:13.805867Z">2026-10-31T22:30:13.805867Z</relative-time> | `a9f516f` | PR opened |



<details> <summary>ℹ️ About Codex in GitHub</summary>
<br/>

[Your team has set up Codex to review pull requests in this repo](https://chatgpt.com/codex/cloud/settings/general). Reviews are triggered when you
- Open a pull request for review
- Mark a draft as ready
- Comment "@codex review" or "@codex security review".

Codex reacts with 👀 while any review is running, comments if it has suggestions, and reacts with 👍 once all reviews finish with no findings.

</details>

### Pull request #6 — Improve README readability

*open; opened 2026-11-10 by babunidev.*

*Not merged. Its changes are kept on the branch `archive/ActionEmotes-1-pr6` of this repository.*

This documentation pass makes the README easier to scan and groups links by what the reader is looking for.
