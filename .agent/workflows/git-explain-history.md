---
description: Discover the historical decisions and evolution behind a specific file or block of code.
---
# /git-explain-history

**Architecture Note**: Whenever this workflow references `.agent/rules` or `.agent/skills`, you MUST first look for them inside the *local* repository's `.agent/` folder. If they do not exist locally, fallback to the organization's defaults in `../.github/.agent/`.

Use this workflow when you need to understand *why* a block of code was written a specific way, rather than just *what* the syntax does.

1. **Target Identification**: The user specifies a file or a block of code.
2. **Context Extraction - Blame**: Extract the exact commit hash that introduced the lines in question by running `git blame <file>`. Identify the author and the date.
3. **Context Extraction - Patch**: Retrieve the complete semantic patch that introduced the block by running `git log -S "code snippet" -p <file>` or `git show <commit_hash>`.
4. **Historical Synthesis**: Explain the historical context. Read the extracted commit message. Why was the code added? Was it part of a larger feature? Did it fix a bug?
5. **Evolution Mapping**: If the block has been touched multiple times, use `git log -p <file>` to map its evolution and explain the trajectory of the file's design over time.
