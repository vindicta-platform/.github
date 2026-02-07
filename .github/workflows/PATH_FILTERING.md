# CI Path Filtering — Caller Examples

These example workflows demonstrate how repositories should invoke
the shared CI templates with **path filtering** to minimize CI costs
per the **Economic Prime Directive**.

## Python Repository Example

```yaml
# .github/workflows/ci.yml
name: CI

on:
  push:
    branches: [main]
    paths-ignore:
      - '**.md'
      - 'docs/**'
      - '.antigravity/**'
      - '.specify/**'
      - 'LICENSE'
      - '.gitignore'
  pull_request:
    branches: [main]
    paths-ignore:
      - '**.md'
      - 'docs/**'
      - '.antigravity/**'
      - '.specify/**'
      - 'LICENSE'
      - '.gitignore'

jobs:
  ci:
    uses: vindicta-platform/.github/.github/workflows/ci-python-template.yml@main
```

## Node.js Repository Example

```yaml
# .github/workflows/ci.yml
name: CI

on:
  push:
    branches: [main]
    paths-ignore:
      - '**.md'
      - 'docs/**'
      - '.antigravity/**'
      - '.specify/**'
      - 'LICENSE'
      - '.gitignore'
  pull_request:
    branches: [main]
    paths-ignore:
      - '**.md'
      - 'docs/**'
      - '.antigravity/**'
      - '.specify/**'
      - 'LICENSE'
      - '.gitignore'

jobs:
  ci:
    uses: vindicta-platform/.github/.github/workflows/ci-node-template.yml@main
```

## Standard `paths-ignore` List

All repositories **MUST** include the following paths-ignore to comply
with the Economic Prime Directive:

```yaml
paths-ignore:
  - '**.md'           # All markdown files
  - 'docs/**'         # Documentation directory
  - '.antigravity/**' # Agent context artifacts
  - '.specify/**'     # SDD specification bundles
  - 'LICENSE'         # License file
  - '.gitignore'      # Git ignore rules
```

## Notes

- Path filtering is applied at the **caller** level, not in the
  reusable template, because `workflow_call` does not support
  `paths-ignore` triggers directly.
- Repos with **mandatory branch protection checks** should use
  step-level conditionals instead of job-level `if:` to avoid
  blocking merges on docs-only PRs (see ci-python-template.yml
  for the `check-python` pattern).
