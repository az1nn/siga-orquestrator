# SPEC-001 — SIGA Observatory no ChatGPT
**Estado:** planejamento, não implementado. **Home:** `az1nn/siga-orquestrator`.

## Problema
Os dashboards auditáveis de repositórios já mostram specs, tarefas, PRs, issues, CI, gates e handoffs, mas abrir HTMLs e criar contextos manualmente é custoso. Precisamos reunir inspeção e continuidade via SIGA em uma experiência no chat.

## Usuários e histórias
**US-01 — Overview:** como mantenedor, quero selecionar repositório público e visualizar métricas sustentadas por SHA e fonte, inclusive status STALE/UNKNOWN.
**US-02 — Drill-down:** quero clicar em PR/issue e ler diffs, HEAD, checks, bloqueios, links, dependências e owner sem confundir issue com PR.
**US-03 — Skills:** quero obter recomendação de skills a partir do registro canônico SIGA, confirmar ou substituir, sem que a seleção dispare execução.
**US-04 — Handoff:** quero preparar um pacote versionado para continuar resolução no chat atual ou exportar para nova conversa quando suportado.
**US-05 — Memória:** quero recuperar contexto ai-memory apenas para leitura, com citações, namespace do projeto e degradação segura.
**US-06 — Futuro:** quero solicitar execução MCP após aprovação específica, autorização e controle de concorrência; fora da V1.

## Requisitos funcionais
- FR-01: listar repositórios explicitamente permitidos e com leitura pública.
- FR-02: overview de specs, checklists, PRs, issues, gates e CI com timestamp e SHA.
- FR-03: separar PRs de issues em contagens, páginas e filtros.
- FR-04: distinguir CI success histórico, exact-head e desconhecido.
- FR-05: filtrar tarefas individuais por spec, prioridade e status com links para linhas do SHA.
- FR-06: oferecer inspeção de PR ou issue com referências verificáveis.
- FR-07: sugerir skills a partir de registro canônico confirmado; exigir confirmação humana.
- FR-08: emitir HandoffEnvelope portátil com authorization=false na V1.
- FR-09: ai-memory opcional somente leitura; falha não bloqueia overview.
- FR-10: não persistir snapshots nem ingerir diariamente na V1; deltas só com duas fontes externamente comprovadas.
- FR-11: permitir fallback textual/exportação quando widgets ou abertura de novo chat não suportados.
- FR-12: não registrar ferramentas mutantes no MCP da V1.

## Critérios de aceitação
- CA01: PR e issue abrem visualizações distintas com URL/evidência.
- CA02: recommendation + confirmação humana não muda nenhum recurso.
- CA03: handoff validado por schema com repo, item, SHAs, fontes, restrições e authorization=false.
- CA04: ai-memory isolado por projeto e read-only; indisponibilidade explicitada.
- CA05: estado GitHub prevalece sobre memória/fixture, mesmo se contraditório.
- CA06: UI em Android/desktop com filtros funcionais e estados loading/error/empty/stale.
- CA07: nenhuma escrita, nenhum snapshot persistente e nenhuma autenticação privada na V1.
- CA08: executor futuro isolado por feature, aprovação e testes de claims/CAS/exact-head.
- CA09: nenhuma afirmação de CI verde atual baseada apenas em check histórico.
- CA10: handoff exportável se novo chat automático indisponível.

## Dados de regressão (históricos)
Fixture Growing-Rio 2026-10-26: 45 arquivos tasks.md; 623 concluídas / 131 pendentes; 2 PR draft e 5 issues excluindo PRs; quatro checks master SUCCESS datados de 15/10; R06 WATCH, City runtime REJECT_ALL. Esses números NÃO são estado live de 27/10.

## Fora do escopo
Implementação de MCP/UI, deploy, novo chat universal, GitHub privado, execução automática, gravação no ai-memory, merges e cron de histórico.
