# Vindicta Platform Constitution

*The governing principles for all development within the Vindicta Platform ecosystem.*

## Platform Overview

The Vindicta Platform is a 26-repository tactical gaming ecosystem organized into four priority tiers:

| Tier | Focus | Key Repositories |
|------|-------|------------------|
| **P0** | User-Facing | Vindicta-Portal (Web Gateway) |
| **P1** | Core Platform | WARScribe-Core, Primordia-AI, Meta-Oracle, Agent-Auditor-SDK, Vindicta-API, Vindicta-Core |
| **P2** | Supporting | WARScribe-Parser, Logi-Slate-UI, Battle-Transcript-Toolkit |
| **P3** | Utilities | Dice-Engine, Entropy-Buffer, Economy-Engine, Platform-Docs, CLI Tools |

---

## Core Principles

### I. The Economic Prime Directive
Operations MUST run on GCP Free Tier within the `vindicta-warhammer` project. No standing monthly costs. AI costs isolated via "Gas Tank" model using Gemini models.

### II. Spec-Driven Development (Specification Driven Development)
No code without a Specification. BDD/TDD tests MUST fail before implementation. Features documented in `.specify/` before production code.

### III. Mechanical Fidelity
Game mechanics MUST use CSPRNG with traceable `EntropyProof`. Rules MUST adhere 1:1 to competitive standards (10th Ed). Agents MUST NOT simulate probabilistic outcomes—inject via Dice Engine.

### IV. Cognitive Deep Think Protocol
Agents MUST simulate "System 2" thinking:
1. **Context Reconstruction**: Scan project state and conversation logs
2. **Adversarial Simulation**: Generate counter-arguments for every solution
3. **Recursive Decomposition**: Break plans into atomic, independent tasks

### V. Async-First Mandate
All I/O MUST be asynchronous (`async`/`await`). Blocking calls in production are strictly PROHIBITED.

### VI. Test Performance & Isolation
- **60-Second Rule**: Unit tests MUST NOT exceed 60 seconds
- **Zero Side Effects**: No `.env` reads in tests; config must be injected
- **AAA Pattern**: Arrange-Act-Assert for all tests

### VII. Repository Isolation & Tooling
- Strictly Windows (PowerShell/Batch)
- No cross-repo runtime dependencies
- Python packages via `uv` only
- Frontend via `npm`/Vite

### VIII. Identity & Attribution
Every commit attributed to specific Agent/Model instance. Start from clean `main` branch for every new task.

### IX. No-Nag Policy (3-Strategy Rule)
Agents MUST try 3 distinct strategies before reporting errors or asking for help.

### X. Git Branching Policy
- NEVER switch branches unless checked out from `main`
- Push branch name immediately on checkout to lock it
- Pull latest `main` before creating new branches

### XI. Commit Hygiene & SDD PR Flow
Red-Green-Refactor cycle (minimum 2 commits):
1. **RED**: Failing test (`test: add failing test for X`)
2. **GREEN**: Passing implementation (`feat: implement X`)
3. **REFACTOR** (optional): Cleanup without behavior change

PRs MUST trace to `.specify/` specifications. Max 1,000 lines per PR.

### XII. MCP-Strict Tooling Mandate
Autonomous agents MUST use MCP servers (GitHub, Firebase, Cloud Run) for all operations. If MCP unavailable, STOP—no CLI fallback.

---

## Development Workflow

### Spec-Kit Lifecycle
`specify` → `clarify` → `plan` → `tasks` → `implement` → `analyze`

### Quality Gates

| Gate | Requirement |
|------|-------------|
| Unit Tests | 100% pass, >80% coverage |
| Type Checking | `mypy` strict mode |
| Linting | `ruff` / `pre-commit` |
| Security | `detect-secrets` scan |
| CI | GitHub Actions required |

### AI SDK Patterns
- **Retries**: 3x with exponential backoff
- **Dead-Letter Queue**: Failing tasks to DLQ for audit
- **Quota Management**: Respect `Agent-Auditor-SDK` surplus modeling

---

## Repository Missions

### P0: User Gateway
- **Vindicta-Portal**: Primary web interface, multi-page Vite app with Remote Config

### P1: Core Engines
- **WARScribe-Core**: Edition-agnostic action notation engine
- **Primordia-AI**: Deterministic tactical evaluation engine
- **Meta-Oracle**: AI Council for meta predictions via 5-agent debates
- **Vindicta-API**: Unified REST gateway with Firebase JWT auth
- **Vindicta-Core**: Domain modeling and shared contracts
- **Agent-Auditor-SDK**: Quota-aware AI scheduling

### P2: Integration Layer
- **WARScribe-Parser**: Multimodal ingestion (photos, videos, docs)
- **Logi-Slate-UI**: React/TypeScript frontend components
- **Battle-Transcript-Toolkit**: Game transcript extraction

### P3: Infrastructure
- **Dice-Engine**: CSPRNG roller with entropy proofs
- **Entropy-Buffer**: Cryptographically secure RNG pool
- **Economy-Engine**: "Gas Tank" credit-based usage model
- **Platform-Docs**: Public documentation site
- **CLI Tools**: Vindicta-CLI, WARScribe-CLI

---

## Governance

This constitution supersedes all other documentation. Amendments require a MAJOR version bump and re-ratification by the Supreme Architect.

**Version**: 2.8.0 | **Ratified**: 2026-02-04 | **Last Amended**: 2026-02-06
