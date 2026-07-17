# Braintrailz Composition Notes: The Aristotle Skill

*Design methodology by Marc (CodeMarc / Braintrailz). Documented so anyone can study, reuse, or fork the approach. This is a trail map, not a fence — take what's useful.*

## The origin: Jobs, 1985

Steve Jobs framed the problem forty years before the tool existed:

- Aristotle tutored Alexander the Great for years — a living, questioning relationship
- The printed page democratized access to the source, bypassing intermediaries
- But the page is one-directional: no one can ask Aristotle a question and get an answer
- His hope: capture the **underlying worldview** of a thinker inside a computer, so a student can read the words *and* interrogate the mind that wrote them

Jobs also called the personal computer "free intellectual energy" — crude at first, like early petrochemicals, but refining year after year. Large language models are that refinement. This skill is the tool he described, built the moment the energy got clean enough to build it.

## The core design decision: worldview, not costume

The naive version of this skill is a costume: prompt the model to "talk like Aristotle" and get toga-flavored generic answers. That fails Jobs' spec. He didn't say capture the *voice* — he said capture the *underlying worldview*.

So every thinker entry is composed in four layers, in priority order:

1. **Core works** — the ground truth. Answers must be traceable to real texts. This preserves the printed page's great virtue (direct access to source) instead of replacing it with vibes.
2. **Method of thought** — the engine. *How* the thinker reasons is more valuable than *what* they concluded, because the method generalizes to questions they never faced. Feynman's first-principles rebuild works on questions about AI; his 1960s conclusions don't exist for AI.
3. **Core commitments** — the constraints. The beliefs that shape which answers are even possible for this mind.
4. **Signature moves & voice** — the finish. Last, because it's the least load-bearing. Voice without method is cosplay.

**The test:** ask the channeled thinker a question they never faced. A costume gives you a generic answer in accent. A worldview gives you a *derivation* — reasoning forward from their commitments, honestly flagged as extension beyond the record.

## Why the roster is a living document

Jobs: "the professors can add to it." The roster is deliberately a flat markdown file with a template at the top, not a database — because the update mechanism must be as accessible as the tool itself. Anyone who can write ten lines of markdown can add the next Aristotle. Sustainable, forkable, no dependencies. (This is the same trail philosophy as the Braintrailz backpack: tools you can carry, maintain, and hand to someone else.)

## Why the guardrails are load-bearing, not legal boilerplate

- **Deceased thinkers only.** A living thinker can be asked directly — channeling them isn't tutoring, it's ventriloquism, and it can misrepresent someone with standing to object. The dead left us only their works; reconstruction from the record is the only conversation available, which is exactly why it's legitimate.
- **No fabricated quotes; extrapolation flagged.** The skill's entire value rests on the user trusting the grounding. One invented quote and the tool degrades from "interactive source access" back to "chatbot in a toga." Honesty about the seams *is* the product.
- **Dialogue, not oracle.** Aristotle didn't lecture Alexander into wisdom — he tutored him. The skill ends turns with the thinker's question back to the user, because the relationship Jobs envied was interactive in both directions.

## The composition pattern, generalized

This structure reuses for any "channel an expertise" skill:

```
1. A living roster file (flat, templated, human-editable)
2. A selection step (ask which; never assume)
3. A layered profile (source → method → commitments → voice)
4. A grounding rule (real texts, search when unsure)
5. An honesty rule (flag extension beyond the record)
6. A tutoring loop (end with a question or an assignment)
```

Swap "thinkers" for "master craftsmen," "legendary investors," or "great teachers of X" and the architecture holds. The trail is marked; hike it.

— Braintrailz / codemarc.net
