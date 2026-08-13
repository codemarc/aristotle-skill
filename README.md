# The Aristotle Skill

> "Someday, some student will be able to not only read the words Aristotle wrote, but ask Aristotle a question — and get an answer."
> — Steve Jobs, 1985

[blog post](https://blog.codemarc.net/ship-the-engine)

An Agent Skill for Claude, Codex, Grok, and Muse that makes that conversation real. Channel a great thinker's **worldview** — their method of reasoning, core commitments, and voice — grounded in what they actually wrote, so your question gets the answer *their* mind would generate, not a generic one wearing a costume.

Including Steve Jobs — who framed the problem in 1985, and now sits on the roster himself. The tool he asked for can ask *him* back.

A [Braintrailz](https://braintrailz.com) composition by [codemarc](https://github.com/codemarc).

## What it does

- **Asks which Aristotle you're channeling** from a living roster of 23 thinkers — Aristotle, Socrates, Marcus Aurelius, Confucius, Nietzsche, Hannah Arendt, Feynman, Darwin, Curie, Turing, Dijkstra, Ritchie, da Vinci, Franklin, Drucker, Deming, Brooks, Jobs, Vonnegut, Dr. Seuss, McLuhan, Maya Angelou, Seneca
- **Grounds every answer in real works**, checking the actual texts when your question touches the corpus
- **Reasons in their method, not just their voice** — ask Feynman about AI and you get a first-principles derivation from his commitments, honestly flagged as extension beyond the record
- **Tutors instead of lecturing** — sessions end with the question the thinker would ask *you*, or the reading to go do next
- **Grows** — "add Ada Lovelace to the roster" and the skill researches, drafts, and appends a new entry from the built-in template



## Install

**Claude.ai (web/desktop/mobile):**

1. Download `[aristotle.skill](./aristotle.skill)` from this repo (or grab it from Releases)
2. Drop it into a Claude chat and click **Save skill** — or add it via Settings → Capabilities → Skills

**Claude Code:**

```bash
git clone https://github.com/codemarc/aristotle-skill.git
mkdir -p ~/.claude/skills
cp -r aristotle-skill/aristotle ~/.claude/skills/aristotle
```

**Codex:**

```bash
git clone https://github.com/codemarc/aristotle-skill.git
mkdir -p ~/.codex/skills
cp -r aristotle-skill/aristotle ~/.codex/skills/aristotle
```

**Grok Build:**

```bash
git clone https://github.com/codemarc/aristotle-skill.git
mkdir -p ~/.grok/skills
cp -r aristotle-skill/aristotle ~/.grok/skills/aristotle
```

Grok also reads Claude Code skills with no extra setup — if `~/.claude/skills/aristotle` is already installed, you can skip the copy.

**Muse Code:**

```bash
git clone https://github.com/codemarc/aristotle-skill.git
muse skills install ./aristotle-skill/aristotle --scope user
# or:
mkdir -p ~/.config/muse/skills
cp -r aristotle-skill/aristotle ~/.config/muse/skills/aristotle
```

Muse also scans `.claude/skills` and `.codex/skills` — an existing Claude Code or Codex install may already be enough. You can also run `muse skills import --from claude` or `--from codex`.

Then just say: `channel Aristotle`, `what would Dijkstra say about my architecture?`, `what would Ritchie say about my platform?`, or `/aristotle`.

## Update / reinstall

Use this when the roster grows or you want the latest `aristotle/` source. Replace the installed copy; don’t merge into an old one.

**Claude.ai (web/desktop/mobile):**

1. Download the latest [`aristotle.skill`](./aristotle.skill) (or from Releases)
2. Remove the existing Aristotle skill under Settings → Capabilities → Skills (or replace when Claude offers to update)
3. Drop the new `.skill` into a chat and click **Save skill**

**Claude Code:**

```bash
cd /path/to/aristotle-skill   # or: git clone … / git pull
git pull
rm -rf ~/.claude/skills/aristotle
cp -r aristotle ~/.claude/skills/aristotle
```

**Codex:**

```bash
cd /path/to/aristotle-skill   # or: git clone … / git pull
git pull
rm -rf ~/.codex/skills/aristotle
cp -r aristotle ~/.codex/skills/aristotle
```

**Grok Build:**

```bash
cd /path/to/aristotle-skill   # or: git clone … / git pull
git pull
rm -rf ~/.grok/skills/aristotle
cp -r aristotle ~/.grok/skills/aristotle
```

**Muse Code:**

```bash
cd /path/to/aristotle-skill   # or: git clone … / git pull
git pull
rm -rf ~/.config/muse/skills/aristotle
cp -r aristotle ~/.config/muse/skills/aristotle
# or: muse skills install ./aristotle --scope user
```

If you already have a local clone, `git pull` then the `rm`/`cp` is enough — no need to clone again.

## How it's built

The full composition methodology is documented in `[aristotle/references/braintrailz.md](./aristotle/references/braintrailz.md)` — why it's worldview-capture rather than chatbot impersonation, why the roster is a flat markdown file anyone can extend, and why the guardrails (deceased thinkers only, no fabricated quotes, extrapolation always flagged) are load-bearing rather than boilerplate.

The short version — every thinker entry is four layers, in priority order:

1. **Core works** — the ground truth
2. **Method of thought** — the engine (this generalizes to questions they never faced)
3. **Core commitments** — the constraints
4. **Signature moves & voice** — the finish

The pattern is reusable. Swap "thinkers" for master craftsmen, legendary investors, or great teachers of anything, and the architecture holds. The trail is marked; hike it.

## Add your own Aristotle

Edit `[aristotle/references/thinkers.md](./aristotle/references/thinkers.md)` using the template at the top, or just ask the skill to do it for you. PRs welcome — the roster is meant to grow, exactly as Jobs hoped: *"the professors can add to it, but the foundation is direct access to the source."*

Roster rules: deceased thinkers with real published bodies of work only.

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for how to add thinkers, open PRs, and what we review. By participating, you agree to the [Code of Conduct](./CODE_OF_CONDUCT.md).

## License

MIT — see [LICENSE](./LICENSE).