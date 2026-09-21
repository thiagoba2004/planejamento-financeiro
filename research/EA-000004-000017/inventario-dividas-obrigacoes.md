# Fase 01/06 — Inventário de dívidas e obrigações

**Estratégia:** EA-000004-000017 — Dívidas, crédito e prioridade de uso do capital indenizatório  
**Data:** 21/09/2026  
**Estado:** CONCLUÍDA

## 1. Ponto de partida confirmado

O cenário didático recebe das estratégias anteriores:

- origem do recurso: indenização por dano moral trabalhista;
- capital líquido extraordinário: **R$ 100.000,00**;
- disponibilidade: integral;
- renda recorrente: não criada pelo recebimento;
- existência de dívidas: **DADO_AUSENTE**;
- saldo devedor total: **DADO_AUSENTE**;
- parcelas mensais: **DADO_AUSENTE**;
- garantias e coobrigações: **DADO_AUSENTE**.

A ausência de informação sobre dívidas não pode ser convertida em saldo zero.

## 2. Objetivo da fase

Criar um inventário auditável que permita identificar, para cada obrigação, pelo menos:

1. credor e modalidade;
2. origem e finalidade;
3. saldo devedor informado;
4. saldo para liquidação antecipada;
5. Custo Efetivo Total (CET), quando aplicável;
6. taxa nominal, indexador e demais encargos relevantes;
7. valor e quantidade das parcelas remanescentes;
8. datas de vencimento;
9. situação de adimplência;
10. garantias, coobrigados e bens vinculados;
11. multas, juros de mora e outros efeitos do atraso;
12. condições de amortização, quitação, renegociação ou portabilidade;
13. impacto mensal no fluxo de caixa;
14. documento e data-base que sustentam cada número.

## 3. Universo a pesquisar

O inventário não se limita ao crédito bancário. Deve procurar:

| Grupo | Exemplos | Fonte mínima |
|---|---|---|
| crédito no Sistema Financeiro Nacional | cartão, cheque especial, empréstimo, consignado, financiamento | contrato, fatura/extrato, instituição e SCR/Registrato |
| crédito fora do SCR | crediário, parcelamento direto, empréstimo particular | contrato, cobrança ou comprovante |
| obrigações tributárias | parcelamentos e débitos exigíveis | documento fiscal ou portal oficial |
| obrigações judiciais/familiares | pagamentos fixados ou formalmente assumidos | decisão, acordo ou instrumento |
| serviços e contratos recorrentes em atraso | condomínio, aluguel, mensalidades e outros | contrato, boleto, demonstrativo ou cobrança |
| garantias e coobrigações | fiança, aval, coobrigação, alienação fiduciária | contrato e demonstrativo da obrigação |

O **Relatório de Empréstimos e Financiamentos (SCR)** do Banco Central é fonte importante para dívidas e compromissos informados por instituições do Sistema Financeiro Nacional, mas não substitui contratos, demonstrativos atualizados nem a busca de obrigações fora desse universo. Fonte: **PF-SRC-000071**.

## 4. Hierarquia documental

Para cada obrigação, usar preferencialmente:

1. contrato original e aditivos;
2. demonstrativo atualizado do credor;
3. saldo específico para liquidação antecipada, quando houver intenção de quitar;
4. extratos, faturas e boletos que confirmem pagamentos e atraso;
5. SCR/Registrato como instrumento de descoberta e conciliação do crédito financeiro;
6. documentos fiscais, judiciais ou privados para obrigações não capturadas pelo SCR.

Se duas fontes divergirem, a divergência vira item de reconciliação; não se escolhe silenciosamente o número mais conveniente.

## 5. Estrutura mínima por obrigação

Cada linha do inventário deve conter:

