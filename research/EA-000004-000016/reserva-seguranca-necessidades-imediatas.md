# Fase 02/06 — Reserva de segurança e necessidades imediatas

**Estratégia:** EA-000004-000016 — Liquidez, reserva de segurança e período de decisão pós-indenização  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Objetivo

Dimensionar a reserva de segurança por critérios financeiros e distinguir:

- caixa operacional;
- despesas previsíveis;
- reserva de emergência;
- capital que pode permanecer em decisão;
- capital eventualmente disponível para outras estratégias.

## 2. Referência institucional

O Portal do Investidor/CVM registra que a reserva de emergência deve priorizar **baixo risco e alta liquidez**, e apresenta como referência educacional uma faixa de **6 a 12 meses de gastos**, observando que o valor exato depende, entre outros fatores, do tipo e estabilidade da renda e de quantas pessoas contribuem para a renda familiar.

Fonte: **PF-SRC-000065**.

A faixa não é convertida neste projeto em regra universal.

## 3. Variáveis

Definir:

- **E** = despesa essencial mensal;
- **H** = meses de cobertura escolhidos;
- **R0** = reserva líquida já existente antes da indenização;
- **P12** = despesas previsíveis extraordinárias dos próximos 12 meses;
- **I0** = caixa operacional imediato necessário;
- **C** = capital extraordinário líquido = R$ 100.000,00.

### Meta bruta de segurança

```text
RESERVA_ALVO = E × H
```

### Lacuna de reserva

```text
LACUNA_RESERVA = máximo(0 ; RESERVA_ALVO - R0)
```

### Capital ainda não comprometido após necessidades iniciais

```text
CAPITAL_REMANESCENTE =
C - I0 - P12 - LACUNA_RESERVA
```

Se o resultado for negativo, não existe “excedente para investir”: existe necessidade financeira superior ao capital disponível.

## 4. Como escolher H sem automatismo

H deve ser maior quando houver, por exemplo:
- renda variável;
- fonte única de renda;
- maior dificuldade de recolocação profissional;
- muitos dependentes;
- despesas essenciais altas e rígidas;
- risco de saúde sem cobertura suficiente;
- trabalho autônomo ou sazonal;
- baixa rede de apoio;
- grande concentração patrimonial em ativos ilíquidos.

H pode ser menor, dentro de uma decisão tecnicamente justificada, quando houver combinação robusta de:
- renda estável;
- múltiplas fontes independentes de renda;
- alta capacidade recorrente de poupança;
- boa cobertura de seguros;
- baixa rigidez de despesas;
- patrimônio líquido adicional com alta liquidez.

Nenhum fator isolado define H.

## 5. Despesas previsíveis não são emergência

Separar de RESERVA_ALVO:
- IPTU/IPVA;
- matrícula e material escolar;
- seguro anual;
- manutenção programada;
- viagem já contratada;
- parcela já conhecida;
- imposto com vencimento esperado;
- compra planejada com data definida.

Esses itens integram **P12**, não a reserva de emergência.

## 6. Exemplos reproduzíveis

### Exemplo A — apenas demonstração da fórmula

Premissas didáticas:
- E = R$ 5.000,00;
- H = 6 meses;
- R0 = R$ 10.000,00.

```text
RESERVA_ALVO = 5.000 × 6 = R$ 30.000,00
LACUNA_RESERVA = 30.000 - 10.000 = R$ 20.000,00
```

Esse exemplo não significa que o titular hipotético tenha despesa de R$ 5.000,00.

### Exemplo B — cobertura mais longa

Premissas didáticas:
- E = R$ 5.000,00;
- H = 12 meses;
- R0 = R$ 10.000,00.

```text
RESERVA_ALVO = 5.000 × 12 = R$ 60.000,00
LACUNA_RESERVA = 60.000 - 10.000 = R$ 50.000,00
```

O contraste demonstra por que renda, estabilidade e dependentes alteram materialmente a alocação dos R$ 100.000,00.

## 7. Teste de suficiência dos R$ 100.000,00

O capital extraordinário deve passar por esta ordem:

```text
1. CAIXA OPERACIONAL
2. DESPESAS PREVISÍVEIS DE CURTO PRAZO
3. LACUNA DE RESERVA
4. SOMENTE DEPOIS → CAPITAL REMANESCENTE
```

Não existe percentual obrigatório para cada etapa.

## 8. Qualidade mínima da reserva

Uma alternativa usada como reserva deve ser avaliada por:

1. liquidez efetiva;
2. ausência ou baixo nível de carência;
3. baixa volatilidade;
4. risco de crédito;
5. risco operacional;
6. proteção institucional aplicável;
7. tributação;
8. custo;
9. facilidade de acesso em situação adversa;
10. concentração por instituição ou emissor.

Alta rentabilidade não é critério prioritário da reserva.

## 9. Dados ainda ausentes no cenário

Permanecem **DADO_AUSENTE**:
- E;
- H;
- R0;
- P12;
- I0;
- risco de renda;
- número de dependentes;
- patrimônio líquido adicional.

Logo, o valor exato a reservar dentro dos R$ 100.000,00 **não pode ser calculado ainda**.

## 10. Fontes

- **PF-SRC-000065** — Portal do Investidor/CVM, Emergências e aposentadoria;
- **PF-SRC-000044** — Portal do Investidor/CVM, Liquidez;
- materiais canônicos do projeto sobre Gestão Financeira e julgamento profissional, conforme PLANEJAR_SOURCES.md.

## 11. Gate da Fase 02

**SATISFEITO.**

Foram documentados:
- fórmula de reserva;
- lacuna de reserva;
- separação de despesas previsíveis;
- critérios para escolha do horizonte;
- critérios de qualidade da reserva;
- dois exemplos reproduzíveis;
- impossibilidade de fixar valor sem os dados ausentes.

## 12. Próxima fase

**Fase 03/06 — Estacionamento financeiro temporário.**
