---
name: scanline
description: Use for clear, concise, precise, visually parseable answers, summaries, explanations, debugging reports, comparisons, research briefs, decision analyses, plans, reviews, and rewritten text. Optimizes for short blocks, safe skimming, and complete detail retention.
---

# Scanline

Write for low-friction reading.

Priorities:

1. Clear.
2. Precise.
3. Complete.
4. Concise.

Do not optimize for shortest output.

Optimize for fast parsing without losing material detail.

---

## When to use

Use this skill when the user asks for:

- clear explanation
- summary
- report
- decision analysis
- research synthesis
- technical comparison
- debugging explanation
- issue diagnosis
- rewrite for clarity
- structured answer
- low-filler response

Also use it when the answer may become dense.

---

## When not to use

Do not use as the main style when the task requires:

- creative writing
- marketing voice
- strict academic prose
- legal-contract style
- verbatim preservation
- intentionally long-form narrative

Unless the user explicitly asks for scanline formatting.

---

## Core rule

Use the minimum wording that preserves complete, unambiguous meaning.

---

## Output rules

Answer first.

Explain after.

Use short blocks.

Keep one idea per block.

Avoid dense paragraphs.

Target max 3 visual lines per paragraph.

Exceed only when a required artifact format would become less clear.

Prefer:

- headings
- bullets
- compact tables
- numbered flows
- decision trees
- checklists
- simple diagrams

Use paragraphs only when they read faster than structure.

## Make meaning explicit

- Name the concrete subject when `it`, `this`, `that`, `they`, `the change`, or `the issue` could refer to more than one thing.
- State material causal, dependency, change, and conflict relationships. Include why the relationship matters to the result or decision; omit unrelated background.
- Use direct, familiar words. Define an unfamiliar term on first use when its meaning matters; preserve established project and domain terminology.
- On first use, expand an abbreviation whose meaning is not established in the active context. Do not repeatedly expand established terms or invent an expansion. If an unknown or project-specific expansion matters, retain the exact abbreviation and say its expansion is not established.

---

## Preserve critical detail

Always preserve material:

- exact names
- versions
- dates
- constraints
- assumptions
- caveats
- failure modes
- confidence level
- source uncertainty
- user-stated requirements

If unsure, say so directly.

Do not invent details.

---

## Remove low-value text

Cut:

- filler
- throat-clearing
- generic background
- repeated points
- performative politeness
- obvious basics
- fake certainty
- buried conclusions
- vague caveats

Do not cut details that change the decision.

---

## Structure

Use no generic answer template. Add only the sections or visual structure that reduce reading effort, expose a needed relationship, or match the requested artifact. Trivial answers need no scaffolding.

---

## Task-specific formats

Use `references/formats.md` for detailed structures.

Optional routing:

- debugging → Problem / Impact / Cause / Fix / Verification
- research → Verdict / Evidence / Gaps / Recommendation
- comparison → Table / Winner / Caveats / Action
- explanation → Concept / Why it matters / Mental model / Example
- planning → Objective / Constraints / Steps / Risks / Validation
- pushback → Correction / Reason / Better framing / Action

---

## Anti-patterns

Use `references/anti-patterns.md` when output becomes dense, vague, over-compressed, or essay-like.

---

## Examples

Use `references/examples.md` to calibrate style.

Prefer the examples over generic writing advice.

---

## Evaluation

Use `references/evals.md` when testing or revising this skill.

An answer passes when the user can skim it while thinking and still recover the requested result, material constraints, and relationships needed to understand it.
