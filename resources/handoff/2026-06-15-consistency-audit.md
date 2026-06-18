# Consistency Audit — 2026-06-15

Scope: `skills/phase1-storyboarding/SKILL.md`, `skills/phase2-storyboarding/SKILL.md`, `skills/phase3-storyboarding/SKILL.md`, `skills/phase4-storyboarding/SKILL.md`, `skills/storyboarding-beat-generator/SKILL.md`, `README.md`.

`shared-principles.md` and `ideas-backlog.md` were not found anywhere in the repo — flagged below.

---

## Terminology drift

- [ ] **Phase names in beat-generator frontmatter are wrong.** The `storyboarding-beat-generator` description reads: *"across Phase 1 (Observation), Phase 2 (Constraint Sketching), Phase 3 (Break Genre), or Phase 4 (Intention First)."* Every other file (all phase SKILL.mds and README) names Phase 2 as **Sequence** (or "reading sequences") and Phase 3 as **Direct** (or "script-based / translating a script into shots"). "Constraint Sketching" and "Break Genre" look like old names that survived only in the beat-generator frontmatter. Fix: update the beat-generator description to match the current phase names used everywhere else.

- [ ] **"phone timer" (Phase 1) vs "iPhone timer" (Phases 2–4).** Phase 1 says "phone timer" throughout (intro, `Session shape`, `What this skill does NOT do`). Phases 2, 3, and 4 consistently say "iPhone timer." Pick one term and apply it across all four phases.

- [ ] **Phase 2 drawing surface omits tablet/iPad.** Phase 2 intro reads: *"The user does the drawing on paper."* Phases 1, 3, and 4 all say "paper or tablet" / "paper (or iPad)" / "paper or iPad." Unless Phase 2 intentionally prohibits digital, bring it in line.

- [ ] **"rough → resolve → focus" vs "rough → refine → focus."** Inside Phase 2 SKILL.md, the `What Phase 2 trains` paragraph describes the three passes as **rough → resolve → focus**. The step headers (Step 4 and Step 5) label them **refine** and **focus** respectively. The README also uses **refine**. "Resolve" is a lone outlier. Fix: change "resolve" in the Phase 2 intro sentence to "refine" (or update the step name — pick one and make them match).

---

## Step wording contradictions

- [ ] **Phase 1 session body time doesn't add up.** `Session shape` says *"one round, ~8 min body + ~5 min wrap-up after final round."* Adding Steps 1–3 for a pair: 5 min (sketch) + 5 min (annotate) + ~4 min (commentary, 2 min × 2 people) = ~14 min. Even solo is 10 min (per the Solo mode section). 8 min is wrong. Fix: recalculate and update the session shape summary line.

- [ ] **Timer-cue-in-header pattern still present in Phase 1 and Phase 3 — Phase 4 v3 changelog flagged it but did not apply the fix.** Phase 4's v3 changelog says: *"Cross-skill flag (not yet applied): the timer-cue-lost problem affects any conversational opening step holding its timer in the header. Check Phase 1 / Phase 2 / Phase 3 SKILL.md for that pattern; move the cue next to 'say done.'"* The unfixed instances:
  - **Phase 1 Step 1 header:** `### Step 1 — Set 5 min. Sketch 4 frames + 1 freestyle. Say done when time's up.` — timer is in the header, not at the action point.
  - **Phase 3 Step 1 header:** `### Step 1 — Script Generator. 4 min. Start your 4-min timer.` — timer is in the header.
  - Phase 2 Step 1 is borderline (timer appears in both the header via "4 min. GO!" and in the body as "Start your 4-min timer"), but the body line covers it.
  Fix per Phase 4's v3 pattern: move the timer-start cue to a `▶ Start your X-min timer. Say done when it's up.` line at the bottom of the step body.

- [ ] **Phase 4 v2 changelog references old step numbers that don't match the current v3 file.** The v2 changelog uses step labels from before v3 renumbering (e.g., "Step 1b" is now Step 2; "Step 3b" is now Step 5; "Step 7b" is now Step 11; "Step 10" is now Step 14). Most consequential: changelog item 11 says *"don't skip Step 8 or Step 9 when the user requests a session log mid-flow"* — the current `What this skill does NOT do` correctly says Step 12 or Step 13, so the functional text is right, but the changelog is misleading if read as a reference. Consider adding a brief note to the v2 changelog header that step numbers were renumbered in v3.

- [ ] **Phase 3 session shape table is missing a Round 2 hand-off row.** Phase 1 (Step 4), Phase 2 (Step 7), and Phase 4 (Step 12) all include a "Round 2 hand-off" row in their session shape tables. Phase 3's table goes directly from Step 7 (2nd Pitch + Notes) to Step 8 (Round wrap-up). The hand-off logic exists as a prose section after Step 7, but the table omits it. Minor, but makes Phase 3's table look incomplete relative to the other phases.

- [ ] **Phase 2 peer-to-peer glance is not in the session shape table.** A ~30-second optional glance is mentioned after Step 4 (2nd pass — refine) ends, but it has no row in the session shape table. All other inter-step actions are either in the table or explicitly marked as optional/unlisted. Clarify or add a "(optional) Peer glance — 30 sec" note to the table.

---

## Missing files and dead references

- [ ] **`shared-principles.md` does not exist.** Not found anywhere in the repo. If it was planned, create it; if it was abandoned, remove any references to it (none found in the SKILL.mds, but it was part of this audit's scope — confirm whether it was ever intended to exist here).

- [ ] **`ideas-backlog.md` does not exist.** Same as above.

- [ ] **`session-log-companion` skill referenced but missing.** Phase 4 SKILL.md references the `session-log-companion` skill extensively (SLC integration section, Step 13 hand-off, `What this skill does NOT do`). No `skills/session-log-companion/` directory or SKILL.md exists in the repo. Either add the skill file or add a `(parked)` note to every reference the way `animatic-from-existing-boards` is handled.

- [ ] **`workshop-3hr` skill referenced in README but missing.** README lists `workshop-3hr` as a supporting skill and shows install instructions for it. No `skills/workshop-3hr/` directory or SKILL.md exists. Same fix as above.

- [ ] **Session template paths cannot be verified (exist outside this repo).** All four phases reference template files:
  - Phase 1: `resources/phase1-session-template/phase1-session-template-v3.md`
  - Phase 2: `resources/phase2-session-template/phase2-session-template-v3.md`
  - Phase 3: `resources/phase3-session-template/phase3-session-template-v1.md`
  - Phase 4: `resources/phase4-session-template/` (noted as future)
  These are noted as living "in the user's project directory," so they're expected to be absent here. No action required in this repo, but note that Phase 4's template path placeholder may want to be promoted to a real path once created.

- [ ] **`workflow-knowledge-logs/2026-05-14-2143-Emergent-vs-Taught-Patterns.md` referenced in beat-generator but not in repo.** The beat-generator SKILL.md links to this path in the "Register shapes" section. Not found in repo. Same category as the session templates — lives in the user's project directory — but worth confirming.

---

## Suspicious or stale links

- [ ] **`http://www.floobynooby.com/comp1.html` (Phase 1, Step 5 references section)** — HTTP only, no HTTPS; site is old and may be down. Verify it loads; if dead, find an archived version or replacement.

