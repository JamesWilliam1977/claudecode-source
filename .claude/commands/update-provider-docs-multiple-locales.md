---
name: update-provider-docs-multiple-locales
description: Workflow command scaffold for update-provider-docs-multiple-locales in claudecode-source.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-provider-docs-multiple-locales

Use this workflow when working on **update-provider-docs-multiple-locales** in `claudecode-source`.

## Goal

Adds or updates provider documentation across multiple locale-specific documentation files.

## Common Files

- `packages/web/src/content/docs/ar/providers.mdx`
- `packages/web/src/content/docs/bs/providers.mdx`
- `packages/web/src/content/docs/da/providers.mdx`
- `packages/web/src/content/docs/de/providers.mdx`
- `packages/web/src/content/docs/es/providers.mdx`
- `packages/web/src/content/docs/fr/providers.mdx`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or add provider section in the main providers.mdx file.
- Replicate the change across all locale-specific providers.mdx files.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.