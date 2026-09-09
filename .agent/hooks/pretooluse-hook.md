# Hard enforcement: PreToolUse hook (the real ".claudeignore")

Claude Code does **not** natively honor a `.claudeignore` file. The closest
working equivalent is a `PreToolUse` hook that inspects each `Read` call and
blocks paths matching an ignore list. `permissions.deny` is the lighter-weight
native option, but has had enforcement bugs across versions; a hook is the
reliable hard block.

## How it works
1. A `.claudeignore`-style pattern file lives in the repo root.
2. A small script runs as a `PreToolUse` hook on the `Read` matcher.
3. The script exits non-zero (code 2) when the target path matches a pattern,
   which blocks the read before any tokens are spent on it.

## Wiring (in `.claude/settings.json`)

```json
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Read",
        "hooks": [
          { "type": "command", "command": "<path-to-your-ignore-check-script>" }
        ]
      }
    ]
  }
}
```

## Notes
- A community package (`li-zhixin/claude-ignore` on npm/GitHub) implements this
  pattern with hierarchical `.claudeignore` discovery. Vet third-party hooks
  before trusting them — a hook runs arbitrary code on every matching tool call.
- For pure token savings (not security), `permissions.deny` + `.gitignore` +
  the `CLAUDE.md` "do not read" list is usually enough and adds no dependency.
- Use a hook when you need a guarantee — e.g. keeping secrets or large vendored
  trees out of context no matter what the model decides to do.
