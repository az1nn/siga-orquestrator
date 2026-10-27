# SPEC-001 — Tasks
Cada item aberto exige evidência de execução antes de ser marcado [x]. Esta lista não é uma autorização.

## M0 — Base de planejamento
- [x] T001 Confrontar estado real do repositório canônico, HEAD e branches (27/10).
- [x] T002 Registrar decisões G1–G7 em documento canônico.
- [x] T003 Consolidar SPEC-001, plano e contratos MCP/handoff em branch isolada.
- [ ] T004 Confirmar PR draft e verificações exact-head da branch.
- [ ] T005 Ratificar constituição proposta e aprovar próximo milestone.

## M1 — Integração Spec Kit
- [ ] T101 Instalar e executar CLI oficial Spec Kit no projeto, preservando constituição aprovada.
- [ ] T102 Executar `/speckit.analyze` e corrigir divergências.
- [ ] T103 Preparar matriz de testes para parser specs, GitHub PR/issue, CI e permissões.

## M2 — MCP leitura GitHub
- [ ] T201 Implementar adapter GitHub público com paginação, rate-limits e timestamps.
- [ ] T202 Implementar validação SHA/exact-head e contagens PR/issue separadas.
- [ ] T203 Testes de fixture, falhas parciais, erros e segurança.

## M3 — UI e handoffs
- [ ] T301 Implementar overview ChatGPT e estados loading/error/unknown.
- [ ] T302 Drill-down PR/issue, links GitHub e seleção de skill recomendada.
- [ ] T303 HandoffEnvelope versionado e exportação sem API de novo chat.

## M4 — ai-memory lookup
- [ ] T401 Validar implantação do ai-memory e permissões de consulta read-only.
- [ ] T402 Testar recuperação por namespace e fallback seguro.

## M5 — Executor futuro (separado da V1)
- [ ] T501 Abrir nova SPEC/ADRs para autorização, tokens e modelo de confiança.
- [ ] T502 Contratos CAS/claims, idempotência, exact-head, gates e reversibilidade.

## Restrições
Não fazer merge, não implantar servidor, não registrar tool de escrita, não modificar outros repositórios.
