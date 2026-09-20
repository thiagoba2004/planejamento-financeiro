# Fase 03/06 — Cenários de fluxo de caixa parental

**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## Regra central

O planejamento modela impactos financeiros de arranjos confirmados ou hipóteses explicitamente condicionais. Não prevê decisão judicial.

## 1. Três camadas de fluxo

### Fluxo do filho
Despesas necessárias e objetivos vinculados ao filho, independentemente de quem paga.

### Fluxo de cada responsável
Renda, despesas próprias, despesas dos filhos pagas diretamente, transferências confirmadas e custos logísticos.

### Fluxo consolidado
Visão familiar para identificar dupla contagem, desperdícios operacionais e insuficiência global.

## 2. Transferência entre responsáveis

Uma transferência interna:
- é saída para um responsável;
- é entrada para o outro;
- não é renda nova no consolidado familiar.

## 3. Cenários mínimos

### Cenário confirmado
Somente:
- despesas comprovadas;
- pagamentos efetivos;
- alimentos fixados/confirmados;
- calendário confirmado quando financeiramente relevante.

### Cenário A
Hipótese explícita de custeio/convivência.

### Cenário B
Hipótese alternativa.

Os cenários devem manter o mesmo conjunto de dados básicos para que a comparação seja válida.

## 4. Custos logísticos

O calendário de convivência pode alterar:
- transporte;
- alimentação fora de casa;
- duplicação de roupas/itens;
- cuidador;
- deslocamentos;
- viagens;
- necessidade de espaço ou equipamentos em duas residências.

Isso deve ser modelado como impacto financeiro, não como argumento jurídico sobre qual convivência é preferível.

## 5. Fórmulas

### Custo mensal equivalente dos filhos

```text
soma das despesas mensais equivalentes
```

### Saída líquida de cada responsável

```text
despesas próprias
+ despesas dos filhos pagas diretamente
+ transferências confirmadas
− transferências recebidas
```

### Fluxo livre pós-filhos

```text
renda líquida
− despesas próprias essenciais
− impacto líquido confirmado dos filhos
```

### Cobertura global

```text
renda líquida consolidada ÷ despesas essenciais consolidadas
```

A cobertura global não define obrigação jurídica individual.

## 6. Exemplo reproduzível

Dados fictícios:
- educação: R$ 1.800/mês;
- saúde: R$ 600/mês;
- alimentação incremental: R$ 900/mês;
- transporte/logística: R$ 500/mês;
- material escolar anual: R$ 2.400 → R$ 200/mês.

Custo mensal equivalente:

```text
1.800 + 600 + 900 + 500 + 200 = R$ 4.000/mês
```

Se um cenário financeiro apenas para teste assumir divisão de R$ 2.500 e R$ 1.500:
- o total permanece R$ 4.000;
- a distribuição é hipótese financeira;
- não representa percentual de alimentos juridicamente devido.

## 7. Gate

Satisfeito. Fluxos individual/consolidado, transferências, logística, cenários e fórmulas foram documentados.
