# Phase 1 Storyboarding — Changelog

_Repo-only scoreboard. Answers one question at a glance: **is the claude.ai version behind, and by what?**_

How it works:
- A change lands in the repo → add a line under **⚠️ Pending upload to claude.ai**.
- You package + re-upload to claude.ai → move that line down to **✅ Live on claude.ai**.

This file does not upload or apply anything — it's just the honest list of what's pushed vs. waiting. (`package-skill.sh` excludes it from the claude.ai bundle, like `MAINTAINING.md`.)

Full version-history notes (v7, v6, v5, …) live below under **Version history**.

---

## ⚠️ Pending upload to claude.ai

- [2026-06-21] Naming pass — sidebars→sidenotes, agent observations→companion's observations, run/run log→practice/practice log (preserved runner, round, verb "run"). Also `<vault>`→`<notes-root>`, "notes vault"→"notes root folder", and the `phase1/runs/` path token throughout → `phase1/practices/`. Applied via `handoff/zz-archives/2026-06-20-naming-conventions-handoff.md` (folded in the 2026-06-20 vault-term things-to-do note). Pure terminology — no behavioral change.
- [2026-06-21] Practices folder reshaped — landed at `<notes-root>/practices/phase1/` (was `<notes-root>/phase1/practices/`). The structure is now `practices/` at the project root with a subfolder per phase. Decided after a grill: each phase skill only scans its own subfolder; if a runner studies the same source across phases they echo the title slug across logs; folder auto-created on first write. Convention documented in the project's CLAUDE.md so Phase 2/3/4 ports inherit it. On disk: moved Frieren log into `practices/phase1/`. Also updated MAINTAINING.md's stale `<vault>/phase1/runs/` reference. Zip name kept as `YYYY-MM-DD-HHMM-phase1-practice.zip`.

## ✅ Live on claude.ai

- [2026-06-20] v8 — Dual-mode delivery in Close-out: detect environment and act (never ask "claude.ai or Code?"). In Code → write run log + attachments to `<vault>/phase1/runs/` as before. In claude.ai → show run log as viewable artifact first, then on go-ahead bundle as `YYYY-MM-DD-HHMM-phase1-run.zip` for the runner to drop into the vault by hand — uploaded 2026-06-20
- [2026-06-20] v8 — Attachments handling branched by environment: Code uses jsonl extraction as before; claude.ai uses the chat-uploaded images directly (no jsonl access). Visually-verify-and-prune rule still applies both sides — uploaded 2026-06-20

---

## Version history

**v8 (2026-06-20)** — claude.ai-ready: dual-mode delivery + supporting infrastructure. The behavioral change is small (close-out delivery branches on environment), but it's the change that lets the runner use this skill on mobile via claude.ai instead of only in Code. Supporting infrastructure landed alongside:

1. **Dual-mode delivery (Close-out → Where it goes)** — borrowed wholesale from DNC. Code: write straight into `<vault>/phase1/runs/`. claude.ai: show the run log as a viewable artifact, wait for go-ahead, then bundle into `YYYY-MM-DD-HHMM-phase1-run.zip` and suggest saving to the vault by hand. Never ask the runner which environment they're in — detect and act.
2. **Attachments dual-mode** — Code: jsonl extraction (unchanged). claude.ai: use the runner's chat-uploaded images directly; no jsonl access. The visually-verify-and-prune rule applies both sides.
3. **`MAINTAINING.md` added** — repo-only maintenance notes (uploading-on-claude.ai protocol, sync-before-replace rule, CHANGELOG-as-scoreboard convention).
4. **CHANGELOG reshaped to a scoreboard** — ⚠️ Pending / ✅ Live sections on top answering "is claude.ai behind?". v7/v6/v5 notes preserved below under **Version history**.
5. **Symlinked into `resources/agent-skills-library/`** so `./package-skill.sh phase1-storyboarding` works the same way DNC does.

**v7 (2026-06-20)** — close-out beat + DNC-style references + learning loop. Applied via handoff `2026-06-20-phase1-closeout-and-references-handoff.md`. Major changes:

