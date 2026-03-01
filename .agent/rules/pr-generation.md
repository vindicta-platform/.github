---
description: Pull Request Agentic Rules and Template Resolution Constraints
---
# Git Tree PR Generation Rule

When tasked with creating or formatting a Pull Request (via workflows like `/git-pr-from-tree`), you **MUST** adhere to the following template resolution order and structural rules.

## Template Resolution Rules
You must dynamically locate the correct structural template for the PR body by checking these paths in order:

1. **Local Priority**: Attempt to read the file `.github/PULL_REQUEST_TEMPLATE.md` (or `.github/pull_request_template.md`) in the *current repository*. If it exists, you MUST use its exact headers and structure.
2. **Organization Fallback**: If the local repository does not have a PR template, you must fall back to the organization's default template. Read the file located at `../.github/.github/PULL_REQUEST_TEMPLATE.md` (assuming the `.github` repo is cloned adjacently).
3. **Failsafe Default**: If neither template is found, construct the PR body using the following Markdown headers:
   - `## Summary`
   - `## Changes`
   - `## Why`
   - `## Verification`

## Content Generation Rules
When parsing the Git Tree (e.g., from `git log` and `git diff`), apply these rules to the template:

1. **Infer Purpose**: Use Conventional Commits (e.g., `feat:`, `fix:`, `chore:`) from the `git log` to determine the "Why" or core business value of the PR.
2. **Abstract the Diff**: Do not simply paste the diff. Synthesize the `git diff --stat` into human-readable bullet points under the "Changes" section.
3. **No Inline Bodies**: You must NEVER output the PR body directly to a command-line flag like `--body`. You must ALWAYS write the synthesized content to a local file named `PR_BODY.md`.
