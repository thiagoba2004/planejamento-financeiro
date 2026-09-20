# Fase 04/06 — Liquidez e reserva de transição

**Estratégia:** EA-000004-000005  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Princípio

A ruptura pode transformar uma família patrimonialmente solvente em duas unidades com baixa liquidez. Por isso, patrimônio total e caixa disponível devem ser medidos separadamente.

Não será usada uma regra universal de “X meses de reserva”. A necessidade de caixa é derivada do fluxo projetado, dos vencimentos e dos riscos documentados.

## 2. Camadas de liquidez

### L0 — caixa imediato
- saldo em conta de uso livre;
- dinheiro disponível;
- aplicações com resgate imediato, desde que juridicamente disponíveis.

### L1 — até 7 dias
- aplicações resgatáveis em poucos dias;
- recebimentos certos e documentados com vencimento próximo.

### L2 — 8 a 30 dias
- ativos líquidos com prazo operacional;
- recebíveis com data e risco conhecidos.

### L3 — acima de 30 dias / condicionais
- ativos que dependem de venda;
- valores sujeitos a negociação;
- recebimentos sem data firme;
- recursos sujeitos a decisão jurídica.

### NÃO DISPONÍVEL PARA RESERVA
- bem litigioso sem disponibilidade confirmada;
- limite de crédito;
- patrimônio de filho/dependente;
- previdência ou FGTS sem hipótese de saque disponível;
- ativo indivisível sem venda/cessão factível;
- valor apenas pretendido judicialmente.

## 3. Caixa mínimo de transição

O caixa necessário é calculado pela maior insuficiência acumulada do horizonte analisado.

```text
NECESSIDADE_MINIMA_DE_CAIXA =
MAX(0; - MENOR_CAIXA_PROJETADO_NO_HORIZONTE)
```

Se o caixa projetado nunca fica negativo, a necessidade mínima de caixa para cobrir o cenário-base é zero. Isso **não significa** que risco ou contingência sejam zero.

Contingências devem ser modeladas por cenários de estresse explícitos, por exemplo:
- atraso de receita;
- custo de mudança maior;
- despesa médica;
- decisão provisória diferente;
- manutenção temporária de dois imóveis;
- inadimplência de contraparte.

Não aplicar percentuais arbitrários sem justificar a hipótese.

## 4. Calendário de obrigações

Cada saída deve ter:
- data;
- valor;
- unidade responsável;
- natureza;
- recorrência;
- possibilidade de adiamento;
- consequência financeira do atraso;
- status jurídico/contratual.

### Prioridade operacional de caixa

A prioridade de planejamento não altera prioridade jurídica. Para continuidade financeira, classificar:
1. sobrevivência e segurança: moradia, alimentação, saúde, utilidades essenciais;
2. obrigações de filhos/dependentes e ordens/acordos confirmados;
3. compromissos que preservam moradia, trabalho ou ativo essencial;
4. dívidas e tributos conforme custo e consequência;
5. despesas ajustáveis;
6. objetivos adiáveis.

## 5. Fontes de liquidez

### Fonte própria
- caixa;
- aplicação resgatável;
- renda corrente;
- recebível confirmado.

### Conversão patrimonial
- venda de ativo;
- resgate;
- liquidação de posição.

Registrar:
- valor bruto;
- passivo;
- custo de transação;
- imposto estimado apenas quando tecnicamente fundamentado;
- prazo;
- rótulo jurídico;
- valor líquido esperado.

### Crédito
Crédito não é reserva.

Se modelado como ponte:
- taxa/CET;
- prazo;
- prestação;
- efeito sobre dívida total;
- risco de refinanciamento;
- cenário de pagamento.

Usar crédito para cobrir déficit estrutural sem plano de correção é sinal de insustentabilidade, não solução permanente.

## 6. Métricas

- caixa L0;
- liquidez L0+L1;
- liquidez em até 30 dias;
- meses de despesas essenciais cobertos;
- menor caixa projetado em 30/90/365 dias;
- necessidade mínima de caixa;
- maior concentração de vencimentos;
- proporção do patrimônio total que é efetivamente líquido;
- custo financeiro de eventual ponte de crédito.

## 7. Gatilhos de revisão

Recalcular imediatamente se houver:
- decisão sobre alimentos;
- mudança de residência;
- perda/ganho relevante de renda;
- venda ou bloqueio de ativo;
- nova dívida;
- alteração de guarda/convivência com impacto logístico;
- custo jurídico relevante confirmado;
- despesa extraordinária dos filhos;
- mudança de situação empresarial.

## 8. Gate

Gate satisfeito:
- ativos classificados por disponibilidade;
- itens que não podem ser tratados como reserva explicitados;
- fórmula de necessidade mínima de caixa definida;
- calendário de obrigações estruturado;
- fontes de liquidez e crédito separadas;
- gatilhos de revisão persistidos.
