# Fase 02/06 — Custo efetivo e risco financeiro

**Estratégia:** EA-000004-000017 — Dívidas, crédito e prioridade de uso do capital indenizatório  
**Data:** 21/09/2026  
**Estado:** CONCLUÍDA

## 1. Objetivo

Transformar o inventário da Fase 01 em métricas reproduzíveis de custo, comprometimento do fluxo, risco de inadimplência e custo de oportunidade, sem fabricar valores quando faltarem dados.

## 2. Âncora normativa para o CET

A Resolução CMN nº 4.881/2020 define o **Custo Efetivo Total (CET)** como taxa que consolida encargos e despesas da operação. Seu cálculo considera, conforme o contrato, amortizações, juros, tarifas, tributos, seguros e outras despesas vinculadas. A norma também exige apresentação do CET antes da contratação e demonstrativo de cálculo no contrato. Fonte: **PF-SRC-000072**.

Consequência metodológica: comparar dívidas apenas pela taxa nominal pode ocultar custos relevantes. Sempre que houver CET válido e comparável, ele é a métrica-base do custo contratual.

## 3. Métricas por dívida

Para cada obrigação `i`:

```text
SD_i  = saldo devedor informado
SQ_i  = saldo para quitação na data-base
P_i   = parcela mensal atual
N_i   = número de parcelas remanescentes
CET_i = custo efetivo total anual, quando aplicável
```

Não substituir `SQ_i` por `SD_i` quando a decisão analisada for liquidação antecipada. O valor relevante é o efetivamente exigido para quitar na data escolhida.

### 3.1 Comprometimento de renda

```text
COMPROMETIMENTO_MENSAL = soma(P_i) / RENDA_LIQUIDA_MENSAL
```

No cenário atual:

```text
RENDA_LIQUIDA_MENSAL = DADO_AUSENTE
COMPROMETIMENTO_MENSAL = NÃO CALCULÁVEL
```

Não criar um percentual substituto.

### 3.2 Economia nominal potencial na liquidação

Quando os fluxos remanescentes forem fixos e conhecidos:

```text
ECONOMIA_NOMINAL_APARENTE =
SOMA_DOS_FLUXOS_FUTUROS_CONTRATADOS - SALDO_PARA_QUITACAO
```

Essa diferença não é, sozinha, taxa de retorno e não deve ser usada sem considerar datas, indexadores, seguros, tarifas, efeitos tributários e demais condições contratuais.

### 3.3 Alívio de fluxo

```text
ALIVIO_MENSAL = PARCELA_ANTES - PARCELA_DEPOIS
```

Para quitação total, a parcela futura da obrigação pode ir a zero. Para amortização parcial ou renegociação, é obrigatório usar a simulação real do credor.

## 4. Liquidação antecipada

O Banco Central informa que empréstimos, financiamentos e outras operações de crédito elegíveis podem ser liquidados antecipadamente, total ou parcialmente, com redução proporcional de juros e demais acréscimos conforme as regras aplicáveis; quando solicitado, a instituição deve fornecer contrato e planilha demonstrando a evolução da dívida e o saldo para quitação. Fonte: **PF-SRC-000073**.

Logo, antes de calcular a vantagem de quitar:

1. obter saldo de quitação com data-base;
2. obter demonstrativo da evolução da dívida;
3. conferir se o fluxo é fixo ou indexado;
4. separar desconto econômico real de mera antecipação de principal;
5. registrar validade temporal da proposta.

## 5. Matriz de risco financeiro

Não criar um “score” sintético sem calibração. Avaliar dimensões separadas:

| Dimensão | Pergunta | Estado atual |
|---|---|---|
| adimplência | há atraso ou risco imediato de atraso? | DADO_AUSENTE |
| custo contratual | qual o CET e os encargos efetivos? | DADO_AUSENTE |
| fluxo de caixa | quanto da renda mensal está comprometida? | NÃO CALCULÁVEL |
| garantia | há bem ou direito relevante exposto? | DADO_AUSENTE |
| coobrigação | terceiros ou patrimônio alheio estão envolvidos? | DADO_AUSENTE |
| variabilidade | há indexador/taxa que pode alterar o custo? | DADO_AUSENTE |
| liquidez | quanto do capital de R$ 100 mil seria consumido? | depende de SQ_i |
| contestação | a obrigação ou o valor são reconhecidos? | DADO_AUSENTE |

## 6. Custo de oportunidade

A comparação correta não é:

> “CET da dívida” versus “rentabilidade bruta anunciada de um investimento”.

A comparação precisa aproximar bases equivalentes:

- mesmo horizonte;
- mesma moeda;
- rentabilidade líquida de tributos e custos;
- liquidez compatível;
- risco considerado;
- garantia e volatilidade consideradas;
- custo certo evitado pela quitação versus retorno incerto da alternativa.

Regra:

```text
RETORNO_ALTERNATIVO_COMPARAVEL =
retorno esperado líquido, ajustado ao risco, horizonte e liquidez
```

Se esse retorno não puder ser estimado com base confiável, registrar `NÃO COMPARÁVEL` em vez de inventar taxa.

## 7. Relação com a reserva de segurança

A Fase 02 não autoriza usar os R$ 100.000,00 integralmente para dívida. A estratégia anterior deixou como dados ausentes:

- renda líquida;
- despesas essenciais;
- reserva prévia;
- risco de renda;
- necessidades previsíveis.

Portanto:

```text
CAPITAL_DISPONIVEL_PARA_REDUCAO_DE_DIVIDA
= NÃO CALCULÁVEL AINDA
```

até que a reserva e as necessidades imediatas sejam dimensionadas.

## 8. Saída reproduzível

Para cada dívida futura, a ficha mínima de análise passa a exigir:

```text
SD
SQ
CET
PARCELA
N_PARCELAS
STATUS
ATRASO
GARANTIA
COOBRIGACAO
INDEXADOR
ALIVIO_DE_FLUXO
COMPROMETIMENTO_DE_RENDA
ECONOMIA_NOMINAL_APARENTE
CUSTO_DE_OPORTUNIDADE_COMPARAVEL
```

## 9. Gate da Fase 02

**SATISFEITO.**

Foram persistidos:

- métricas mínimas;
- fórmulas reproduzíveis;
- distinção entre saldo devedor e saldo de quitação;
- regra de comprometimento de renda;
- dimensões de risco sem score arbitrário;
- metodologia de custo de oportunidade em bases comparáveis;
- documentação necessária à liquidação antecipada.

Os valores concretos permanecem `DADO_AUSENTE` ou `NÃO CALCULÁVEL` quando dependem de informações não fornecidas.

## 10. Próxima fase

**Fase 03/06 — Cenários de quitação, amortização e manutenção.**
