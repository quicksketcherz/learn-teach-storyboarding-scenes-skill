# Maintaining this skill

_Repo-only notes — `package-skill.sh` excludes this file from the claude.ai bundle._

## Updating on claude.ai — never hand-pick files
claude.ai installs a skill as **one bundle**. If you upload just `SKILL.md`, the
`references/` files (`vocabulary.md`, `learned-patterns.md`) get silently dropped
and the skill misbehaves with no error. **Always upload the whole folder.**

Don't zip by hand — from the repo root (`agent-skills-library/`) run:

```
./package-skill.sh phase1-storyboarding
```

That zips the entire folder to `dist/`, refuses to package if the description is
over the **1024-char limit**, and prints what's inside. Then:

claude.ai → **Settings → Capabilities → Skills** → re-upload that whole zip.

## Before you replace the skill on claude.ai — sync references back FIRST
Re-uploading **replaces the entire bundle**. Any reference edits that surfaced
during claude.ai sessions — new vocabulary in `vocabulary.md`, new rules in
`learned-patterns.md` — live *only* in the claude.ai copy and are **gone** the
moment you upload a new version.

So the order is always:
1. **Merge first.** Paste any new vocabulary / learned patterns from your
   claude.ai sessions into the **repo** copies of the reference files (the source
   of truth). For now this is a manual paste — phase 1 doesn't yet have a
   self-describing repo-sync block like DNC's `dnc-repo-sync v2`. If a claude.ai
   session generates a lot of edits, consider porting that block over too.
2. **Repackage** with `package-skill.sh` (step above).
3. **Then** delete / re-upload on claude.ai.
4. **Update the scoreboard.** In `CHANGELOG.md`, move every line you just
   shipped from "⚠️ Pending upload to claude.ai" down to "✅ Live on claude.ai".

If you delete before merging, you lose the additions. The repo must always be
ahead of (or equal to) what's live on claude.ai — never behind.

## CHANGELOG.md — the sync scoreboard
A repo-only list of changes split into **⚠️ Pending upload** and **✅ Live on
claude.ai**, with the full version-history notes (v8, v7, v6, …) preserved
below under **Version history**. New change → add a ⚠️ line; after re-upload →
move it to ✅. The scoreboard tells you at a glance whether the claude.ai bundle
is behind. It does nothing automatic — it's just the honest list so nothing gets
forgotten. Excluded from the bundle by `package-skill.sh`.

## Practice-log destination — where the skill writes its session output
The skill itself writes one practice log per session to `<notes-root>/practices/phase1/`
(Code) or a `YYYY-MM-DD-HHMM-phase1-practice.zip` for the runner to drop in
(claude.ai). This is data, not skill-source — it never goes back into the skill
folder. If the delivery mechanic changes (e.g. new filename pattern, new section
structure in the practice log), update both branches in SKILL.md's **Close-out →
Where it goes** section and add a ⚠️ CHANGELOG entry.

## Updating for Claude Code — nothing to do
This skill is symlinked from `~/.claude/skills/phase1-storyboarding`, so editing
the files here is already "installed" (live on the next Claude Code restart).
The same source folder is symlinked into `resources/agent-skills-library/` so
`package-skill.sh` can find it — one source of truth, two symlinks.

## Three-way promotion pass — runs alongside re-packaging
At re-packaging time, also run the **three-way maintenance pass** described at
the bottom of `SKILL.md` (Promote / Retire / Keep) over `references/learned-patterns.md`.
Mature workflow rules graduate into SKILL.md and are deleted from learned-patterns;
stale or contradicted rules retire. The pass is what keeps `references/` a holding
pen instead of an archive that grows unboundedly.
