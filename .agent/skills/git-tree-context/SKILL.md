---
name: git-tree-context
description: Extract semantic meaning and historical context from the Git history tree.
---
# Git Tree Context Skill

Agentic workflows rely on `git diff` and `git log` to understand pattern evolution. Because the repository history has been optimized to exclude noisy lockfiles and compiled assets, the Git Tree is a highly effective LLM context window.

## Usage

When explicitly invoked by a workflow, or when you need to understand the historical context of a branch/file, follow these steps:

### 1. Extracting Branch Context (For PRs)
To understand what a current unmerged branch accomplishes, run:
```bash
# Get the semantic commit history
git log main..HEAD --format="- %s%n%b"

# Get the exact file changes and line-level diffs
git diff --stat main..HEAD
git diff main..HEAD
```

### 2. Extracting Historical Decisions (For Code Review)
If asked *why* a block of code exists or how it evolved:
```bash
# Find who wrote the line and the exact commit hash
git blame <file>

# Read the commit message and the exact patch that introduced it
git log -S "code snippet" -p <file>
git show <commit_hash>
```

### 3. Extracting Architectural Precedent (For Planning)
To understand how a folder or system boundary has evolved over time:
```bash
# Review the last 6 months of architectural changes in a directory
git log --since="6 months ago" --oneline -- <directory_path>
```
