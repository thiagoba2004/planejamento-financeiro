# Fase 02 — Renda, transferências e rateios

## Regra de classificação

A renda do outro cônjuge não entra automaticamente no denominador das métricas do cliente. Classificar cada fluxo em uma destas categorias:

1. **Renda própria recorrente do cliente** — salário, pró-labore, benefício, aluguel etc.
2. **Renda própria não recorrente** — bônus, indenização, venda de ativo etc.
3. **Transferência recebida** — valor efetivamente transferido pelo outro cônjuge/genitor.
4. **Despesa paga diretamente por terceiro** — reduz a parcela de despesa suportada pelo cliente, mas não vira renda própria.
5. **Rateio de despesa compartilhada** — registrar a fração efetivamente suportada por cada parte.
6. **Renda meramente informativa do outro cônjuge** — contexto econômico, sem incorporação automática ao fluxo do cliente.
7. **Fluxo juridicamente controvertido** — cenário, não dado confirmado.

## Fórmulas

### Renda operacional própria
`RENDA_OPERACIONAL_CLIENTE = rendas próprias recorrentes confirmadas`

### Transferências
`TRANSFERENCIAS_LIQUIDAS = transferências recebidas - transferências pagas`

Não misturar transferências com renda laboral recorrente nas análises que precisem distinguir capacidade própria de suporte.

### Despesa efetivamente suportada
`DESPESA_CLIENTE = despesa total compartilhada × percentual/valor efetivamente pago pelo cliente`

Quando o rateio não estiver comprovado, usar cenários.

### Fluxo livre da unidade do cliente
`FLUXO_LIVRE_U1 = RENDA_OPERACIONAL_CLIENTE + TRANSFERENCIAS_RECEBIDAS_CONFIRMADAS - DESPESAS_EFETIVAMENTE_SUPORTADAS - SERVICO_DA_DIVIDA_PROPRIO_CONFIRMADO - TRANSFERENCIAS_PAGAS_CONFIRMADAS`

## Proibição de dupla contagem

Não:
- somar a renda integral do outro cônjuge e também subtrair apenas a parte de despesas do cliente;
- registrar transferência recebida como renda nova da família consolidada;
- atribuir a mesma despesa integralmente a duas unidades;
- tratar pagamento direto da escola/plano de saúde pelo outro genitor como dinheiro recebido pelo cliente.

## Métricas com denominadores diferentes

Dependendo da pergunta:
- **comprometimento próprio:** dívida do cliente / renda operacional própria;
- **fluxo de caixa próprio:** inclui transferências efetivamente recebidas/pagas;
- **orçamento consolidado dos filhos:** soma recursos destinados aos filhos, sem transformar transferência interna em renda nova;
- **cenário familiar agregado:** somente para análise específica, nunca como substituto automático do orçamento individual.

## Comunicação

O relatório financeiro deve dizer explicitamente se a métrica usa:
- renda própria;
- renda própria + transferências;
- renda familiar consolidada;
- cenário hipotético.

Nenhuma dessas bases é intercambiável.
