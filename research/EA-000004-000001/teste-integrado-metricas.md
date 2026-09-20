# Teste integrado de métricas — EA-000004-000001

**Projeto:** PRJ-000004 — Planejamento Financeiro  
**Estratégia:** EA-000004-000001 — Compreender o fenômeno do Superendividamento das Pessoas Físicas  
**Fase:** 04/08 — Diagnóstico e métricas  
**Natureza:** caso didático fictício  
**Data:** 20/09/2026

## 1. Objetivo

Testar se o dicionário de métricas:
- calcula corretamente;
- não transforma um único índice em diagnóstico;
- distingue solvência de liquidez;
- trata divisor zero;
- preserva dados ausentes;
- mantém métricas financeiras separadas da conclusão jurídica.

## 2. Caso fictício A — patrimônio forte, liquidez apertada

### Dados

| Variável | Valor |
|---|---:|
| Ativos totais | R$ 1.000.000 |
| Passivos totais | R$ 300.000 |
| Ativos de curto prazo | R$ 30.000 |
| Passivos de curto prazo | R$ 60.000 |
| Realizável de longo prazo | R$ 70.000 |
| Ativos financeiros | R$ 100.000 |
| Ativos investidos | R$ 450.000 |
| Renda líquida mensal | R$ 15.000 |
| Despesas mensais totais, excluído serviço da dívida | R$ 8.000 |
| Despesas essenciais mensais | R$ 7.000 |
| Serviço mensal da dívida | R$ 6.000 |
| Renda passiva mensal | R$ 1.500 |
| Resultado mensal disponível para investir | R$ 1.000 |

## 3. Cálculos

### M01 — Patrimônio líquido

```text
1.000.000 - 300.000 = 700.000
```

**Resultado:** R$ 700.000.

### M04 — Dívida sobre patrimônio líquido

```text
300.000 / 700.000 = 0,428571
```

**Resultado:** aproximadamente 42,86%.

### M05 — Liquidez corrente

```text
30.000 / 60.000 = 0,50
```

**Resultado:** 0,50.

### M07 — Ativos financeiros sobre total de ativos

```text
100.000 / 1.000.000 = 0,10
```

**Resultado:** 10%.

### M08A — Participação de renda passiva

```text
1.500 / 15.000 = 0,10
```

**Resultado:** 10%.

### M10 — Solvência

```text
1.000.000 / 300.000 = 3,333333
```

**Resultado:** aproximadamente 3,33.

### C01 — Cobertura de despesas essenciais por ativos líquidos

```text
30.000 / 7.000 = 4,285714
```

**Resultado:** aproximadamente 4,29 meses.

### C02 — Serviço da dívida sobre renda

```text
6.000 / 15.000 = 0,40
```

**Resultado:** 40%.

### C04 — Fluxo livre após essenciais e dívida

```text
15.000 - 7.000 - 6.000 = 2.000
```

**Resultado:** R$ 2.000.

### M03 — Índice de poupança

```text
1.000 / 15.000 = 0,066667
```

**Resultado:** aproximadamente 6,67%.

## 4. Interpretação profissional

O caso mostra por que métricas isoladas são perigosas:

- solvência de aproximadamente 3,33 sugere patrimônio total amplamente superior aos passivos;
- liquidez corrente de 0,50 mostra que os ativos de curto prazo não cobrem integralmente os passivos de curto prazo;
- serviço da dívida de 40% da renda produz pressão relevante no fluxo mensal;
- cobertura de cerca de 4,29 meses fornece algum amortecedor de ativos líquidos, mas não resolve por si a concentração das obrigações;
- patrimônio líquido positivo e elevado não impede uma crise de caixa.

**Conclusão correta:** o cliente fictício pode ser patrimonialmente solvente e, ao mesmo tempo, financeiramente pressionado no curto prazo.

**Conclusão proibida:** “não está superendividado porque tem patrimônio” ou “está superendividado porque o serviço da dívida é 40%”. Ambas exigiriam análise mais ampla e, no segundo caso, eventual análise jurídica própria.

## 5. Caso-limite B — patrimônio líquido igual a zero

```text
ATIVOS_TOTAIS = 300.000
PASSIVOS_TOTAIS = 300.000
PATRIMONIO_LIQUIDO = 0
```

Para `DIVIDA_SOBRE_PL = PASSIVOS / PL`:

**Estado esperado:** `NAO_INTERPRETAVEL_DIVISOR_ZERO`.

É proibido gerar infinito e tratá-lo como índice financeiro ordinário.

## 6. Caso-limite C — ausência de passivo de curto prazo

```text
PASSIVOS_CP = 0
```

Para liquidez corrente:

**Estado esperado:** `SEM_PASSIVO_CP`.

A ferramenta pode indicar que não existe obrigação corrente no denominador; não deve exibir infinito silenciosamente.

## 7. Caso-limite D — renda igual a zero

Se `RENDA_LIQUIDA = 0`:
- serviço da dívida/renda → `NAO_INTERPRETAVEL_DIVISOR_ZERO`;
- índice de poupança → `NAO_INTERPRETAVEL_DIVISOR_ZERO`;
- dívida/renda anual → `NAO_INTERPRETAVEL_DIVISOR_ZERO`.

O diagnóstico deve então se apoiar em valores absolutos, fontes alternativas de recursos e análise de fluxo/patrimônio, sem fabricar percentuais.

## 8. Caso-limite E — dado ausente

Se o saldo total de uma dívida não for fornecido:

```text
SALDO_TOTAL = NAO_INFORMADO
```

O cálculo dependente deve permanecer:
```text
RESULTADO = NAO_CALCULAVEL_DADO_AUSENTE
```

Nunca converter dado ausente em zero.

## 9. Caso-limite F — dado declarado não comprovado

Um valor informado verbalmente pelo cliente pode integrar cenário preliminar, mas deve carregar:

```text
status = DECLARADO_NAO_COMPROVADO
```

O relatório deve indicar que o resultado mudará se o documento confirmar valor diferente.

## 10. Testes

| Teste | Resultado |
|---|---|
| Fórmulas reproduzíveis | PASSA |
| Solvência x liquidez não confundidas | PASSA |
| Serviço da dívida não vira corte jurídico | PASSA |
| Divisor zero tratado explicitamente | PASSA |
| Dado ausente não vira zero | PASSA |
| Dado não comprovado preserva estado | PASSA |
| Métricas financeiras separadas do conceito jurídico | PASSA |
| Interpretação multivariada | PASSA |

## 11. Gate da Fase 04

**SATISFEITO.**

O dicionário, o template tabular e este teste integrado demonstram cálculo reproduzível, tratamento de exceções e interpretação contextual. A Estratégia pode avançar à Fase 05 — Prevenção, intervenção e recuperação.
