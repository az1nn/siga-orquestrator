# SPEC-001 — Plano técnico
**Estado:** PLAN READY / IMPLEMENTATION BLOCKED.

## Arquitetura proposta
`ChatGPT UI → ferramentas MCP read-only → SIGA skill registry / GitHub public adapter / ai-memory read-only (opcional)`.
SIGA Central é o único orquestrador. Observatory não interpreta gates como autorizações nem decide execuções por conta própria.

## Contratos e separação
1. Adaptador GitHub consulta somente dados públicos permitidos; normaliza PRs/issues, HEADs, CI e source completeness.
2. Registry de skills reflete capabilities existentes do SIGA; não inventa skills disponíveis.
3. HandoffEnvelope portátil, versionado e independente de UI/modelo, com origem e limitações.
4. ai-memory consulta namespace por projeto apenas; nunca altera contexto persistente na V1.
5. UI MCP Apps ou host compatível é progressive enhancement; ferramentas fornecem resposta útil sem UI.
6. `request_siga_execution` reservado para módulo posterior, com gate de autorização, reconcile, CAS, idempotência, exact-head, verify e handoff.

## Milestones
- M0 (este PR): consolidar base documental, decisões G1–G7, contratos e reconciliação canônica.
- M1 (futura autorização): inicializar CLI oficial Spec Kit, executar análise e corrigir inconsistências; projetar testes de normalização.
- M2 (futura autorização): implementar tools read-only do GitHub público, schema e testes de fixture/live.
- M3 (futura autorização): dashboard MCP Apps com navegação PR/issue, filtros, skills e handoff.
- M4 (futura autorização): lookup ai-memory read-only, segurança de integração e UX resiliente.
- M5 (spec separada): gateway de execução SIGA autorizado, sem alterar o contrato da V1.

## Riscos
- R01 confundir fixture/histórico com live: `source_type`, `observed_at`, SHA obrigatório.
- R02 contagem GitHub issue/PR: filtrar `pull_request` antes de contar issues.
- R03 paginação/rate-limit: `partial`/`UNKNOWN`, nunca preencher com zero.
- R04 skill sugerida inexistente: verificar registry canônico e falhar com mensagem.
- R05 ai-memory ser tomado como verdade atual: nunca substituir GitHub verified.
- R06 abertura de chat não suportada: fallback copiar/exportar.
- R07 execução sem consentimento: ferramentas mutantes nem sequer registradas na V1.

## Validação e rollback
Validar via testes offline, spec checklist, revisão de ADRs e, em milestone posterior, CI exact-head. Reverter a branch documental sem afetar `master`; nenhum servidor ou integração ativa.
