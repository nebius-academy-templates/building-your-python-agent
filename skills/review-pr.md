<!--
TODO: workflow skill that runs the full review on one command
(`/review-pr <n>` in Claude Code, `$review-pr <n>` in Codex).
Steps: fetch the PR via GitHub MCP, apply app-conventions to non-test files, apply
test-conventions to test files, flag security issues, compile findings into the output
format, present them, and ask for confirmation before posting. Post only on yes or post.
TODO: update the steps to delegate to the three sub-agents and consolidate.
Codex has no named-role selector: spawn a real child per reviewer and pass it the
developer_instructions from the matching .codex/agents/<role>.toml explicitly.
-->

## Steps

[PLACEHOLDER]
