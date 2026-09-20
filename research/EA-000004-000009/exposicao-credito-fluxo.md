# Fase 02/06 — Exposição de crédito e fluxo

**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Separar dívida atual de exposição potencial

### Dívida atual
Valor já utilizado/contratado e devido.

### Exposição contingente
Limites ainda disponíveis ou autorizações que podem gerar nova obrigação.

Exemplos:
- limite de cartão;
- cheque especial;
- crédito pré-aprovado;
- cartão adicional;
- recorrência autorizada.

Limite disponível não é patrimônio nem liquidez.

## 2. Campos financeiros mínimos

Para cada obrigação:
- saldo devedor;
- prestação mínima/contratada;
- data de vencimento;
- número de parcelas restantes;
- taxa;
- CET;
- custo total remanescente quando calculável;
- garantia;
- status de adimplência;
- responsável pelo pagamento atual;
- fonte de pagamento;
- data-base.

## 3. Métricas

### Serviço mensal da dívida

```text
soma das parcelas e pagamentos mínimos confirmados no mês
```

### Comprometimento financeiro interno

```text
serviço mensal da dívida ÷ renda líquida disponível
```

É indicador interno de fluxo; não substitui política de concessão de crédito.

### Fluxo livre após dívida

```text
renda líquida
− despesas essenciais
− serviço mensal da dívida
− demais obrigações confirmadas
```

### Exposição de curto prazo

```text
vencimentos confirmados nos próximos 30 dias
+ faturas
+ parcelas vencidas
+ eventos contratuais conhecidos
```

## 4. Cartão de crédito

Separar:
- fatura corrente;
- compras parceladas futuras;
- eventual financiamento/rotativo;
- assinaturas recorrentes;
- limite disponível.

Não somar limite total como dívida.

## 5. Reconciliação com o SCR

O SCR é instrumento de conferência, não substitui:
- contrato;
- fatura atual;
- saldo para liquidação;
- condições de renegociação.

Diferenças de data-base devem ser identificadas.

## 6. CET e comparação

Quando houver renegociação, consolidação ou portabilidade:
- comparar CET;
- comparar custo total;
- comparar prazo;
- comparar garantias;
- comparar parcela;
- comparar efeito na liquidez.

Parcela menor não significa custo menor.

## 7. Gate

Satisfeito. Dívida, exposição contingente, dados mínimos, métricas, cartão, SCR e critérios de comparação foram estruturados.
