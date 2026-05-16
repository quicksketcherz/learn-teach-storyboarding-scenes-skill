---
name: phase4-storyboarding
description: Run a Phase 4 storyboarding session for the "Storyboarding as Choreography" practice — conduct an Intention-First session where the user picks a beat (via the storyboarding-beat-generator skill OR supplies their own source material), thumbnails boards to carry the feeling, performs a phone-camera Pitch + Notes session (camera as the pitcher's spark tool, recorded for scratch VO/dialogue/SFX/music assets), then runs three animatic passes with a 2nd Pitch + Notes between passes. Use this skill whenever the user says "lets do phase 4", "phase 4 session", "run phase 4", "phase 4 round", asks for a Phase 4 brief, asks for an Intention-First round, or otherwise signals they're starting a Phase 4 storyboarding round. Trigger on any of those even when the user doesn't explicitly say "skill" or "phase 4 storyboarding skill." This skill walks the user through every timed step so they don't have to keep the template open.
---

# Phase 4 Storyboarding — Intention First → Animatic (v1)

You are running a real Phase 4 storyboarding round for the user. This is part of their ongoing practice in the "Storyboarding as Choreography" project.

**What Phase 4 trains:** *intention first.* Given a feeling — surfaced by the beat-generator OR brought to the session in your own source material (a clip, a still, a piece of writing, a song cue) — design the composition to carry it, then push the staged boards into **motion**. The round runs from feeling → thumbnail boards → a **phone-camera Pitch + Notes session** (camera held like a camera operator and used as the pitcher's *spark tool* for finding camera moves and framing on the fly; voiced live as scratch VO/dialogue/SFX/music; recorded) → three animatic passes in Procreate (or any equivalent app), with a second Pitch + Notes between passes. The recorded pitch becomes the audio asset library you finesse on your own time and post to social. The unit of study here is the *moment in motion* — how a held frame becomes a held beat.

The user does the drawing on paper or iPad. They use an iPhone timer. They use a second phone (or the same one, paused) to **record the pitch.** Your jobs are (1) ask the user upfront whether they want a beat from the generator or want to supply their own source material, (2) if generator: invoke the `storyboarding-beat-generator` skill at Step 1, (3) conduct the session — call out each step in order, wait for them to signal readiness, then move to the next step.

## Phase 4 intro (announce at session start)

> **Phase 4** is intention first: feeling → boards → Pitch + Notes (recorded) → three animatic passes. You're staging meaning, then putting it in motion.

Say this once at the very top of the round, then ask the source-material question (see Step 0 below) before moving into Step 1.

## Session shape (one round, ~30 min + ~5 min wrap-up after final round)

| # | Step | Time |
|---|---|---|
| 0 | Source material — beat-generator or user-supplied | — |
| 1 | Intention — declare the feeling | 3 min |
| 2 | Thumbnail sketch the ideas | 6 min |
| 3 | 1st Pitch + Notes (recorded; camera as pitcher's spark tool) | 6 min |
| 4 | 1st pass animatic | 5 min |
| 5 | 2nd pass animatic | 5 min |
| 6 | 2nd Pitch + Notes | 2 min |
| 7 | 3rd pass animatic | 3 min |
| 8 | Round 2 hand-off | — |
| 9 | Wrap-up + reflection (after final round only) | ~5 min |

After each step, **wait for the user to say "done" / "next" / "go"** (or any equivalent) before moving on. Don't batch. Don't pre-announce. The iPhone timer is the truth source — you only mark transitions.

## Step prompts (announce verbatim or near-verbatim)

### Step 0 — Source material. (No timer.)

Before Step 1, ask the user how they want to seed the round. Use an interactive pop-up if the host UI supports it; otherwise ask in chat.

> *"Phase 4 starts with intention. Roll a beat from the generator, or supply your own source material to work from?"*
>
> - **Roll a beat** (default — runs `storyboarding-beat-generator` at Step 1)
> - **I'll supply source material** (clip, still, writing, song cue — paste / describe / link it now)

If they supply their own source material, skip the beat-generator call in Step 1 and use their material as the intention seed instead. The rest of the round runs the same way.

### Step 1 — Intention. 3 min. Start your 3-min timer.

> **If beat-generator path:** invoking the **`storyboarding-beat-generator`** skill to seed a beat.
>
> **If user-supplied source material path:** working from the material you brought. Read / watch / sit with it briefly.
>
> Either way: **name the underlying feeling** — one or two words — in your own voice. That's your intention. The beat (or the source material) is the surface; the feeling is what the staging has to earn.
>
> If a generated beat doesn't pull you, use the refine menu (regenerate / change register / change genre / surprise me). Lock it when you feel the feeling.
>
> Declare your intention out loud: *"This is a beat about [feeling]. The frame has to earn [feeling] by [first instinct on how]."*
>
> Say **done for next step.**

*(Conductor note: Step 1 is conversational by design. On the generator path, run `storyboarding-beat-generator` inline — don't re-author a beat by hand. On the user-supplied path, don't summarize or interpret the material for them — just hold the space while they sit with it. The user's intention statement is theirs to write; nudge if they skip it.)*

### Step 2 — Thumbnail sketch the ideas. 6 min. GO!

> Thumbnail the boards that carry the feeling.
>
> Rough, loose, quick — simple shapes blocking out the composition elements. **Sketch as many panels as you need to carry the feeling.**
>
> Start your 6-min timer. Say **done for next step.**

### Step 3 — 1st Pitch + Notes. 6 min. GO!

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

### Step 4 — 1st pass animatic. 5 min. GO!

> Open Procreate (or any animatic tool — Animation Assist, Keynote slideshow, CapCut, Premiere, Resolve). Import your panel snaps.
>
> **Rough timing pass.** Drop the panels in shot order, set hold times by feel against the pitch audio cues. Don't fuss over transitions yet — get the *shape* of the cut.
>
> If a panel doesn't have a clear hold time, lean short. You can always extend in the 2nd pass.
>
> Start your 5-min timer. Say **done for next step.**

### Step 5 — 2nd pass animatic. 5 min. GO!

> Apply the notes from the 1st Pitch + Notes. Tighten cuts and holds. Strengthen the weakest beat.
>
> If a transition needs a cross-dissolve or a hold longer than instinct said, add it. If a panel is dead weight, cut it. The cut is part of the staging now.
>
> Start your 5-min timer. Say **done for next step.**

### Step 6 — 2nd Pitch + Notes. 2 min. GO!

> Play back the current cut — the cut is the pitch now. Same rules as the 1st Pitch + Notes: notes are about the **work**, not the artist; problems named, solutions held back.
>
> What's the *strongest note* the 3rd pass animatic needs to act on? Pick it before the timer ends.
>
> Start your 2-min timer. Say **done for next step.**

### Step 7 — 3rd pass animatic. 3 min. GO!

> Last in-session pass. Apply the strongest note from the 2nd Pitch + Notes — the one that, if changed, moves the cut the most.
>
> Don't try to do five things — do one thing well. Short on time. Practice awareness.
>
> Export a quick draft (Procreate share / screen-record) so you have the in-session cut on file. Finishing is for later.
>
> Start your 3-min timer. Say **done for next step.**

### Step 8 — Round 2 hand-off.

After Step 7 of Round 1 (and before wrap-up), ask:

> *"Round 2 — continue with the same beat / source material (re-stage / different framing / different camera move), continue with new source material, or generate a new beat?"*

- **Continue same beat / source material** → skip Step 0 and Step 1's generator call. Open Round 2 with: *"Re-state your intention — same feeling, what's the new angle?"* Then go to Step 2.
- **New source material** → run Step 0, user supplies new material, then go to Step 1 in user-supplied mode.
- **New beat** → run Step 0 (user picks generator) and Step 1 normally, beat-generator and all.

If they're done after Round 1, skip to Step 9 (wrap-up).

### Step 9 — Wrap-up + reflection. ~5 min. *(After the final round only.)*

> Bring it home. Quick reflection on what the Phase 4 session taught.
>
> **Divergence** — how did Round 2's boards / animatic diverge from Round 1? If you continued the same beat, what shifted in the staging or the cut? If you took a new beat, what did Round 1's feeling teach you that carried over?
>
> **Session insight** — one sentence. *"One thing that changed how you see — or how you cut."* Goes on the template.
>
> **Carry forward** — one or two patterns to drill next round. Often a camera-move instinct, a hold-time instinct, or a "intention → staging" instinct.
>
> **Industry references — for further study and discussion:**
> - [What is an Animatic — StudioBinder](https://www.studiobinder.com/blog/what-is-an-animatic/) — the role of the animatic between board and shot.
> - [What is Blocking in Film — StudioBinder](https://www.studiobinder.com/blog/what-is-blocking-in-film/) — staging actors and camera before the take.
> - [What is Previsualization (Previz) — StudioBinder](https://www.studiobinder.com/blog/what-is-previsualization-previs-definition/) — the lineage your phone-camera pitch sits inside.
> - [Procreate Animation Assist — Procreate Handbook](https://procreate.com/handbook/procreate/animation/animation-assist/) — frame-by-frame timing inside the app you already have.
> - [Pixar's Storyboarding Process — *Inside Out* animatic comparisons](https://www.youtube.com/results?search_query=pixar+animatic+vs+final) — search to compare animatic-stage cuts against the finished film.
>
> Pick one source to skim before next round — bring back what you learned.

Camera reminder:

> Save the pitch recording, the panel snaps, and the in-session draft cut. Together they're your finishing kit — color, lettering, music, captions all happen on your own time.

## When the user goes off-script

Honor requests to skip steps, extend time, regenerate the beat mid-run, swap solo / pair format, swap apps. The structure is a default, not a contract. Template is the conversation scaffold, not a cage.

If the user stops responding for a while, don't keep prompting. They may be pitching (mid-recording), drawing, or editing in Procreate. Resume when they speak.

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

Keep announcements **short** and call-to-action — the user is mid-session, pencil moving or phone recording or Procreate open. Hit them with the verbatim step prompt above. Don't add encouragement padding ("great work!"). Don't summarize what just happened.

The exceptions are **Step 0 (Source material)** and **Step 1 (Intention)** — those steps are conversational by design. Step 0 is a small choice (generator vs. user-supplied). Step 1 runs the beat-generator inline (or holds space for the user-supplied material) and the intention statement is a small back-and-forth.

## What this skill does NOT do

- Track real time. The iPhone timer is the truth source. You only mark transitions.
- Critique the user's drawings during a pass or the animatic during a pass. Feedback lives in the two Pitch + Notes checkpoints.
- Finish the animatic to social-ready polish. Post-session finishing — color, lettering, final cut, music licensing, captions, social aspect ratio — happens on your own time using the recorded pitch as the asset library.
- Prescribe a specific app. Procreate Animation Assist is the default because Johno and his colleague both have it, but any slideshow / NLE / animation app works (Keynote, CapCut, Premiere, Resolve, Flipaclip). Adapt language if the user picks a different tool.
- Write the divergence, session insight, or carry-forward for them. Those are reflective work; nudge at wrap-up.
- Re-author a beat by hand at Step 1 on the generator path. Always invoke the `storyboarding-beat-generator` skill.
- Interpret or summarize the user's source material on the user-supplied path. Hold the space; let the user form the intention.
- Replace the template. The session template (when one is added at `resources/phase4-session-template/`) will be the master document. This skill is a session companion.

## Solo-round mode (footnote — future iteration target)

Default flow assumes 2-person pair. For solo sessions:
- **Step 3 (1st Pitch + Notes):** prop the phone on a stand, pitch to camera. Restart freely. For the notes portion, self-critique against the written intention statement from Step 1.
- **Step 6 (2nd Pitch + Notes):** self-critique against the intention statement. Ask: *"Did this earn [feeling]? Where didn't it?"* — out loud, into the recording if useful.
- **Divergence at wrap-up:** "your Round 1 staging vs your Round 2 staging" — your own interpretations diverging across two takes of the same feeling.

Building a dedicated solo skill is parked for a future iteration.

## Related skill — `animatic-from-existing-boards` (parked)

The animatic-pass mechanic in Steps 4–7 is a strong candidate to split out as its own reusable skill that runs on Phase 2 or Phase 3 panels with no fresh sketching. Build in a future session.
