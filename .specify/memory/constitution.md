# Constituição proposta — SIGA Central / Observatory
**Versão documental:** 0.3.0-draft · **Ratificação:** pendente.

## I — Estado real e VERIFY-FIRST
REAL STATE > HANDOFF > MEMORY > CHAT. Afirmações operacionais precisam indicar fonte, SHA, instante de observação e completude; ausência de evidência é UNKNOWN, nunca PASS.

## II — Um único orquestrador
SIGA Central detém RECONCILE → CLASSIFY (RESUME/WATCH/ADVANCE) → EXECUTE → VERIFY → HANDOFF. Observatory é superfície de observação e navegação; não assume ownership, não altera gates nem cria autorizações.

## III — V1 estritamente read-only
V1 consulta apenas fixtures e GitHub público. Nenhuma escrita em PRs, issues, arquivos, branches, deploys ou claims; nenhuma ação de executor exposta. G4=B refere-se a capacidade futura sujeita a aprovação independente.

## IV — Integridade temporal
Verificar HEAD do PR, commit base, SHA dos checks e suas datas. Check verde antigo não representa check atual. Contagens de issues excluem PRs; correção de contagem não equivale a issue criada.

## V — Gates e concorrência
Gates ART/SCENE/ARCH/QA/INSPECTOR e decisões humanas (incluindo REJECT_ALL) prevalecem sobre métricas automáticas. Claims históricos não são leases ativos. Execução futura requer CAS, idempotência, exact-head, autorização e auditoria.

## VI — Handoff portátil
Cada handoff contém contrato versionado, repositório, item de trabalho, refs/SHA, evidências, restrições, skill recomendada e consentimento de execução explicitamente false na V1. Nova conversa somente com suporte comprovado; caso contrário exportar/copiar.

## VII — Memória auxiliar
ai-memory é consulta opcional e isolada por projeto, nunca fonte de verdade para GitHub atual. G6=A proíbe writes, hooks e retenção pelo Observatory.

## VIII — Privacidade e segurança
Sem secrets em browser, fixtures, mensagens ou UI. Aplicar limites de taxa, allowlist pública, validação de inputs, proteção contra conteúdo malicioso em PR/issue e separação de projetos. Autenticação privada é futura.

## IX — UI testável
Dashboard acessível em Android e desktop, filtros funcionais, feedback para estados vazios/erro/stale, URLs para evidências e conteúdo textual completo sem depender de widgets.

## X — Governança Spec Kit
Especificação → ADR → plano → tarefas → testes/evidências. Constituição permanece proposta até ratificação explícita. Merge e deploy sempre independentes da aprovação do planejamento.
