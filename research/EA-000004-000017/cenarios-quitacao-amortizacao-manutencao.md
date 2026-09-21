# Fase 03/06 — Cenários de quitação, amortização e manutenção

**Estratégia:** EA-000004-000017 — Dívidas, crédito e prioridade de uso do capital indenizatório  
**Data:** 21/09/2026  
**Estado:** CONCLUÍDA

## 1. Objetivo

Comparar, dívida por dívida, quatro alternativas possíveis sem assumir que uma delas é universalmente superior:

1. manter o contrato;
2. quitar totalmente;
3. amortizar parcialmente;
4. renegociar ou portar.

## 2. Regra de comparabilidade

Todo cenário deve usar a mesma data-base e registrar:

- desembolso imediato;
- saldo ou fluxo futuro;
- parcela após a decisão;
- prazo restante;
- CET ou custo equivalente;
- garantias preservadas ou liberadas;
- efeito no caixa;
- efeito no risco;
- custos de transação;
- validade da simulação.

Não comparar uma simulação de hoje com saldo contratual de outra data.

## 3. Cenário A — manutenção

Perguntas:

- a dívida está em dia?
- o CET é conhecido?
- o custo é fixo ou variável?
- a parcela cabe no fluxo?
- a manutenção preserva liquidez necessária?
- existe garantia relevante?
- há benefício econômico real em manter a dívida?

Saídas:

```text
DESEMBOLSO_IMEDIATO = 0
CAPITAL_INDENIZATORIO_PRESERVADO = R$ 100.000,00, antes de outras destinações
PARCELA_FUTURA = P_i
PRAZO = N_i
CUSTO_REMANESCENTE = conforme contrato
```

## 4. Cenário B — quitação total

Usar o saldo específico `SQ_i` na data-base.

```text
CAPITAL_APOS_QUITACAO_i = 100.000 - SQ_i
ALIVIO_MENSAL_i = P_i
```

Esse cálculo mostra apenas o efeito bruto sobre o capital extraordinário. Não significa que todo o saldo remanescente esteja livre para investir, porque reserva e despesas previsíveis continuam não dimensionadas.

Verificar:

- desconto proporcional de juros e acréscimos;
- liberação de garantia, quando aplicável;
- extinção de coobrigação;
- custos ou procedimentos operacionais;
- prazo para baixa de registros;
- eventual impacto em outros contratos vinculados.

## 5. Cenário C — amortização parcial

Exigir simulações concretas do credor, porque o efeito pode variar conforme o contrato:

- reduzir prazo;
- reduzir parcela;
- alterar ambos;
- exigir valor mínimo;
- manter ou modificar condições acessórias.

Métricas:

```text
APORTE_PARCIAL = A_i
NOVA_PARCELA = P2_i
NOVO_PRAZO = N2_i
ALIVIO_MENSAL = P_i - P2_i
CAPITAL_RESTANTE = 100.000 - A_i
```

Nunca supor que reduzir prazo e reduzir parcela produzem o mesmo resultado econômico.

## 6. Cenário D — renegociação ou portabilidade

Comparar o contrato atual e a proposta nova por:

- CET;
- saldo refinanciado;
- prazo;
- parcela;
- custo total;
- garantias;
- seguros e tarifas;
- carência;
- indexadores;
- custo de encerramento ou transferência;
- risco de alongar excessivamente o endividamento.

Uma parcela menor pode decorrer apenas de prazo maior e não representar redução de custo total.

## 7. Matriz comparativa por dívida

| Critério | Manter | Quitar | Amortizar | Renegociar/portar |
|---|---|---|---|---|
| desembolso imediato | baixo/zero | alto | intermediário | variável |
| liquidez preservada | maior | menor | intermediária | variável |
| parcela futura | mantida | zero | reduzida ou prazo menor | conforme proposta |
| custo financeiro futuro | mantido | eliminado após quitação | reduzido conforme simulação | pode cair ou subir |
| garantia | permanece | tende a ser liberada conforme contrato | permanece até quitação | pode mudar |
| complexidade | baixa | baixa/média | média | média/alta |

A tabela é estrutural. A escolha depende dos dados de cada obrigação.

## 8. Condições que impedem conclusão automática

Não escolher cenário definitivo quando:

- dívida não foi confirmada;
- saldo de quitação está desatualizado;
- CET está ausente em operação em que deveria ser comparado;
- taxa é variável e não foi modelada;
- há contestação;
- garantia ou efeito jurídico não foi compreendido;
- reserva mínima ainda não foi dimensionada;
- proposta de renegociação não apresenta custo total comparável.

## 9. Estado do cenário hipotético

Como nenhuma dívida concreta foi informada:

```text
CENARIO_A_MANUTENCAO = METODOLOGIA PRONTA; VALOR NÃO CALCULÁVEL
CENARIO_B_QUITACAO = METODOLOGIA PRONTA; VALOR NÃO CALCULÁVEL
CENARIO_C_AMORTIZACAO = METODOLOGIA PRONTA; VALOR NÃO CALCULÁVEL
CENARIO_D_RENEGOCIACAO = METODOLOGIA PRONTA; VALOR NÃO CALCULÁVEL
```

## 10. Gate da Fase 03

**SATISFEITO.**

Foram documentados quatro cenários reproduzíveis, suas métricas, condições de comparabilidade e travas contra conclusões sem dados.

## 11. Próxima fase

**Fase 04/06 — Prioridade entre reserva, dívida e investimento.**
