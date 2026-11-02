# SPEC-SKILLS-002 — Skills Governance v2

Status: APPROVED FOR DOCUMENTATION ONLY (2026-11-02). Implementation M1–M5 NOT AUTHORIZED. Constitution ratification NOT IMPLIED.
Canonical roadmap target: `docs/ROADMAP.md` in `az1nn/siga-orquestrator` after verified merge.
Scope: governance and portable contracts only. Each project retains its own operational authority, state, claims, CI and specialist definitions.

## Problem
SIGA and specialists have diverged across projects; duplicate routing, unclear ownership, incomplete handoffs and unproven distributed concurrency increase risk. Do not copy a project's runtime/claims to another repository.

## Functional requirements
- FR01: Inventory installed and proposed skills, consumers, versions, entrypoints, ownership, dependencies, status and existing PRs; distinguish merged from draft.
- FR02: Define portable SIGA orchestration: identity -> reconcile -> classify RESUME/WATCH/ADVANCE -> scoped claim when mutating -> route -> execute -> verify -> durable handoff.
- FR03: Compose SIGA with domain specialists (ART, ARCH, SCENE, DESIGN, INSPECTOR, LORE on demand) without creating independent orchestrators. Alias interception is only claimed for verified installed entrypoints.
- FR04: Preserve domain authority, independent QA/INSPECTOR, human visual/constitutional gates and project-local constraints; RELATORIO may be folded into SIGA only after capability parity evidence.
- FR05: Require collision-safe mutation, exact-head freshness, single-writer semantics, atomic CAS/fencing where claimed, and fail-closed WATCH when ownership is ambiguous.
- FR06: Persist compact schema-versioned handoffs, stable task keys and evidence references; current repository state overrides handoff and chat.
- FR07: Keep Spec Kit spec/plan/tasks, ADRs, tests, canonical roadmap and traceability in Git; derived graphs and caches never become canonical.
- FR08: Define adapters for Pi, Codex, Claude Code and ChatGPT without claiming unsupported global alias interception or tool availability.
- FR09: Pilot in MemeMon, then migrate each repository via independent authorized scoped PRs; never synchronize mutable state or automatically merge across repositories.
- FR10: CI and read-only audit verify schema, routes, ownership, drift, gates, missing artifacts and continuity; no success claim from static-only checks.
- FR11: Reconcile existing PRs #18/#19 in az1nn/az1nn and #28 in az1nn/meme-mon; preserve Observatory PR #1 as independent draft and its constitution as proposed.
- FR12: Approval of this spec authorizes documentation publication and guarded merge only. M1–M5 implementation, activation, cross-repo edits and constitutional ratification require separate authorization.

## Non-goals
No runtime coordinator deployment, production aliases, distributed lock claim, project migrations, new backend, plugin activation, asset changes or M1–M5 implementation in this PR.

## Acceptance
- CA01: Four documents exist with consistent M0–M5 dependency order and traceable FR IDs.
- CA02: Each phase has scope, dependencies, exit gate and explicit approval boundary.
- CA03: No changed file outside this spec folder and docs/ROADMAP.md.
- CA04: Existing Observatory PR #1 is untouched and not implicitly merged.
- CA05: Branch/PR exact-head checks, review, mergeability and required repository protections are reconciled before any merge.
- CA06: Master is only declared canonical after confirmed merge and fresh master read.
- CA07: No claims of completed M1–M5 work, production CAS or ratified constitution.
