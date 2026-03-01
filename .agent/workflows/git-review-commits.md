---
description: Perform an iterative, step-by-step code review of a proposed branch.
---
# /git-review-commits

**Architecture Note**: Whenever this workflow references `.agent/rules` or `.agent/skills`, you MUST first look for them inside the *local* repository's `.agent/` folder. If they do not exist locally, fallback to the organization's defaults in `../.github/.agent/`.

Large PRs with squashed diffs are inherently hard to review. This workflow assists human reviewers by stepping through the author's logical progression commit-by-commit.

1. **Context Extraction**: Identify the divergence point between the feature branch and `main` using `git log main..HEAD --oneline`.
2. **Iterative Analysis**: For each commit hash returned in the history trajectory:
    *   Extract the commit message and the exact patch using `git show <commit_hash>`.
    *   Analyze the diff: What logical step is the author taking here? Are there any obvious bugs introduced in this specific isolated change?
3. **Progressive Summary**: Rather than summarizing the entire PR at once, output a timeline of the author's work. Explain how step A led to step B.
4. **Review Conclusion**: Provide a final macro-level review. Does the sum of the commits successfully achieve the stated goal? Report any final code review concerns.
