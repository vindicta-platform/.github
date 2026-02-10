<div align="center">

# ⚔️ Vindicta Platform

*Provably fair competitive gaming, powered by cryptographically auditable mechanics and AI-driven strategic insights.*

[![Documentation](https://img.shields.io/badge/docs-Platform--Docs-7000ff?style=flat-square)](https://vindicta-platform.github.io/Platform-Docs/)
[![Roadmap](https://img.shields.io/badge/roadmap-v1.0.0%20Mar%202026-FFD700?style=flat-square)](https://github.com/vindicta-platform/.github/blob/main/ROADMAP.md)
[![PR Dashboard](https://img.shields.io/badge/PRs-Dashboard-00ff88?style=flat-square)](https://github.com/orgs/vindicta-platform/projects/3)

</div>

---

## 🚀 Quick Start

```bash
# Install domain packages via uv
uv pip install git+https://github.com/vindicta-platform/vindicta-foundation.git
uv pip install git+https://github.com/vindicta-platform/vindicta-engine.git
uv pip install git+https://github.com/vindicta-platform/warscribe-system.git
```

```bash
# Clone the Portal for local development
git clone https://github.com/vindicta-platform/Vindicta-Portal.git
cd Vindicta-Portal && npm install && npm run dev
```

---

## 📦 Domain Contexts

The platform is organized into **7 domain-driven meso-repos**, each owning a single bounded context.

| Domain         | Repository                                                                                                                                  | Responsibility                              | Stack                          |
| :------------- | :------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------ | :----------------------------- |
| **Foundation** | [vindicta-foundation](https://github.com/vindicta-platform/vindicta-foundation)                                                             | Base models, Architecture, Centralized Docs | Python 3.12, Pydantic V2, `uv` |
| **Engine**     | [vindicta-engine](https://github.com/vindicta-platform/vindicta-engine)                                                                     | Physics, Dice, Entropy, AI Core             | Python 3.12, Pydantic V2, `uv` |
| **Scribe**     | [warscribe-system](https://github.com/vindicta-platform/warscribe-system)                                                                   | WARScribe Notation, Parsing, Transcripts    | Python 3.12, Pydantic V2, `uv` |
| **Economy**    | [vindicta-economy](https://github.com/vindicta-platform/vindicta-economy)                                                                   | Ledger, GasTank, Quotas, Metering           | Python 3.12, Pydantic V2, `uv` |
| **Oracle**     | [vindicta-oracle](https://github.com/vindicta-platform/vindicta-oracle)                                                                     | Prediction, Debate Council, ML              | Python 3.12, Pydantic V2, `uv` |
| **Platform**   | [Vindicta-Portal](https://github.com/vindicta-platform/Vindicta-Portal) / [Vindicta-API](https://github.com/vindicta-platform/Vindicta-API) | Frontend Portal & API Gateway               | Vite 7+ / FastAPI              |
| **Agents**     | [Vindicta-Agents](https://github.com/vindicta-platform/Vindicta-Agents)                                                                     | SDKs, Workflows, Swarm Orchestration        | Python 3.12, Pydantic V2, `uv` |

---

<details>
<summary><strong>📁 Archived Legacy Repos</strong> — Consolidated into meso-repos above</summary>

The following repositories have been archived as part of the [008-platform-consolidation](https://github.com/vindicta-platform/.specify). Their code now lives in the domain contexts above.

| Legacy Repository                                                          | Consolidated Into          |
| :------------------------------------------------------------------------- | :------------------------- |
| Vindicta-Core                                                              | vindicta-foundation        |
| Dice-Engine, Entropy-Buffer, Primordia-AI                                  | vindicta-engine            |
| WARScribe-Core, WARScribe-Parser, WARScribe-CLI, Battle-Transcript-Toolkit | warscribe-system           |
| Economy-Engine, Atomic-Ledger-Py, Metered-SaaS-Logic, Quota-Manager        | vindicta-economy           |
| Meta-Oracle, Arbiter-Predictor                                             | vindicta-oracle            |
| Agent-Auditor-SDK, Audit-Log-Pro                                           | Vindicta-Agents            |
| Logi-Slate-UI, Vindicta-CLI                                                | Vindicta-Portal (Platform) |

</details>

---

## 🔗 Developer Resources

| Resource                | Link                                                                                                                               |
| :---------------------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| 📚 **Documentation**     | [Platform-Docs](https://vindicta-platform.github.io/Platform-Docs/)                                                                |
| 🗺️ **Roadmap**           | [Release Schedule](https://github.com/vindicta-platform/.github/blob/main/ROADMAP.md)                                              |
| 📋 **PR Dashboard**      | [GitHub Projects](https://github.com/orgs/vindicta-platform/projects/3)                                                            |
| 🏷️ **Good First Issues** | [Search across repos](https://github.com/search?q=org%3Avindicta-platform+label%3A%22good+first+issue%22+state%3Aopen&type=issues) |

---

## 🤝 Contributing

We welcome contributions! Each repository follows **Spec-Driven Development** patterns.

1. Check the repository's `CONTRIBUTING.md` and open issues
2. Look for issues labeled [`good first issue`](https://github.com/search?q=org%3Avindicta-platform+label%3A%22good+first+issue%22+state%3Aopen&type=issues)
3. Follow the async-first mandate: all I/O uses `async/await`
4. Run tests locally before submitting PRs

---

<div align="center">

**Status Legend:** ✅ Active &nbsp;|&nbsp; 🟡 Beta &nbsp;|&nbsp; 📦 Archived

*Built with 🎲 by the Vindicta Team*

</div>
