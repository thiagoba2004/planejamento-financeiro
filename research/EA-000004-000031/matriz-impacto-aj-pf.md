# Matriz de impacto — Ações Judiciais → Planejamento Financeiro

**Data de corte:** 21/09/2026

## Conclusão

Há repercussão material suficiente para atualização do PRJ-000004. O impacto não exige reconstrução da arquitetura do projeto, mas exige atualização de premissas, casos e gates profissionais.

## Impactos confirmados

| Achado jurídico recente | Impacto financeiro | Superfícies principais |
|---|---|---|
| Separação de fato sem divórcio formal | distinguir estado civil de unidade econômica efetiva | superendividamento-pf; divorcio-transicao-financeira; plano integrado pós-divórcio |
| Renda do outro cônjuge não se soma automaticamente | separar renda própria, transferências, rateios e despesas efetivamente suportadas | superendividamento-pf; filhos; transição financeira |
| Patrimônio comum não partilhado e bens financiados | separar valor bruto, saldo, direito aquisitivo, meação potencial e liquidez | patrimonio-partilha-liquidez; moradia; dívidas |
| Financiamento imobiliário e certos créditos garantidos fora da repactuação | dívida juridicamente excluída continua financeiramente relevante | superendividamento-pf; indenizacao-superendividamento; dívidas |
| Capital indenizatório superveniente | melhora liquidez sem virar renda recorrente; pode exigir gate jurídico antes de pagamento seletivo | indenizacao-superendividamento; dividas-capital-indenizatorio; plano pós-indenização |
| Leis 15.411/2026 e 15.412/2026 | risco de moradia emergencial, duplicação de custos, alimentos provisórios/provisionais e reserva de contingência | divorcio-transicao-financeira; moradia; filhos; plano integrado |
| Art. 699-A do CPC e risco de violência | gatilho de contingência financeira e encaminhamento jurídico imediato | transição; filhos; moradia |
| Correções de autoria doutrinária e Tema 215/TST | impacto financeiro direto baixo | sem necessidade de frente financeira própria |

## Decisão de arquitetura

Criar três estratégias derivadas:
1. EA-000004-000032 — Separação de fato e unidade econômica no planejamento financeiro.
2. EA-000004-000033 — Gate jurídico-financeiro no superendividamento e uso de capital indenizatório.
3. EA-000004-000034 — Planejamento financeiro de contingência em ruptura familiar com medidas protetivas.

A EA-000004-000031 permanece como estratégia integradora e não duplica o trabalho material dessas três frentes.
