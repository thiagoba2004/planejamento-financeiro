# Fase 05/06 — Casos e competências CFP®

**Estratégia:** EA-000004-000017 — Dívidas, crédito e prioridade de uso do capital indenizatório  
**Data:** 21/09/2026  
**Estado:** CONCLUÍDA

## 1. Objetivo

Treinar julgamento profissional sobre dívida, custo efetivo, liquidez, garantias e prioridade de uso de um capital extraordinário de **R$ 100.000,00 líquidos e integralmente disponíveis**.

Os valores abaixo são premissas didáticas de cada caso. **Não são fatos do cenário-base**, no qual existência, saldo, CET, parcelas e garantias continuam como `DADO_AUSENTE`.

## Caso 1 — Rotativo de cartão com custo muito elevado

Premissas didáticas:

- capital extraordinário: R$ 100.000,00;
- saldo para quitação do rotativo: R$ 12.000,00;
- CET anual informado no contrato/fatura: 350%;
- reserva e despesas previsíveis já separadas: R$ 50.000,00;
- capital potencialmente decisório antes da dívida: R$ 50.000,00.

```text
CAPITAL_APOS_QUITACAO = 100.000 - 12.000 = R$ 88.000,00
CAPITAL_DECISORIO_REMANESCENTE = 50.000 - 12.000 = R$ 38.000,00
```

**Diagnóstico:** o custo contratual é muito elevado e a quitação não consome a reserva definida no caso.

**Decisão profissional:** obter saldo atualizado de quitação e documentação antes de executar; com esses dados confirmados, a redução do passivo tende a merecer prioridade sobre a busca de retorno incerto para a mesma parcela do capital.

**Competência CFP®:** comparar custo certo evitado com retorno alternativo compatível, sem usar rentabilidade bruta como contraponto.

**Erro a evitar:** investir os R$ 100.000,00 e manter simultaneamente dívida de custo muito elevado apenas porque o capital está líquido.

## Caso 2 — Consignado com custo moderado e fluxo relevante

Premissas didáticas:

- saldo para quitação: R$ 30.000,00;
- CET: 24% a.a.;
- parcela: R$ 950,00;
- renda líquida mensal: R$ 8.000,00;
- reserva adequada já existente fora da indenização.

```text
COMPROMETIMENTO_DA_PARCELA = 950 / 8.000 = 11,875%
CAPITAL_APOS_QUITACAO = 100.000 - 30.000 = R$ 70.000,00
ALIVIO_MENSAL_APOS_QUITACAO = R$ 950,00
```

**Diagnóstico:** a decisão não depende apenas do CET. O alívio de fluxo de R$ 950,00 por mês pode ser relevante para objetivos e capacidade de poupança.

**Decisão profissional:** comparar manutenção, quitação e amortização parcial usando saldo de quitação, prazo remanescente, custo efetivo, liquidez necessária e destino do fluxo liberado.

**Competência CFP®:** integrar balanço patrimonial e fluxo de caixa.

**Erro a evitar:** tratar dívida mais barata que o rotativo como automaticamente irrelevante.

## Caso 3 — Financiamento relativamente barato, mas liquidez ainda incompleta

Premissas didáticas:

- saldo para quitação: R$ 55.000,00;
- CET: 9% a.a.;
- parcela mensal: R$ 1.800,00;
- lacuna de reserva de segurança: R$ 30.000,00;
- despesas previsíveis dos próximos 12 meses: R$ 20.000,00.

```text
CAPITAL_APOS_RESERVA_E_PREVISTOS = 100.000 - 30.000 - 20.000
= R$ 50.000,00

SALDO_PARA_QUITACAO = R$ 55.000,00
```

**Diagnóstico:** quitar integralmente exigiria mais do que o capital que sobra depois das funções de liquidez definidas no próprio caso.

**Decisão profissional:** não sacrificar reserva e compromissos previsíveis apenas para eliminar uma dívida de custo relativamente baixo; estudar manutenção ou amortização compatível com a liquidez.

**Competência CFP®:** preservar continuidade financeira antes de perseguir redução patrimonial de passivos.

**Erro a evitar:** concluir que “toda dívida deve ser quitada” sempre que surge capital extraordinário.

## Caso 4 — Dívida garantida por bem essencial e atraso confirmado

Premissas didáticas:

- saldo para quitação: R$ 70.000,00;
- duas parcelas vencidas;
- garantia vinculada a bem essencial;
- renda líquida atual reduzida;
- custo e efeitos do atraso confirmados documentalmente;
- reserva mínima ainda precisa ser preservada.

**Diagnóstico:** além do CET, há risco patrimonial e operacional associado ao atraso e à garantia.

**Decisão profissional:** priorizar a regularização do risco, pedir simulações de quitação/amortização/renegociação e preservar o caixa mínimo necessário. A análise financeira não substitui orientação jurídica quando houver dúvida sobre cobrança, garantia, execução ou contestação.

