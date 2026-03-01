---
description: Analyze a feature domain boundary over the last N months to establish architectural precedents.
---
# /git-arch-review

**Architecture Note**: Whenever this workflow references `.agent/rules` or `.agent/skills`, you MUST first look for them inside the *local* repository's `.agent/` folder. If they do not exist locally, fallback to the organization's defaults in `../.github/.agent/`.

Before starting a new feature or complex refactor, leverage the historical repository context to establish domain precedents.

1. **Define the Domain**: Identify the directory or module boundary where the feature code will reside.
2. **Context Extraction**: Run the `.agent/skills/git-tree-context` extraction over that specific directory for the last 6 months (e.g., `git log --since="6 months ago" --oneline -- <directory>`).
3. **Architectural Guardrails**: Provide an executive summary of how that domain has evolved. What precedents exist? Are there historical design patterns that you MUST NOT violate while writing the new feature?
4. **Draft Implementation Plan**: Apply those historical guardrails against the user's prompt to generate a highly-contextualized task checklist.
