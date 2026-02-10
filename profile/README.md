<div align="center">

# ⚔️ Vindicta Platform

*Provably fair competitive gaming, powered by cryptographically auditable mechanics and AI-driven strategic insights.*

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Launch%20Portal-FF0000?style=for-the-badge&logo=firebase)](https://vindicta-platform.web.app)
<br/>
[![Documentation](https://img.shields.io/badge/docs-Platform--Docs-7000ff?style=flat-square)](https://vindicta-platform.github.io/Platform-Docs/)
[![Roadmap](https://img.shields.io/badge/roadmap-v1.0.0%20Mar%202026-FFD700?style=flat-square)](https://github.com/vindicta-platform/.github/blob/main/ROADMAP.md)
[![PR Dashboard](https://img.shields.io/badge/PRs-Dashboard-00ff88?style=flat-square)](https://github.com/orgs/vindicta-platform/projects/3)

</div>

---

## 🗺️ System Architecture

The Vindicta Platform consolidates 7 domain contexts into a unified e-sports ecosystem.

```mermaid
C4Container
    title Container diagram for Vindicta Platform
    
    Container(platform, "Platform & Portal", "Vindicta-Portal / API", "User Interface, API Gateway, and Identity.")
    Container(foundation, "Foundation", "vindicta-foundation", "Shared Kernel: Base Models & Architecture.")
    Container(engine, "Engine", "vindicta-engine", "Physics, Dice, and AI Core.")
    Container(scribe, "Scribe", "warscribe-system", "Notation Parsing & Vision.")
    Container(economy, "Economy", "vindicta-economy", "Ledger, Quotas & Billing.")
    Container(oracle, "Oracle", "vindicta-oracle", "Predictive Models & Meta Analysis.")
    Container(agents, "Agents", "vindicta-agents", "Swarm Orchestration & SDKs.")

    Rel(platform, foundation, "Inherits")
    Rel(platform, engine, "Simulates")
    Rel(platform, scribe, "Parses")
    Rel(platform, economy, "Bills")
    Rel(platform, oracle, "Predicts")
    Rel(agents, platform, "Automates")
```

---

## ⚡ Quick Start

Get up and running with our **"Hello World"** examples in the [Orchestrator Repository](https://github.com/vindicta-platform/vindicta-platform/tree/main/examples).

```bash
# Clone the orchestrator
git clone --recurse-submodules https://github.com/vindicta-platform/vindicta-platform.git
cd vindicta-platform

# Run the Dice Engine example
uv run examples/dice_roll.py

# Run the WARScribe Action example
uv run examples/warscribe_actions.py
```

---

## ⚔️ Choose Your Class

Join the development squad that matches your skills and interests.

| Class                | Skills                    | Quest                                          | Realm                                                                     |
| :------------------- | :------------------------ | :--------------------------------------------- | :------------------------------------------------------------------------ |
| **Tech-Priest**      | Python, Math, Probability | Build the physics engine and entropy proofs.   | [vindicta-engine](https://github.com/vindicta-platform/vindicta-engine)   |
| **Logos Historian**  | NLP, Vision, Parsing      | Decode WARScribe notation and parse rosters.   | [warscribe-system](https://github.com/vindicta-platform/warscribe-system) |
| **Meta-Seer**        | ML, Data Science, Stats   | Train predictive models and evaluating lists.  | [vindicta-oracle](https://github.com/vindicta-platform/vindicta-oracle)   |
| **Void Banker**      | DeFi, Ledgers, SQL        | Manage the atomic economy and gas tanks.       | [vindicta-economy](https://github.com/vindicta-platform/vindicta-economy) |
| **Portal Architect** | React, UX/UI, Design      | Craft the player experience and visualization. | [Vindicta-Portal](https://github.com/vindicta-platform/Vindicta-Portal)   |

---

## 📦 Domain Contexts

| Domain         | Repository                                                                      | Status   | Stack                    |
| :------------- | :------------------------------------------------------------------------------ | :------- | :----------------------- |
| **Foundation** | [vindicta-foundation](https://github.com/vindicta-platform/vindicta-foundation) | ✅ Active | Python 3.12, Pydantic V2 |
| **Engine**     | [vindicta-engine](https://github.com/vindicta-platform/vindicta-engine)         | ✅ Active | Python 3.12, Pydantic V2 |
| **Scribe**     | [warscribe-system](https://github.com/vindicta-platform/warscribe-system)       | ✅ Active | Python 3.12, Pydantic V2 |
| **Economy**    | [vindicta-economy](https://github.com/vindicta-platform/vindicta-economy)       | ✅ Active | Python 3.12, Pydantic V2 |
| **Oracle**     | [vindicta-oracle](https://github.com/vindicta-platform/vindicta-oracle)         | 🟡 Beta   | Python 3.12, Pydantic V2 |
| **Platform**   | [Vindicta-Portal](https://github.com/vindicta-platform/Vindicta-Portal)         | 🟡 Active | Vite 7+, Cloud Run       |
| **Agents**     | [Vindicta-Agents](https://github.com/vindicta-platform/Vindicta-Agents)         | ✅ Active | Python 3.12, Pydantic V2 |

<details>
<summary><strong>📁 Archived Legacy Repos</strong></summary>

The following repositories have been consolidated into the domain contexts above:
*   `Vindicta-Core` → `vindicta-foundation`
*   `Dice-Engine`, `Primordia-AI` → `vindicta-engine`
*   `WARScribe-Core`, `WARScribe-Parser` → `warscribe-system`
*   `Economy-Engine`, `Atomic-Ledger-Py` → `vindicta-economy`
*   `Meta-Oracle` → `vindicta-oracle`

</details>

---

<div align="center">

*Built with 🎲 by the Vindicta Team*

</div>
