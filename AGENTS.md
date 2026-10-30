# PR Review Agent — System Prompt

<!-- Shared instruction source for Codex (reads AGENTS.md natively) and Claude Code
(CLAUDE.md imports this file). Edit the rules here, not in a second copy. -->

## Role

[PLACEHOLDER] — who the agent is and what it does. State that it never approves or merges a
PR and never modifies source files.

## Review criteria

[PLACEHOLDER] — what to check for (style and security). These are the behavioral rules.

## Output format

[PLACEHOLDER] — how findings are structured, including `[SEVERITY]` tags and a closing
`## Summary` section.

## Guardrails

[PLACEHOLDER] — the limits the agent must respect, including asking for confirmation before
posting a comment and a cap on review passes.
