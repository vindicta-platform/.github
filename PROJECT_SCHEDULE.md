> **Historical document.** Written in early 2026 for a six-week push; the platform was not launched and work stopped in March 2026. Kept for the record.

# Vindicta Platform — Daily Project Schedule

> **Timeframe**: Feb 4 - Mar 17, 2026 (6 Weeks)  
> **Last Updated**: 2026-02-05

This document provides the detailed daily task allocation for all Vindicta Platform products.

---

## 📅 Week 1: Feb 4-10 — Foundation Sprint ✅

**Status**: 90% complete (18/20 tasks) | 8 PRs merged | 3 issues created for Week 2

### Monday, Feb 4 ✅
| Product | Task | Priority | Status |
|---------|------|----------|--------|
| Vindicta-Portal | Initialize Firebase Remote Config | P0 | ✅ PR #21 |
| WARScribe-Core | Schema refinement and validation | P1 | ✅ PR #7 |
| Primordia AI | Define heuristic evaluation interface | P1 | ✅ PR #5 |
| Agent-Auditor-SDK | Implement priority queue with human P0 preemption | P1 | ✅ PR #11 |
| Platform-Docs | Configure Material theme | P2 | ✅ PR #2 |

### Tuesday, Feb 5 ✅
| Product | Task | Priority | Status |
|---------|------|----------|--------|
| Vindicta-Portal | Implement feature flag system | P0 | ✅ PR #21 |
| WARScribe-Core | Design edition abstraction layer | P1 | ✅ PR #8 |
| Primordia AI | Continue heuristic evaluation | P1 | ✅ PR #5 |
| Agent-Auditor-SDK | Gemini rate limiting implementation | P1 | ✅ PR #12 |
| Platform-Docs | Apply Vindicta branding | P2 | ✅ PR #2 |

