---
name: review-pr
description: "Run a complete Python PR review of a course PR. Explicit invocation only, with a case number from 1 to 5 (e.g. /review-pr 3)."
disable-model-invocation: true
---

Read `skills/review-pr.md` relative to the repository root and follow its steps in order.
The shared workflow decides whether this practice uses sub-agents.

When the shared workflow calls for delegation, use the Agent tool with the named
`style-reviewer`, `security-reviewer` and `architecture-reviewer` sub-agents. Run them one
at a time and pass each the same target, scope and complete diff. If a named agent is
unavailable, report it instead of simulating it.

Case number supplied by Claude Code: $ARGUMENTS.
