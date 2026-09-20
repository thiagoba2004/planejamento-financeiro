# Dicionário de métricas — Gestão Financeira e Superendividamento

**Projeto:** PRJ-000004 — Planejamento Financeiro  
**Estratégia:** EA-000004-000001 — Compreender o fenômeno do Superendividamento das Pessoas Físicas  
**Fase:** 04/08 — Diagnóstico e métricas  
**Data:** 20/09/2026  
**Estado:** VERSÃO 1 — REPRODUZÍVEL

## 1. Regra de evidência para fórmulas

Cada métrica possui um `formula_status`:

- `OFICIAL_VIGENTE_DIRETO` — fórmula lida diretamente no material vigente;
- `OFICIAL_HISTORICA_CORROBORADA` — fórmula verificada em material oficial histórico e coerente com o tópico vigente;
- `GRAU_B_ATUAL` — nomenclatura/tópico vigente confirmado e fórmula materialmente corroborada em material atual não canônico;
- `PROJETO_OPERACIONAL` — fórmula adotada pelo projeto para diagnóstico prático, sem afirmar que é a fórmula oficial da prova;
- `PENDENTE_FORMULA_OFICIAL` — nome vigente confirmado, fórmula oficial atual ainda não extraída.

A interpretação profissional nunca deve exceder o grau de evidência da fórmula.

## 2. Métricas centrais do Módulo II

### M01 — Patrimônio líquido pessoal

```text
PL = ATIVOS_TOTAIS - PASSIVOS_TOTAIS
```

**Unidade:** moeda.  
**Uso:** fotografia patrimonial líquida.  
**Interpretação:** PL positivo não garante liquidez; PL negativo indica passivos superiores aos ativos.  
**Não prova:** capacidade mensal de pagamento.  
**formula_status:** definição matemática/contábil básica compatível com o programa vigente.

### M02 — Liquidez geral / capacidade patrimonial realizável

O programa vigente lista `Liquidez` separadamente de `Liquidez corrente`. Para o diagnóstico do Projeto:

```text
LIQUIDEZ_GERAL_OPERACIONAL =
(ATIVOS_CURTO_PRAZO + REALIZAVEL_LONGO_PRAZO) / PASSIVOS_TOTAIS
```

**Unidade:** razão.  
**Uso:** visão ampla de ativos realizáveis versus obrigações.  
**Não prova:** caixa imediato, nem superendividamento jurídico.  
**formula_status:** `GRAU_B_ATUAL`.

### M03 — Índice de poupança

```text
INDICE_POUPANCA =
RESULTADO_DISPONIVEL_PARA_INVESTIR / RECEITAS
```

No diagnóstico mensal:
```text
RESULTADO_DISPONIVEL =
RECEITA_LIQUIDA - DESPESAS_TOTAIS
```

**Unidade:** percentual/razão.  
**Uso:** capacidade de gerar excedente.  
**Não prova:** existência de reserva já acumulada.  
**formula_status:** `OFICIAL_HISTORICA_CORROBORADA` — fórmula consta em lista oficial histórica da Planejar; tópico continua no programa vigente.

### M04 — Dívida sobre patrimônio líquido

```text
DIVIDA_SOBRE_PL =
PASSIVOS_TOTAIS / PATRIMONIO_LIQUIDO
```

**Unidade:** razão.  
**Uso:** alavancagem patrimonial e dependência relativa de capital de terceiros.  
**Alerta:** se PL <= 0, a razão perde interpretação convencional; registrar condição separadamente em vez de dividir mecanicamente.  
**formula_status:** `GRAU_B_ATUAL`.

### M05 — Liquidez corrente

```text
LIQUIDEZ_CORRENTE =
ATIVOS_CURTO_PRAZO / PASSIVOS_CURTO_PRAZO
```