- identificador;
- credor;
- modalidade;
- natureza;
- data de contratação;
- saldo devedor;
- saldo para quitação na data-base;
- CET anual, quando aplicável;
- taxa nominal e indexador;
- parcela atual;
- parcelas remanescentes;
- próximo vencimento;
- situação: EM_DIA, VENCIDA, CONTESTADA ou DADO_AUSENTE;
- dias de atraso, quando aplicável;
- garantia;
- coobrigado;
- bem essencial vinculado;
- multa/juros de mora;
- condição de amortização;
- condição de quitação;
- condição de renegociação/portabilidade;
- documento-fonte;
- data-base;
- observações.

O arquivo `inventario-dividas-template.csv` materializa essa estrutura sem criar números fictícios.

## 6. Classificação operacional

### Situação

- **EM_DIA** — obrigação existente e sem atraso confirmado;
- **VENCIDA** — atraso confirmado por documento;
- **CONTESTADA** — existência, valor ou titularidade formalmente questionada;
- **DADO_AUSENTE** — informação insuficiente para classificar.

### Garantia e consequência

Registrar separadamente:

- sem garantia conhecida;
- garantia real/fiduciária;
- fiança/aval/coobrigação;
- bem essencial potencialmente exposto;
- vencimento antecipado ou outra consequência contratual relevante;
- consequência ainda não verificada.

### Custo

Nesta fase, o custo não recebe rótulo arbitrário de “alto” ou “baixo”. O inventário apenas captura os dados que permitirão a comparação na Fase 02.

## 7. Perguntas de diagnóstico

1. Existe alguma dívida bancária ativa?
2. Existe rotativo de cartão?
3. Existe cheque especial utilizado?
4. Existe empréstimo pessoal?
5. Existe crédito consignado?
6. Existe financiamento imobiliário?
7. Existe financiamento de veículo?
8. Existe dívida garantida por bem essencial?
9. Existe parcelamento tributário?
10. Existe obrigação judicial ou familiar vencida?
11. Existe empréstimo particular?
12. Existe dívida em nome de terceiro pela qual o trabalhador é coobrigado?
13. Existe fiança ou aval prestado?
14. Há dívida contestada ou não reconhecida?
15. Qual o saldo atualizado de cada obrigação?
16. Qual o saldo específico para quitação hoje?
17. Qual o CET de cada operação de crédito?
18. Há taxa variável ou indexador?
19. Qual a soma das parcelas mensais?
20. Há parcela vencida?
21. Há multa, mora ou cobrança adicional?
22. Quantas parcelas faltam?
23. Há desconto real para antecipação?
24. A amortização parcial reduz prazo, parcela ou ambos?
25. Há custo para renegociação ou portabilidade?
26. Alguma dívida expõe moradia, veículo de trabalho ou outro bem essencial?
27. Algum compromisso não aparece no SCR?
28. Algum documento possui data-base defasada?

## 8. Estado do caso hipotético

```text
CAPITAL_LIQUIDO_INDENIZATORIO = R$ 100.000,00
EXISTENCIA_DE_DIVIDAS = DADO_AUSENTE
SALDO_DEVEDOR_TOTAL = DADO_AUSENTE
SALDO_TOTAL_PARA_QUITACAO = DADO_AUSENTE
PARCELAS_MENSAIS_TOTAIS = DADO_AUSENTE
CET_POR_DIVIDA = DADO_AUSENTE
ATRASOS = DADO_AUSENTE
GARANTIAS = DADO_AUSENTE
COOBRIGACOES = DADO_AUSENTE
```

Isso não significa “sem dívidas”. Significa apenas que nenhuma dívida foi informada no cenário.

## 9. Gate da Fase 01

**SATISFEITO.**

O inventário está classificado porque:

- o universo de obrigações foi definido;
- a hierarquia de documentos foi definida;
- os campos obrigatórios foram persistidos;
- o estado atual do caso foi classificado como `DADO_AUSENTE`, sem passivos inventados;
- foi criado um template estruturado para receber dados concretos.

## 10. Próxima fase

**Fase 02/06 — Custo efetivo e risco financeiro.**
