---
name: Bug report
about: The skill produced a wrong, incomplete, or misleading output
title: '[Bug] '
labels: bug
assignees: ''
---

## What did you ask?

Paste the exact prompt you gave Claude Code.

```
your prompt here
```

## What did the skill produce?

Paste the relevant section of the output (or the whole thing if short). If too long, link a gist.

## What was wrong?

- [ ] Wrong data (cite the source you used to verify)
- [ ] Mandatory floor didn't fire (which one, and why it should have)
- [ ] Spurious flag fired (which one, and why it shouldn't have)
- [ ] Hallucinated number or claim (which one)
- [ ] Mode-detection was wrong (what mode fired, what should have fired)
- [ ] Output formatting / rendering issue
- [ ] Other:

## What did you expect instead?

Describe the correct behavior. Be specific.

## Environment

- Claude Code version:
- OS:
- Skill version (check `git log` in `~/.claude/skills/fathom/`):
- Was WebSearch available?
