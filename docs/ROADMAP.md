# SIGA — Canonical Roadmap

Repository: `az1nn/siga-orquestrator`
Document status: approved for documentary publication 2026-11-02; canonical only after verified merge into `master`.
Constitution: proposed, NOT ratified. This roadmap does not authorize M1–M5 implementation.

## Workstreams
| Workstream | Spec | Status | Boundary |
|---|---|---|---|
| Skills Governance v2 | [SPEC-SKILLS-002](../specs/002-skills-governance-v2/spec.md) | DOCUMENTATION APPROVED / M0–M5 PLANNED | No implementation without separate authorization |
| SIGA Observatory | [SPEC-001 on draft PR #1](https://github.com/az1nn/siga-orquestrator/pull/1) | DRAFT / PROPOSED | Separate PR, no merge or constitutional ratification implied |

## Skills Governance v2 milestone roadmap
| Order | Milestone | Priority | Status | Next gate |
|---|---|---|---|---|
| 0 | M0 Inventory and conflict matrix | P0 | NOT STARTED | Authorize inventory execution |
| 1 | M1 Portable SIGA v2 and composed specialist contracts | P0 | NOT STARTED | Approve design and implementation separately |
| 2 | M2 Distributed concurrency and safe recovery | P0 | NOT STARTED | Two independent writers and fencing evidence |
| 3 | M3 MemeMon pilot | P1 | NOT STARTED | Pilot exact-head acceptance |
| 4 | M4 Controlled migrations | P1 | NOT STARTED | Each repository's local gates |
| 5 | M5 Continuous audit and CI | P2 | NOT STARTED | Auditable regression evidence |

Detailed tasks: [tasks.md](../specs/002-skills-governance-v2/tasks.md). Delivery plan: [plan.md](../specs/002-skills-governance-v2/plan.md).

## Invariants
- REAL STATE > HANDOFF > MEMORY > CHAT.
- SIGA owns orchestration; specialists own their domain; QA/INSPECTOR independently verify; human gates are not bypassed.
- Repository-local authority and state never migrate automatically.
- Existing draft PRs #18/#19 (az1nn/az1nn), #28 (MemeMon) and Observatory #1 are not ratified or merged by this roadmap.
- A passing static documentation check does not prove runtime safety.
