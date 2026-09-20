# Fase 02/06 — Dados financeiros e qualidade da informação

**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Documentos mínimos

Conforme porte e disponibilidade:
- contrato/estatuto e alterações;
- QSA/CNPJ;
- balanço patrimonial;
- DRE;
- balancetes;
- demonstração de fluxo de caixa, quando existente;
- razão/contas contábeis relevantes;
- extratos bancários;
- endividamento;
- relação de garantias;
- contas a receber/pagar;
- estoque;
- imobilizado;
- obrigações fiscais;
- folha/pró-labore;
- atas/deliberações de lucros;
- ECF/ECD quando cabível;
- documentos de distribuição;
- contratos relevantes.

## 2. Qualidade do dado

Classificar:
- `AUDITADO_OU_ASSEGURADO`;
- `CONTABILIDADE_REGULAR`;
- `BALANCETE_GERENCIAL`;
- `INFORMADO_SEM_DOCUMENTO`;
- `DIVERGENTE`;
- `DESATUALIZADO`;
- `DADO_AUSENTE`.

## 3. Separar empresa de pessoa física

Não consolidar como renda pessoal:
- faturamento;
- receita bruta;
- caixa da empresa;
- EBITDA;
- lucro contábil não distribuído;
- limite bancário empresarial.

Para renda pessoal, usar pagamentos efetivamente recebidos ou cenários explicitamente aprovados/documentados.

## 4. Indicadores operacionais

### Receita
Comparar:
- últimos 12 meses;
- últimos 24/36 meses quando disponíveis;
- sazonalidade;
- concentração por cliente;
- recorrência.

### Margem
Não usar margem sem reconciliar:
- regime contábil;
- despesas não recorrentes;
- remuneração do sócio;
- itens extraordinários.

### Endividamento
Registrar:
- dívida financeira;
- fornecedores relevantes;
- tributos parcelados;
- garantias;
- covenants quando houver;
- vencimentos.

### Capital de giro
Mapear:
- caixa;
- contas a receber;
- estoques;
- fornecedores;
- impostos;
- necessidade operacional.

## 5. Distribuições

Separar:
- lucro contábil;
- lucro disponível para distribuição;
- deliberação societária;
- pagamento efetivo;
- retenção para capital de giro/investimento.

A Receita Federal alterou a tributação de lucros/dividendos a partir de 2026; o efeito fiscal concreto deve ser tratado pela estratégia tributária e fonte vigente.

## 6. Reconciliações obrigatórias

- faturamento ≠ lucro;
- lucro ≠ caixa;
- caixa ≠ valor disponível ao sócio;
- lucro distribuível ≠ distribuição efetiva;
- pró-labore ≠ dividendo;
- patrimônio líquido contábil ≠ valor econômico da empresa.

## 7. Gate

Satisfeito. Documentos, estados de qualidade, reconciliações, renda/distribuições e dados necessários foram classificados.
