# siga-orquestrator

> SIGA Central · SIGA Observatory — base documental SPEC-001 (v0.3.0 reconciliada).

**Estado:** planejamento em PR draft; sem servidor MCP implantado, sem plugin instalado, sem ações sobre outros repositórios.

## Fonte canônica
- Repositório: `az1nn/siga-orquestrator`.
- Orquestrador: SIGA Central (único responsável por RECONCILE → CLASSIFY → EXECUTE → VERIFY → HANDOFF).
- Observatory: interface de consulta de specs, tarefas, PRs, issues, CI, gates, skills e handoffs dentro do ChatGPT.
- Integrações previstas: GitHub público via ferramentas MCP read-only, componentes de UI, ai-memory opcional somente leitura.

## Ler nesta ordem
1. `.specify/memory/constitution.md` — constituição proposta, ainda não ratificada.
2. `docs/GRILLING.md` — decisões humanas G1–G7.
3. `specs/001-chatgpt-dashboard/spec.md` — requisitos, cenários e limites.
4. `specs/001-chatgpt-dashboard/plan.md` — arquitetura e sequência de milestones.
5. `specs/001-chatgpt-dashboard/tasks.md` — backlog sem marcações fictícias.
6. `specs/001-chatgpt-dashboard/contracts/mcp-tools.md` — ferramentas propostas, não implementadas.
7. `specs/001-chatgpt-dashboard/contracts/handoff-envelope.md` — contrato de continuidade.
8. `docs/adrs/` — registro de decisões; `docs/RECONCILIATION-2026-10-27.md` — estado verificado da migração.

## Regras vigentes
- G1=B: integrado ao SIGA Central, neste repositório.
- G2=A: V1 somente fixtures e leitura de repositórios públicos, sem conexão privada.
- G3=C: V1 sem armazenamento persistente de snapshots pelo Observatory.
- G4=B: gateway de execução futura com autorização específica; não expor ferramentas de escrita na V1.
- G5=B: handoff portátil; continuidade no chat atual ou novo chat somente se houver suporte verificado.
- G6=A: ai-memory opcional em modo leitura, sem gravação.
- G7=B: SIGA recomenda skills, usuário confirma ou substitui.

## Validação e status
Esta branch contém documentação proposta. Não confundir testes offline anteriores do pacote com CI do GitHub. CLI oficial Spec Kit e `/speckit.analyze` ainda exigem execução em ambiente apropriado; não se presume implementação aprovada.

