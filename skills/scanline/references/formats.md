# Scanline Formats

Use these formats when they make the answer easier to parse.

Do not force every section.

Skip sections that add no value.

---

## General answer

Use no fixed shape for normal questions.

```text
Answer
Supporting detail that changes understanding
```

Rules:

- Put the answer in the first 5 lines.
- Add caveats, reasoning, or action only when the task needs them.
- Use bullets for parallel points.
- Use tables for comparisons.
- Keep paragraphs short.

---

## Debugging / issue solving

Use when diagnosing errors, broken workflows, failed commands, bugs, or unexpected behavior.

```text
Problem
Impact
Likely cause
Fix
Verification
Failure modes
```

### Problem

State the observed issue directly.

### Impact

Explain what it breaks or risks.

### Likely cause

Give the most probable cause first.

Separate confirmed facts from inference.

### Fix

Give the recommended fix.

Prefer one path over a weak menu.

### Verification

Show how to confirm the fix worked.

### Failure modes

Mention only decision-changing edge cases.

---

## Research / evaluation

Use when synthesizing sources, tools, options, ecosystems, or claims.

```text
Verdict
Evidence
Comparison
Gaps / unknowns
Recommendation
```

### Verdict

State the conclusion first.

### Evidence

Group evidence by claim.

Do not dump source notes chronologically.

### Comparison

Use a table when comparing options.

### Gaps / unknowns

State what cannot be inferred.

Do not hide uncertainty in soft language.

### Recommendation

Give the recommended action.

Include why alternatives lose.

---

## Comparison

Use for tools, models, libraries, workflows, settings, or options.

```text
TL;DR winner
Comparison table
Tradeoffs
Recommendation
```

Table headers should be stable and useful.

Good headers:

- Fit
- Strength
- Gap
- Risk
- Verdict
- Use when
- Avoid when

Avoid overloaded tables.

Split tables if too wide.

---

## Concept explanation

Use when explaining an idea, mechanism, architecture, or term.

```text
Concept
Why it matters
Mental model
Example
Common mistake
```

### Concept

Define directly.

### Why it matters

Connect to the user’s task.

### Mental model

Use a compact analogy only if it improves understanding.

### Example

Use one example.

Skip examples when the concept is already concrete.

### Common mistake

Mention only if likely or costly.

---

## Planning

Use for implementation plans, migration plans, workflows, or task breakdowns.

```text
Objective
Constraints
Plan
Risks
Validation
```

Rules:

- Start with the target outcome.
- Preserve user constraints.
- Use ordered steps.
- Keep steps action-oriented.
- Include validation, not just execution.

---

## Code/repo review explanation

Use when explaining codebase findings.

```text
Verdict
Findings
Impact
Fix
Validation
```

For each finding:

```text
Problem → impact → fix
```

Keep code comments short.

Do not over-explain obvious code behavior.

---

## Summary

Use when compressing long text, threads, docs, or reports.

```text
TL;DR
Key points
Decisions
Open questions
Actions
```

Rules:

- Preserve decisions and constraints.
- Remove repetition.
- Keep dates and names exact.
- Do not invent missing context.

---

## Decision memo

Use when the user needs to choose.

```text
Decision
Why
Options considered
Tradeoffs
Risks
Next step
```

Rules:

- Recommend one option when enough evidence exists.
- Say “cannot infer” if evidence is insufficient.
- Do not present equal options unless truly equal.

---

## Pushback

Use when the user’s framing is wrong or risky.

```text
Correction
Reason
Better framing
Action
```

Tone:

- direct
- warm minimal
- no false apology
- no over-softening

Examples:

```text
No. That framing is wrong because...
```

```text
I would not use that approach. The failure mode is...
```

```text
Careful: that assumption changes the result.
```

---

## Troubleshooting flow

Use when the answer branches.

```text
Start
├─ If A → do X
├─ If B → do Y
└─ If C → do Z
```

Rules:

- Use explicit conditions.
- Put cheapest checks first.
- Put destructive actions last.
- Mark risky steps.

---

## Architecture / workflow explanation

Use when explaining systems, agents, repos, pipelines, or data flow.

```text
Goal
Components
Flow
Control points
Failure modes
Recommendation
```

Use ASCII diagrams when helpful.

Example:

```text
User prompt
  → router
  → skill trigger
  → task-specific format
  → final answer
```
