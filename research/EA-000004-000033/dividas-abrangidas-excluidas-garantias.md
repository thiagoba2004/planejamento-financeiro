# Fase 02 — Dívidas abrangidas, excluídas, garantias e efeitos financeiros

## Duas classificações independentes

Cada obrigação deve ter:
1. **status jurídico no processo de repactuação**, importado do Projeto Ações Judiciais ou de análise profissional competente;
2. **status financeiro**, calculado pelo Planejamento Financeiro.

Uma dívida juridicamente excluída da repactuação pode continuar sendo a principal pressão de caixa do cliente.

## Campos mínimos

- modalidade;
- credor;
- saldo para quitação;
- parcela;
- CET/taxa/indexador;
- prazo;
- atraso;
- garantia/gravame;
- bem associado;
- status jurídico no processo;
- impacto mensal;
- risco patrimonial;
- possibilidade contratual de amortização/quitação;
- dependência de validação jurídica.

## Matriz de tratamento

### Dívida elegível ao plano
Medir saldo, serviço, CET e cenários, mas não presumir ordem individual de pagamento fora da lógica jurídica/negocial.

### Dívida excluída da repactuação
Manter integralmente no orçamento e nos testes de sustentabilidade. **Fora do plano não significa fora do fluxo.**

### Financiamento imobiliário
Tratar prestação, saldo, valor líquido do imóvel, moradia e risco de perda/execução conforme o contrato e premissas jurídicas. Não confundir exclusão do rito com irrelevância financeira.

### Crédito garantido / bem gravado
Separar dívida, valor do bem e garantia. Venda, entrega, quitação ou amortização podem exigir consentimento/efeitos contratuais e jurídicos.

### Dívida de classificação controvertida
Manter status `JURIDICAMENTE_A_CONFIRMAR` e trabalhar cenários financeiros paralelos; nunca resolver a classificação pelo cálculo.

## Sustentabilidade global

O orçamento pós-plano deve incluir tanto obrigações tratadas no plano quanto obrigações que permanecem fora dele.

`FLUXO_POS = RENDA_RECURRENTE - DESPESAS_ESSENCIAIS - PARCELAS_DO_PLANO - OBRIGACOES_FORA_DO_PLANO`

Um plano aparentemente sustentável pode ser inviável se excluir do teste financeiro uma prestação imobiliária, veículo garantido ou outra obrigação relevante.
