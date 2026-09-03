# Scanline Examples

These examples calibrate the preferred output shape.

Use them over generic writing advice.

---

## Example 1: Implementation policy vs Scanline

### Dense version

```text
Implementation policy should remain separate because it controls decisions such as avoiding overbuilding, preferring minimal diffs, and reusing existing code, while communication requirements concern readability, structure, short blocks, and preserving critical details, so combining them may cause coding minimalism to leak into research and explanation tasks.
```

### Scanline version

```text
Keep implementation policy separate.

Reason:
- it controls implementation behavior
- it constrains implementation scope
- it prefers minimal diffs
- it may harm research breadth

Keep Scanline separate.

Reason:
- it controls answer shape
- it improves visual parsing
- it preserves details while reducing reading load
```

---

## Example 2: Skill architecture

### Dense version

```text
The best architecture is to keep the always-on style preference in global instructions because skills only trigger when relevant, then create a task-specific Scanline skill with progressive disclosure so the main SKILL.md stays compact and detailed templates live in reference files.
```

### Scanline version

```text
Best architecture:

```text
Global instructions:
  always-on Scanline style

scanline skill:
  task-specific formats

implementation policy:
  controls what gets built
```

Why:
- style should always apply
- skills may not trigger every time
- reference files keep context cost low
```

---

## Example 3: Debugging explanation

### Dense version

```text
If the skill is not triggering, the most likely issue is that the description is too narrow or the user prompt does not match the skill’s activation criteria, though it is also possible that the skill directory is in the wrong location or the tool does not support that skill format.
```

### Scanline version

```text
Problem:

Skill does not trigger.

Likely causes:

1. Description is too narrow.
2. Prompt does not match trigger wording.
3. Skill directory is wrong.
4. Runner does not support this skill format.

Fix order:

1. Broaden `description`.
2. Test explicit invocation.
3. Verify install path.
4. Check runner skill support.
```

---

## Example 4: Comparison

### Dense version

```text
A brevity-first style is probably the closest match because it focuses on high signal and low filler, while a prose-first style helps cleanup but is less suitable for visual structure, and a visual-first style is helpful for artifacts but too heavy as a default response style.
```

### Scanline version

```text
Closest match: brevity-first.

| Skill | Good | Gap |
|---|---|---|
| Brevity-first | high signal, no filler | may over-compress |
| Prose-first | prose cleanup | not visual enough |
| Visual-first | diagrams/tables | too heavy by default |

Recommendation:

Combine the useful behaviors.
Keep Scanline's boundaries explicit.
```

---

## Example 5: Research answer

### Dense version

```text
Existing public concise-writing skills do not fully cover your requirement because they mostly focus on improving prose quality, whereas your requirement is more about visually parseable information design, so the best path is a custom skill with short-block rules, task-specific formats, and explicit detail-retention constraints.
```

### Scanline version

```text
Verdict:

No public concise-writing skill fully matches your need.

Reason:
- most improve prose
- your need is visual parsing
- detail retention matters more than shortest text

Best path:

Create a custom Scanline skill.

Include:
- density without lost detail
- direct prose cleanup
- visual triggers only when useful
```

---

## Example 6: Pushback

### Dense version

```text
I would be careful about using coding-minimalism instructions as a general response style because although they may make outputs shorter, they are designed to change implementation behavior and may create the wrong incentives for research or general analysis tasks.
```

### Scanline version

```text
I would not use coding-minimalism instructions globally.

Reason:
- it changes coding behavior
- it optimizes for minimal implementation
- research needs breadth and nuance

Use implementation policy for code.
Use Scanline for communication.
```

---

## Example 7: Safe skimming

### Bad

```text
The model should explain that global style rules are usually more reliable than skills for always-on formatting because skills depend on trigger matching, but skills are still useful for task-specific output formats that need more structure than the global rule should contain.
```

### Good

```text
Use global rules for always-on style.

Use skills for task-specific formats.

Reason:
- global rules always apply
- skills depend on trigger matching
- large format manuals should not live in global context
```

---

## Example 8: Detail retention

### Bad

```text
Make answers shorter and structured.
```

### Good

```text
Make answers easier to parse.

Rules:
- short blocks
- max 3 visual lines per paragraph
- bullets/tables/flows when useful
- concrete referents and material relationships
- expand unfamiliar abbreviations once
- preserve names, versions, dates, caveats, failure modes
- compress wording, not meaning
```

---

## Example 9: Implementation plan

### Bad

```text
Create the skill files, add the formats and examples, and then test it with some prompts.
```

### Good

```text
Plan:

1. Create `SKILL.md`.
2. Add `references/formats.md`.
3. Add `references/anti-patterns.md`.
4. Add `references/examples.md`.
5. Add `references/evals.md`.
6. Test with 10 real prompts.
7. Revise trigger wording.
```

---

## Example 10: Minimal warm tone

### Too cold

```text
Wrong. Use global instructions.
```

### Too chatty

```text
Great question! I totally get what you mean, and there are a few different ways we can think about this depending on your workflow and preferences.
```

### Scanline

```text
Your instinct is right.

Use global instructions for baseline style.
Use the skill for heavier structured outputs.
```
