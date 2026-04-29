---
name: ignore-api-specs
description: Workflow command scaffold for ignore-api-specs in claudecode-source.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /ignore-api-specs

Use this workflow when working on **ignore-api-specs** in `claudecode-source`.

## Goal

Commits that ignore or update the API specification file, typically for brainstorming or non-functional changes.

## Common Files

- `packages/opencode/specs/v2/api.ts`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit packages/opencode/specs/v2/api.ts with new ideas or notes.
- Commit with an 'ignore' message.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.