# SIGA Observatory — Grilling G1–G7
Decisões expressas pelo usuário para o planejamento; não representam aprovação de implementação ou merge.

| ID | Escolha | Decisão vinculante |
|---|---|---|
| G1 | B | Repositório canônico SIGA Central; agora `az1nn/siga-orquestrator` |
| G2 | A | Fixtures + GitHub público na V1; sem credenciais privadas |
| G3 | C | Sem histórico persistente de dashboards na V1 |
| G4 | B | Execução futura mediada por MCP, com autorização e gates |
| G5 | B | Handoff portátil e escolha de continuidade conforme suporte do host |
| G6 | A | ai-memory somente leitura, opcional e não autoritativo |
| G7 | B | SIGA recomenda skill, usuário confirma ou substitui |

**Precedência:** qualquer proposta legada de persistência ou OAuth privado na V1 está SUPERSEDED por G2=A/G3=C. Nenhum tool de escrita será exposto no MVP.

**Autorização operacional da retomada:** ao dizer 'Siga' após definir o repositório, o usuário autorizou o próximo marco documental anunciado: branch de documentação e PR draft sem merge. Isso não autoriza implementar MCP, publicar plugin, modificar outras branches, executar skills ou escrever em outros projetos.
