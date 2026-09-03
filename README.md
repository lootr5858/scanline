# Scanline Style

Scanline Style helps AI agents produce clear, precise, complete answers that remain easy to scan.

It compresses wording, not meaning.

## Who it is for

Use Scanline when you want:

- the answer before the explanation
- short blocks with one idea each
- concrete referents and explicit relationships
- useful bullets, tables, flows, and diagrams
- exact constraints, caveats, failure modes, and uncertainty preserved

## Boundary

Scanline controls how information is presented.

It does not change facts, task scope, implementation strategy, safety requirements, or the detail required for a correct answer.

## Components

- `skills/scanline/`: task-triggered formats, examples, anti-patterns, and evaluations
- `baseline/scanline-always-on.md`: compact always-on style rules
- `hooks/hooks.json`: injects the baseline at session and subagent start

The plugin has no network service, account connection, or runtime dependency.

## Installation

This repository is a Codex plugin source. Clone it as `plugins/scanline-style` inside a local Codex marketplace, add its entry to `.agents/plugins/marketplace.json`, then configure and install that marketplace:

```bash
codex plugin marketplace add /path/to/marketplace
codex plugin add scanline-style@MARKETPLACE_NAME
```

The marketplace entry should use:

```json
{
  "name": "scanline-style",
  "source": {
    "source": "local",
    "path": "./plugins/scanline-style"
  },
  "policy": {
    "installation": "AVAILABLE",
    "authentication": "ON_INSTALL"
  },
  "category": "Productivity"
}
```

Codex discovers the manifest at `.codex-plugin/plugin.json`, the skill under `skills/`, and the hooks under `hooks/`.

## Usage

Scanline can trigger implicitly for explanations, summaries, comparisons, reports, plans, reviews, and rewrites.

Invoke it explicitly with `$scanline` when you want to force the style:

```text
Use $scanline to summarize this decision.
```

```text
Use $scanline to compare these options.
```

```text
Use $scanline to rewrite this explanation in short, scan-friendly blocks.
```

The session hooks also load the compact baseline automatically when the plugin is enabled.

## Validation

With Codex's `plugin-creator` and `skill-creator` system skills installed:

```bash
python3 /path/to/plugin-creator/scripts/validate_plugin.py .
python3 /path/to/skill-creator/scripts/quick_validate.py skills/scanline
```

Basic syntax checks:

```bash
jq empty .codex-plugin/plugin.json hooks/hooks.json
```

## License

MIT. See `LICENSE`.
