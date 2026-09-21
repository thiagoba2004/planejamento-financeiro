# Fase 02/06 — Balanço antes e depois da indenização

**Estratégia:** EA-000004-000021 — Plano financeiro integrado e monitoramento pós-indenização
**Data:** 21/09/2026
**Estado:** CONCLUÍDA

## 1. Fotografia imediatamente antes

| Item | Estado |
|---|---|
| ativos líquidos | DADO_AUSENTE |
| demais ativos | DADO_AUSENTE |
| passivos | DADO_AUSENTE |
| patrimônio líquido | NÃO_CALCULÁVEL |
| renda recorrente | DADO_AUSENTE |
| despesas essenciais | DADO_AUSENTE |
| serviço da dívida | DADO_AUSENTE |
| fluxo livre | NÃO_CALCULÁVEL |
| reserva | DADO_AUSENTE |

## 2. Evento

+ R$ 100.000,00 líquidos e integralmente disponíveis.

## 3. Fotografia imediatamente depois do recebimento

ATIVOS_LIQUIDOS_APOS = ATIVOS_LIQUIDOS_ANTES + 100.000

PATRIMONIO_LIQUIDO_APOS = PATRIMONIO_LIQUIDO_ANTES + 100.000

RENDA_RECORRENTE_APOS = RENDA_RECORRENTE_ANTES

SERVICO_DA_DIVIDA_APOS = SERVICO_DA_DIVIDA_ANTES, até que haja intervenção efetiva

FLUXO_LIVRE_APOS = FLUXO_LIVRE_ANTES, como efeito direto do recebimento

## 4. Balanço após decisões

Depois de qualquer decisão, reconstruir:

ATIVOS_LIQUIDOS_FINAIS = ATIVOS_LIQUIDOS_APOS - SAIDAS_EXECUTADAS + ENTRADAS_POSTERIORES

PASSIVOS_FINAIS = PASSIVOS_ANTES - QUITACOES - AMORTIZACOES + NOVOS_PASSIVOS

PATRIMONIO_LIQUIDO_FINAL = ATIVOS_TOTAIS_FINAIS - PASSIVOS_FINAIS

FLUXO_LIVRE_FINAL = RENDA_RECORRENTE - DESPESAS_ESSENCIAIS - SERVICO_DA_DIVIDA_FINAL - NOVOS_CUSTOS_RECORRENTES

## 5. Livro de alocação

| Categoria | Valor | Fonte da decisão | Estado |
|---|---:|---|---|
| caixa operacional | NÃO_CALCULÁVEL | EA-000004-000016 | PENDENTE |
| despesas previsíveis | NÃO_CALCULÁVEL | EA-000004-000016 | PENDENTE |
| reserva | NÃO_CALCULÁVEL | EA-000004-000016 | PENDENTE |
| redução de dívidas | NÃO_CALCULÁVEL | EA-000004-000017 | PENDENTE |
| investimentos | NÃO_CALCULÁVEL | EA-000004-000018 | PENDENTE |
| objetivos | NÃO_CALCULÁVEL | EA-000004-000019 | PENDENTE |
| proteção | NÃO_CALCULÁVEL | EA-000004-000019 | PENDENTE |
| uso discricionário | NÃO_CALCULÁVEL | EA-000004-000020 | PENDENTE |
| não alocado | R$ 100.000,00 enquanto nada for decidido | plano integrado | CONFIRMADO |

## 6. Regra de atualização

Ao executar qualquer decisão, reduzir CAPITAL_AINDA_NAO_ALOCADO e preencher exatamente uma categoria de destino.

Se a decisão altera passivo ou fluxo, atualizar também:
- saldo de dívida;
- parcela mensal;
- custos recorrentes;
- liquidez;
- patrimônio líquido.

## 7. Controles

- a soma das alocações executadas + saldo não alocado deve ser sempre R$ 100.000,00;
- nenhum valor pode aparecer em duas categorias;
- decisões futuras não entram como executadas;
- rendimentos dos investimentos devem ser registrados separadamente do capital original;
- novas rendas não são atribuídas ao evento indenizatório sem causa econômica própria.

## 8. Gate

**SATISFEITO.**

O balanço integrado é reproduzível e permite atualização incremental a cada decisão, sem exigir números inexistentes.

## 9. Próxima fase

**Fase 03/06 — Plano de alocação do valor líquido.**