**Unidade:** razão.  
**Uso:** capacidade de cobrir obrigações de curto prazo com ativos de curto prazo.  
**Alerta:** passivo de curto prazo igual a zero → reportar `SEM_PASSIVO_CP`, não infinito silencioso.  
**formula_status:** `OFICIAL_HISTORICA_CORROBORADA`.

### M06 — Coeficiente de investimento

```text
COEF_INVESTIMENTO =
ATIVOS_INVESTIDOS / ATIVOS_TOTAIS
```

**Unidade:** percentual/razão.  
**Uso:** parcela do patrimônio direcionada a ativos com finalidade de investimento/geração de retorno.  
**Não confundir:** ativo investido é categoria mais ampla que ativo financeiro.  
**formula_status:** `GRAU_B_ATUAL`.

### M07 — Ativos financeiros sobre total de ativos

```text
ATIVOS_FINANCEIROS_PCT =
ATIVOS_FINANCEIROS / ATIVOS_TOTAIS
```

**Unidade:** percentual/razão.  
**Uso:** composição patrimonial e flexibilidade financeira.  
**Não prova:** liquidez, porque um ativo financeiro pode ter carência/volatilidade.  
**formula_status:** `GRAU_B_ATUAL` pela própria denominação do índice vigente.

### M08 — Renda passiva

O programa vigente lista `Renda passiva`, mas a fórmula oficial atual não foi extraída diretamente. O projeto mantém duas leituras distintas:

```text
PARTICIPACAO_RENDA_PASSIVA =
RENDA_PASSIVA / RENDA_TOTAL
```

```text
COBERTURA_DESPESAS_POR_RENDA_PASSIVA =
RENDA_PASSIVA / DESPESAS_TOTAIS
```

**Uso:** a primeira mede composição da renda; a segunda mede cobertura do padrão de despesas.  
**formula_status:** `PROJETO_OPERACIONAL` até confirmação da convenção oficial do exame.

### M09 — Custo da dívida

Para contrato individual, priorizar **CET** quando disponível.

Para carteira, o projeto pode usar:
```text
CUSTO_DIVIDA_APROX =
ENCARGOS_FINANCEIROS_ANUALIZADOS / SALDO_MEDIO_DA_DIVIDA
```

ou custo efetivo ponderado por saldos, quando as taxas forem comparáveis e a metodologia estiver documentada.

**Unidade:** taxa anualizada.  
**Uso:** comparar custo e priorizar análise de refinanciamento/renegociação.  
**Alerta:** não misturar taxas nominais, efetivas, mensais e anuais.  
**formula_status:** `PROJETO_OPERACIONAL`; nomenclatura `Custo da dívida` é vigente.

### M10 — Solvência

```text
SOLVENCIA =
ATIVOS_TOTAIS / PASSIVOS_TOTAIS
```

**Unidade:** razão.  
**Uso:** verificar capacidade patrimonial hipotética de cobrir todas as obrigações.  
**Alerta:** solvência alta pode coexistir com liquidez baixa.  
**formula_status:** `GRAU_B_ATUAL`.

## 3. Métricas complementares para diagnóstico de superendividamento

### C01 — Cobertura de despesas por ativos líquidos

```text
COBERTURA_MESES =
ATIVOS_LIQUIDOS_CURTO_PRAZO / DESPESAS_MENSAIS_ESSENCIAIS
```

**Unidade:** meses.  
**Uso:** amortecedor de liquidez.  
**formula_status:** conceito histórico consolidado no material CFP® e `PROJETO_OPERACIONAL` para despesas essenciais.

### C02 — Serviço da dívida sobre renda

```text
DEBT_SERVICE_RATIO =
SERVICO_MENSAL_DA_DIVIDA / RENDA_LIQUIDA_MENSAL
```

**Unidade:** percentual.  
**Uso:** pressão mensal da dívida sobre renda.  
**Importante:** no estudo do Banco Central, serviço da dívida > 50% é **um** de quatro critérios do indicador de endividamento de risco; não é corte jurídico nem CFP® universal.

