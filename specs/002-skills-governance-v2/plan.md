# SPEC-SKILLS-002 — Plan

Status: APPROVED DOCUMENTATION; NO IMPLEMENTATION AUTHORIZED.

## Architecture
Central portable contract, repository-local implementations. SIGA controls lifecycle and orchestration; domain owners control technical/artistic outcomes; QA/INSPECTOR independently validate evidence; human gates remain binding. Never promote a local lease to distributed mutex. Use source-controlled contracts; derived graph is disposable.

## Milestones
| Milestone | Priority | Deliverable | Dependencies | Exit gate |
|---|---|---|---|---|
| M0 Inventory | P0 | Reconciled skill/consumer/entrypoint inventory and conflict matrix | Approved spec | Live repo references, draft/merged distinctions, human review |
| M1 SIGA v2 contract | P0 | Versioned aliases, routing, owners, handoff schema and ADRs | M0 | Contract tests, compatibility review, explicit implementation approval |
| M2 Concurrency | P0 | Atomic claim/fencing and recovery proof or narrower fail-closed contract | M1 | Independent two-writer live contention, stale-head/recovery/adversarial tests |
| M3 MemeMon pilot | P1 | Bounded adapter and cross-session continuation | M2 | Exact-head CI, domain gates, no fabricated artifacts |
| M4 Controlled migrations | P1 | Independent repository-by-repository adapters | M3 | Each repo's constitution, tests, gates, authorized PR |
| M5 Continuous audit | P2 | CI contract checks, read-only orphan/drift audit and observability | M4 | Reproducible evidence and no automatic mutations by audit |

## Existing work reconciliation
- az1nn/az1nn PR #18: portable Godot skill tree, draft; do not duplicate/merge implicitly.
- az1nn/az1nn PR #19: SKR grilling and Spec Kit, draft; integrate only by contract review.
- az1nn/meme-mon PR #28: SIGA Central M1 docs draft, not runtime activation; issue #24 live CAS remains open.
- az1nn/growing-rio PR #230 and az1nn/marica-game PR #93: skill simplifications already merged; do not recreate.
- az1nn/siga-orquestrator PR #1: Observatory documentation draft; keep isolated. Constitution proposed, not ratified.

## Delivery and safety
This PR adds only four Markdown documents. Publish on a dedicated branch, check exact head, review, no overlapping writes, check repository rules and mergeability. Merge only when applicable gates pass; otherwise leave PR open and report blocker. M0 inventory is planned, not completed by this initial reconciliation. Every implementation milestone requires separate approval.
