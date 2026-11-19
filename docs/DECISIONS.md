# Decisions — Classic WoW Addons

## 2026-11-19 — One repository for the finished 1.12 and 3.3.5 addons

**Status:** Accepted. **Directed by:** Babuni.

**Choice:** The 20 addons for the 1.12 and 3.3.5 clients and the EnchantVisuals client mod live in this repository, one folder each, with their full Git history. Install zips are in `downloads/`. The former repositories are deleted after this one is published.

**Criterion:** Addons with entries for further development keep their own repository. The old roadmaps contained only verification checklists and unapproved ideas from the October 2026 documentation audits; Babuni decided these do not count, so all 21 moved. The active WoW Forever addons (FlourishForever, RoarForever, SocialForever, ResistForever, ClearViewForever, FavorCraft, GatherMap) stay separate; most publish to CurseForge, whose packager expects one addon per repository.

**Alternatives (AI-proposed):** One repository per client version (rejected: the 3.3.5 group has only two addons); archiving the old repositories instead of deleting them (rejected by Babuni because archived repositories stay in the GitHub list).

**Correction, same evening:** The Great Iceflow Relay was given a WoW Forever development plan at 20:43, after the roadmap check, so it returned to its own repository. The collection holds 19 addons and EnchantVisuals.

**Consequences:** On babuni.dev the 21 tiles become one project with a folder module per addon; old project addresses forward to it. Installing an old addon means downloading its zip from this repository rather than a release page.
