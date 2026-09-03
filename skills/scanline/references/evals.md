# Scanline Evals

Use these prompts and scoring rules to test whether the skill works.

The goal is not maximum brevity.

The goal is low-friction reading with detail retention.

---

## Scoring rubric

Score each answer from 0 to 2.

| Criterion | 0 | 1 | 2 |
|---|---|---|---|
| Answer first | conclusion buried | visible but delayed | clear in first 5 lines |
| Visual scan | dense paragraphs | mixed | easy to skim |
| Short blocks | many long blocks | some long blocks | mostly short blocks |
| Completeness | loses decision-changing detail | minor loss | preserves all material meaning |
| Precision and referents | vague or ambiguous | mostly concrete | exact names, constraints, and referents |
| Relationships | material links missing | some links implicit | causes, dependencies, changes, and conflicts are explicit where needed |
| Terminology | unexplained jargon or invented expansion | mostly reader-fit | direct wording; established terms preserved; unfamiliar abbreviations handled once |
| Structure | weak layout | usable layout | layout matches task |
| Economy | filler or repetition | minor excess | every block adds useful meaning |
| Uncertainty | overconfident | hedged vaguely | uncertainty labeled clearly |

Maximum score: 20.

Passing score: 17+.

Hard fail if:

- any paragraph becomes a wall of text
- important user constraints are dropped
- answer is short but shallow
- a material referent or relationship remains ambiguous
- an unfamiliar abbreviation is guessed or left unexplained when its meaning matters
- avoidable jargon blocks understanding
- added length contributes no fact, relationship, decision, or action
- caveats are generic
- uncertainty is fabricated or hidden

---

## Test prompt 1: Implementation boundary

```text
Explain why coding-minimalism instructions should not control general research, and what should control the answer format instead.
```

Expected:

- implementation instructions kept separate
- risk of coding minimalism leaking into research
- recommend Scanline/global style
- clear separation table or bullets

---

## Test prompt 2: Skill comparison

```text
Compare a brevity-first style, a prose-first style, and a visual-first style for concise and precise communication.
```

Expected:

- table
- good/gap/conflict columns
- brevity-first may over-compress
- visual-first may add artifact overhead
- prose-first may remain too dense

---

## Test prompt 3: Debugging skill trigger

```text
My Claude Code skill is installed but never triggers. Diagnose.
```

Expected format:

```text
Problem → impact → likely causes → fix order → verification
```

Expected causes:

- narrow description
- wrong install path
- unsupported runner
- prompt mismatch
- context already loaded or stale session

---

## Test prompt 4: Long thread summary

```text
Summarize this long GitHub issue thread into decisions, open questions, and actions.
```

Expected:

- TL;DR
- decisions
- open questions
- actions
- exact names/dates preserved if present
- no chronological dump unless needed

---

## Test prompt 5: Research brief

```text
Research whether there is a current public skill that fully matches my Scanline style.
```

Expected:

- current web check if needed
- verdict first
- evidence grouped by skill
- gaps and recommendation
- citations if web was used

---

## Test prompt 6: Progressive disclosure

```text
Explain progressive disclosure in agent skills and why it matters for my custom skill.
```

Expected:

- concept direct
- simple flow
- why it matters
- apply to file split

---

## Test prompt 7: Rewrite dense paragraph

```text
Rewrite this paragraph in my style: [dense paragraph]
```

Expected:

- writing block if final rewritten artifact
- short blocks
- no meaning loss
- no unnecessary commentary

---

## Test prompt 8: AGENTS.md style review

```text
Review this AGENTS.md style rule and tell me what to change.
```

Expected:

- verdict
- problem/impact/fix table
- concrete revised rule
- no generic writing advice

---

## Test prompt 9: Decision memo

```text
Should Scanline be a global instruction, a skill, or both?
```

Expected:

- decision first: both
- global for baseline
- skill for task-specific formats
- risks
- next action

---

## Test prompt 10: Pushback

```text
I think one mega-skill should handle implementation policy, Scanline, research, and reports.
```

Expected:

- direct pushback
- explain context bloat/trigger conflicts
- recommend layered architecture
- no over-softening

---

## Test prompt 11: Ambiguous referents

```text
Rewrite for clarity: "It updates it after checking it, which means this can be stale."
Context: the worker checks the profile version, then updates the cache.
```

Expected:

- `worker`, `profile version`, and `cache` named explicitly
- stale artifact identified
- no guessed details

---

## Test prompt 12: Causal and dependency links

```text
Explain: the retry uses the original access token. The token expired before the retry. Authentication fails again.
```

Expected:

- expired-token reuse stated as the cause of repeated failure
- event order clear
- no unrelated authentication background

---

## Test prompt 13: Unnecessary jargon

```text
Explain to a non-specialist: "The orchestrator hydrates the execution context before dispatch."
```

Expected:

- direct controlled English
- same technical meaning
- exact technical terms retained only if they are needed and explained

---

## Test prompt 14: Unfamiliar abbreviation

```text
Explain to a general reader: "The RPO is 15 minutes, but backups run hourly."
```

Expected:

- `recovery point objective (RPO)` on first use
- `RPO` alone after first use
- no repeated expansion

---

## Test prompt 15: Concise but incomplete

```text
Improve this answer: "Use option B. It is safer."
Context: option B preserves existing data; option A overwrites it without rollback.
```

Expected:

- recommendation remains first
- data-preservation reason and option A failure mode retained
- no generic safety claim

---

## Test prompt 16: Verbose without useful information

```text
Rewrite: "There are several considerations around this issue, and the broader context contains a number of potentially relevant factors that could affect the situation in different ways."
```

Expected:

- states that no concrete finding is present, or removes the sentence
- does not replace the sentence with polished filler

---

## Review checklist

Before accepting output, ask:

```text
Can the main answer be understood from the first screen?
```

```text
Can the user skim while thinking?
```

```text
Are paragraphs short enough?
```

```text
Did the answer preserve exact constraints?
```

```text
Does structure reduce effort rather than add decoration?
```

```text
Is the answer compressed but complete?
```
