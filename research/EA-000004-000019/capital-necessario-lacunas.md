# Fase 02/06 — Capital necessário e lacunas

**Estratégia:** EA-000004-000019 — Objetivos de vida, aposentadoria, seguros e proteção patrimonial
**Data:** 21/09/2026
**Estado:** CONCLUÍDA

## 1. Objetivo

Definir como calcular a necessidade de capital de cada objetivo e quanto o capital extraordinário pode reduzir lacunas sem comprometer liquidez, reserva e decisões anteriores.

## 2. Capital disponível para objetivos

O ponto de partida não é R$ 100.000,00 integralmente.

CAPITAL_PARA_OBJETIVOS = CAPITAL_EXTRAORDINARIO - CAIXA_OPERACIONAL - DESPESAS_PREVISIVEIS - LACUNA_DE_RESERVA - DECISOES_DE_DIVIDA - OUTROS_COMPROMISSOS_CONFIRMADOS

Sem os dados dessas parcelas:

**CAPITAL_PARA_OBJETIVOS = NÃO_CALCULÁVEL**

## 3. Lacuna por objetivo

Para um objetivo com valor-alvo conhecido:

GAP_OBJETIVO = VALOR_ALVO - RECURSOS_JA_DESTINADOS - APORTES_FUTUROS_PROJETADOS

Se o resultado for menor ou igual a zero, não há lacuna financeira naquele cenário.

## 4. Atualização temporal

Se o objetivo está no futuro, o valor-alvo deve ser trazido para a data do objetivo por premissa explícita de inflação/custo.

VALOR_FUTURO_ALVO = VALOR_ATUAL_ALVO × FATOR_DE_ATUALIZACAO

O fator não pode ser inventado. Deve usar premissa documentada e revisável.

## 5. Cobertura pelo capital extraordinário

COBERTURA_DO_GAP = ALOCACAO_DO_CAPITAL_EXTRAORDINARIO / GAP_OBJETIVO

Esse indicador mede quanto da lacuna seria reduzida. Não significa que deva ser usada a totalidade do capital disponível.

## 6. Aportes futuros

Para objetivos de acumulação:

NECESSIDADE_DE_APORTE_FUTURO = GAP_REMANESCENTE ajustado por prazo e retorno esperado líquido de custos/tributação

Não calcular retorno esperado sem premissas de carteira e horizonte.

## 7. Teste de competição entre objetivos

Se a soma dos gaps prioritários superar o capital disponível:

1. preservar liquidez e reserva;
2. respeitar compromissos já confirmados;
3. ordenar objetivos por prioridade e prazo;
4. testar postergação ou redução de metas flexíveis;
5. distribuir capital somente após documentar o trade-off.

## 8. Matriz de lacunas

| Objetivo | Valor-alvo | Recursos existentes | Gap | Prazo | Prioridade | Capital extraordinário proposto | Gap remanescente |
|---|---:|---:|---:|---|---|---:|---:|
| objetivo A | DADO_AUSENTE | DADO_AUSENTE | NÃO_CALCULÁVEL | DADO_AUSENTE | NÃO_CLASSIFICADO | NÃO_CALCULÁVEL | NÃO_CALCULÁVEL |

## 9. Regra contra dupla contagem

A mesma parcela dos R$ 100.000,00 não pode simultaneamente:
- compor reserva;
- quitar dívida;
- financiar objetivo;
- ser investida para aposentadoria;
- financiar prêmio de seguro;
- permanecer como caixa remanescente.

## 10. Gate da Fase 02

**SATISFEITO.**

Foram documentadas as fórmulas de capital disponível, gap, cobertura, atualização temporal e competição entre objetivos, preservando os dados ausentes.

## 11. Próxima fase

**Fase 03/06 — Aposentadoria e previdência.**
