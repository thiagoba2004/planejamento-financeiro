# Fase 02/06 — Inventário patrimonial e qualidade dos dados

**Estratégia:** EA-000004-000006  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Regra de inventário

Uma linha representa um ativo, direito, passivo ou posição economicamente distinta.

Não agrupar itens quando isso esconder:
- datas de aquisição diferentes;
- titulares formais diferentes;
- regimes jurídicos diferentes;
- passivos vinculados diferentes;
- liquidez diferente;
- origem de recursos diferente.

## 2. Campos mínimos

### Identificação
- ID;
- categoria;
- subcategoria;
- descrição;
- titular formal;
- instituição/registro;
- data de aquisição/constituição.

### Jurídico — somente importado
- regime de bens;
- status jurídico;
- percentual confirmado;
- marco jurídico/data relevante;
- fonte jurídica;
- controvérsia.

### Econômico
- quantidade/unidade;
- valor bruto;
- saldo passivo vinculado;
- custos de conversão;
- valor líquido estimado;
- moeda;
- data-base;
- método de avaliação;
- camada de liquidez;
- prazo estimado para conversão;
- renda/fruto associado;
- essencialidade para moradia/trabalho.

### Qualidade
- fonte do valor;
- status de comprovação;
- data do documento;
- divergência;
- dado pendente;
- observações.

## 3. Estados de comprovação

- `COMPROVADO_PRIMARIO` — documento originário ou registro oficial;
- `COMPROVADO_SECUNDARIO` — evidência confiável, mas não originária;
- `INFORMADO_NAO_COMPROVADO`;
- `DIVERGENTE`;
- `DADO_AUSENTE`.

## 4. Hierarquia de fontes por classe

### Imóveis
Preferir:
1. matrícula/registro;
2. contrato e extrato de financiamento;
3. laudo ou avaliação documentada;
4. referências de mercado comparáveis;
5. valor informado sem comprovação, apenas como hipótese.

### Veículos
Preferir:
1. documento de propriedade/gravame;
2. contrato de financiamento;
3. referência pública de mercado;
4. avaliação comercial quando o estado do bem justificar ajuste.

### Investimentos e contas
Preferir:
1. extrato da instituição/custodiante;
2. posição em data-base;
3. documento tributário apenas como conferência histórica.

### Previdência
Preferir:
1. extrato e regulamento do plano;
2. informação de saldo de resgate/benefício;
3. classificação jurídica importada do Ações Judiciais.

### Empresas
Preferir:
1. contrato social/registro;
2. demonstrações contábeis;
3. documentos de distribuição;
4. avaliação técnica quando cabível.

### Dívidas
Preferir:
1. contrato;
2. extrato/saldo para liquidação;
3. cronograma;
4. garantia;
5. informação sobre custo e vencimento.

## 5. Reconciliação

Antes de usar o inventário:
- soma de contas deve fechar com extratos;
- investimentos devem ter a mesma data-base ou ajuste explícito;
- saldo devedor deve corresponder ao mesmo período do valor do ativo;
- ativos em moeda estrangeira devem registrar taxa/data de conversão;
- bens repetidos em documentos diferentes devem ser deduplicados;
- passivo vinculado não pode ser descontado duas vezes;
- frutos/rendimentos não podem ser confundidos com o valor principal;
- valor contábil não pode ser tratado automaticamente como valor de mercado.

## 6. Dado jurídico controvertido

Quando `status_juridico = CONTROVERTIDO`:
- não preencher percentual definitivo;
- manter o valor econômico do item;
- gerar cenários separados;
- não somar o valor ao patrimônio disponível de qualquer parte no cenário confirmado.

Quando `status_juridico = NAO_ANALISADO`:
- inventariar existência e valor quando possível;
- bloquear alocação em cenário de partilha;
- marcar a dependência jurídica.

## 7. Indicadores de qualidade do inventário

- percentual de itens com documento primário;
- percentual do valor bruto com data-base válida;
- percentual do patrimônio com valor não mensurado;
- percentual do patrimônio em controvérsia jurídica;
- percentual do patrimônio com passivo reconciliado;
- percentual do patrimônio líquido com liquidez classificada.

Esses indicadores medem qualidade do diagnóstico, não qualidade do patrimônio.

## 8. Gate

Gate satisfeito:
- schema tabular criado;
- estados de comprovação definidos;
- fontes hierarquizadas por classe;
- regras de reconciliação documentadas;
- tratamento de controvérsia e não análise definido;
- indicadores de qualidade do inventário persistidos.
