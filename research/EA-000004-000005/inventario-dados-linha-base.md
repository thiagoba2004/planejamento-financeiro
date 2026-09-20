# Fase 02/06 — Inventário de dados e linha de base

**Estratégia:** EA-000004-000005  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Regra de qualidade dos dados

Cada dado financeiro deve possuir:
- unidade/parte a que pertence;
- período ou data-base;
- valor;
- recorrência;
- fonte;
- status de comprovação;
- rótulo jurídico quando aplicável;
- observação sobre incerteza.

Estados de comprovação:
- `COMPROVADO`;
- `INFORMADO_NAO_COMPROVADO`;
- `DIVERGENTE`;
- `DADO_AUSENTE`.

Não preencher ausências com médias arbitrárias.

## 2. Dados mínimos

### Identificação financeira
- unidade A/B;
- dependentes;
- residência atual;
- contas bancárias operacionais;
- datas de pagamento de renda.

### Receitas
- salário líquido recorrente;
- pró-labore;
- renda variável;
- benefícios;
- aluguéis;
- pensões/alimentos já recebidos;
- outras receitas regulares ou extraordinárias.

### Despesas essenciais
- moradia;
- energia, água, telecomunicações;
- alimentação;
- transporte;
- saúde;
- seguros essenciais;
- educação;
- cuidados;
- despesas essenciais dos filhos.

### Despesas discricionárias
- lazer;
- assinaturas;
- compras não essenciais;
- despesas que podem ser ajustadas na transição.

### Despesas de transição
- mudança;
- caução/entrada;
- mobília mínima;
- honorários/custas conhecidos;
- perícias/avaliações conhecidas;
- viagens/logística extraordinária;
- regularização documental.

### Dívidas
- credor;
- devedor formal;
- saldo;
- prestação;
- taxa/CET quando disponível;
- vencimento;
- garantia;
- débito automático;
- conta de pagamento;
- status jurídico quando compartilhada/controvertida.

### Patrimônio e liquidez
- caixa;
- contas;
- investimentos;
- ativos com liquidez;
- imóveis;
- veículos;
- FGTS;
- previdência;
- quotas/empresa;
- outros ativos;
- valor bruto, passivo vinculado e valor líquido;
- rótulo jurídico do PRJ-000003.

### Filhos
Importar a estrutura jurídica:
- categoria;
- descrição;
- valor;
- frequência;
- valor mensal equivalente;
- beneficiário;
- pagador atual;
- comprovante;
- classificação ordinária/extraordinária/sazonal;
- essencialidade;
- regra de reembolso/rateio quando confirmada.

## 3. Fontes documentais

### Alta confiabilidade
- extrato bancário;
- contracheque;
- informe de rendimentos;
- declaração fiscal;
- fatura;
- contrato;
- boleto/documento de cobrança;
- extrato de financiamento;
- decisão judicial;
- acordo homologado;
- documento oficial do PRJ-000003.

### Complementares
- planilha do cliente;
- aplicativo de finanças;
- histórico manual;
- mensagem/recibo;
- orçamento/cotação.

Dados complementares são úteis para triagem, mas devem ser identificados como não comprovados quando não houver documento primário.

## 4. Linha de base

A linha de base deve permitir três leituras simultâneas:

### Antes da ruptura
- renda familiar;
- despesas totais;
- fluxo livre;
- dívida mensal;
- reserva;
- principais ativos/passivos.

### Situação atual
- renda por unidade;
- despesas já separadas;
- despesas ainda compartilhadas;
- caixa por unidade;
- vencimentos de 30/90 dias;
- compromissos confirmados.

### Cenários
- cenário juridicamente confirmado;
- cenário A;
- cenário B;
- variáveis controvertidas;
- variáveis ausentes.

## 5. Controles contra dupla contagem

1. Despesa dos filhos não pode ser integralmente lançada em A e B ao mesmo tempo sem explicação.
2. Prestação de imóvel não pode aparecer como despesa de moradia e dívida separada sem reconciliação.
3. Transferência entre A e B não é receita familiar nova.
4. Resgate de investimento é conversão patrimonial, não renda recorrente.
5. Venda de ativo é entrada de caixa não recorrente e deve descontar passivos/custos.
6. Alimento pedido não entra em fluxo confirmado.
7. Bem litigioso não entra como liquidez disponível.
8. Cartão deve ser decomposto quando a fatura já contém despesas classificadas para evitar duplicidade.

## 6. Testes de consistência

Antes de calcular cenários:
- receitas fecham com extratos/contracheques?
- despesas somam com faturas/extratos?
- saldos de dívida reconciliam com contratos/extratos?
- ativos têm data-base?
- fluxos internos entre partes foram eliminados da renda consolidada?
- valores mensais equivalentes foram normalizados corretamente?
- cada premissa jurídica está rotulada?
- há dado ausente material?

## 7. Gate

Gate satisfeito:
- dados necessários classificados;
- fontes documentais hierarquizadas;
- estados de comprovação definidos;
- linha de base antes/atual/cenários estruturada;
- controles contra dupla contagem persistidos;
- template tabular criado para execução reproduzível.
