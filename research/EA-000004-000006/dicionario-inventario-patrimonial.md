# Dicionário do inventário patrimonial financeiro

## Campos jurídicos importados

- **status_juridico:** CONFIRMADO_COMUNICAVEL / CONFIRMADO_PARTICULAR / CONTROVERTIDO / NAO_ANALISADO.
- **percentual_juridico_confirmado:** somente preencher quando houver confirmação jurídica verificável.
- **fonte_juridica:** referência ao documento/resultado do PRJ-000003.
- **controversia:** resumo da questão pendente, sem resolução pelo PRJ-000004.

## Campos econômicos

- **valor_bruto:** valor do ativo antes de passivos/custos.
- **saldo_passivo_vinculado:** dívida diretamente ligada ao item.
- **custos_conversao_estimados:** venda, resgate, transferência ou outros custos apenas quando fundamentados.
- **valor_liquido_estimado:** valor bruto menos passivo vinculado e custos fundamentados.
- **data_base_valor:** data à qual o valuation se refere.
- **metodo_avaliacao:** método econômico usado.
- **camada_liquidez:** LIQUIDO_IMEDIATO / LIQUIDO_CURTO_PRAZO / ILIQUIDO_NEGOCIAVEL / INDIVISIVEL_OU_COMPLEXO / CONDICIONADO_A_EVENTO / VALOR_NAO_MENSURADO.
- **prazo_conversao_dias:** estimativa econômica, não promessa de venda.

## Qualidade

- **status_comprovacao:** COMPROVADO_PRIMARIO / COMPROVADO_SECUNDARIO / INFORMADO_NAO_COMPROVADO / DIVERGENTE / DADO_AUSENTE.
- **dado_pendente:** documento, avaliação ou definição necessária.

## Regra crítica

Não preencher `percentual_juridico_confirmado` por conveniência financeira. Um cenário econômico pode simular percentuais, mas o campo jurídico permanece vazio enquanto não houver confirmação no projeto jurídico.
