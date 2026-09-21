# Fase 04/06 — Prioridade entre reserva, dívida e investimento

**Estratégia:** EA-000004-000017 — Dívidas, crédito e prioridade de uso do capital indenizatório  
**Data:** 21/09/2026  
**Estado:** CONCLUÍDA

## 1. Objetivo

Construir uma regra de decisão para ordenar o uso potencial do capital extraordinário entre:

- continuidade operacional;
- reserva de segurança;
- regularização ou redução de dívidas;
- investimento de médio e longo prazo.

A regra não fixa percentuais universais e não presume que toda dívida deva ser quitada.

## 2. Princípio de precedência

O capital de R$ 100.000,00 é líquido e disponível, mas não é automaticamente “capital investível”.

Antes de uma alocação definitiva, separar:

```text
CAPITAL_TOTAL_EXTRAORDINARIO = 100.000
(-) NECESSIDADES_IMEDIATAS
(-) DESPESAS_PREVISIVEIS
(-) LACUNA_DE_RESERVA_DE_SEGURANCA
(=) CAPITAL_POTENCIALMENTE_DECISORIO
```

Como as três deduções ainda dependem de dados ausentes, o valor final não é calculável neste momento.

## 3. Sequência decisória

### Passo 1 — validar a obrigação

Não usar capital para pagar uma dívida apenas porque ela apareceu em um relatório.

Confirmar:
- existência;
- titularidade;
- valor;
- data-base;
- condições contratuais;
- eventual contestação.

Dívida contestada exige reconciliação antes da decisão econômica.

### Passo 2 — proteger continuidade e liquidez mínima

Aplicar a metodologia da EA-000004-000016:

- despesas imediatas;
- compromissos previsíveis;
- reserva de segurança;
- risco de interrupção de renda.

Não converter quitação de dívida em nova vulnerabilidade de caixa.

### Passo 3 — tratar risco de inadimplência e exposição patrimonial

Dar atenção especial, sem criar ranking numérico artificial, a obrigações com:

- atraso confirmado;
- encargos de mora relevantes;
- risco de vencimento antecipado;
- garantia sobre bem essencial;
- coobrigados;
- consequências contratuais ou patrimoniais materiais.

### Passo 4 — comparar custo certo evitado

Para dívida válida e em dia, comparar:

- custo efetivo remanescente;
- saldo de quitação;
- economia econômica da antecipação;
- alívio de fluxo;
- risco e garantia;
- custo de oportunidade em base equivalente.

Uma dívida barata e sustentável pode ter decisão diferente de um crédito rotativo caro, mas nenhum rótulo deve ser atribuído sem CET e demais dados.

### Passo 5 — avaliar amortização ou renegociação

Se a quitação integral consumir liquidez excessiva:

- simular amortização;
- verificar redução de prazo versus parcela;
- solicitar proposta de renegociação/portabilidade;
- comparar CET e custo total, não apenas prestação.

### Passo 6 — liberar investimento apenas sobre o residual

A EA-000004-000018 deve receber apenas capital que não esteja comprometido com:

- continuidade;
- reserva;
- compromissos previsíveis;
- decisões de dívida já justificadas.

## 4. Matriz de prioridade qualitativa

A matriz não é um score; é uma ordem de perguntas.

| Situação | Pergunta dominante | Resposta metodológica |
|---|---|---|
| obrigação não confirmada | a dívida existe e o valor é correto? | validar antes de pagar |
| dívida vencida | qual o custo e a consequência do atraso? | quantificar e regularizar cenário |
| dívida com garantia relevante | o patrimônio essencial está exposto? | incluir risco da garantia |
| dívida cara e líquida | qual custo certo pode ser eliminado? | comparar quitação/amortização |
| dívida de custo moderado e sustentável | preservar liquidez cria valor? | comparar manter versus reduzir |
| capital residual | há objetivo, horizonte e perfil definidos? | encaminhar à EA-000004-000018 |

## 5. Trava contra comparação inadequada

Não decidir assim:

> “se o investimento rende mais que os juros, mantenha a dívida”.

A comparação exige retorno **líquido**, risco, prazo e liquidez equivalentes. O custo contratual evitado pela quitação é diferente de uma rentabilidade futura incerta.

## 6. Trava contra dupla contagem

Uma mesma parcela do capital não pode ser simultaneamente registrada como:

- reserva de segurança;
- valor destinado à quitação;
- investimento;
- gasto discricionário.

Usar:

```text
100.000 =
CAIXA_OPERACIONAL
+ DESPESAS_PREVISIVEIS
+ RESERVA
+ REDUCAO_DE_DIVIDAS
+ INVESTIMENTO
+ OUTROS_USOS_JUSTIFICADOS
+ CAPITAL_AINDA_NAO_ALOCADO
```

A soma deve reconciliar exatamente o capital disponível.

## 7. Limites profissionais

Esta estratégia:

- organiza dados financeiros;
- calcula cenários;
- compara custo e liquidez;
- explicita riscos;
- prepara perguntas para credores e profissionais especializados.

Ela não substitui análise jurídica de dívida contestada, garantia, prescrição ou obrigação judicial, nem aconselhamento tributário quando houver questão fiscal específica.

## 8. Estado atual

```text
RESERVA_ALVO = DADO_AUSENTE
NECESSIDADES_IMEDIATAS = DADO_AUSENTE
DESPESAS_PREVISIVEIS = DADO_AUSENTE
DIVIDAS_CONFIRMADAS = DADO_AUSENTE
CAPITAL_PARA_REDUCAO_DE_DIVIDAS = NÃO CALCULÁVEL
CAPITAL_PARA_INVESTIMENTO = NÃO CALCULÁVEL
```

## 9. Gate da Fase 04

**SATISFEITO.**

Foram persistidos:

- sequência decisória;
- regra de precedência entre liquidez, dívida e investimento;
- tratamento específico de inadimplência, garantia e coobrigação;
- comparação por custo de oportunidade em bases equivalentes;
- trava contra dupla contagem;
- limites profissionais explícitos.

## 10. Próxima fase

**Fase 05/06 — Casos e competências CFP®.**
