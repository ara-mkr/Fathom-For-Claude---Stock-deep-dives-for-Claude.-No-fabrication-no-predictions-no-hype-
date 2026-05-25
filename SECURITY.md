# Security Policy

## What's "security" mean for a prompt-engineering skill?

Fathom is a Claude Code skill — markdown instructions and templates, no executable code. Traditional CVE-style vulnerabilities don't really apply. But there are still things worth reporting privately.

## What to report privately

Open a private security advisory ([GitHub Security Advisories](https://docs.github.com/en/code-security/security-advisories)) or email the maintainer rather than filing a public issue if you find:

1. **A prompt-injection path** that causes the skill to bypass one of its hard rules (predict prices, fabricate data, continue on claimed MNPI, recommend buy/sell)
2. **A path that causes the skill to leak private user data** from Claude Code's context (extremely unlikely, but flag if you find one)
3. **A misleading-by-design output pattern** that would create material financial harm if a user acted on it without realizing the skill was tricked

## What to file publicly

Everything else — wrong data, missed flags, missed sectors, bad UX — should be a regular issue.

## What we won't treat as security issues

- General LLM hallucination patterns that affect all Claude skills equally
- Cases where the user gave Claude bad information and Claude acted on it
- Disagreements about analysis (file a test case issue instead)

## Disclosure timeline

We aim to respond to security reports within 7 days and patch within 30 days for confirmed issues. Given this is a hobby-scale project, that's a best-effort commitment, not a guarantee.
