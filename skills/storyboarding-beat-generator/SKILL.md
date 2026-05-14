---
name: storyboarding-beat-generator
description: Generate single storyboard beats or short beat sequences for storyboarding practice in the Storyboarding as Choreography curriculum. Outputs a present-tense action line and a shift annotation — the smallest narrative unit a storyboard panel resolves. Use this whenever Johno asks for a beat, a sketching prompt, a scene moment, a panel prompt, or a starting point to sketch from — across Phase 1 (Observation), Phase 2 (Constraint Sketching), Phase 3 (Break Genre), or Phase 4 (Intention First). Trigger on phrases like "let's make a story beat", "give me a beat", "seed a sketch", "prompt for today's session", "beat for Phase 1/2/3/4", "story beat", "panel prompt", "scene moment for sketching", "generate a starting point", or any request to seed a sketching exercise with a beat to draw from.
---

# Storyboarding Beat Generator

A reusable beat generator for the **Storyboarding as Choreography** curriculum. Produces a single storyboard beat — the smallest narrative unit a panel resolves — framed for sketching, not for screenwriting.

The skill positions itself as a **collaborative screenwriter**: it writes the page, you (and your sketching partner) edit it. The generated beat reads cleanly first; refinement comes after.

## What a beat is here

The unit smaller than a scene and smaller than a screenwriter's beat. A screenwriter's beat is a narrative shift ("Lionel walks up, the car horn sounds, Claire arrives"). A **storyboard beat** in this skill's sense is one *moment within that shift* — the frame where the staging earns the feeling.

A well-formed beat has two parts:

- **The image** — 1–3 lines of present-tense action-line prose, presented in a screenplay-style action block. Only what can be seen and heard. No internal thoughts, no "she feels."
- **The shift** — a single-line annotation naming what changes between the start and end of the moment. **The shift is a margin note, not a tagline.** It belongs to the same tradition as ekonte left-column annotations, screenplay margin notes, and a storyboard artist's scribble next to a panel. It is *the thinking about the frame, sitting next to the frame*. It should never drift toward summary, caption, or punchline.

That's it. Composition, framing, and camera are the participant's job — the skill should not prescribe them by default.

## How the skill behaves on trigger

**Generate immediately. Don't ask questions first.** Roll random defaults across the parameters and produce a beat in the default Format 2 layout. Show the user *which* defaults rolled, so they can course-correct. Then offer the refine menu.

This is the "collaborative screenwriter" pattern. The page reads first; the editorial conversation happens after.

### Pattern on first trigger

```
Rolling random defaults:
- Scale: [single panel / mini-sequence]
- Emotional register: [register]
- Genre: [single genre / hybrid (genre × genre)] [(sub-tag: X)  ← only if a sub-tag rolled]
- Era tint: [contemporary (default — line omitted) / historical-X / near-future / far-future]
- Commitment level: [light tint / full commitment]
- Named-work register: [none — fresh / in the register of X]
- Constraint modifier: [none / named constraint]

[Beat output in Format 2]

[Refine menu via input UI]
```