**Additional**: ADR-0002 created (PR #3) - AI-assisted coding requirement

### Wednesday, Feb 6 ✅
| Product | Task | Priority | Status |
|---------|------|----------|--------|
| Vindicta-Portal | Complete design system tokens | P0 | ✅ PR #22 |
| WARScribe-Core | Implement edition abstraction interfaces | P1 | ✅ PR #8 |
| Primordia AI | Opening book database design | P1 | ✅ Issue #3 |
| Agent-Auditor-SDK | Gemini adapter implementation | P1 | ✅ PR #12 |

### Thursday, Feb 7 ⚠️
| Product | Task | Priority | Status |
|---------|------|----------|--------|
| Vindicta-Portal | Mobile-first layout (part 1) | P0 | ⚠️ Moved to Week 2 |
| WARScribe-Core | Unit tests for schema | P1 | ✅ PR #8 |
| Primordia AI | DuckDB setup for opening book | P1 | ✅ PR #6 |
| Agent-Auditor-SDK | Unit tests | P1 | ⚠️ Issue #13 (Week 2) |

### Friday, Feb 8
| Product | Task | Priority | Status |
|---------|------|----------|--------|
| Vindicta-Portal | Mobile-first layout (part 2) | P0 | ⚠️ Moved to Week 2 |
| WARScribe-Core | Complete unit tests | P1 | ✅ 100% coverage |
| Platform-Docs | GitHub Pages deployment | P2 | ⏸️ Deferred |

### Saturday, Feb 9
*Reduced schedule*

### Sunday, Feb 10 — **Release Day**
| Product | Release | Target | Status |
|---------|---------|--------|--------|
| Vindicta-Portal | v0.1.0 | Foundation release | 📅 Feb 11 (75% complete) |
| WARScribe-Core | v0.1.5 | Schema release | ✅ Ready (90% complete) |

**Week 1 Highlights**:
- ✅ 8 PRs merged across 5 repositories
- ✅ ADR infrastructure established
- ✅ Rate limiting prevents 429 errors
- ✅ Edition abstraction complete with tests
- ⚠️ 2 tasks slipped to Week 2 (mobile layout, BDD tests)

**Week 2 Issues Created**:
- Agent-Auditor-SDK #13: Add BDD tests for rate limiter
- Primordia-AI #7: Type OpeningBookDB with Pydantic models
- WARScribe-Core #9: Document EditionPlugin interface

---

## 📅 Week 2: Feb 11-17 — Core Feature Development

### Monday, Feb 11
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | Firebase Auth integration (part 1) | P0 |
| WARScribe-Core | Edition plugin architecture | P1 |
| Primordia AI | Opening book data population | P1 |
| Meta-Oracle | DebateEngine core implementation | P1 |
| WARScribe-Parser | BattleScribe XML parser | P2 |
| Logi-Slate-UI | React/Zustand foundation | P2 |

### Tuesday, Feb 12
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | Firebase Auth integration (part 2) | P0 |
| WARScribe-Core | 10th Edition plugin (part 1) | P1 |
| Primordia AI | Opening book data population | P1 |
| Meta-Oracle | Stub agent implementations | P1 |
| WARScribe-Parser | ROS file parser | P2 |
| Logi-Slate-UI | Design system components | P2 |

### Wednesday, Feb 13
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | List Grader MVP (part 1) | P0 |
| WARScribe-Core | 10th Edition plugin (part 2) | P1 |
| Primordia AI | State encoding implementation | P1 |
| Meta-Oracle | Home agent implementation | P1 |
| WARScribe-Parser | JSON parser | P2 |
| Logi-Slate-UI | Component library setup | P2 |

### Thursday, Feb 14
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | List Grader MVP (part 2) | P0 |
| WARScribe-Core | Tests for edition plugin | P1 |
| Primordia AI | Evaluation functions | P1 |
| Meta-Oracle | Adversary agent implementation | P1 |
| WARScribe-Parser | Parser tests | P2 |

### Friday, Feb 15
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | Meta Snapshot feature | P0 |
| WARScribe-Core | Complete tests | P1 |

### Saturday, Feb 16
*Reduced schedule*

### Sunday, Feb 17 — **Release Day**
| Product | Release | Notes |
|---------|---------|-------|
| WARScribe-Core | v0.2.0 | Edition Layer release |
| Meta-Oracle | v0.1.0 | Foundation release |
| Primordia AI | v0.1.0 | Foundation release |

---

## 📅 Week 3: Feb 18-24 — Integration Sprint

### Monday, Feb 18
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | Meta Snapshot polish | P0 |
| Agent-Auditor-SDK | Quota prediction algorithm | P1 |
| Primordia AI | Opening book database implementation | P1 |
| Vindicta-API | FastAPI project scaffold | P1 |
| Vindicta-Core | Module extraction planning | P1 |
| Battle-Transcript-Toolkit | Pydantic schemas design | P2 |

### Tuesday, Feb 19
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | Upset Detector (part 1) | P0 |
| Agent-Auditor-SDK | SQLite journal implementation (part 1) | P1 |
| Primordia AI | Faction analysis features | P1 |
| Vindicta-API | Dice endpoint implementation | P1 |
| Vindicta-Core | WARScribe module extraction | P1 |
| Battle-Transcript-Toolkit | GameEvent model | P2 |

### Wednesday, Feb 20
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | Upset Detector (part 2) | P0 |
| Agent-Auditor-SDK | SQLite journal implementation (part 2) | P1 |
| Primordia AI | Recommendation API | P1 |
| Vindicta-API | Oracle endpoint implementation | P1 |
| Vindicta-Core | Oracle module extraction | P1 |
| Battle-Transcript-Toolkit | Report model | P2 |

### Thursday, Feb 21
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | Integration testing | P0 |
| Agent-Auditor-SDK | Batch job processing | P1 |
| Vindicta-API | OpenAPI documentation | P1 |
| Vindicta-Core | Unit tests | P1 |

### Friday, Feb 22
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | Integration polish | P0 |

### Saturday, Feb 23
*Reduced schedule*

### Sunday, Feb 24 — **Release Day**
| Product | Release | Notes |
|---------|---------|-------|
| Vindicta-Portal | v0.2.0 | Core Features release |
| Agent-Auditor-SDK | v0.2.0 | Prediction release |
| Primordia AI | v0.1.5 | Opening Book release |
| Battle-Transcript-Toolkit | v0.1.0 | Foundation release |

---

## 📅 Week 4: Feb 25 - Mar 3 — AI Sprint

### Monday, Feb 25
| Product | Task | Priority |
|---------|------|----------|
| Meta-Oracle | Arbiter agent implementation | P1 |
| Primordia AI | MCTS foundation (part 1) | P1 |
| WARScribe-Parser | Whisper integration setup | P2 |
| Logi-Slate-UI | Game tracker component | P2 |
| Vindicta-API | WARScribe endpoint | P1 |

### Tuesday, Feb 26
| Product | Task | Priority |
|---------|------|----------|
| Meta-Oracle | Rule-Sage agent implementation | P1 |
| Primordia AI | MCTS foundation (part 2) | P1 |
| WARScribe-Parser | Audio pipeline implementation | P2 |
| Logi-Slate-UI | Turn entry interface | P2 |
| Vindicta-API | Auth middleware | P1 |

### Wednesday, Feb 27
| Product | Task | Priority |
|---------|------|----------|
| Meta-Oracle | Council protocol (part 1) | P1 |
| Primordia AI | Search depth implementation | P1 |
| WARScribe-Parser | Timestamp segment extraction | P2 |
| Logi-Slate-UI | WARScribe export | P2 |
| Vindicta-API | Rate limiting | P1 |

### Thursday, Feb 28
| Product | Task | Priority |
|---------|------|----------|
| Meta-Oracle | Council protocol (part 2) | P1 |
| Primordia AI | Evaluation improvements | P1 |
| WARScribe-Parser | Parser tests | P2 |

### Friday, Mar 1
| Product | Task | Priority |
|---------|------|----------|
| Meta-Oracle | Integration tests | P1 |

### Saturday, Mar 2
*Reduced schedule*

### Sunday, Mar 3 — **Release Day**
| Product | Release | Notes |
|---------|---------|-------|
| Meta-Oracle | v0.2.0 | Agents release |
| WARScribe-Parser | v0.2.0 | Audio release |
| Logi-Slate-UI | v0.1.5 | Core UI release |

---

## 📅 Week 5: Mar 4-10 — Polish & Integration

### Monday, Mar 4
| Product | Task | Priority |
|---------|------|----------|
| Agent-Auditor-SDK | Meta-Oracle integration | P1 |
| Primordia AI | MCTS polish | P1 |
| Vindicta-Portal | Game Tracker MVP (part 1) | P0 |
| Vindicta-Core | API contracts finalization | P1 |
| Vindicta-API | Integration tests | P1 |

### Tuesday, Mar 5
| Product | Task | Priority |
|---------|------|----------|
| Agent-Auditor-SDK | Primordia integration | P1 |
| Primordia AI | Move depth 3+ | P1 |
| Vindicta-Portal | Game Tracker MVP (part 2) | P0 |
| Vindicta-Core | Unit tests | P1 |
| Vindicta-API | Performance optimization | P1 |

### Wednesday, Mar 6
| Product | Task | Priority |
|---------|------|----------|
| Agent-Auditor-SDK | WARScribe integration | P1 |
| Primordia AI | Performance optimization | P1 |
| Vindicta-Portal | PWA setup (part 1) | P0 |
| Vindicta-Core | PyPI preparation | P1 |
| Vindicta-API | Documentation | P1 |

### Thursday, Mar 7
| Product | Task | Priority |
|---------|------|----------|
| Agent-Auditor-SDK | Integration tests | P1 |
| Primordia AI | Tests | P1 |
| Vindicta-Portal | PWA setup (part 2) | P0 |

### Friday, Mar 8
*Buffer day for overflow tasks*

### Saturday, Mar 9
*Reduced schedule*

### Sunday, Mar 10 — **Release Day**
| Product | Release | Notes |
|---------|---------|-------|
| Agent-Auditor-SDK | v0.3.0 | Integration release |
| Primordia AI | v0.2.0 | MCTS release |
| Vindicta-API | v0.2.0 | Core APIs release |

---

## 📅 Week 6: Mar 11-17 — v1.0 Release Week ⭐

### Monday, Mar 11
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | Primordia overlay integration | P0 |
| Meta-Oracle | List Grader API | P1 |
| Logi-Slate-UI | AI overlay feature | P2 |

### Tuesday, Mar 12
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | PWA install testing | P0 |
| Meta-Oracle | Upset Detector feature | P1 |
| Logi-Slate-UI | Replay player | P2 |

### Wednesday, Mar 13 — **v1.0 Release: Vindicta-Core**
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | Final testing | P0 |
| **Vindicta-Core** | **v1.0.0 PyPI publish** | **P1** |
| Meta-Oracle | Integration testing | P1 |
| Logi-Slate-UI | Tests | P2 |

### Thursday, Mar 14 — **v1.0 Release: Vindicta-API**
| Product | Task | Priority |
|---------|------|----------|
| Vindicta-Portal | Bug fixes | P0 |
| **Vindicta-API** | **v1.0.0 Release** | **P1** |

### Friday, Mar 15 — **v1.0 Release: Vindicta-Portal** ⭐
| Product | Task | Priority |
|---------|------|----------|
| **Vindicta-Portal** | **v1.0.0 Production Release** | **P0** |

### Saturday, Mar 16
*Reduced schedule*

### Sunday, Mar 17 — **Final Releases**
| Product | Release | Notes |
|---------|---------|-------|
| Meta-Oracle | v0.3.0 | User Features release |
| Logi-Slate-UI | v0.2.0 | Game Tracking release |

---

## 📊 Daily Update Cadence

Products receiving continuous small updates:

| Product | Frequency | Type |
|---------|-----------|------|
| Platform-Docs | Daily | Documentation |
| Dice-Engine | Weekly | Bug fixes |
| Entropy-Buffer | Weekly | Bug fixes |
| Economy-Engine | Bi-weekly | README updates |
| Atomic-Ledger-Py | Bi-weekly | Tests & docs |

---

## 🏷️ Task Labels

Use these labels when creating GitHub Issues:

```
priority:p0-critical
priority:p1-high
priority:p2-medium
priority:p3-low
type:feature
type:bugfix
type:docs
type:test
week:1
week:2
week:3
week:4
week:5
week:6
```

---

*This schedule is the source of truth for daily task allocation. Updated weekly.*
