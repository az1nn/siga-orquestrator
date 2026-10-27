# Contratos MCP propostos — SPEC-001
Ferramentas abaixo são DESIGN ONLY; nenhuma está registrada ou implantada.

| Ferramenta | Entrada | Saída / Garantias | V1 |
|---|---|---|---|
| `list_repositories` | filtro | repositórios públicos permitidos + completude | Sim |
| `get_repository_overview` | repo, ref? | métricas, SHA, observed_at, source_type | Sim |
| `list_spec_tasks` | repo, sha, filtros, cursor | tasks.md do SHA e links de linha | Sim |
| `list_pull_requests` | repo, cursor | PR + HEAD, draft, checks | Sim |
| `list_issues` | repo, cursor | issues sem PRs | Sim |
| `get_ci_evidence` | repo, sha | runs, conclusão, times, exact-head | Sim |
| `get_blockers` | repo | gates, owner, evidências e unknown | Sim |
| `inspect_work_item` | repo, `pr|issue`, number | inspeção detalhada, provenance | Sim |
| `list_siga_capabilities` | contexto/repo | registry canônico verificado | Sim |
| `recommend_siga_skills` | contexto | skills com racional; requer confirmação | Sim |
| `prepare_handoff` | item, skills confirmadas | HandoffEnvelope versionado | Sim |
| `recall_project_context` | repo, query | ai-memory read-only, opcional | Opcional |
| `compare_repository_snapshots` | duas referências externas | delta auditável ou UNAVAILABLE | Condicional |
| `request_siga_execution` | autorização, CAS, idempotência | mutante, novo milestone | **Não** |
| `get_execution_status` | execution_id | estado auditado quando existir executor | **Não** |

## Envelope de resposta
`schema_version`, `source_type` (`live_github|imported_fixture`), `repo`, `observed_at`, `ref_sha`, `completeness` (`complete|partial|unknown`), `errors[]`, `sources[]`, `data`.

Em fixture histórica, `observed_at=null` e `source_date` informa quando foi capturada. Nunca converter erro em contagem zero ou status verde. UI não recebe tokens. Limitar repo/number, prevenir prompt injection em comentários/PR, respeitar rate limit.
