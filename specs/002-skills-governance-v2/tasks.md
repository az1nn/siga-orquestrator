# SPEC-SKILLS-002 — Tasks

Status: DOCUMENTATION APPROVED. The checked items below are publication preparation only, not M0–M5 implementation.

## Publication
- [x] User approved SPEC-SKILLS-002 and M0–M5 documentation on 2026-11-02.
- [x] Reconcile destination repository master and open Observatory PR #1 before branch creation.
- [ ] Commit spec.md, plan.md, tasks.md and docs/ROADMAP.md to isolated branch.
- [ ] Open documentary PR; inspect diff, overlap, current master/head, required checks, reviews and protections.
- [ ] Merge only if all applicable gates are satisfied; confirm master contains canonical roadmap.

## M0 — Inventory (not authorized to implement)
- [ ] Inventory every skill, version, entrypoint, consumer, owner, capability and dependency.
- [ ] Reconcile existing draft/merged PRs and identify duplication/conflicts.
- [ ] Review inventory and approve M1 implementation scope.

## M1 — SIGA v2 contract (not authorized)
- [ ] Specify aliases, owner matrix, fail-closed routing and portable handoff schema.
- [ ] Define ADRs, adapter contracts and contract tests.
- [ ] Obtain separate approval.

## M2 — Concurrency (not authorized)
- [ ] Identify every mutating writer and enforce safe claims or document exclusions.
- [ ] Prove independent live two-writer contention, fencing and stale-head behavior.
- [ ] Test expiry/recovery and gate freeze; obtain separate approval.

## M3 — MemeMon pilot (not authorized)
- [ ] Integrate a bounded adapter without touching unrelated work.
- [ ] Test cross-session resume, human-gate stops and exact-head evidence.
- [ ] Obtain separate approval.

## M4 — Controlled migration (not authorized)
- [ ] Plan per-repository PRs preserving local constitutions and gates.
- [ ] Validate compatibility, regression and ownership per project.
- [ ] Obtain separate approval per migration.

## M5 — Continuous audit (not authorized)
- [ ] Add contract CI and read-only drift/orphan audit.
- [ ] Validate reports, observability and fail-closed behavior.
- [ ] Obtain separate approval.
