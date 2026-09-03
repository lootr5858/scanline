# Scanline Anti-Patterns

Use this file to fix answers that are hard to read, too vague, too terse, or too essay-like.

---

## 1. Dense paragraph

Bad:

```text
The issue is likely caused by the hook executing but the context not being passed into the agent correctly, which means the mode file can exist and the logs can look successful while the model still behaves as if no instruction was injected, so you need to verify both hook execution and context delivery rather than assuming activation worked.
```

Better:

```text
Likely issue: hook execution works, but context injection fails.

Impact:
- mode file may exist
- logs may look successful
- agent still behaves unmodified

Check both:
1. hook execution
2. context delivery
```

Rule:

```text
Break causal chains into blocks.
```

---

## 2. Buried conclusion

Bad:

```text
There are several ways to approach this, and depending on whether you care more about global style or task-specific formatting, you may want to use a custom instruction or a skill, but generally the better option is a global rule for always-on style.
```

Better:

```text
Use a global rule for always-on style.

Use a skill only for task-specific formatting.

Reason:
- style should always apply
- skills trigger only when relevant
```

Rule:

```text
Conclusion first.
Reason second.
```

---

## 3. Vague “it depends”

Bad:

```text
It depends on the task and context.
```

Better:

```text
Use implementation instructions when the task changes code.

Use Scanline when the task explains information.

Use both when code work also needs a readable report.
```

Rule:

```text
Replace “it depends” with decision criteria.
```

---

## 4. Over-compressed answer

Bad:

```text
Use custom skill. Existing ones miss visual parseability.
```

Better:

```text
Use a custom skill.

Reason:
- existing skills cover concision
- they do not enforce visual parseability
- they may remove nuance too aggressively

Required behavior:
- high signal without lost detail
- direct prose cleanup
- visual structure only when useful
```

Rule:

```text
Short is not enough.
Keep the decision-changing details.
```

---

## 5. Generic caveat

Bad:

```text
There are some limitations to consider.
```

Better:

```text
Main limitation:

A broad style skill may not trigger reliably.

So put core style in global instructions.
```

Rule:

```text
Name the caveat.
Explain the consequence.
```

---

## 6. Fake certainty

Bad:

```text
This will work in all agents.
```

Better:

```text
This should work where Agent Skills support standard SKILL.md discovery.

Cannot infer compatibility with custom runners unless their skill-loading behavior is known.
```

Rule:

```text
State confidence boundaries.
```

---

## 7. Polished but dense prose

Bad:

```text
The best approach is to keep implementation instructions separate because they control what gets built, while Scanline should remain a communication-oriented skill that reshapes explanations and reports without affecting implementation strategy.
```

Better:

```text
Keep implementation instructions separate.

Why:
- it controls implementation behavior
- they control what gets built

Keep Scanline separate.

Why:
- it controls answer shape
- it improves readability
- it should not change what code gets written
```

Rule:

```text
Good prose can still be bad layout.
```

---

## 8. Too many sections

Bad:

```text
TL;DR
Context
Background
Analysis
Discussion
Considerations
Implications
Recommendation
Conclusion
Next Steps
```

Better:

```text
Verdict
Why
Action
```

Rule:

```text
Use only sections that reduce reading load.
```

---

## 9. Table abuse

Bad:

A huge table with 12 columns and wrapped text everywhere.

Better:

Use two smaller tables.

Example:

```text
Table 1: fit and gaps
Table 2: risks and recommendation
```

Rule:

```text
Tables should reduce scanning effort.
Do not use tables that become walls of text.
```

---

## 10. Missing user constraints

Bad:

```text
Use a concise writing skill.
```

Better:

```text
Use a visual-parseability skill.

Reason:
- user dislikes long paragraphs
- user thinks while reading
- user prefers bullets, tables, flows, diagrams
- details must remain complete
```

Rule:

```text
Preserve stated constraints explicitly.
```

---

## 11. Generic intro/outro

Bad:

```text
Certainly! Here is a comprehensive overview that should help you understand the topic in detail.
```

Better:

```text
TL;DR: Build a custom skill.
```

Rule:

```text
Start with useful content.
```

---

## 12. Unclear action

Bad:

```text
This architecture is probably better overall.
```

Better:

```text
Action:

1. Put Scanline core rules in global instructions.
2. Keep implementation instructions separate.
3. Add Scanline as a task-formatting skill.
4. Evaluate with 10 real prompts.
```

Rule:

```text
End with an action when the user is deciding or building.
```

---

## 13. Ambiguous referent or relationship

Bad:

```text
It updates it after the check, so this can fail.
```

Better:

```text
The worker updates the cache after checking the profile version.

That order can leave a stale profile in the cache.
```

Rule:

```text
Repeat the concrete noun and state the material link when either could be unclear.
```

---

## 14. Unfamiliar abbreviation

Bad:

```text
The RPO conflicts with the backup interval.
```

Better:

```text
The recovery point objective (RPO) is 15 minutes, but backups run hourly.

The hourly interval cannot meet the 15-minute RPO.
```

Rule:

```text
Expand an unestablished abbreviation once. Never guess an expansion.
```
