---
name: review-pr
description: "Run a complete Python PR review of a course PR. Explicit invocation only, with a case number from 1 to 5 (e.g. $review-pr 3)."
---

Read `skills/review-pr.md` relative to the repository root and follow its steps in order.
The shared workflow decides whether this practice uses sub-agents.

When the shared workflow calls for delegation, spawn one real child agent per reviewer
(`style_reviewer`, `security_reviewer`, `architecture_reviewer` from `.codex/agents/`). If
roles cannot be selected by name, pass the child the `developer_instructions` from the
matching TOML file explicitly. Run them one at a time and pass each the same target, scope
and complete diff. If a child cannot be started, report it instead of simulating it.

Read the case number from the user request, e.g. `$review-pr 3`.
