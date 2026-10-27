# HandoffEnvelope v1 — proposta
Formato portátil e não executável por si só. JSON de exemplo usa dados históricos do Growing-Rio, não consulta live.

```json
{
  "schema_version": "1.0.0",
  "repository": "az1nn/growing-rio",
  "work_item": {"type": "issue", "number": 232},
  "related_prs": [213],
  "orchestrator": "SIGA",
  "recommended_skills": ["ARCH", "ARTIST"],
  "selected_skills": [],
  "classification": "WATCH",
  "execution_authorized": false,
  "provenance": {"source_type": "imported_fixture", "verified_live": false, "source_date": "2026-10-26", "ref_sha": null},
  "evidence": [],
  "restrictions": ["no_writes", "reconcile_live_before_execution"],
  "memory_mode": "read_only"
}
```

Obrigatórios em handoff real: repo, tipo+número do item, SHA/HEAD quando verificável, links de fonte, observed_at, completude, riscos, política de autorização. Não aceitar SHA ausente como se verificado.
Escolha do usuário: continuar na conversa ou exportar/copiar. Um novo chat só poderá ser criado se a capacidade do host for comprovada.
