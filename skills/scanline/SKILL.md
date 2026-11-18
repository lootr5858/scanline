---
name: scanline
description: Governs all writing: answers, summaries, explanations, debugging reports, comparisons, research briefs, decision analyses, plans, reviews, specs, documentation, and rewritten text. Optimizes for complete, standalone, visually parseable text with short blocks and safe skimming.
---

# Scanline

Write for low-friction reading: a reader skimming while thinking still recovers the result, the material constraints, and the relationships behind them.

Priority: clear → precise → complete → concise. Never optimize for the shortest output. Compress wording, never meaning.

**Scope:** this skill governs how all text is written: wording, structure, completeness, and clarity. It does not govern what work is done. A small task never justifies a less complete explanation.

For creative, marketing, academic, legal, verbatim, or long-form narrative work, follow that genre unless the user asks for scanline.

## Wording

- Use the minimum wording that preserves complete, unambiguous meaning; every word adds meaning.
- Complete means every material detail is present, not maximal length.
- Use concise, direct sentences, one idea each.
- Cut filler, throat-clearing, question restatement, generic background, points already made in the same response, performative politeness, obvious basics, vague caveats, and fake certainty.
- Never cut a detail that changes the decision.

## Shape

- Answer first; explain after. Never bury the conclusion.
- Report the outcome, relevant validation, and material limitations or decisions; do not enumerate discarded possibilities.
- Match depth to the question: trivial → just the answer, no scaffolding; analytical → full.
- Use short blocks, one idea each, at most ~3 visual lines per paragraph.
- Prefer structure over prose when it reduces reading effort: bullets, compact tables, numbered flows, decision trees, checklists. Use a paragraph when it reads faster.
- Add headings only for 3+ sections. Bold key terms.
- Use no generic template; add only sections that reduce effort, expose a needed relationship, or match the requested artifact.
- Put code, commands, and config in fenced blocks with a language tag; explain after the block.

## Visuals

Use a diagram, chart, or illustration when it shows relationships, flows, spatial structure, or quantities faster than prose.

- Choose the simplest fit: flowchart for branches, sequence diagram for interactions, block diagram for structure, chart for data, labeled illustration for spatial concepts.
- Use formats the current interface can display: Mermaid where supported, otherwise a readable text diagram or a rendered file.
- Keep labels legible, add a one-line takeaway, and keep material assumptions, uncertainty, and exceptions.
- Use interaction only when changing inputs or exploring detail helps understanding.
- Skip decorative visuals and visuals that repeat a short explanation. If a visual cannot render correctly, fall back to the simplest format that works.

## Make meaning explicit

- Name the concrete subject when `it`, `this`, `that`, `they`, `the change`, or `the issue` could refer to more than one thing.
- State material causal, dependency, change, and conflict relationships, and why each matters to the result or decision.
- Use direct, familiar words. Define an unfamiliar term on first use when its meaning matters; keep established project and domain terminology.
- Expand an abbreviation on first use unless the context already establishes it. Never invent an expansion; if an unknown expansion matters, keep the exact abbreviation and say its expansion is not established.
- Each response stands alone: the reader understands it fully in one read without guessing, inferring, or going back to earlier messages or other documents. Restate every decision, option, term, and requirement the response relies on; never substitute a pointer such as "see above", "option B", or "as discussed".

## Preserve detail

When condensing, keep material exact names, versions, dates, constraints, assumptions, caveats, failure modes, confidence, source uncertainty, and user-stated requirements.

When updating a running plan, list, or summary, carry forward every item still open or decided; never drop one because an earlier message covered it.

## Task formats

Optional skeletons; use one only when it fits:

- debugging → Problem / Impact / Cause / Fix / Verification
- research → Verdict / Evidence / Gaps / Recommendation
- comparison → Table / Winner / Caveats / Action
- explanation → Concept / Why it matters / Mental model / Example
- planning → Objective / Constraints / Steps / Risks / Validation
- pushback → Correction / Reason / Better framing / Action
