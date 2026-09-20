# Fase 03/06 — Fluxo de caixa e cenários provisórios

**Estratégia:** EA-000004-000005 — Diagnóstico financeiro da ruptura e orçamento de transição  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Objetivo

Transformar a linha de base em cenários de caixa reproduzíveis para 30, 90 e 365 dias, sem confundir:
- hipótese jurídica com obrigação confirmada;
- venda/resgate de ativo com renda recorrente;
- transferência entre as partes com criação de renda familiar;
- patrimônio litigioso com liquidez disponível.

## 2. Unidade de cálculo

Cada cenário é calculado separadamente para cada unidade financeira.

Campos essenciais:
- caixa líquido inicial disponível;
- entradas recorrentes mensais;
- saídas recorrentes mensais;
- transferências confirmadas ou condicionais;
- custos pontuais por janela de tempo;
- ativos líquidos efetivamente disponíveis;
- eventos com data prevista;
- rótulo jurídico da premissa.

## 3. Fórmulas

### Saldo operacional mensal

```text
SALDO_OPERACIONAL_MENSAL =
ENTRADAS_RECORRENTES
− SAÍDAS_RECORRENTES
```

Transferências entre as partes devem estar embutidas nas entradas/saídas da unidade, mas eliminadas quando se produzir visão consolidada da família.

### Caixa projetado em 30 dias

```text
CAIXA_30 =
CAIXA_INICIAL
+ ENTRADAS_30
− SAÍDAS_RECORRENTES_30
− CUSTOS_PONTUAIS_0_30
```

### Caixa projetado em 90 dias

```text
CAIXA_90 =
CAIXA_INICIAL
+ ENTRADAS_90
− SAÍDAS_RECORRENTES_90
− CUSTOS_PONTUAIS_0_90
```

### Caixa projetado em 365 dias

```text
CAIXA_365 =
CAIXA_INICIAL
+ ENTRADAS_365
− SAÍDAS_RECORRENTES_365
− CUSTOS_PONTUAIS_0_365
```

Para aproximação mensal:
- 30 dias = 1 mês;
- 90 dias = 3 meses;
- 365 dias = 12 meses.

Quando datas reais forem relevantes, a implementação futura deve usar calendário de eventos e não apenas múltiplos mensais.

## 4. Liquidez

### Meses de despesas essenciais cobertos

```text
LIQUIDEZ_EM_MESES =
ATIVOS_LIQUIDOS_DISPONIVEIS
÷ DESPESAS_ESSENCIAIS_MENSAIS
```

Essa métrica não representa uma meta universal. Ela apenas expressa cobertura atual.

### Cobertura de déficit

Se o saldo operacional mensal for negativo:

```text
COBERTURA_DO_DEFICIT_EM_MESES =
ATIVOS_LIQUIDOS_DISPONIVEIS
÷ ABS(SALDO_OPERACIONAL_MENSAL)
```

Não usar essa fórmula quando o saldo mensal for zero ou positivo.

## 5. Arquitetura de cenários

### Cenário confirmado
Usa apenas:
- rendas comprovadas;
- despesas comprovadas;
- decisões/acordos já vigentes;
- ativos líquidos juridicamente disponíveis.

### Cenário A
Inclui premissas marcadas `CENARIO_A`.

### Cenário B
Inclui premissas marcadas `CENARIO_B`.

### Variáveis controvertidas
Não entram silenciosamente. Devem:
- ficar fora do cenário confirmado;
- aparecer como campo separado;
- ser testadas apenas em cenário explícito.

## 6. Eventos de transição

Custos pontuais devem ser lançados por janela:
- 0–30 dias;
- 31–90 dias;
- 91–365 dias.

Exemplos:
- mudança;
- caução;
- mobília mínima;
- honorários contratualmente conhecidos;
- custas/perícias efetivamente estimadas;
- matrícula/transferência escolar;
- despesas extraordinárias de transporte.

## 7. Regras contra erros

1. Alimentos apenas pedidos não entram no cenário confirmado.
2. Bem litigioso não entra como caixa.
3. Venda de ativo entra como evento não recorrente, líquida de passivos/custos conhecidos.
4. Resgate de aplicação reduz patrimônio e aumenta caixa; não é renda.
5. Em visão consolidada, transferências entre A e B se anulam.
6. Despesa de filho lançada diretamente por um genitor não pode ser novamente integralmente registrada como transferência.
7. Financiamento não pode ser simultaneamente contado como prestação e novamente como despesa integral do bem.
8. Custos anuais devem ser normalizados apenas para análise; no caixa real, usar a data de pagamento.

## 8. Teste reproduzível

Fixture:
- caixa inicial: R$ 12.000;
- entradas recorrentes: R$ 8.000/mês;
- saídas-base: R$ 6.000/mês;
- cenário A: transferência/obrigação de R$ 1.000/mês;
- cenário B: transferência/obrigação de R$ 1.500/mês;
- custos pontuais: R$ 4.000 até 30 dias, mais R$ 2.000 até 90 dias, mais R$ 6.000 entre 91 e 365 dias.

Resultados:

| Métrica | Cenário A | Cenário B |
|---|---:|---:|
| Saídas recorrentes/mês | R$ 7.000 | R$ 7.500 |
| Saldo operacional/mês | R$ 1.000 | R$ 500 |
| Caixa em 30 dias | R$ 9.000 | R$ 8.500 |
| Caixa em 90 dias | R$ 9.000 | R$ 7.500 |
| Caixa em 365 dias | R$ 12.000 | R$ 6.000 |

O teste mostra que uma diferença mensal relativamente pequena pode produzir diferença relevante em 12 meses, razão pela qual hipóteses jurídicas devem permanecer visíveis.

## 9. Limites

O modelo não incorpora automaticamente:
- inflação;
- rendimento dos ativos;
- juros de dívida;
- tributação;
- eventos estocásticos;
- datas exatas de fluxo.

Esses fatores devem ser adicionados somente quando relevantes e documentados.

## 10. Gate

Gate satisfeito:
- fórmulas de fluxo definidas;
- cenários confirmado/A/B separados;
- horizontes 30/90/365 definidos;
- eventos pontuais estruturados;
- controles contra dupla contagem persistidos;
- teste numérico reproduzível validado.
