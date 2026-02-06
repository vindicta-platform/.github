# Contributing to the Vindicta Platform

Thank you for your interest in contributing to the Vindicta Platform! This guide outlines the requirements and best practices for all contributors across all repositories in this organization.

## ⚠️ Mandatory Requirements

### Pre-Commit Hooks (REQUIRED)

**All contributors MUST install and configure `pre-commit` before making any commits.**

Pre-commit is our first line of defense for code quality, ensuring consistent formatting, linting, and security checks across the entire platform.

#### Installation

```bash
# Install pre-commit (if not already installed)
pip install pre-commit

# OR using uv (recommended for Python projects)
uv pip install pre-commit

# Navigate to your repository
cd <repository-name>

# Install the pre-commit hooks
pre-commit install

# (Optional) Run against all files to verify setup
pre-commit run --all-files
```

#### Why This Is Required

1. **Consistency**: Ensures all code follows the same formatting and style guidelines.
2. **Security**: Runs `detect-secrets` to prevent accidental credential commits.
3. **CI Efficiency**: Catches issues locally before they fail in CI/CD pipelines.
4. **Quality Gates**: All PRs run pre-commit checks as the first CI job—failures will block the PR.

> **Note**: If a repository does not have a `.pre-commit-config.yaml` file, please create one following the [Platform Standards](#pre-commit-configuration-standards) or contact the maintainers.

## Pre-Commit Configuration Standards

All repositories should include at minimum the following in their `.pre-commit-config.yaml`:

### Python Repositories
```yaml
repos:
  - repo: https://github.com/astral-sh/ruff-pre-commit
    rev: v0.3.0
    hooks:
      - id: ruff
        args: [--fix]
      - id: ruff-format

  - repo: https://github.com/Yelp/detect-secrets
    rev: v1.4.0
    hooks:
      - id: detect-secrets
```

### Node.js Repositories
```yaml
repos:
  - repo: https://github.com/pre-commit/mirrors-eslint
    rev: v8.56.0
    hooks:
      - id: eslint
        additional_dependencies:
          - eslint@8.56.0

  - repo: https://github.com/Yelp/detect-secrets
    rev: v1.4.0
    hooks:
      - id: detect-secrets
```

### Markdown Link Validation (Recommended for all)
```yaml
repos:
  - repo: https://github.com/tcort/markdown-link-check
    rev: v3.12.2
    hooks:
      - id: markdown-link-check
        args: ['--config', '.markdown-link-check.json']
        types: [markdown]
```

## Development Workflow

1. **Clone** the repository
2. **Install pre-commit** (see above - this is MANDATORY)
3. **Create a feature branch** from `main` (or `master` for legacy repos)
4. **Make your changes** with descriptive commits
5. **Push** your branch and open a Pull Request
6. **Wait for CI** - all checks must pass before merge

## Code of Conduct

All contributors are expected to follow professional and respectful communication standards. We're building something awesome together!

## Questions?

Open a Discussion in the relevant repository or reach out to the maintainers.

---

*This contributing guide applies to all repositories in the `vindicta-platform` organization.*
