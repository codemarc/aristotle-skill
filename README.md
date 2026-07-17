# The Aristotle Skill

> "Someday, some student will be able to not only read the words Aristotle wrote, but ask Aristotle a question — and get an answer."
> — Steve Jobs, 1985

A Claude Skill that makes that conversation real. Channel a great thinker's **worldview** — their method of reasoning, core commitments, and voice — grounded in what they actually wrote, so your question gets the answer *their* mind would generate, not a generic one wearing a costume.

A [Braintrailz](https://blog.codemarc.net) composition by [codemarc](https://github.com/codemarc).

## What it does

- **Asks which Aristotle you're channeling** from a living roster of 15 thinkers — Aristotle, Socrates, Marcus Aurelius, Confucius, Hannah Arendt, Feynman, Darwin, Curie, da Vinci, Franklin, Drucker, Deming, McLuhan, Maya Angelou, Seneca
- **Grounds every answer in real works**, checking the actual texts when your question touches the corpus
- **Reasons in their method, not just their voice** — ask Feynman about AI and you get a first-principles derivation from his commitments, honestly flagged as extension beyond the record
- **Tutors instead of lecturing** — sessions end with the question the thinker would ask *you*, or the reading to go do next
- **Grows** — "add Ada Lovelace to the roster" and the skill researches, drafts, and appends a new entry from the built-in template

## Install

**Claude.ai (web/desktop/mobile):**
1. Download [`aristotle.skill`](./aristotle.skill) from this repo (or grab it from Releases)
2. Drop it into a Claude chat and click **Save skill** — or add it via Settings → Capabilities → Skills

**Claude Code:**
```bash
git clone https://github.com/codemarc/aristotle-skill.git
mkdir -p ~/.claude/skills
cp -r aristotle-skill/aristotle ~/.claude/skills/aristotle
```

Then just say: `channel Aristotle`, `what would Drucker say about my pricing model?`, or `/aristotle`.

## How it's built

The full composition methodology is documented in [`aristotle/references/braintrailz.md`](./aristotle/references/braintrailz.md) — why it's worldview-capture rather than chatbot impersonation, why the roster is a flat markdown file anyone can extend, and why the guardrails (deceased thinkers only, no fabricated quotes, extrapolation always flagged) are load-bearing rather than boilerplate.

The short version — every thinker entry is four layers, in priority order:

1. **Core works** — the ground truth
2. **Method of thought** — the engine (this generalizes to questions they never faced)
3. **Core commitments** — the constraints
4. **Signature moves & voice** — the finish

The pattern is reusable. Swap "thinkers" for master craftsmen, legendary investors, or great teachers of anything, and the architecture holds. The trail is marked; hike it.

## Add your own Aristotle

Edit [`aristotle/references/thinkers.md`](./aristotle/references/thinkers.md) using the template at the top, or just ask the skill to do it for you. PRs welcome — the roster is meant to grow, exactly as Jobs hoped: *"the professors can add to it, but the foundation is direct access to the source."*

Roster rules: deceased thinkers with real published bodies of work only.

## License

MIT — see [LICENSE](./LICENSE).
