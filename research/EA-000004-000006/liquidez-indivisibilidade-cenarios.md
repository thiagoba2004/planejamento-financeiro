# Fase 04/06 — Liquidez, indivisibilidade e cenários de partilha

**Estratégia:** EA-000004-000006 — Patrimônio, avaliação econômica e liquidez na partilha  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Regra

O Planejamento Financeiro compara consequências econômicas de diferentes **cenários de alocação**.

Não decide:
- qual cenário é juridicamente devido;
- qual parte deve receber determinado bem;
- se haverá venda, adjudicação ou condomínio;
- qual percentual de partilha é aplicável.

Percentuais entram apenas quando juridicamente confirmados ou explicitamente marcados como hipótese.

## 2. Cenários econômicos modeláveis

### Venda e conversão em caixa
Avaliar:
- valor líquido de venda;
- tempo para venda;
- custos de conversão;
- necessidade de moradia/substituição do ativo;
- risco de preço.

### Alocação do ativo a uma parte com compensação financeira
Avaliar:
- valor líquido do ativo;
- valor dos demais ativos recebidos;
- compensação necessária no cenário;
- caixa disponível para pagar a compensação;
- eventual necessidade de financiamento;
- efeito do novo endividamento.

### Troca de ativos
Avaliar se combinações de ativos reduzem a necessidade de pagamento compensatório sem destruir liquidez.

### Manutenção temporária da copropriedade econômica
Avaliar:
- custos recorrentes;
- financiamento;
- manutenção;
- receitas do ativo;
- prazo;
- risco de dependência financeira continuada;
- evento de saída.

### Pagamento diferido
Modelar somente como cenário financeiro:
- valor;
- prazo;
- indexação/taxa apenas quando definida;
- risco de crédito;
- impacto no caixa de quem paga e de quem recebe.

## 3. Métricas

### Patrimônio líquido total do cenário

```text
PATRIMONIO_LIQUIDO_CENARIO =
SOMA DOS VALORES LIQUIDOS DOS ITENS ELEGIVEIS NO CENARIO
```

### Valor-alvo de uma parte

Somente quando houver percentual confirmado ou hipótese explícita:

```text
VALOR_ALVO_PARTE =
PATRIMONIO_LIQUIDO_CENARIO × PERCENTUAL_DO_CENARIO
```

### Gap de alocação

```text
GAP =
VALOR_LIQUIDO_DOS_ATIVOS_RECEBIDOS
− VALOR_ALVO_PARTE
```

Gap positivo indica que, **naquele cenário econômico**, a parte recebeu valor acima do alvo modelado; gap negativo, abaixo.

### Compensação econômica teórica

```text
COMPENSACAO_TEORICA =
ABS(GAP)
```

Esse número **não é determinação jurídica**. Serve apenas para testar a estrutura econômica do cenário.

### Liquidez pós-alocação

```text
PERCENTUAL_LIQUIDO =
ATIVOS_LIQUIDOS_RECEBIDOS
÷ PATRIMONIO_LIQUIDO_RECEBIDO
```

### Concentração

```text
CONCENTRACAO_MAIOR_ATIVO =
VALOR_DO_MAIOR_ATIVO
÷ PATRIMONIO_LIQUIDO_RECEBIDO
```

## 4. Indivisibilidade

Um ativo é tratado como economicamente indivisível quando sua fragmentação:
- não é operacionalmente viável;
- reduz materialmente o valor;
- depende de terceiro;
- exige liquidação integral;
- altera a natureza econômica do ativo.

Indivisibilidade econômica não equivale a indivisibilidade jurídica.

## 5. Risco de equalização por dívida

Quando a compensação é maior que o caixa disponível:

```text
NECESSIDADE_DE_FINANCIAMENTO =
MAX(0; COMPENSACAO_TEORICA − CAIXA_DISPONIVEL_PARA_COMPENSAR)
```

O cenário deve então incluir:
- CET/taxa quando conhecida;
- prestação;
- prazo;
- efeito sobre fluxo de caixa;
- risco de concentração patrimonial + dívida.

Não tratar “ficar com o imóvel” como economicamente equivalente a “ficar com caixa” sem examinar essa necessidade.

## 6. Fixture — patrimônio líquido de R$ 498 mil

Itens:
- imóvel: R$ 360 mil líquidos;
- veículo: R$ 58 mil líquidos;
- investimento: R$ 80 mil líquidos.

Para **mera simulação financeira**, usar hipótese de 50%/50%:

```text
VALOR_ALVO_POR_PARTE = 498.000 × 50% = 249.000
```

### Cenário 1 — venda/conversão integral
Após os custos já incorporados aos valores líquidos do fixture:
- A: R$ 249 mil;
- B: R$ 249 mil;
- elevada liquidez após efetiva venda;
- exposição ao prazo e execução da venda.

### Cenário 2 — imóvel para A; veículo + investimento para B
Antes de compensação:
- A: R$ 360 mil;
- B: R$ 138 mil;
- gap de A: +R$ 111 mil;
- gap de B: −R$ 111 mil;
- compensação econômica teórica: R$ 111 mil.

Se A não possuir R$ 111 mil de caixa disponível, o equilíbrio nominal pode exigir venda parcial de outros ativos, pagamento diferido ou dívida — todos como cenários, não como determinação.

### Cenário 3 — manutenção temporária do imóvel
O valor econômico permanece no patrimônio, mas:
- liquidez imediata do imóvel continua baixa;
- custos de manutenção/financiamento continuam existindo;
- a independência financeira entre as partes pode ficar incompleta.

## 7. Comparação neutra

| Aspecto | Venda | Alocação + compensação | Manutenção temporária |
|---|---|---|---|
| liquidez imediata | depende da venda, depois tende a ser alta | assimétrica | baixa |
| custo de conversão | pode existir | pode ser menor se não houver venda | pode ser postergado |
| necessidade de financiamento | menor após venda concluída | pode ser alta | depende dos custos correntes |
| concentração | tende a cair | pode aumentar para quem recebe ativo grande | permanece |
| dependência entre partes | tende a cair | pode persistir se pagamento for diferido | tende a permanecer |
| risco de execução | prazo/preço de venda | crédito/compensação | manutenção/saída futura |

A tabela não escolhe cenário.

## 8. Gate

Gate satisfeito:
- cinco estruturas de cenário modeladas;
- métricas de alvo, gap, compensação, liquidez e concentração definidas;
- indivisibilidade econômica separada da jurídica;
- risco de financiamento de compensação incorporado;
- fixture reproduzível validado;
- comparação apresentada sem recomendação de partilha.
