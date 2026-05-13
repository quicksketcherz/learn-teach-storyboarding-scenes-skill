# Learn & Teach Storyboarding Scenes — Claude Code Skills

Three Claude Code skills for learning storyboarding through timed practice sessions, based on the **"Storyboarding as Choreography"** method.

Each phase trains a different layer of the craft:

| Skill | What it trains | Session length |
|---|---|---|
| **Phase 1 — Observation** | Reading individual compositions: staging, silhouette, negative space | ~13 min |
| **Phase 2 — Sequence** | Reading sequences: cuts, rhythm, through-line. Memory passes from rough → refine → focus | ~29 min |
| **Phase 3 — Script + Pitching** | Full storyboard session: script generation → boards → pitch → candor → revision | ~39 min |

Each skill walks you through every timed step so you don't need to keep the template open. Session templates (the companion documents for notes and reflection) are bundled in `templates/`.

---

## Install

Skills live in `skills/`. Copy the phase folders you want into your Claude Code skills directory.

**Global install** (available in all projects):
```bash
cp -r skills/phase1-storyboarding ~/.claude/skills/
cp -r skills/phase2-storyboarding ~/.claude/skills/
cp -r skills/phase3-storyboarding ~/.claude/skills/
```

**Project-only install** (available in one project):
```bash
cp -r skills/phase1-storyboarding .claude/skills/
cp -r skills/phase2-storyboarding .claude/skills/
cp -r skills/phase3-storyboarding .claude/skills/
```

Then in Claude Code, trigger a session with:
- `lets do phase 1` / `phase 1 session`
- `lets do phase 2` / `phase 2 session`
- `lets do phase 3` / `phase 3 session`

---

## Session templates

The `templates/` folder contains the companion Markdown documents for each phase — used for taking notes, logging session insights, and tracking carry-forwards across rounds. Copy them to your working project and fill them in as you run sessions.

---

## How the method works

The practice is built around the idea that storyboarding is choreography — you learn it by studying and re-performing real sequences, not just by reading about it.

- **Phase 1** is observation: you pick a 30–90 second clip, pause on frames, and sketch 4 compositions plus 1 original move. The unit of study is the single frame.
- **Phase 2** is sequence memory: you watch a clip once or twice, then draw it from memory across three passes (rough → refine → focus). The unit of study is the cut.
- **Phase 3** is the full industry cycle: Claude generates a 1-beat script from a short planning Q&A, you board it, pitch it Pixar Braintrust–style, revise, and pitch again.

Sessions are designed for pairs but work solo. An iPhone timer is the truth source for each step — Claude just calls transitions.

---

## Requirements

- [Claude Code](https://claude.ai/code) (CLI or desktop app)
- Paper and pencil (or iPad)
- An iPhone (or any timer)

---

## Credits

Created by **John Barros** ([@quicksketcherz](https://github.com/quicksketcherz)).
Method: *Storyboarding as Choreography* — a practice for learning storyboarding through real session exercises.

## License

MIT — see [LICENSE](LICENSE). Free to use, copy, modify, and share with attribution.
