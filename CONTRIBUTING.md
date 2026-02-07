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

### Spec-Driven Development (SDD) (REQUIRED)

**Every new feature or significant change MUST follow the Spec-Driven Development lifecycle BEFORE implementation.**

1.  **Propose**: Create a new specification bundle in the [`.specify`](https://github.com/vindicta-platform/.specify) repository.
2.  **Review**: Specification bundles (spec, plan, tasks) must be reviewed and approved by the maintainers in the `.specify` hub.
3.  **Commit**: Once approved, the specification bundle is committed to the target repository's `.specify/specs/` directory.
4.  **Implement**: Implementation tasks are tracked via GitHub issues generated from the `tasks.md` file.

## Development Workflow

1.  **Propose Spec**: Open a PR in the `.specify` hub with your feature specification.
2.  **Clone Target Repo**: Once the spec is approved, clone the repository where the feature will live.
3.  **Sync Spec**: Commit the approved `.specify/specs/[ID]-[name]/` bundle to the target repository.
4.  **Install pre-commit**: (MANDATORY - see above).
5.  **Create Branch**: Use the standard `feature/[ID]-[name]` naming convention.
6.  **Execute Tasks**: Implement changes following the approved `tasks.md`.
7.  **Push & PR**: Open a Pull Request in the target repository for implementation review.
8.  **Verify**: All checks and acceptance criteria must be satisfied.

## Branch Naming Conventions

All repositories in the Vindicta Platform use **`main`** as the default branch.

### Protected Branches
- **`main`**: Production-ready code. All changes must go through Pull Requests with required reviews.

### Feature Branches
Use the following naming conventions when creating feature branches:

- **Features**: `feature/[ID]-[name]` (e.g., `feature/042-credit-ledger`)
- **Bug Fixes**: `fix/[ID]-[name]` or `bugfix/[issue-number]-[description]`
- **Chores**: `chore/[description]` (e.g., `chore/update-dependencies`)
- **Hotfixes**: `hotfix/[description]` (for emergency production fixes)

### Branch Protection Rules
All repositories enforce the following on the `main` branch:
- Pull request reviews required before merging
- Status checks must pass before merging
- Linear history enforced (no merge commits)
- Force pushes and deletions are blocked


## Code of Conduct

All contributors are expected to follow professional and respectful communication standards. We're building something awesome together!

## Questions?

Open a Discussion in the relevant repository or reach out to the maintainers.

---

*This contributing guide applies to all repositories in the `vindicta-platform` organization.*
