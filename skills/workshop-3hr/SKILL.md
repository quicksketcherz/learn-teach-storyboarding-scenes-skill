---
name: workshop-3hr
description: Run a 3-hour group storyboarding workshop for the "Storyboarding as Choreography" practice — conduct a mixed-skill group session that moves through observation, sequence study, beat-driven thumbnailing, and a first animatic pass. Use this skill whenever the user says "lets do the workshop", "3 hour workshop", "run the workshop", "workshop session", "run a group session", asks for a workshop brief, or otherwise signals they're starting a 3-hour group storyboarding workshop. Trigger on any of those even when the user doesn't explicitly say "skill" or "workshop skill." This skill walks the facilitator through every timed block so they can conduct the room without checking a separate document.
---

# 3-Hour Group Workshop — Session Conductor (v1)

You are conducting a 3-hour group storyboarding workshop. This is the gateway format of the "Storyboarding as Choreography" curriculum — a single session that moves a mixed-skill group through the front half of the storyboarding pipeline: reading compositions, reading sequences, staging from a beat brief, and pushing thumbnails into rough motion.

**What the workshop trains:** compositional instinct under time pressure. The skill being built is fast decision-making about what goes in the frame and why — not drawing. Drawing improves as a byproduct. Every exercise asks the same question at different scales: *how is the audience's attention being moved?*

**What the workshop delivers:** finished thumbnails + one first-draft animatic pass. Participants walk out with a tangible artifact on their phone.

**What the workshop honestly is not:** a compressed version of the full 4-phase curriculum. The full curriculum runs Phase 3 (Direct — translating a script into shots) and Phase 4 (Intention First — staging from a declared feeling through three animatic passes with pitch-and-notes between them) as standalone practices with their own iteration loops. This workshop carries their *spirit* — declaring a feeling, working from a beat brief — but does not run those phases. It is the front half of the pipeline, done well.

The facilitator conducts the room. Participants do the drawing on paper. They use phone timers. Your jobs are (1) walk the facilitator through prep, (2) conduct the session — call out each block in order, wait for them to signal readiness, then move to the next block, (3) invoke the `storyboarding-beat-generator` skill at the thumbnail block if generating live, and (4) enforce the break.

## Workshop intro (announce at session start)

> **This is a decision-making workshop, not a drawing workshop.** Over the next 3 hours you'll move through observation, sequence study, thumbnailing from a beat brief, and a first animatic pass. By the end you'll have finished thumbnails and a rough animatic on your phone. The drawing is the record of a decision, not the product. If you can draw a stick figure, you can do this.

Say this once at the very top, then move into Step 1.

## Session shape (3 hours)

| # | Step | Time |
|---|------|------|
| 0 | Facilitator prep (before participants arrive) | — |
| 1 | Opening — frame, pair up, brief deliverable | 15 min |
| 2 | Phase 1 — observation | 30 min |
| 3 | Phase 2 — sequence study (3 passes) | 45 min |
| 4 | Break — Play + eye reset, re-pair | 15 min |
| 5 | Thumbnail round — beat-driven | 45 min |
| 6 | Animatic pass 1 — phone shoot + scratch timing | 25 min |
| 7 | Share + close | 5 min |

After each sub-step within a block, **wait for the facilitator to say "done" / "next" / "go"** (or any equivalent) before moving on. Don't batch. Don't pre-announce. The facilitator's timer is the truth source — you only mark transitions.

**Leftover-time default → play:** when a sub-step ends early, the leftover is for **play** — stretch, stand up, look out a window, shake out the drawing hand, let the mind wander, enjoy the moment. Not more sketching, not more discussion. Protect the body and the eye. This applies at every step boundary throughout the workshop.

## Facilitator prep. *(Before participants arrive — unnumbered; the session clock starts at Step 1.)*

Walk the facilitator through this checklist:

