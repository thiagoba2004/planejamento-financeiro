# Fase 01/06 — Delimitação do horizonte de transição

**Estratégia:** EA-000004-000016 — Liquidez, reserva de segurança e período de decisão pós-indenização  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Ponto de partida confirmado

O cenário didático recebe da estratégia anterior:

- origem: indenização por dano moral trabalhista;
- capital líquido: **R$ 100.000,00**;
- disponibilidade: integral;
- natureza financeira: capital extraordinário;
- renda recorrente: não;
- destino definitivo: ainda não definido.

A existência de R$ 100.000,00 líquidos não autoriza, por si só, concluir quanto deve ficar em reserva, quanto pode ser investido ou quanto pode ser consumido.

## 2. Objetivo da fase

Criar um período de transição no qual o capital permaneça suficientemente líquido enquanto se esclarecem:

1. necessidades dos próximos 3 meses;
2. necessidades dos próximos 6 meses;
3. necessidades dos próximos 12 meses;
4. risco de redução ou interrupção de renda;
5. reserva de segurança já existente;
6. compromissos previsíveis;
7. decisões que podem ser adiadas sem custo material.

O horizonte de transição não é prazo obrigatório de “espera”. É uma estrutura de diagnóstico.

## 3. Três horizontes operacionais

### 0 a 3 meses — continuidade imediata

Mapear:
- moradia;
- alimentação;
- saúde;
- transporte;
- educação;
- seguros essenciais;
- prestações contratuais;
- tributos e contas já vencendo;
- despesas processuais ou profissionais ainda pendentes;
- qualquer risco concreto de perda de renda.

Pergunta central:

> Quanto de caixa precisa estar disponível sem depender de venda, carência ou oscilação relevante?

### 4 a 6 meses — estabilização

Mapear:
- despesas recorrentes;
- ajuste de orçamento após o evento extraordinário;
- eventual mudança profissional;
- manutenção ou recomposição de reserva;
- despesas previsíveis de semestre;
- dívidas cuja decisão não pode esperar;
- objetivos já assumidos contratualmente.

Pergunta central:

> Que parcela do capital precisa continuar protegendo o fluxo de caixa enquanto o diagnóstico financeiro amadurece?

### 7 a 12 meses — consolidação

Mapear:
- tributos e despesas anuais;
- seguros e matrículas;
- manutenção de bens;
- viagens ou gastos já contratados;
- transições profissionais;
- metas de curto prazo;
- necessidade de preservar capacidade de decisão antes de comprometer capital em longo prazo.

Pergunta central:

> Quais saídas de caixa previsíveis do próximo ano não devem ser confundidas com emergência?

## 4. Separação obrigatória

A estratégia distingue quatro caixas conceituais:

| Caixa | Função | Estado atual |
|---|---|---|
| operacional | pagamentos imediatos e fluxo corrente | DADO_AUSENTE |
| despesas previsíveis | compromissos conhecidos dos próximos 12 meses | DADO_AUSENTE |
| reserva de segurança | choques não previstos e perda de renda | DADO_AUSENTE |
| capital ainda não alocado | valor que pode aguardar diagnóstico | a calcular |

Não usar a reserva de emergência para despesas anuais previsíveis apenas porque ainda não ocorreram.

## 5. Perguntas de diagnóstico

### Renda e estabilidade
1. Qual é a renda líquida mensal recorrente?
2. A renda é fixa, variável ou mista?
3. Quantas pessoas contribuem para a renda familiar?
4. Existe risco concreto de desemprego ou redução de renda nos próximos 12 meses?
5. Há benefícios, comissões ou rendas que podem cessar?
6. Em quanto tempo seria plausível recompor a renda se ela cair?

### Despesas e dependência econômica
7. Qual é a despesa essencial mensal?
8. Qual é a despesa total média mensal?
9. Há dependentes econômicos?
10. Existem gastos médicos recorrentes ou risco de gasto relevante não coberto?
11. Existem despesas educacionais recorrentes?
12. Há prestação de moradia, aluguel ou financiamento?

### Reserva já existente
13. Existe reserva de emergência antes da indenização?
14. Qual seu valor líquido?
15. Onde está aplicada?
16. Qual o prazo real de resgate?
17. Há carência ou risco de perda relevante no resgate?

### Compromissos previsíveis
18. Quais gastos extraordinários já conhecidos ocorrerão em 3 meses?
19. E em 6 meses?
20. E em 12 meses?
21. Há impostos, seguros, matrículas, manutenção ou viagens já contratadas?
22. Há obrigação judicial ou familiar previsível?

### Decisões que podem esperar
23. Existe compra relevante que não é urgente?
24. Existe intenção de emprestar ou doar dinheiro a terceiros?
25. Existe intenção de aplicar em produtos de longo prazo?
26. Existe projeto empresarial ainda não validado?
27. Existe desejo de elevar permanentemente o padrão de vida?
28. Alguma decisão pode ser adiada sem multa, perda contratual ou dano material?

## 6. Regra de não invenção

Enquanto os dados acima não existirem:

- não fixar percentual de reserva;
- não presumir que “6 meses” ou “12 meses” é automaticamente correto;
- não aplicar os R$ 100.000,00 integralmente;
- não presumir que a indenização substitui renda;
- não confundir gasto previsível com emergência;
- não liberar capital para longo prazo apenas porque ele está líquido.

## 7. Saída mínima da fase

A fase cria a seguinte estrutura:

```text
CAPITAL_EXTRAORDINARIO = R$ 100.000,00

HORIZONTE_3M = necessidades imediatas a mapear
HORIZONTE_6M = estabilização a mapear
HORIZONTE_12M = compromissos previsíveis a mapear
RISCO_DE_RENDA = DADO_AUSENTE
RESERVA_PREVIA = DADO_AUSENTE
DESPESA_ESSENCIAL_MENSAL = DADO_AUSENTE
CAPITAL_LIBERAVEL_PARA_LONGO_PRAZO = NÃO CALCULÁVEL AINDA
```

## 8. Competências CFP® mobilizadas

**SABER**
- diferença entre liquidez, reserva, gasto previsível e investimento de longo prazo;
- relação entre estabilidade de renda e necessidade de caixa.

**FAZER**
- decompor necessidades em 3, 6 e 12 meses;
- separar dado confirmado de dado ausente;
- organizar perguntas de diagnóstico.

**DECIDIR**
- reconhecer quando ainda não há base para alocação definitiva;
- preservar opcionalidade sem transformar cautela em paralisação indefinida.

## 9. Gate da Fase 01

**SATISFEITO.**

Persistidos:
- horizontes de 3, 6 e 12 meses;
- quatro caixas conceituais;
- 28 perguntas de diagnóstico;
- fronteiras entre reserva, previsibilidade e capital ainda não alocado;
- regra explícita de não inventar percentuais.

## 10. Próxima fase

**Fase 02/06 — Reserva de segurança e necessidades imediatas.**
