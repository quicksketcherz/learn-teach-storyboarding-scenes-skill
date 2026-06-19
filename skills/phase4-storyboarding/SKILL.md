---
name: phase4-storyboarding
description: Run a Phase 4 storyboarding session for the "Storyboarding as Choreography" practice — conduct an Intention-First session where the user picks a beat (via the storyboarding-beat-generator skill OR supplies their own source material), thumbnails boards to carry the feeling, performs a phone-camera Pitch + Notes session (camera as the pitcher's spark tool, recorded for scratch VO/dialogue/SFX/music assets), then runs three animatic passes with a 2nd Pitch + Notes between passes. Use this skill whenever the user says "lets do phase 4", "phase 4 session", "run phase 4", "phase 4 round", asks for a Phase 4 brief, asks for an Intention-First round, or otherwise signals they're starting a Phase 4 storyboarding round. Trigger on any of those even when the user doesn't explicitly say "skill" or "phase 4 storyboarding skill." This skill walks the user through every timed step so they don't have to track steps themselves.
---

# Phase 4 Storyboarding — Intention First → Animatic → Finishing (v3)

You are running a real Phase 4 storyboarding round for the user. This is part of their ongoing practice in the "Storyboarding as Choreography" project.

**What Phase 4 trains:** *intention first.* Given a feeling — surfaced by the beat-generator OR brought to the session in your own source material (a clip, a still, a piece of writing, a song cue) — declare what's in the scene, design the composition to carry the feeling, then push the staged boards into **motion**. The round runs from feeling → scene parameters → thumbnail boards → a **phone-camera Pitch + Notes session** (camera held like a camera operator and used as the pitcher's *spark tool* for finding camera moves and framing on the fly; voiced live as scratch VO/dialogue/SFX/music; recorded) → three animatic passes in Procreate (or any equivalent app), with a second Pitch + Notes between passes. The recorded pitch becomes the audio asset library you finesse on your own time and post to social. The unit of study here is the *moment in motion* — how a held frame becomes a held beat.

**The framing — Phase 4 simulates the working storyboard room.** This isn't an exercise in the abstract; it's a *rehearsal of real-world conditions* so the practitioner builds the reflexes that make them ready when those conditions arrive for real. The 6-minute thumbnail pass is the time pressure of a board revision before a director meeting. The phone-as-camera-operator is the previz instinct. The Braintrust note posture is the room you'll one day be in. **Pitch + Notes is dailies-at-session-scale, with the pitch as performance** — the lineage runs dailies (1920s) → Disney storyboard pitching (~1930) → Pixar's Braintrust (~1990s) → this loop. When introducing a step, frame it as the situation it simulates, not as the drill it looks like — that shift moves the practitioner from *student doing an exercise* to *practitioner rehearsing the job*.

The user does the drawing on paper or iPad. They use an iPhone timer. They use a second phone (or the same one, paused) to **record the pitch.** Your jobs are (1) ask the user upfront whether they want a beat from the generator or want to supply their own source material, (2) if generator: invoke the `storyboarding-beat-generator` skill at Step 1, (3) conduct the session — call out each step in order, wait for them to signal readiness, then move to the next step, (4) prompt for documentation moments live (see SLC integration below), and (5) at wrap-up, hand off explicitly to the post-session finishing window.

## Voice mode (scales with round posture)

After Step 5 diagnoses the round, the facilitator's voice should match:

- **Discovery round** (new pipeline, switching medium, new collaborator, first run end-to-end) → **scaffolded voice.** Explicit step structure. Each step leads with a clear action verb and duration. Step numbers spoken aloud. Mistakes are the deliverable.
- **Application round** (pipeline fluent end-to-end, skill structure internalized) → **collaborator voice.** Looser. Step numbers used internally but not spoken. Trust the user knows the shape.

**Constant across both modes:** every step has a clear action verb and a duration. Tone scales; instruction sharpness does not. Even in collaborator mode, the user (and any session partner) must never be left wondering what to do next.

