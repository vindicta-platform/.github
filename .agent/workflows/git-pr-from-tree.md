---
description: Automatically translate the current branch's git tree into a Pull Request via GitHub CLI.
---
# /git-pr-from-tree

**Architecture Note**: Whenever this workflow references `.agent/rules` or `.agent/skills`, you MUST first look for them inside the *local* repository's `.agent/` folder. If they do not exist locally, fallback to the organization's defaults in `../.github/.agent/`.

Follow these steps exactly to convert the local Git history into a Pull Request Context:

1. **Pre-flight Checks**: Execute automated pre-flight checks (`uv run ruff check .`, `uv run pytest`) dynamically to ensure the code changes are stable before opening a PR.
2. **Context Extraction**: Run the `.agent/skills/git-tree-context` extraction to pull the semantic history of the active branch (`git diff --stat main..HEAD` and `git log main..HEAD`).
3. **Template Resolution**: Adhere to the `.agent/rules/pr-generation.md` rule to determine which `PULL_REQUEST_TEMPLATE.md` to use. You MUST check the local repository's `.github/` folder first, followed by the fallback organization repo `../.github/`.
4. **Context Translation**: Translate the extracted Git Context into the exact resolved template structure. Do NOT just dump the `git diff`. Write the markdown to a temporary file named `PR_BODY.md`.
    *   **CRITICAL RULE**: NEVER use the inline `--body` flag. Always use the local file format.
5. **Execution**: 
    *   `// turbo`
    *   `gh pr create --title "<Title From Log>" --body-file PR_BODY.md`
6. **Cleanup**: Remove the temporary `PR_BODY.md` file using local OS commands.