When **era tint = contemporary**, omit that line entirely (contemporary is the silent default — only surface era when it's doing work). Same for **sub-tag**: only show when one rolled.

## Output format — Format 2

Default output is **lean** — image + shift, nothing else. The look-and-feel borrows from screenplay typography (fixed-width feel for the action block) but does not force full screenplay format (no slugline, no character cues unless dialogue is actually in the beat).

**Single panel:**

````
```
[1–3 lines of present-tense action-line prose.
Visible and audible only. Fixed-width feel —
borrow the rhythm of a screenplay action block.]
```

> **Shift:** [one-line margin note — what changes between the start and end of the beat]
````

**Mini-sequence (3–5 panels):**

````
**Panel 1**
```
[image]
```
> **Shift:** [shift]

**Panel 2**
```
[image]
```
> **Shift:** [shift]

...
````

The fenced code block carries the screenplay-action-block feel (fixed-width, page-like). The blockquote carries the margin-note feel for the shift. Together they evoke a screenplay page being marked up by a director — without pretending to *be* one.

## Runtime parameters

| Parameter | What it controls | Default behaviour |
|---|---|---|
| **Scale** | Single panel or mini-sequence (3–5 panels for the ekonte page) | Roll random — single more often than sequence |
| **Emotional register** | The tone the beat should carry (dread, tenderness, awe, restrained anger, anticipation tipping into disappointment, etc.) | Roll random from a broad register pool |
| **Genre** | The genre tint the beat sits in. Pool of 17 (see below). | Roll random from the genre pool. ~20% of rolls produce a **hybrid** (two genres combined, e.g. sci-fi × fantasy, horror × romance, noir × western). Some genres carry **sub-tags** (cyberpunk under sci-fi, folk horror under horror, etc.) — when the parent rolls, the sub-tag rolls ~25% of the time. |
| **Era tint** | Orthogonal time-period axis that *stacks on top of* genre. Most rolls are **contemporary** (default, silent). Occasional rolls land a non-contemporary era — historical periods or futures — which combine with whatever genre rolled. | Roll random with low rate: ~85% contemporary, ~15% non-contemporary spread across the era pool (see below). |
| **Commitment level** | How visible the genre cue is in the action lines. *Light tint:* a hum from a vent, a hilt at the hip, a curse half-spoken — genre present but peripheral. *Full commitment:* the airlock, the dragon's shadow, the duel on the ridge — genre is the event. | Roll random — roughly 60% light tint, 40% full commitment. Light is more sketchable and avoids "too grand." |
| **Named-work register** | Optional. "In the register of [named work]" — borrows tonal vocabulary from a named lineage (e.g. *Blade Runner 2049*, *Princess Mononoke*, *Mad Max: Fury Road*). | Default to none (fresh). Only used when the user asks. |
| **Constraint modifier** | Optional. One composition rule the beat must accommodate (low angle, no faces, single light source, BG carries meaning, one static camera, negative space dominant) | Default to none. Only used when the user asks. |

**Note on the beat-type parameter:** the v1 spec included a `beat type` parameter (action / emotional / turning / reveal). It was cut in v2 — across testing it never surfaced, was never missed, and added overhead. The taxonomy remains useful as orientation in writing, but it is not exposed as a runtime knob.

## Genre, era, and commitment — design notes

**Why genre is its own parameter.** Without it, the generator drifts to prestige-drama domestic interiors by default — restrained gestures, kitchen tables, doorways. That register is good but narrow. Genre as a rolled parameter forces the generator out of that gravity well.

**Genre × emotional register is the productive pairing.** "Awe + sci-fi" is different from "awe + fantasy" is different from "awe + noir." The emotional register anchors the beat; the genre tints the *world* it sits in. Always roll both.

### Genre pool (17)

The pool reflects what Johno actually encounters across professional storyboarding work, not a neat critical taxonomy.

| # | Genre | Beat-shape note |
|---|---|---|
| 1 | Drama | Restrained gesture, domestic interior, internal stakes externalised. |
| 2 | Sci-fi | Future tech, anomaly, system-under-strain. Sub-tag available. |
| 3 | Action-adventure | Mobile bodies, terrain, stakes that move. |
| 4 | Fantasy | Made worlds, magic logic, threshold-crossings. Sub-tags available. |
| 5 | Horror | Dread accumulation, the thing-not-quite-seen. Sub-tag available. |
| 6 | Thriller | Time pressure, surveillance, peril without violence yet. |
| 7 | Noir | Moral register more than visual one. Doubt, compromise, smoke. |
| 8 | Western | Open space, code, the line between civilization and not. |
| 9 | Romance | Attention as the event. Eyes, hands, room geometry. |
| 10 | Comedy | Timing, mismatch, dignity-on-the-edge. Sub-tags available. |
| 11 | Mystery | Clue logic. Beats often resolve on a *noticing*, not an action. |
| 12 | Crime / heist | Planning mode. Tools, maps, the rehearsal before the act. |
| 13 | War | Procedural, weighty, command-and-comply. Distinct from action-adventure. |
| 14 | Coming-of-age | Threshold-crossings at small scale. Bedrooms, hallways, first jobs. |
| 15 | Survival | Resource logic. Weather, water, the count-down body. |
| 16 | Post-apocalyptic | Inhabited ruin. Time-after rules. Distinct visual grammar from sci-fi. |
| 17 | Magical realism | The everyday with one impossible thing. Distinct from fantasy — no world rebuild. |

### Sub-tags

Some genres carry sub-tags. When the parent rolls, the sub-tag rolls **~25% of the time** (so most rolls of "sci-fi" stay general; one in four lands a sub-tag). Show the sub-tag in parentheses on the rolled-defaults line.

| Parent | Sub-tags |
|---|---|
| Sci-fi | cyberpunk |
| Fantasy | epic fantasy, urban fantasy |
| Horror | folk horror |
| Comedy | screwball, dark comedy |

The sub-tag list is intentionally short — these are sub-genres with *strong, distinct visual grammar*. Other sub-genres exist (cosmic horror, slasher, body horror, etc.) but until they earn calibration examples here, they aren't part of the roll.

### Era tint (orthogonal axis)

Era tint is **not** a genre. It's a time-period overlay that stacks on top of whatever genre rolled. Most rolls are contemporary (silent default). The non-contemporary slice is spread across:

- **Historical:** ancient, medieval, early-modern, Edo, Victorian, WWI–WWII, mid-century
- **Future:** near-future, far-future

When era tint rolls non-contemporary, it combines with the genre cleanly: *"noir × historical-mid-century"* (a 1950s diner phone booth), *"fantasy × historical-Edo"* (a torch-lit corridor in a feudal keep), *"romance × near-future"* (a first date through translation earpieces).

Era tint is a *flavour event*, not a default — keep the contemporary majority. If the rolled era is doing nothing for the beat, drop it.

### Hybrid genres

Roughly **1 in 5 rolls** combines two genres (e.g. *sci-fi × fantasy*, *horror × romance*, *western × noir*, *comedy × action-adventure*). Hybrids are not equal-weighted blends — pick one as the *world* and the other as the *intrusion*. A horror × romance beat is a romance world with a horror intrusion (a candle in a wine glass, smoke rising sideways), not a horror world with a romantic subplot.

### Commitment level

**Commitment level matters more than people think.** The instinct on hearing "sci-fi" is to reach for the starship. But a sci-fi beat can be a server light blinking once in an empty server room, or a thumbprint smudge on a glass console. That's *light tint* — and it's almost always more sketchable than full commitment. Default to mostly light. Full commitment is reserved for beats that *want* to be a big composition (the airlock, the gate of the keep, the kaiju on the horizon).

**Anti-grandness rule.** If a rolled combination is pulling toward spectacle, prefer the smaller frame: a sentry's bored shift on the wall over the army at the gate; a single magic-light flicker on a tavern table over the wizard's duel. The participant has to be able to sketch it in five minutes.

### Ratios (current — tunable)

| Roll | Rate |
|---|---|
| Hybrid genre | ~20% |
| Sub-tag (when parent has one) | ~25% |
| Non-contemporary era tint | ~15% |
| Light tint vs full commitment | ~60% / 40% |

These ratios are first-pass; adjust as live rolls reveal what feels right.

## The refine menu (post-generation)

After every generation, surface a menu via the input UI. The menu is **conditional** — options only appear when they make sense given current state:

**Always available:**
- Regenerate (same parameters)
- Change register
- Change genre (single → hybrid, or reroll)
- Change era tint (contemporary ↔ non-contemporary, or reroll)
- Flip commitment level (light tint ↔ full commitment)
- Change scale (single ↔ mini-sequence)
- Add a constraint modifier
- Try a named-work register
- Done — lock the changes / wrap up

**Conditional on a constraint being active:**
- Change constraint
- Drop the constraint, keep the beat

**Conditional on a named-work register being active:**
- Try a different named work
- Switch back to fresh (no named-work register)

**Conditional on a hybrid genre being active:**
- Drop one half of the hybrid
- Reroll the other half

**Conditional on hooks/lineage not yet shown:**
- Show compositional hook
- Show reference lineage

**"Surprise me" should always be an option** wherever the user is making a choice (register, named work, constraint, panel count). Don't omit it.

## What to hold back by default

These exist but stay hidden unless the user asks via the refine menu or directly:

- **Reference lineage** — which director/show the tonal lineage borrows from. The principle is instinct-first: pre-loading the reference biases the eye before the sketch.
- **Compositional hook** — what the staging needs to earn. Surfaces only on request, or automatically when the constraint modifier is active (because the constraint is what the hook explains).

## Writing rules for the beat itself

Borrowed from screenwriting action-line craft, adapted for storyboard practice:

- **Present tense, active voice.** "She runs," not "she is running" or "she ran."
- **Only what can be seen and heard.** No "she feels," no "he remembers." If an internal state matters, externalise it — what's visible on the face, in the body, in the environment.
- **Specific verbs over generic ones.** "Saunters," "tiptoes," "marches" — not "walks."
- **Concrete physical detail carries mood.** A "sinister" house is a tell; a house "with one window lit from the inside, curtains drawn" is a show.
- **Brevity.** 1–3 lines maximum per panel. White space matters. If it won't fit, the beat is too big and should be split.
- **The shift is the margin note.** One line. Not a tagline. Not a summary. The thinking about the frame, sitting next to the frame.

## Compositional hook — length rule

When surfaced, the compositional hook should be **2–4 sentences**, and should name **the one compositional question the staging has to answer** — not a checklist of staging concerns.

The hook is the editorial note in the margin of the page, not the production brief. If it starts listing depth, light, framing, negative space, and scale all in one paragraph, it has drifted into briefing — pull it back to the *one question*.

For mini-sequences with a constraint modifier active, each panel gets its own hook, each still 2–4 sentences.

## The reference bank (parked — to be designed separately)

A separate file will hold **director/show register specs** at `resources/storyboarding-knowledge-logs/beat-reference-bank.md`. These are not example beats and not full scripts — they are *the rules a work operates by*: tonal register, compositional rules, rhythm rules, what the work borrows from, what it refuses.

The bank is parked until its format is designed. Until then, when the user asks for a beat "in the register of [named work]," generate fresh from general knowledge of the work and surface a **bank-empty flag**:

> ⚠️ Bank empty for: [Work title]. Generated fresh. Add an entry to `resources/storyboarding-knowledge-logs/beat-reference-bank.md` once the bank is built.

The flag is itself useful — it prompts bank-building over time. Don't suppress it.

## Anti-patterns to avoid

Things this skill should **not** do, even if asked:

- **Don't prescribe shot type or camera angle by default.** That's the participant's compositional decision. Constraints are explicit (via the modifier parameter); inferred staging is not.
- **Don't generate full scenes.** If the output reads like a paragraph from a screenplay, it's too big. The unit is one moment.
- **Don't force screenplay format.** Format 2 borrows the *look and feel* of a screenplay page (action block + margin note), but does not force a slugline, character cues, or scene structure. The beat is smaller than a scene.
- **Don't borrow Save the Cat or feature-length beat structures.** Those are macro tools for whole scripts; this is a single-shot generator.
- **Don't substitute pattern-matching for design.** If a request is vague, generate with random defaults and let the refine menu do the steering — don't ask a form's worth of questions before producing anything.
- **Don't lead with the reference.** Lineage is held back by default. The participant's instinct comes first.
- **Don't let the shift drift into summary.** The shift is a margin note. If it's longer than one sentence, it's wrong.
- **Don't let the compositional hook drift into a brief.** 2–4 sentences. One question.
- **Don't default to prestige-drama domestic register.** Doorways, kitchen tables, folded letters, and breath on glass are *one* register, not the register. Rolled genre is not optional — honour it.
- **Don't reach for spectacle when light tint is rolled.** A sci-fi beat at light tint is a server light, not a starship. A fantasy beat at light tint is a candle that won't go out, not a dragon. The smaller frame is almost always the sketchable one.
- **Don't make hybrid genres equal-weighted blends.** One genre is the world, the other is the intrusion. *Horror × romance* is a romance world a horror intrudes on, not a 50/50 mash.

## Calibration examples

A well-formed single-panel beat, restrained anger register, no constraint:

````
```
A man folds a letter back into its envelope. He
sets it down on the kitchen table. Aligns its
edge with the edge of the table. Then aligns it
again.
```

> **Shift:** the second alignment is the moment the letter becomes the thing he can't put down.
````

A mini-sequence, 3 panels, anticipation tipping into disappointment register, with the "no faces visible" constraint applied:

````
**Panel 1**
```
A backpack on small shoulders, framed against
a window. Breath fogs the glass. Below, a car
turns into the driveway.
```

> **Shift:** waiting resolves into recognition — read in the stillness of the shoulders, not the face.

**Compositional hook:** the staging has to make the shoulders carry the recognition — usually a face's job. Negative space above the head matters: leaving it empty has to feel like a choice, not a crop.

**Panel 2**
```
A small hand lifts toward the glass. The car
rolls past the driveway and continues down
the street.
```

> **Shift:** the hand is mid-rise when the meaning of the car changes. The hand does not finish the gesture.

**Compositional hook:** the lifting hand is now the entire emotional event. The staging has to give the hand enough scale to carry that without making it the subject of the frame.

**Panel 3**
```
The hand lowers. The shoulders stay where they
were. The fog of breath has spread further on
the glass.
```

> **Shift:** the waiting hasn't ended — it has only been corrected.

**Compositional hook:** the cruelty of the shift is that nothing in the body has changed, only the meaning of the waiting. The fog of breath has to read as accumulation — evidence of time.
````

A single-panel beat, awe register, **genre: sci-fi**, **commitment: light tint**, no constraint:

````
```
An engineer pauses at a console. One indicator
light on the panel pulses, slow, where the others
are steady. She lowers her coffee without looking
at it.
```

> **Shift:** the pulse is when routine becomes attention — before she has named what she's seeing.
````

A single-panel beat, dread register, **genre: fantasy × horror** (fantasy world, horror intrusion), **commitment: full**, no constraint:

````
```
A torch on a stone wall burns sideways. Its flame
points down the corridor, away from the draft.
The hound at the steward's heel will not cross
the threshold.
```

> **Shift:** the room stops being a room the moment the fire chooses a direction.
````

A mini-sequence, 3 panels, anticipation tipping into disappointment register, **genre: noir × western** (noir world, western intrusion), **commitment: light tint**, no constraint:

````
**Panel 1**
```
Rain on a precinct window. A man in a wet coat
hangs a hat on a hook. Spurs, faintly, in the
hallway behind him.
```

> **Shift:** the city is the room he's in; the spurs are the room he came from.

**Panel 2**
```
He sets a folder on the desk. The spurs stop
at the doorway. A hand, gloved, rests on the
frame.
```

> **Shift:** the conversation has begun before either man has spoken.

**Panel 3**
```
The folder sits untouched. The hand on the
doorframe is gone. Water drips from the brim
of the hat onto the floor.
```

> **Shift:** the meeting that was going to happen has already not happened.
````

All examples obey the rules: present tense, visible/audible only, brief, fixed-width feel in the action block, shift as a one-line margin note. Hooks (when shown) are 2–4 sentences each and name a single compositional question. None prescribe camera angle in the beat itself. The genre-tinted beats avoid spectacle — the sci-fi beat is a server room, the fantasy × horror beat is a torch and a hound, the noir × western beat is a precinct doorway. Sketchable in five minutes.

## Known gaps (carry forward)

- **Phase context untested.** The skill claims it's curriculum-wide (Phase 1–4) but the test session never invoked phase-specific behaviour. Whether the output should adjust based on phase is a real question that needs a real session to answer.
- **Bank format is not yet designed.** The director/show register spec format needs to be drafted. The skill currently reads the bank only as a fallback; once specs exist, register-fidelity should rise noticeably.
- **Compositional hook with no constraint active is undefined.** Currently the hook is only surfaced when constraint is active or on direct request. Whether "no-constraint" hooks should look different (and how) hasn't been tested.
- **Genre + commitment + era landed in this iteration (2026-05-14).** Pool expanded from 10 → 17 genres because the v2 generator drifted to prestige-drama by default. Sub-tags added for the four genres with distinct sub-grammars. Era tint added as an orthogonal axis. Needs live test rolls to confirm: (a) the 20% hybrid rate feels right, (b) the 60/40 light-vs-full split feels right, (c) the 15% era-tint rate feels like flavour and not noise, (d) the 25% sub-tag rate feels right when parents roll, (e) light tint actually lands as light and not as drama with a prop. Adjust ratios if rolls feel skewed.
- **Sub-tag list is short on purpose.** Only sub-genres with strong distinct visual grammar are in scope (cyberpunk, folk horror, epic/urban fantasy, screwball/dark comedy). If a new sub-tag earns a calibration example here, it can join the roll.
- **Era pool is curated, not exhaustive.** Pre-ancient eras and very specific micro-periods (Belle Époque, Tang dynasty, etc.) aren't in the pool yet. Expand only if a session shows the existing pool is too coarse.