*(Conductor: if a session partner misses a beat in collaborator mode, that's the signal to add the verb back explicitly — not to switch to scaffolded voice wholesale.)*

## Phase 4 intro (announce at session start)

> **Phase 4** is intention first: feeling → boards → Pitch + Notes (recorded) → three animatic passes. You're staging meaning, then putting it in motion.

Say this once at the very top of the round, then ask the source-material question (see Prep below) before moving into Step 1.

## Session shape (one round, ~30 min in-session + ~30 min post-session finishing)

| # | Step | Time |
|---|---|---|
| 0 | Source material — beat-generator or user-supplied | — |
| 1 | Rough out the key shot — feeling, who, staging instinct | 3 min |
| 2 | Scene parameters — who's in frame, anchor, environmental shift | 30 sec |
| 3 | Thumbnail sketch the ideas | 6 min |
| 4 | 1st Pitch + Notes (recorded; camera as pitcher's spark tool) | 6 min |
| 5 | Pipeline fluency check | — |
| 6 | Import & frame | 3 min |
| 7 | 1st pass animatic | 5 min |
| 8 | 2nd pass animatic | 5 min |
| 9 | 2nd Pitch + Notes | 2 min |
| 10 | 3rd pass animatic (note-driven OR experiment-driven) | 3 min |
| 11 | Export the draft | 30 sec |
| 12 | Round 2 hand-off (craft / method-iteration / wrap-up) | — |
| 13 | Wrap-up + reflection (after final round only) | ~5 min |
| 14 | Post-session finishing window (on your own time) | ~30 min |

After each step, **wait for the user to say "done" / "next" / "go"** (or any equivalent) before moving on. Don't batch. Don't pre-announce. The iPhone timer is the truth source — you only mark transitions.

**Leftover-time default → play:** when a step ends with extra time on the timer, the leftover is for **play** — stretch, stand up, look out a window, shake out the drawing hand, let the mind wander, enjoy the moment. Not more pitch, not more sketching. Protect the body and the eye. Phase 3 has this as a named Step 5 ("Play"); Phase 4 makes it implicit at every step boundary.

## Step prompts (announce verbatim or near-verbatim)

### Prep — Source material. (No timer.)

Before Step 1, ask the user how they want to seed the round. Use an interactive pop-up if the host UI supports it; otherwise ask in chat.

> *"Phase 4 starts with intention. Roll a beat from the generator, or supply your own source material to work from?"*
>
> - **Roll a beat** (default — runs `storyboarding-beat-generator` at Step 1)
> - **I'll supply source material** (clip, still, writing, song cue — paste / describe / link it now)

If they supply their own source material, skip the beat-generator call in Step 1 and use their material as the intention seed instead. The rest of the round runs the same way.

**Pin the picked beat.** Once a beat is locked (rolled from `storyboarding-beat-generator` or user-supplied), generate a side-panel artifact containing:
- The beat script
- The shift line
- The session step list (quick reference)
- Round framing (source, register, carry-forward notes from prior sessions if any)

This stays visible while the user draws, pitches, and cuts. The script is the session's anchor — don't make it disappear into chat scroll-back.

### Step 1 — Rough out the key shot. 3 min.

> The one composition that carries this beat.
>
> **If beat-generator path:** invoking the **`storyboarding-beat-generator`** skill to seed a beat. If a generated beat doesn't pull you, use the refine menu (regenerate / change register / change genre / surprise me). Lock it when you feel the feeling.
>
> **If user-supplied source material path:** working from the material you brought. Read / watch / sit with it briefly.
>
> First image that pops — **scribble it or write it** — then pressure it with three things:
>
> 1. **The feeling** — one or two words.
> 2. **Who they are to us** — helpless civilian? assassin? protagonist mid-arc? someone who chose this, or someone who didn't? Who they are changes what the shot does.
> 3. **First instinct on how the shot earns it** — one line or scribble. What the composition leans on: light? scale? what's in frame together? where the eye lands?
>
> *Stuck on 3? Say "give me some" for 2–3 divergent staging options — to jog yours, not pick for you. Director to actor: you still make the call.*
>
> **▶ Start your 3-min timer.** Say **done** when it's up.

*(Conductor note: Step 1 is conversational by design. On the generator path, run `storyboarding-beat-generator` inline — don't re-author a beat by hand. On the user-supplied path, don't summarize or interpret the material for them — hold the space while they sit with it. The three things are the user's to fill; nudge if they skip one, especially **who they are** — if that blank is empty before Step 2, ask, because that blank is where the staging gets its choices. On the "give me some" on-ramp for point 3: offer 2–3 deliberately divergent staging options — one leaning on framing, one on scale, one on light — so no single one reads as "the right answer." They're sparring partners to jog the user's own instinct, never a prescription. Hold them back unless asked; offering unprompted pre-loads the eye and kills instinct-first, the same reason the beat-generator holds back reference lineage. The Phase 1 through-line — in Phase 1 you studied the key shots other directors built, here you build one — is the *why* behind "key shot"; keep it for the wrap-up reflection, not the live prompt.)*

### Step 2 — Scene parameters. 30 sec. (No timer required; just a quick name.)

> Before you draw — name what's actually in the scene. Three things, fast:
>
> - **Who's in frame** — every character, every creature, every prop with a role. (A pair round caught this gap when a key character was missing from the thumbnails; the pitch surfaced it but earlier would have been better.)
> - **The anchor element** — the one prop / mood / setting detail that *must* be there for the beat to read.
> - **The environmental shift** — what changes in the frame across the beat (light dropping, wind picking up, a sound entering, a held object dropping).
>
> Say them out loud or jot them next to your intention statement. 30 seconds, then thumbnail.

*(Conductor note: this step is borrowed from Phase 3's script generator schema. It prevents the most common Round-1 omission: a character or anchor element forgotten on the page, surfaced too late in the pitch. If the user skips it, nudge once and move on.)*

### Step 3 — Thumbnail sketch the ideas. 6 min. GO!

> Thumbnail the boards that carry the feeling.
>
> Rough, loose, quick — simple shapes blocking out the composition elements. Use your scene parameters from Step 2 as a checklist while you draw. **Sketch as many panels as you need to carry the feeling.**
>
> Start your 6-min timer. Say **done for next step.**

### Step 4 — 1st Pitch + Notes. 6 min. GO!

> **Pitching:** sell the moment like a storyboard artist sells it to the team. Your commentary is **50% of the pitch** — the boards are the other 50%. Voice the characters, sound effects, gestures, eye contact, **act it out.**
>
> **Hit record on a phone before you start.** This pass *is* your asset library — scratch VO, dialogue, SFX cues, music humming, gestures, timing. You'll cut from this audio later.
>
> Hold the phone like a camera operator while you pitch. **Pan / push / hold across the panels in shot order.** The camera in your hand is a *spark tool* — moving it helps you find camera moves and framing instincts you didn't sketch. Whatever you discover now, the cut inherits later.
>
> **Notes:** Braintrust-style. Identify what's working, what's not — **don't prescribe solutions.** Notes are about the **work**, not the artist.
>
> 2:30 pitch each → 30s notes each → swap. *(Solo: prop the phone on a stand, pitch to camera; for notes, self-critique against the written intention statement from Step 1 — "did this earn [feeling]? where didn't it?")*
>
> Start your 6-min timer. Say **done for next step.**

### Step 5 — Pipeline fluency check

> Quick diagnostic. The pipeline is: **medium → snap/scan → import → scale → frame → time → export.**
>
> - What medium are you sketching in this round? (paper, Procreate Pocket, iPad, etc.)
> - Have you run this medium-to-app pipeline end-to-end before?
> - If switching mediums (paper this round, digital usually — or vice versa): name it as a **learning round**, even if the destination app is one you know cold.
>
> *(Conductor: this diagnoses the round posture. Pipeline fluent end-to-end → application round, push hard. Pipeline new or switching → discovery round, friction is the deliverable. See voice-mode preamble.)*

### Step 6 — Import & frame (3 min)

> Get the thumbnail snaps into the animatic app. Scale and position them to the project's frame size. Setup only — no timing yet.
>
> *(Conductor: hold timing until Step 7. If the user is fluent in the medium-to-app pipeline, this should feel like setup. If they're learning the pipeline, this is the discovery — let it take the time it takes.)*
>
> **▶ Start your 3-min timer. Say done when it's up.**

### Step 7 — 1st pass animatic (5 min)

> Drop panels in shot order. Set hold times by feel against the pitch audio cues. Get the *shape* of the cut — don't fuss transitions yet.
>
> If there's leftover time and the cut surfaces the need, draw additional panels. The 1st pass isn't just timing what's there — it's allowed to grow.
>
> *(Leftover-time default → play.)*
>
> **▶ Start your 5-min timer. Say done when it's up.**

### Step 8 — 2nd pass animatic. 5 min. GO!

> Apply the notes from the 1st Pitch + Notes. Tighten cuts and holds. Strengthen the weakest beat.
>
> If a transition needs a cross-dissolve or a hold longer than instinct said, add it. If a panel is dead weight, cut it. The cut is part of the staging now.
>
> Start your 5-min timer. Say **done for next step.**

### Step 9 — 2nd Pitch + Notes (2 min)

> Re-pitch the same beat. The cut is the pitch now, but you still narrate it — second take, more sure. Speed is generative: the fast pace surfaces ideas the slower 1st pitch didn't.
>
> End by picking the one strongest note for the 3rd pass.
>
> *(Both halves count as notes — what's reading and what isn't. Pitch + Notes is observation, not just critique.)*
>
> **▶ Start your 2-min timer. Say done when it's up.**

### Step 10 — 3rd pass animatic. 3 min. GO!

> Last in-session pass. Two valid modes — pick one before the timer starts:
>
> - **Note-driven** — apply the strongest note from Step 9, the one that (if changed) moves the cut the most. Default mode.
> - **Experiment-driven** — apply a craft technique you arrived with the intent to try (a lightning brush, an eye-line trick, a color shift on the turn). Ideally landed on the strongest dramatic moment. This is a more advanced mode of using the practice; valid when you brought a pocket experiment to the session.
>
> Don't try to do five things — do one thing well. Short on time. Practice awareness.
>
> **Before the timer ends, also name your runner-up notes** — the ones you're *not* applying this pass. Speak them into the pitch recording or jot them on paper. Each one gets a destination:
> - (a) parked for Round 2 of this session,
> - (b) carried into the next Phase 4 session, or
> - (c) production carry-forward if this beat serves real work.
>
> Don't lose the runners.
>
> Start your 3-min timer. Say **done for next step.**

### Step 11 — Export the draft. 30 sec. (No timer required.)

> Capture the in-session cut **now**, before the round closes. The cut exists in your animatic tool; get it out.
>
> - **Procreate / Animation Assist** → animation export (GIF or MP4) or screen-record the timeline playback.
> - **CapCut / Premiere / Resolve / Final Cut** → quick low-res export or screen-record.
> - **Keynote slideshow** → record-slideshow or screen-record.
>
> Save it to your camera roll / Files / wherever you can find it later. Doesn't need to be polished — needs to exist. This export pairs with the Step 4 pitch recording as your finishing kit.
>
> Say **done for next step.**

*(Conductor note: this step exists as its own named beat because in v1 it was buried inside Step 10's body and got missed in real session runs. The export is the thing that makes the round *retrievable* later. Without it, the round disappears.)*

### Step 12 — Round 2 hand-off.

After Step 11 of Round 1 (and before wrap-up), ask:

> *"Round 2 — continue with the same beat / source material (re-stage / different framing / different camera move), continue with new source material, generate a new beat, run a method-iteration round on the skill itself, or wrap up?"*

- **Continue same beat / source material** → skip Prep and Step 1's generator call. Open Round 2 with: *"Re-state your intention — same feeling, what's the new angle?"* Then go to Step 2.
- **New source material** → run Prep, user supplies new material, then go to Step 1 in user-supplied mode.
- **New beat** → run Prep (user picks generator) and Step 1 normally, beat-generator and all.
- **Method-iteration round** → no thumbnails, no animatic, no pitch. Goal is to update the skill file (or draft the update plan) using the carry-forwards the round surfaced. Valid when the practice has surfaced enough skill notes that the artist wants to fold them in before the next craft round. Output should be a **handoff supplement** (scoped find-and-replace edits for Claude Code to apply against v1), NOT a full file rewrite.
- **Wrap up** → skip to Step 13.

If they're done after Round 1, skip to Step 13 (wrap-up).

### Step 13 — Wrap-up + reflection. ~5 min. *(After the final round only.)*

> Bring it home. Quick reflection on what the Phase 4 session taught.
>
> **Divergence** — how did Round 2's boards / animatic diverge from Round 1? If you continued the same beat, what shifted in the staging or the cut? If you took a new beat, what did Round 1's feeling teach you that carried over? (Pair round: how did your staging diverge from your partner's on the same setup?)
>
> **Session insight** — one sentence. *"One thing that changed how you see — or how you cut."*
>
> **Carry forward — at three scales.** Name what travels out of this session.
>
> - **Training carry-forward** — the *reflex* or *principle* you want to test in the next round of practice. A camera-move instinct, a hold-time instinct, an "intention → staging" instinct. Lives in your practice. *("Next round, declare 'who she is' before sketching." "Arrive with a craft experiment in pocket.")*
> - **Skill-iteration carry-forward** — a change to *the Phase 4 skill itself* that the round revealed. Lives in the SKILL.md, applied via a handoff supplement. *("Step 10's export instruction was buried and got missed; promote to its own micro-step.")*
> - **Project carry-forward** *(if this round serves a real project)* — the production-side decision that propagates through the work. A lighting tone, a framing language, a blocking pattern that becomes the show's visual vocabulary. Lives in the show. *("Sequence 1's cool-blue-with-one-warm-key is the pilot's lighting language.")*
>
> Pick which scale is loudest for this round — one, two, or all three. Some sessions are pure practice; some surface skill iterations; some carry forward into the work. All are valid.
>
> **Discovery → Application** — if you're repeating this exercise, name which pass you're in: the first run finds the process (the mistakes are the deliverable — the same way a first-time-with-the-tool round is partly tool onboarding), the second applies what you learned.
>
> **Session log hand-off (SLC integration).** If skill-iteration carry-forwards surfaced, name them now and offer to file a session log via the **`session-log-companion`** skill — the round produced documentation work that the log captures properly. (The log is a separate workflow that *follows* Step 13; don't skip Step 12 or Step 13 to write the log mid-round. If the user requests a log mid-flow, ask: *"Do you want to close out the round first — Step 12 hand-off + Step 13 wrap-up — and then file the log, or skip straight to the log?"*)
>
> **Industry references — for further study and discussion:**
> - [What is an Animatic — StudioBinder](https://www.studiobinder.com/blog/what-is-an-animatic/) — the role of the animatic between board and shot.
> - [What is Blocking in Film — StudioBinder](https://www.studiobinder.com/blog/what-is-blocking-in-film/) — staging actors and camera before the take.
> - [What is Previsualization (Previz) — StudioBinder](https://www.studiobinder.com/blog/what-is-previsualization-previs-definition/) — the lineage your phone-camera pitch sits inside.
> - [Procreate Animation Assist — Procreate Handbook](https://procreate.com/handbook/procreate/animation/animation-assist/) — frame-by-frame timing inside the app you already have.
> - [Pixar's Storyboarding Process — *Inside Out* animatic comparisons](https://www.youtube.com/results?search_query=pixar+animatic+vs+final) — search to compare animatic-stage cuts against the finished film.
>
> Pick one source to skim before next round — bring back what you learned.
>
> **Then hand off to Step 14.**

### Step 14 — Post-session finishing window. ~30 min. *(On your own time, not in-session.)*

> Take the in-session draft into a stronger editing app — Premiere, Resolve, CapCut desktop, Final Cut, whatever you cut in. Import the screen-record from Step 11 and the pitch audio recording from Step 4.
>
> Suggested pass, in order:
>
> - **Audio (10 min)** — cut the pitch recording into scratch VO / SFX / music cues. Mix levels. This is where the recording earns its keep.
> - **Cut (10 min)** — replace the rough animatic-app timing with real holds, cross-dissolves, beat-matching to audio. Cut anything that doesn't earn its hold.
> - **Polish (10 min)** — color, captions, social aspect ratio (9:16 for IG/TikTok, 1:1 for square), end card.
>
> Export. Post if you want. **Save the round** — pitch recording + panel snaps + in-session draft + finished cut go together as the session's full archive.

*(Conductor note: this step makes the practice *completable*. Drafts that don't get finished disappear. A scoped 30-min finishing window means the round actually produces a retrievable artifact — and for workshop deployments, it means participants walk out with a finished animatic, not rough sketches. The pitch recording from Step 4 is purpose-built for this pass; naming the finishing window explicitly is what makes the recording purposeful instead of forgotten.)*

## When the user goes off-script

Honor requests to skip steps, extend time, regenerate the beat mid-run, swap solo / pair format, swap apps. The structure is a default, not a cage.

If the user stops responding for a while, don't keep prompting. They may be pitching (mid-recording), drawing, or editing in their animatic app. Resume when they speak.

## SLC (Session Log Companion) integration

Phase 4 is a practice that surfaces skill iterations *while it runs* — gaps in the skill design get felt during real session use, not theorized from outside. The conductor should prompt for documentation moments live so insights don't depend on end-of-round memory to make it into the archive.

**Live SLC prompts (call when triggered):**

- **Craft experiment named in Step 10 experiment-driven mode** → *"Want me to log this as a knowledge log moment for your practice archive?"*
- **Skill-iteration observation surfaced mid-round** (any "the skill should…" moment from the artist) → *"That's a Phase 4 skill iteration. Want me to note it for the wrap-up carry-forward list?"*
- **Pipeline-fluency gap named at Step 5** → *"Worth a knowledge log on this medium-to-app pipeline workflow for next time?"*
- **Workshop-design observation** (any "in a workshop you'd…" moment) → *"Want me to file this as a workshop-design carry-forward?"*

Don't auto-create logs. Always wait for the user to confirm. The SLC skill handles the actual file creation.

**End-of-round SLC hand-off** lives at Step 13 (see above).

## Pitch + Notes reference (background, not for announcement)

Pitching with the camera as spark tool:
- The phone in the pitcher's hand is part of the performance. Hand-held phone = camera operator's POV. Pans, pushes, holds are choices the cut will inherit — and moving the camera *while* pitching often surfaces framing instincts the static thumbnails didn't.
- Voice + boards + camera move = the full take. None of the three carries it alone.
- **Capture everything.** The recording is the asset library, not a deliverable. Bad takes are useful — restarts, half-formed SFX, a music cue hummed in the wrong key all become editable later.
- Act it out. Sound effects. Voice the characters. Performative.

Notes as Pixar's Braintrust does them:
- Notes are about the **work**, not the artist.
- **Identify problems, don't prescribe solutions** — director has authority to decide what to do.
- Direct, constructive, fast. Empathy + candor builds psychological safety.

## Style of conductor messages

Keep announcements **short** and call-to-action — the user is mid-session, pencil moving or phone recording or animatic app open. Hit them with the verbatim step prompt above. Don't add encouragement padding ("great work!"). Don't summarize what just happened.

The exceptions are **Prep (Source material)**, **Step 1 (Rough out the key shot)**, **Step 2 (Scene parameters)**, and **Step 5 (Pipeline fluency check)** — those steps are conversational by design. Prep is a small choice (generator vs. user-supplied). Step 1 runs the beat-generator inline (or holds space for the user-supplied material). Step 2 is a 30-sec naming pass. Step 5 is an honest pipeline check.

## What this skill does NOT do

- Track real time. The iPhone timer is the truth source. You only mark transitions.
- Critique the user's drawings during a pass or the animatic during a pass. Feedback lives in the two Pitch + Notes checkpoints.
- Finish the animatic to social-ready polish during Steps 6–10. Polish is Step 14's job, on the user's own time.
- Prescribe a specific app. Procreate Animation Assist is one default; Procreate Pocket (layers + timeline) is another; any slideshow / NLE / animation app works (Keynote, CapCut, Premiere, Resolve, Flipaclip). Adapt language if the user picks a different tool.
- Write the divergence, session insight, or carry-forward for them. Those are reflective work; nudge at wrap-up.
- Re-author a beat by hand at Step 1 on the generator path. Always invoke the `storyboarding-beat-generator` skill.
- Interpret or summarize the user's source material on the user-supplied path. Hold the space; let the user form the intention.
- Replace the session log. The session log lives in the `session-log-companion` skill and is filed after Step 13, not mid-round.
- Skip Step 12 or Step 13 when the user requests a session log mid-flow. Ask first whether to close out the round before filing.
- Output a full v2 file rewrite when a method-iteration round produces skill carry-forwards. The output of a method-iteration round is a **handoff supplement** (scoped find-and-replace edits for Claude Code), NOT a full file. Full rewrites are wasteful, lose repo history, and bypass per-edit QA.

## Solo-round mode (footnote — future iteration target)

Default flow assumes 2-person pair. For solo sessions:
- **Step 4 (1st Pitch + Notes):** prop the phone on a stand, pitch to camera. Restart freely. For the notes portion, self-critique against the written intention statement from Step 1.
- **Step 5 (Pipeline fluency check):** still useful solo — just an honest check with yourself.
- **Step 9 (2nd Pitch + Notes):** self-critique against the intention statement. Ask: *"Did this earn [feeling]? Where didn't it?"* — out loud, into the recording if useful.
- **Divergence at wrap-up:** "your Round 1 staging vs your Round 2 staging" — your own interpretations diverging across two takes of the same feeling.

Building a dedicated solo skill is parked for a future iteration.

## Related skills

- **`storyboarding-beat-generator`** — invoked at Step 1 on the generator path.
- **`session-log-companion`** — invoked at Step 13 wrap-up for documentation hand-off, and mid-round on SLC prompt triggers.
- **`animatic-from-existing-boards` (parked)** — the animatic-pass mechanic in Steps 6–10 is a strong candidate to split out as its own reusable skill that runs on Phase 2 or Phase 3 panels with no fresh sketching. Build in a future session.

## Changelog

**v3 (2026-05-30)** — reworked Step 1 from a live solo run that spent the whole session pressure-testing the Step 1 prompt. Applied via handoff `phase4-skill-update-handoff-2026-05-30.md`. Changes:

1. **Step 1 retitled** "Intention" → **"Rough out the key shot"** — the title now names what the step produces (an action verb, a target) instead of a category. "The feeling" is shot-level, not scene/sequence (shot = word in the project's vocab).
2. **Timer moved from header to foot** — `▶ Start your 3-min timer. Say done` now sits at the action point, next to "done," fixing the "how long was this again?" cue-lost problem. Duration stays in the title.
3. **Point 3 collapsed to staging-instinct only** — the old declare-out-loud sentence re-stated points 1 and 2; only its staging clause was additive. Added a **"give me some" on-ramp** (2–3 divergent staging options on request, jog-not-prescribe) and **scribble-or-write capture**. Conductor note and session-shape table row updated to match.

**Cross-skill flag (not yet applied):** the timer-cue-lost problem affects any *conversational* opening step holding its timer in the header. Check Phase 1 / Phase 2 / Phase 3 SKILL.md for that pattern; move the cue next to "say done." Track as separate per-file handoffs.

**v2 (2026-05-17)** — folded 11 skill iterations from the Phase 4 pair round of 2026-05-17 (Jade hover bike beat + workshop ideation). Applied via handoff supplement `phase4-skill-update-handoff-2026-05-17.md`. Changes:

1. Added **Step 1b — Scene parameters** between Intention and Thumbnail. Borrowed from Phase 3 script generator schema. Prevents Round-1 omissions like the missing droid in the source round.
2. Added **leftover-time-defaults-to-rest** principle to session shape. Phase 3 has this as a named Step 5 ("Play"); Phase 4 makes it implicit at every step boundary.
3. **Step 7 expanded** to name runner-up notes with explicit destinations (parked for Round 2 / next session / production carry-forward). Don't lose the runners.
4. Added **Step 3b — Tool-fluency check** before animatic passes. Honest naming of whether Round 1's animatic time is pure craft or partly tool onboarding.
5. **Step 3b workshop-mode addition** — peer-demo volunteer for animatic tool import-and-scale workflow. Models the Ranft-room ethos (peers showing peers) without locking the tool.
6. **Step 7 dual mode** — note-driven OR experiment-driven. Names the more advanced practice mode (arriving with a craft experiment in pocket and landing it in Step 7).
7. *(personal practice carry-forward, not skill change — "arrive with a craft experiment in your pocket" lives in the practice, not the SKILL.md.)*
8. Added **Step 7b — Export the draft** as its own named micro-step. Was buried inside Step 7 body in v1 and got missed in real session runs. Now the round can't close without capturing.
9. Added **Step 10 — Post-session finishing window** (~30 min, on user's own time). Audio → cut → polish pass in a stronger editing app. Makes the practice *completable* — drafts that don't get finished disappear. Wrap-up (Step 9) now hands off explicitly to Step 10.
10. **SLC (Session Log Companion) integration** added as a section. Live documentation prompts during the round + explicit hand-off at Step 9. Phase 4 surfaces skill iterations while it runs; the conductor should prompt for them live, not rely on end-of-round memory.
11. **Conductor rule added** — don't skip Step 8 or Step 9 when the user requests a session log mid-flow. Ask first whether to close out the round before filing. (Also added to "What this skill does NOT do.")
12. *(structural carry-forward — Step 8 hand-off gained a fourth option: "method-iteration round" for folding skill iterations into the SKILL.md when enough have surfaced. The round that produced this v2 is the example.)*
13. **Meta-iteration rule added** — method-iteration rounds output handoff supplements, not full v2 rewrites. Full rewrites are wasteful, lose repo history, bypass per-edit QA, and can silently break upload constraints (like the 1024-char description limit). Added to "What this skill does NOT do."

**v1 (earlier)** — original Phase 4 skill, including the 2026-05-16 supplement that trimmed the frontmatter description to 926 chars.