### C03 — Renda disponível após dívida

```text
RENDA_APOS_DIVIDA =
RENDA_LIQUIDA - SERVICO_MENSAL_DA_DIVIDA
```

**Unidade:** moeda.  
**Uso:** capacidade remanescente antes de despesas não incorporadas.  
**Não confundir:** não equivale automaticamente ao mínimo existencial.

### C04 — Fluxo livre após essenciais e dívida

```text
FLUXO_LIVRE =
RENDA_LIQUIDA
- DESPESAS_ESSENCIAIS
- SERVICO_MENSAL_DA_DIVIDA
```

**Unidade:** moeda.  
**Uso:** detectar déficit estrutural.  
**Interpretação:** valor negativo indica necessidade de ajuste/intervenção; não determina sozinho causa ou solução.

### C05 — Dívida sobre renda anual

```text
DIVIDA_RENDA =
SALDO_TOTAL_DIVIDAS / (RENDA_LIQUIDA_MENSAL * 12)
```

**Unidade:** razão/anos de renda.  
**Uso:** comparação de estoque com capacidade de geração de renda.  
**formula_status:** `PROJETO_OPERACIONAL`.

## 4. Indicador do Banco Central — camada analítica separada

O Projeto registra o indicador de `ENDIVIDAMENTO_DE_RISCO_BCB` como instrumento de pesquisa populacional, não como teste do CFP® ou da Lei 14.181/2021.

Quatro sinais do estudo:
1. inadimplência acima de 90 dias;
2. serviço da dívida acima de 50% da renda mensal;
3. exposição simultânea a cheque especial, crédito pessoal sem consignação e crédito rotativo;
4. renda disponível após serviço da dívida abaixo da linha de pobreza usada no estudo.

```text
BCB_RISK_COUNT = soma dos quatro sinais verdadeiros
BCB_ENDIVIDAMENTO_RISCO = BCB_RISK_COUNT >= 2
```

**Proibição:** usar `BCB_RISK_COUNT` para concluir juridicamente “superendividado”.

## 5. Camada jurídica separada

Manter fora do dicionário CFP®:

```text
PARAMETRO_MINIMO_EXISTENCIAL
REQUISITO_BOA_FE
DIVIDAS_ELEGIVEIS
DIVIDAS_EXCLUIDAS
CONCLUSAO_SUPERENDIVIDAMENTO_JURIDICO
```

Esses campos pertencem à análise jurídica e podem dialogar com métricas financeiras sem serem substituídos por elas.

## 6. Dicionário de dados mínimo

Para cada variável registrar:
- nome;
- definição;
- valor;
- unidade;
- data-base;
- período;
- fonte;
- comprovado/declarado;
- bruto/líquido;
- recorrente/variável;
- cenário;
- observação.

## 7. Regras de divisão e dados ausentes

- divisor zero → estado explícito, não erro silencioso;
- dado ausente → `NAO_INFORMADO`;
- valor declarado sem prova → `DECLARADO_NAO_COMPROVADO`;
- saldos divergentes → cenários separados;
- periodicidades diferentes → normalizar antes da divisão;
- não misturar renda bruta com serviço calculado sobre renda líquida sem indicar a escolha.

## 8. Regra de interpretação

Nenhum índice recebe classificação universal `BOM/RUIM` apenas pelo número.

O projeto deve perguntar:
1. qual objetivo da métrica?
2. qual tendência ao longo do tempo?
3. quais outras métricas confirmam ou contradizem o sinal?
4. qual é a estabilidade da renda?
5. qual é a composição familiar?
6. qual é a liquidez real dos ativos?
7. qual é o custo e a estrutura das dívidas?
8. há gatilho transitório ou déficit estrutural?

## 9. Gate

Este dicionário permite cálculo reproduzível. O fechamento da Fase 04 exige ainda um teste integrado de caso fictício, com tratamento de divisores zero, dados ausentes e conflito entre solvência e liquidez.
