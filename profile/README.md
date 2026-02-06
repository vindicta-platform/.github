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
# Install core packages via uv
uv pip install git+https://github.com/vindicta-platform/Vindicta-Core.git
uv pip install git+https://github.com/vindicta-platform/WARScribe-Core.git
uv pip install git+https://github.com/vindicta-platform/Dice-Engine.git
```

```bash
# Clone the Portal for local development
git clone https://github.com/vindicta-platform/Vindicta-Portal.git
cd Vindicta-Portal && npm install && npm run dev
```

---

## 📦 Repository Navigator

### P0: User-Facing Entry Point

| Repository                                                                  | Description                                                  | Status   |
| --------------------------------------------------------------------------- | ------------------------------------------------------------ | -------- |
| [**Vindicta-Portal**](https://github.com/vindicta-platform/Vindicta-Portal) | Web gateway for Army Grading, Meta Analysis & Game Recording | 🟡 Active |

---

<details>
<summary><strong>P1: Core Platform</strong> — Tactical Engines & AI</summary>

| Repository                                                                  | Description                                              | Status       |
| --------------------------------------------------------------------------- | -------------------------------------------------------- | ------------ |
| [WARScribe-Core](https://github.com/vindicta-platform/WARScribe-Core)       | Edition-agnostic notation engine (10th/11th Edition)     | 🟢 Foundation |
| [Primordia-AI](https://github.com/vindicta-platform/Primordia-AI)           | Deterministic tactical engine ("Stockfish of Warhammer") | 🟢 Foundation |
| [Meta-Oracle](https://github.com/vindicta-platform/Meta-Oracle)             | AI Council for meta predictions & adversarial reasoning  | 🟢 Foundation |
| [Agent-Auditor-SDK](https://github.com/vindicta-platform/Agent-Auditor-SDK) | Quota-aware AI scheduling framework                      | 🟢 v0.1.0     |
| [Vindicta-API](https://github.com/vindicta-platform/Vindicta-API)           | Central REST gateway (FastAPI)                           | 🟡 Active     |
| [Vindicta-Core](https://github.com/vindicta-platform/Vindicta-Core)         | Shared domain schemas & interface contracts              | 🟢 Foundation |

</details>

<details>
<summary><strong>P2: Supporting Products</strong> — Integration & UI</summary>

| Repository                                                                                  | Description                                            | Status       |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------ | ------------ |
| [WARScribe-Parser](https://github.com/vindicta-platform/WARScribe-Parser)                   | Multimodal data ingestion (rosters, audio, video)      | 🟢 Foundation |
| [Logi-Slate-UI](https://github.com/vindicta-platform/Logi-Slate-UI)                         | React/TypeScript tactical frontend (Glass-Neon design) | 🟡 Active     |
| [Battle-Transcript-Toolkit](https://github.com/vindicta-platform/Battle-Transcript-Toolkit) | NLP event extraction & game state reconstruction       | 🔴 Scaffold   |

</details>

<details>
<summary><strong>P3: Infrastructure & Utilities</strong></summary>

| Repository                                                                | Description                                     | Status       |
| ------------------------------------------------------------------------- | ----------------------------------------------- | ------------ |
| [Dice-Engine](https://github.com/vindicta-platform/Dice-Engine)           | Statistical dice roller with rejection sampling | ✅ v1.0.0     |
| [Entropy-Buffer](https://github.com/vindicta-platform/Entropy-Buffer)     | CSPRNG entropy pool manager                     | ✅ v1.0.0     |
| [Economy-Engine](https://github.com/vindicta-platform/Economy-Engine)     | Credit-based "Gas Tank" usage model             | 🟢 Scaffold   |
| [Atomic-Ledger-Py](https://github.com/vindicta-platform/Atomic-Ledger-Py) | Tamper-proof financial ledger                   | 🟢 Foundation |
| [Audit-Log-Pro](https://github.com/vindicta-platform/Audit-Log-Pro)       | Dual-sink transactional logging                 | 🔴 Scaffold   |
| [Platform-Docs](https://github.com/vindicta-platform/Platform-Docs)       | MkDocs Material documentation site              | 🟢 Active     |
| [Vindicta-CLI](https://github.com/vindicta-platform/Vindicta-CLI)         | Unified command-line interface                  | 🔴 Scaffold   |

</details>

---

## 🔗 Developer Resources

| Resource                | Link                                                                                                                               |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| 📚 **Documentation**     | [Platform-Docs](https://vindicta-platform.github.io/Platform-Docs/)                                                                |
| 🗺️ **Roadmap**           | [6-Week Release Schedule](https://github.com/vindicta-platform/.github/blob/main/ROADMAP.md)                                       |
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

**Status Legend:** ✅ Production &nbsp;|&nbsp; 🟢 Foundation &nbsp;|&nbsp; 🟡 Active Development &nbsp;|&nbsp; 🔴 Scaffold

*Built with 🎲 by the Vindicta Team*

</div>
