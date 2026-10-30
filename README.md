# PR Review Agent — practice project

You are building a PR Review Agent for the Python team with **Codex CLI or Claude Code**. It
reviews Python pull requests for style, security, and architecture issues, organizes findings
per file with `[SEVERITY]` tags, ends with a `## Summary`, and always asks for confirmation
before posting a comment to GitHub.

## Project layout

Shared instructions live in one place and are read by both tools:

- `AGENTS.md` — the agent system prompt (Codex reads it natively; `CLAUDE.md` imports it).
- `skills/` — skill bodies: `app-conventions`, `test-conventions`, `architecture-guidelines`,
  `review-pr`.
- `reviewers/` — sub-agent prompts: `style-reviewer`, `security-reviewer`,
  `architecture-reviewer`.

Native entry points are thin wrappers that point at the shared files:

| | Codex | Claude Code |
| --- | --- | --- |
| System prompt | `AGENTS.md` | `CLAUDE.md` → `@AGENTS.md` |
| Skills | `.agents/skills/<name>/SKILL.md` | `.claude/skills/<name>/SKILL.md` |
| Sub-agents | `.codex/agents/<name>.toml` | `.claude/agents/<name>.md` |
| Run a review | `$review-pr 3` | `/review-pr 3` |

The wrappers are complete: their descriptions, triggers, tools and models are already set,
so both tools work on the same files at the same time. Every `[PLACEHOLDER]` you fill lives
in exactly one place — `AGENTS.md`, `skills/*.md`, `reviewers/*.md` or `results/` — and
neither tool needs a second copy. Local configuration with credentials (`.mcp.json`,
`.codex/config.toml`, `.claude/settings.local.json`, …) is already in `.gitignore`.

## Files to complete in this task

- `AGENTS.md` — the agent system prompt. Cover four sections: **Role**, **Review criteria**,
  **Output format** (with `[SEVERITY]` tags and a closing `## Summary`), and **Guardrails**.
- `results/test-session-1.md` — a transcript of your three tests: the clean-PR format check, the
  publish-gate confirmation, and the scope refusal.