- [ ] **`https://www.youtube.com/user/everyframeapainting` (Phase 2, Step 8 references section)** — Old YouTube URL format (`/user/`). The channel moved to `/@everyframeapainting`. The old URL may redirect but is non-canonical. Update to: `https://www.youtube.com/@everyframeapainting`

- [ ] **Phase 2 Dropbox library link** — `https://www.dropbox.com/scl/fo/1g8mnw19i9022my3ovgr6/...` contains time-sensitive query params (`st=z4w5r8m4`). These Dropbox shared-folder `st=` tokens can expire. Verify it still loads; regenerate the share link if needed.

- [ ] **`https://www.routledge.com/Cutting-Rhythms-Creative-Film-Editing/Pearlman/p/book/9781041024088` (Phase 2)** — Routledge restructures URLs periodically. Spot-check that this resolves to the correct 3rd-edition book page.

- [ ] **`https://procreate.com/handbook/procreate/animation/animation-assist/` (Phase 4)** — Procreate migrated from `procreate.art` to `procreate.com`. The handbook path structure may have changed. Verify the URL resolves to the Animation Assist page.

- [ ] **`https://www.youtube.com/results?search_query=pixar+animatic+vs+final` (Phase 4)** — This is a YouTube search URL, not a stable link. Results vary over time and the most relevant videos rotate. Either link to a specific video or acknowledge in the text that it's a search prompt rather than a curated link.

- [ ] **`https://vsquad.art/blog/what-is-staging-in-animation-a-complete-beginners-guide` (Phase 1)** — Spot-check; small-studio blog URLs frequently go stale.

- [ ] **`https://underpaintacademy.com/product/storyboarding-the-art-of-pitching-with-patrick-harpin/` (Phase 3)** — Spot-check; academy product pages (courses/workshops) come and go.

- [ ] **`https://blog.celtx.com/what-is-a-story-beat/` (Phase 3)** — Celtx has changed their blog structure. Spot-check this resolves.

---

## Lower-priority notes (no action required now, but log for future)

- The Phase 4 v3 changelog notes the timer-cue fix applied to Phase 4 Step 1 and flags Phase 1–3 as needing the same fix. The items above cover Phase 1 and Phase 3; Phase 2 Step 1 is borderline-OK but worth a second look if Phase 1 and Phase 3 are being touched anyway.

- Phase 4 `Session shape` total in-session time is listed as ~30 min, but timed steps alone (Steps 1–11 excluding untimed steps 0, 5, 12) sum to ~34 min before the wrap-up. The ~30 min figure is likely an approximation rounded from a faster-running session. Not wrong enough to be confusing, but worth updating if the step timings are ever revised.

- Phase 4 Step 2 conductor note says it is "borrowed from Phase 3's script generator schema." This is accurate in spirit but imprecise: Phase 3's schema asks for characters' wants + obstacle + tone + anchor + shift, while Step 2 asks for who's in frame + anchor + environmental shift. If the connection matters, clarifying "adapted from" vs "borrowed from" removes the potential confusion.

- Phase 4 `Solo-round mode` footnote and Phase 3 `Solo-round mode` footnote both say "Building a dedicated solo skill is parked for a future iteration." These are consistent, but worth linking or cross-referencing them once one is built so neither becomes stale independently.
