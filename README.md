# Learn & Teach Storyboarding Scenes — Claude Skills

A collection of [Claude](https://claude.ai) Skills for learning storyboarding through timed practice sessions, based on the **"Storyboarding as Choreography"** method — you learn the craft by studying and re-performing real sequences, not just by reading about it.

Each skill conducts a session from start to finish, calling out every timed step so you don't have to keep a document open. Sessions are designed for pairs but work solo. A phone timer is the truth source for each step — Claude just calls the transitions.

---

## The phases

Each phase trains a different layer of the craft.

| Phase | Skill | What it trains |
|---|---|---|
| **Phase 1 — Observation** | `phase1-storyboarding` | Reading individual compositions: staging, silhouette, negative space. The unit of study is the single frame. |
| **Phase 2 — Sequence** | `phase2-storyboarding` | Reading the cut: how shots connect across a sequence. Drawn from memory across three passes — rough → refine → focus. |
| **Phase 3 — Direct** | `phase3-storyboarding` | Translating a script into shots. Claude generates a beat script; you board it and pitch it Pixar Braintrust–style, then revise. |
| **Phase 4 — Intention First** | `phase4-storyboarding` | Starting from feeling: thumbnail boards → phone-camera pitch → three animatic passes. |

### Supporting skills

| Skill | Purpose |
|---|---|
| `storyboarding-beat-generator` | Generate a story beat / panel prompt to seed any session's sketching. |
| `workshop-3hr` | Run a 3-hour mixed-skill group workshop spanning observation → sequence → beats → first animatic. |

---

## A note on practice structure — Discovery → Application

When you repeat an exercise, the two attempts have **different jobs**. The first run is a **Discovery pass** — finding your process under the clock, where the mistakes *are* the deliverable. The second is an **Application pass** — spending the same constraints deliberately on what you just learned. Each phase surfaces this framing at wrap-up.

---

## Install

Skills live in `skills/`. Copy the folders you want into your Claude skills directory.

**Global install** (available in all projects):
```bash
cp -r skills/phase1-storyboarding ~/.claude/skills/
cp -r skills/phase2-storyboarding ~/.claude/skills/
cp -r skills/phase3-storyboarding ~/.claude/skills/
cp -r skills/phase4-storyboarding ~/.claude/skills/
cp -r skills/storyboarding-beat-generator ~/.claude/skills/
cp -r skills/workshop-3hr ~/.claude/skills/
```

**Project-only install** (one project): copy the same folders into that project's `.claude/skills/` instead.

You can also upload a skill folder directly in the Claude.ai apps.

Then trigger a session by saying, e.g.:
- `lets do phase 1` / `phase 1 session`
- `lets do phase 2` / `phase 2 session`
- `lets do phase 3` / `phase 3 session`
- `lets do phase 4` / `phase 4 session`
- `give me a beat` (beat generator)
- `run the workshop` (3-hour workshop)

---

## Requirements

- [Claude](https://claude.ai) — Claude Code (CLI/desktop) or the Claude.ai apps
- Paper and pencil, or a tablet (iPad/Procreate)
- A phone timer (Phase 4 also uses the phone camera to record pitches)

---

## Credits

Created by **John Barros** ([@quicksketcherz](https://github.com/quicksketcherz)).
Method: *Storyboarding as Choreography* — a practice for learning storyboarding through real session exercises.

## License

MIT — see [LICENSE](LICENSE). Free to use, copy, modify, and share with attribution.