1. **Mode-pick at session start** — "Guided today, or loose?" Guided runs the 7-step structure with timers; loose drops the structure and lets the runner lead conversationally. Same close-out works for both.
2. **Multi-file DNC-style layout** — `SKILL.md` + `CHANGELOG.md` + `references/vocabulary.md` + `references/learned-patterns.md`. Changelog moved out of SKILL.md.
3. **Close-out beat** — fires after Step 7 in solo guided, after Step 5 in pair guided, after runner signals done in loose. Writes one Substack-style narrative run log per session to `<vault>/phase1/runs/` with three divider-separated sections (Narrative / Source & artifacts / Sidebars) plus an Agent observations footer (never empty).
4. **DNC-style attachments handling** — folder when extras, bare `.md` when not. Folder name matches `.md` name exactly. Attachment filenames `NN-short-descriptor-SOURCENAME.ext`. Auto-extract images from session jsonl at close-out + visually verify each fits the session.
5. **References lazy-load by moment** — nothing loaded during the 7 steps (secretary mode). Vocabulary loads at Step 5 annotate. All three references load at close-out (colleague mode).
6. **Secretary vs colleague modes named explicitly** — borrowed from DNC. Secretary = quiet conductor during the steps. Colleague = comes alive at close-out to synthesize.
7. **Propose-and-approve** — at close-out, agent scans recent runs for repeating Sidebar threads, surfaces as proposals. Runner approves → rule lands in `learned-patterns.md`.
8. **Propose-and-retire** — three staleness signals (contradicted / idle / direct request) tracked silently against active rules. Surfaces in promotion pass, not silently changed.
9. **Three-way promotion pass** — runs every 10–20 runs or on demand. Surfaces Promote / Retire / Keep buckets at once. Mature rules graduate into SKILL.md and are deleted from references; stale rules retire.
10. **Carrying-forward check at session start** — agent quickly scans recent runs for unresolved `*Carrying forward:*` items, surfaces them after mode-pick before prep.

**v6 (2026-06-18)** — full solo mode redesign from a step-by-step test run. Applied via handoff `2026-06-18-phase1-solo-redesign-handoff.md`. Numbered v6 (not v5 as the handoff drafted) because the prior 2026-05-31 bump already used v5. Changes:

1. **Prep opener reworded** — "want help choosing?" → "Got a favourite show, anime, or movie in mind? Describe the scene — I'll pull 5 YouTube links" — gives the person something concrete to do.
2. **YouTube search runs parallel to Step 1** — "Start your 5-min timer" fires immediately; search happens while they capture. Eliminates the search-as-blocker problem from previous sessions where 2 links produced too many misses.
3. **New Step 1 — Capture (5 min)** — dedicated frame-hunting pass. Scrub clips, screenshot resonant frames into Photos. Separates looking from drawing — two different modes of attention.
4. **3-pass sketch loop (Steps 2–4, 1 min each)** — rough shapes → resolve → focus. Matches Phase 2/3's iteration mechanic, compressed to 1-min passes on a single frame.
5. **Annotate rewritten (Step 5)** — "describe the frame like you're the director" replaces the anchor/feeling/why checklist. Camera position, movement, FG/MG/BG staging, what the composition is doing and why. One flowing read, not three bullet points.
6. **New Step 6 — Pitch (1 min, recorded)** — phone camera pointed at the frame. Sell the composition. Replaces the old wrap-up insight.
7. **New Step 7 — Post to Stories (3 min)** — post frame + pitch to 24-hour ephemeral social (Instagram Stories, TikTok Stories, Snapchat). Hashtags in a code block for copy-to-clipboard. Instagram 2026 caps at 5 hashtags; keyword-rich captions drive discovery.
8. **New Step 8 — Move. Play. 1 track.** — body reset. No timer — the song is the timer.
9. **Timer-cue-at-bottom pattern applied (solo only)** — addresses the Phase 4 v3 cross-skill flag. All timed solo steps now end with "▶ Start your X-min timer. Say done when it's up." Pair flow timer-cue update still open.
10. **Total solo time ~15 min** (was ~10 min). The added time is real structure, not padding.
11. **Session-template references stripped** — description line, "Goes on the template" in Session insight, off-script reword, and the "Replace the template" NOT-do bullet. The `.docx` template is retired; the skill is the sole session reference.

**v5 (2026-05-31)** — Step 2 "note up / one note that comes easiest" rewrite + official-channel link-verify sourcing on the Need-to-pick branch. Applied via handoff `2026-05-31-phase1-v5-bump-handoff.md`.