**Competência CFP®:** reconhecer quando risco de perda patrimonial e risco de fluxo alteram a ordem da decisão.

**Erro a evitar:** comparar apenas “rentabilidade do investimento versus taxa da dívida” e ignorar atraso e garantia.

## Caso 5 — Renegociação com parcela menor e custo total maior

Contrato atual, premissas didáticas:

- saldo para quitação: R$ 25.000,00;
- 18 parcelas de R$ 1.700,00;
- soma nominal das parcelas restantes: R$ 30.600,00.

Proposta nova:

- 36 parcelas de R$ 1.050,00;
- soma nominal: R$ 37.800,00;
- CET deve ser obtido antes da decisão.

```text
REDUCAO_MENSAL_DA_PARCELA = 1.700 - 1.050 = R$ 650,00
AUMENTO_NOMINAL_DOS_FLUXOS = 37.800 - 30.600 = R$ 7.200,00
```

**Diagnóstico:** a parcela cai, mas o prazo dobra e a soma nominal sobe. O cálculo definitivo exige CET, datas dos fluxos, tarifas, seguros e demais condições.

**Decisão profissional:** não aprovar renegociação com base somente na parcela.

**Competência CFP®:** comparar custo efetivo, prazo, fluxo e custo total em bases equivalentes.

**Erro a evitar:** confundir “parcela que cabe” com “operação financeiramente melhor”.

## Caso 6 — Inventário confirma ausência de dívidas

Premissas didáticas:

- SCR, contratos, faturas, obrigações privadas e demais fontes foram conciliados;
- nenhuma dívida ou obrigação financeira relevante foi confirmada;
- não existem passivos contestados pendentes de reconciliação.

**Diagnóstico:** a estratégia é **não aplicável no caso concreto** quanto à redução de dívida.

**Decisão profissional:** não criar “dívida-alvo” para justificar uso do capital. O capital segue para investimentos, objetivos, proteção e governança comportamental conforme as estratégias seguintes.

**Competência CFP®:** saber encerrar corretamente uma trilha condicional quando o fato gerador não existe.

**Erro a evitar:** transformar uma estratégia prevista no plano em obrigação de encontrar um problema.

## 2. Competências integradas

### SABER
- diferença entre saldo devedor e saldo para quitação;
- função do CET e seus limites de comparabilidade;
- diferença entre custo contratual, risco de inadimplência e exposição por garantia;
- efeitos distintos de quitar, amortizar, manter e renegociar;
- relação entre dívida, reserva e custo de oportunidade.

### FAZER
- inventariar obrigações e reconciliar fontes;
- calcular comprometimento de renda e alívio de fluxo;
- comparar cenários na mesma data-base;
- calcular impacto da quitação sobre liquidez;
- reconhecer quando o retorno alternativo não é comparável;
- documentar `DADO_AUSENTE` sem convertê-lo em zero.

### DECIDIR
- quando a liquidez deve preceder a quitação;
- quando custo e risco justificam análise prioritária de redução do passivo;
- quando amortização pode ser preferível à quitação;
- quando uma renegociação apenas desloca custo no tempo;
- quando a estratégia deve ser encerrada por não aplicabilidade;
- quando encaminhar questões jurídicas, tributárias ou contratuais fora do escopo financeiro.

## 3. Avaliação de domínio

O profissional demonstra domínio quando consegue:

1. obter e usar o saldo de quitação correto;
2. explicar por que CET e parcela respondem perguntas diferentes;
3. comparar cenários sem misturar datas-base;
4. preservar reserva e despesas previsíveis antes de usar o capital;
5. incorporar garantia, atraso e coobrigação sem produzir parecer jurídico;
6. explicar por que parcela menor pode custar mais;
7. reconhecer ausência comprovada de dívida como resultado válido.

## 4. Comunicação profissional

> “Antes de usar a indenização para pagar uma dívida, precisamos confirmar qual obrigação existe, quanto custa quitá-la hoje, qual é o CET, que risco ela traz ao fluxo e ao patrimônio e quanto do capital precisa permanecer líquido. Só então comparamos manter, quitar, amortizar ou renegociar.”

Evitar:

- “Recebeu R$ 100 mil? Quite tudo.”
- “Se a parcela cabe, mantenha.”
- “Se o investimento rende mais que a taxa nominal, não quite.”
- “Parcela menor é sempre melhor.”
- “Não apareceu dívida no cenário, então o saldo é zero.”

## 5. Gate da Fase 05

**SATISFEITO.**

Foram produzidos seis casos progressivos, incluindo rotativo, consignado, financiamento relativamente barato, dívida garantida, renegociação e não aplicabilidade; cálculos reproduzíveis, competências SABER/FAZER/DECIDIR, avaliação de domínio e comunicação profissional.

## 6. Próxima fase

**Fase 06/06 — Publicação, auditoria e atualização.**