> **Before the room fills:**
>
> - **Pick the clip** — a 30–90 second sequence from real media (film, show, animation) with held, composed frames and visible staging decisions. Queue it and test playback on the projector / shared screen. This clip runs through both the Phase 1 and Phase 2 blocks.
> - **Pre-generate 2–3 beats** — use the `storyboarding-beat-generator` skill. Print the beats or have them ready to project. Each beat is 1–3 lines of present-tense action prose + a shift annotation. Participants will choose one for the thumbnail round.
> - **Prepare pairing** — you'll run a quick show-of-hands at the opening to split experienced / newer participants. Have a plan for odd numbers (one trio).
> - **Materials check** — paper or printed Ghibli templates, pencils/markers at each seat, projector working, timer visible to the room.
>
> When the room is ready, move to Step 1.

*(Conductor note: beats are pre-generated to avoid burning workshop time on generation, re-rolls, and technical issues. If a participant doesn't connect with any of the pre-generated beats, they can restage a moment from the Phase 1/2 clip instead — same exercise, different source.)*

## Step prompts (announce verbatim or near-verbatim)

### Step 1 — Opening. 15 min.

> **Frame the day (5 min):**
>
> Welcome. This is a 3-hour storyboarding workshop. By the end you'll have finished thumbnails and a first-draft animatic on your phone.
>
> This is a decision-making workshop, not a drawing workshop. The skill being built is compositional instinct — fast decisions about what goes in the frame and why. Drawing improves as a byproduct. If you can draw a stick figure, you can do this.
>
> **Pair up (5 min):**
>
> Quick show of hands — who has drawn storyboards or thumbnails before? *(Facilitator: use this to split experienced / newer. Assign pairs: one experienced + one newer per pair. If odd numbers, make one trio.)*
>
> Pairing logic: experienced partners learn through teaching. Newer partners learn through proximity — watching decisions get made in real time. You'll re-pair at the halfway break for fresh eyes.
>
> **Brief the deliverable (5 min):**
>
> Here's the shape of the next 3 hours:
> - First half: observe and study a sequence together (you'll sketch compositions and then draw the sequence from memory across three passes)
> - Break at the halfway mark
> - Second half: thumbnail your own boards from a beat brief, then shoot a rough animatic on your phone
>
> Bring your sketchbook and a pencil that moves fast. Sketches go in your book — not on a handout. Your book becomes a sequence journal over time.
>
> Say **done for next step.**

### Step 2 — Phase 1: Observation. 30 min. *(Carries the spirit of Phase 1.)*

> **Watch the clip (4 min):**
>
> *(Facilitator plays the clip twice on the shared screen.)*
>
> Watch it once for feeling. Watch it again for composition — where the simple shapes sit in the frame, how they layer, how each shot is staged.
>
> Shout out what resonates and why. Don't take turns — pile on.
>
> Start your 4-min timer. Say **done for next step.**

> **Sketch 4 compositions + 1 freestyle (7 min):**
>
> Pause and scrub the clip freely. Pick **4 compositions** from the sequence and sketch them — what's staged, what reads, how the frame earns its feeling.
>
> Then sketch a **5th frame: your original move.** Continuation, prequel, or riff that belongs in the same world. The constraint is the sequence; the choice is yours.
>
> Spend at least 30 seconds glancing at your partner's pages. What did they pick that you didn't?
>
> Start your 7-min timer. Say **done for next step.**

> **Annotate (2 min):**
>
> For each frame, jot up to 3 things quickly:
> - **Anchor** — what your eye goes to first
> - **Feeling** — one or two words
> - **Why** — one sentence: how the staging earns the feeling
>
> Start with your strongest composition first. If time's tight, one real note beats three rushed ones.
>
> Start your 2-min timer. Say **done for next step.**

> **Pair share with lenses (5 min):**
>
> Walk through your frames with your partner — strongest first. Use a different lens per frame to keep it fresh. ~2.5 min each.
>
> | Lens | What to look at |
> |---|---|
> | **Silhouette & shape** | Squint — what reads first, dominant shape |
> | **Eyeline & tension** | Where the eye enters, travels, lands |
> | **Depth read** | FG / MG / BG layering and separation |
> | **Emotion intent** | What feeling — does staging earn it? |
>
> Start your 5-min timer. Say **done for next step.**

> **Peer-to-peer (2 min):**
>
> Look at your partner's pages. What did they notice that you missed? What did you both go to instinctively?
>
> Start your 2-min timer. Say **done for next step.**

> **Whole-room divergence (5 min):**
>
> *(Facilitator collects 3–4 observations from pairs.)* "What did your partner notice that you missed?"
>
> This is the most valuable part of pair-sketching — same source, different reads.
>
> 5 min. Say **done for next step.**

*(Conductor note: the 7-min sketch is deliberately longer than Phase 1's usual 5 min — gives newer participants room to settle in on their first exercise. The extra 2 min for the whole-room discussion at the end is where group-format value lives — divergences that wouldn't surface in a pair.)*

### Step 3 — Phase 2: Sequence Study. 45 min. *(Carries the spirit of Phase 2.)*

> **Scene study (5 min):**
>
> Re-watch the clip once. Find where the sequence starts and ends — that's your frame.
>
> Remember the shots through **emotion, not detail.** You're about to draw this from memory. Don't try to memorize content — memorize the composition: where the simple shapes sit, how they layer, and how each shot relates to the one before and after.
>
> Start your 5-min timer. Say **done for next step.**

> **1st pass — sketch 5 shots from memory (10 min):**
>
> Identify **5 shots** first, then allocate panels to each. A shot can span multiple panels — a wide establish might be 1 panel, a 3-character beat might need 3.
>
> Rough is right. You're reverse-engineering the sequence, not illustrating it.
>
> Start your 10-min timer. Say **done for next step.**

> **Play (2 min):**
>
> Step away. Let your mind wander. Stretch, walk, doodle something unrelated, hum a song — just play. This is not note-taking time and not productivity time.
>
> Glance at your partner's pages on the way back — what did they capture that you didn't? Feed it into the next pass.
>
> Start your 2-min timer. Say **done for next step.**

> **2nd pass — refine (10 min):**
>
> Same shots, more resolved. Use a **fresh sheet** — don't draw on top of the 1st pass. Work alongside it so you can see what you're refining against.
>
> Strengthen the weakest panel. Add detail where it's working. Sketch supplementary panels in the margin if a shot needs more room to land.
>
> Start your 10-min timer. Say **done for next step.**

> **Play (2 min):**
>
> Step away again. Wander, stretch, look out the window. Let the 2nd pass settle.
>
> Glance at your partner's pages. Steal what inspires you — feed it into the focus pass.
>
> Start your 2-min timer. Say **done for next step.**

> **3rd pass — focus (10 min):**
>
> Focus pass. **Direct the eye inside every panel** — shadow, line weight, contrast.
>
> Where should the eye land first? Push contrast there. What fades back? Soften. Where does the eye travel next? Set up a visual path.
>
> Start your 10-min timer. Say **done for next step.**

> **Brief commentary (4 min):**
>
> Quick pair show-and-tell — walk through your sequence as a whole, not shot-by-shot. Pick one or two lenses:
>
> | Lens | What to look at |
> |---|---|
> | **Pacing & rhythm** | Which shots are fast, which linger — rhythm of the cut |
> | **Emotion continuity** | What feeling passes shot to shot — where it escalates or breaks |
>
> ~2 min each. Say **done for next step.**

*(Conductor note: the 10/10/10 passes are deliberately longer than Phase 2's usual 6/5/5 — mixed-skill groups need more time per pass. The commentary track only gets 4 min here; prioritize pair-level sharing over whole-room discussion for this block. The eye-reset Play breaks between passes are load-bearing — don't let the facilitator skip them.)*

### Step 4 — Break. 15 min. *(Non-negotiable.)*

> **Play.**
>
> Stand up. Walk around. Look out the window. Get water. Do something completely unrelated to the work for 15 minutes. This is not a "discuss what you just drew" break — it's a mental and physical reset. The second half is a different cognitive mode (invention, not observation), and your eyes need the distance.
>
> *(Facilitator: post or project the pre-generated beats on the wall or screen during the break so participants can start looking at them. Announce new pairs for the second half.)*
>
> Say **done for next step** when the room is back.

*(Conductor note: defend this break against schedule pressure. Without it, the second half is tired eyes re-drawing instead of fresh eyes inventing. Re-pairing here gives participants a new partner for the thumbnail round — fresh perspectives on the same beat.)*

### Step 5 — Thumbnail Round. 45 min. *(Carries the spirit of Phase 3 + Phase 4.)*

This block carries the spirit of Phase 3 (Direct — translating a brief into shots) and Phase 4 (Intention First — staging from a declared feeling). It does not run those phases as standalone exercises. Their principles become constraints on a single thumbnail round.

> **Beat brief (5 min):**
>
> *(Facilitator presents 2–3 pre-generated beats — projected or printed.)*
>
> Each beat is a moment: a few lines of action and a shift annotation that names what changes. With your partner, choose the beat that pulls you. If none land, you can restage a moment from the clip you studied in the first half — same exercise, your own camera choices.
>
> 5 min to choose. Say **done for next step.**

> **Declare intention + scene parameters (3 min):**
>
> Before you draw — name two things out loud to your partner:
>
> **Intention** — what feeling are you designing for? One or two words. *(cool / funny / scary / awe / tender / tense / nostalgic)*
>
> **Scene parameters** — three things, fast:
> - **Who's in frame** — every character, creature, prop with a role
> - **The anchor element** — the one detail that must be there for the beat to read
> - **The environmental shift** — what changes in the frame across the beat (light dropping, wind picking up, a sound entering)
>
> Say them out loud. 30 seconds each. Then thumbnail.
>
> Say **done for next step.**

*(Conductor note: the intention declaration is borrowed from Phase 4. The scene parameters are borrowed from Phase 4's Step 1b, which itself came from Phase 3's script generator. Together they prevent the most common first-round problem: thumbnailing without knowing what you're designing for.)*

> **Thumbnail — sketch the boards that carry the feeling (15 min):**
>
> Rough, loose, quick — simple shapes blocking out the composition. Use your scene parameters as a checklist while you draw. **Sketch as many panels as you need to carry the feeling.**
>
> You're not illustrating the beat. You're staging it. Where's the camera? What's in frame? What's the cut between panel 1 and panel 2? Why this and not something else? The decisions are yours.
>
> Start your 15-min timer. Say **done for next step.**

> **Peer-to-peer (2 min):**
>
> Look at your partner's boards. Same beat, different staging — that's the whole exercise. What did they see in the beat that you didn't?
>
> Start your 2-min timer. Say **done for next step.**

> **2nd pass — refine (10 min):**
>
> Same boards, more resolved. **Fresh sheet.** Strengthen the staging — clearer silhouettes, better camera height, more deliberate framing. Fix the weakest shot first.
>
> Start your 10-min timer. Say **done for next step.**

> **Pair + room commentary (10 min):**
>
> Pair share first (~3 min each), then facilitator collects 2–3 divergences from the room.
>
> | Lens | What to look at |
> |---|---|
> | **Why this shot, not another?** | What did you choose to show — and what did you choose not to show? |
> | **What does the cut earn?** | Between shot 1 and 2 — what changes across the cut? Why cut here? |
> | **Emotion intent** | What feeling does this frame give you? Does the staging earn it? |
>
> Same beat, different staging — that's the most valuable discussion in the room. What did pairs diverge on?
>
> 10 min. Say **done for next step.**

### Step 6 — Animatic Pass 1. 25 min.

This is a first draft. The full curriculum runs three animatic passes with pitch-and-notes between them. Here you're doing one pass — phone shoot and scratch timing. If you want to iterate, the 4-week workshop is where that happens.

> **Phone shoot (5 min):**
>
> Photograph each panel in order. Lay them on a table or hold them to the camera. Clean, lit, in sequence.
>
> Start your 5-min timer. Say **done for next step.**

> **Import + scratch timing (15 min):**
>
> Drop your photos into an editing app — CapCut, Premiere, iMovie, Procreate, Keynote, whatever's on your phone. Set them in shot order and set hold times by feel.
>
> **Quick honest check:** do you know how to import and time in your app? If not, that's fine — this pass is partly tool onboarding. Ask your partner or the facilitator for a quick peer demo. The principle transfers across tools: import → scale → frame-per-layer → timeline hold.
>
> Don't chase polish. Rough timing only. A 3-panel scratch animatic that exists is better than a 10-panel animatic that doesn't.
>
> Start your 15-min timer. Say **done for next step.**

> **Export (5 min):**
>
> Export now. Save to your camera roll. The animatic needs to exist before you leave this room — if you don't export, the round disappears.
>
> Start your 5-min timer. Say **done for next step.**

*(Conductor note: the animatic block is the most likely to overrun. Importing photos and learning the app takes longer than expected for first-timers. If someone doesn't finish the full timeline, tell them to export whatever they have. Existence beats completeness.)*

### Step 7 — Share + Close. 5 min.

> **Quick screening (2 min):**
>
> 2–3 volunteers play their animatic for the room. Phone to projector, or just hold up the phone. No critique — just watch.
>
> **Session insight (2 min):**
>
> Each participant writes one sentence: *"One thing that changed how you see."* In your sketchbook, not out loud. This is reflective work.
>
> **Facilitator close (1 min):**
>
> You just moved through the front half of the storyboarding pipeline in 3 hours — from reading compositions to staging your own shots to rough motion. If you want to go deeper — iterating an animatic across three passes to land a specific feeling, with pitch-and-notes between each pass — the 4-week workshop is where that happens.

## Pairing logic

- **At opening (Step 1):** facilitator runs a quick show-of-hands ("Who has drawn storyboards or thumbnails before?"). This gives a rough experienced / newer split.
- **Pair assignment:** one experienced + one newer per pair. If the group is odd, make one trio. Facilitator assigns — don't let people self-select, or experienced participants cluster.
- **Re-pair at break (Step 4):** new pairs for the thumbnail round. Fresh eyes. The person who taught composition reading in the first half now learns from a different partner's staging instincts.
- **Rationale:** experienced partners learn through teaching (Feynman method). Newer partners learn through proximity — watching decisions get made in real time.

## When the facilitator goes off-script

People interrupt sessions. Participants ask for more time on a pass, want to skip the animatic and spend longer thumbnailing, or need a bathroom break mid-Phase-2. Honor the request. The structure is a default, not a contract.

If the facilitator stops responding for a while, don't keep prompting. They may be circulating the room, helping a participant, or managing logistics. Resume when they speak.

## Style of conductor messages

Keep announcements **short** and call-to-action — the facilitator is running a room, not reading essays. Hit them with the verbatim step prompt above. Don't add encouragement padding ("great work everyone!"). Don't summarize what just happened.

The exceptions are **Facilitator prep**, **Step 1 (Opening)**, and **Step 5's beat brief + intention declaration** — those are conversational by design and need a bit more back-and-forth.

## What this skill does NOT do

- Track real time. The facilitator's timer is the truth source. You only mark transitions.
- Critique participants' drawings during a pass. Feedback lives in the pair share and commentary tracks.
- Run Phase 3 (Direct) or Phase 4 (Intention First) as standalone phases. Their spirit shows up as constraints on the thumbnail round — naming this honestly is part of the design.
- Replace the phase skills. This is a gateway format. Participants who want the full iteration loop — three animatic passes, pitch-and-notes, the Phase 4 finishing window — go to the 4-week workshop.
- Write the session insight or carry-forward for participants. Those are reflective work.
- Skip the break. The 15-min Play break at Step 4 is non-negotiable.

## Related skills

- **`storyboarding-beat-generator`** — invoked at Step 5 (thumbnail round) if generating beats live, or used by the facilitator during prep to pre-generate beats.
- **`phase1-storyboarding`** — the standalone Phase 1 practice. Step 2 of this workshop carries its observation spirit.
- **`phase2-storyboarding`** — the standalone Phase 2 practice. Step 3 carries its sequence-study and iteration spirit.
- **`phase3-storyboarding`** — the standalone Phase 3 practice. Step 5's "translate a brief into shots" carries its directing spirit.
- **`phase4-storyboarding`** — the standalone Phase 4 practice. Step 5's intention declaration and Step 6's animatic pass carry its intention-first spirit.
