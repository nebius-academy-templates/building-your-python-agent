<!--
TODO: workflow skill that runs the full review on one command
(`/review-pr <n>` in Claude Code, `$review-pr <n>` in Codex).
Steps: fetch the PR via GitHub MCP, apply app-conventions to non-test files, apply
test-conventions to test files, flag security issues, compile findings into the output
format, present them, and ask for confirmation before posting. Post only on yes or post.
TODO: update the steps to delegate to the three sub-agents and consolidate.
Write the steps tool-neutrally: the native wrappers in .claude/skills/review-pr and
.agents/skills/review-pr already say how each tool starts the sub-agents.
-->

## Steps

[PLACEHOLDER]
