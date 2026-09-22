# Indenização trabalhista e superendividamento: impacto financeiro no plano

**Cenário didático:** recebimento de **R$ 100.000,00 recebidos em caixa e líquidos das retenções consideradas no cenário** por dano moral trabalhista.

Esta unidade mede o que muda financeiramente quando uma pessoa em situação de superendividamento recebe capital extraordinário. Ela não decide se a ação judicial continua cabível nem qual parcela do valor pertence juridicamente ao plano.

## 1. Estoque muda; fluxo não muda automaticamente

No instante do recebimento:

- ativos líquidos: **+R$ 100.000,00**;
- patrimônio líquido: **+R$ 100.000,00 apenas se o direito à indenização não estava previamente reconhecido como ativo**; se já havia recebível reconhecido, o pagamento apenas troca recebível por caixa;
- renda recorrente: **sem alteração direta**;
- parcela mensal das dívidas: **sem alteração direta**;
- fluxo livre mensal: **sem alteração direta**.

Uma pessoa pode ganhar liquidez e solvência e continuar com déficit mensal.

## 2. Linha de base

Antes de decidir qualquer destinação, levante:

- ativos líquidos anteriores;
- outros ativos;
- passivos totais;
- passivos de curto prazo;
- saldo para quitação de cada dívida;
- parcelas;
- renda líquida;
- despesas essenciais;
- reserva existente;
- atrasos, garantias e CET.

Dado ausente permanece **DADO_AUSENTE**.

## 3. Métricas

**Patrimônio líquido após**

Se a indenização ainda não estava reconhecida como ativo, o patrimônio líquido aumenta em R$ 100.000,00 no reconhecimento/recebimento, conforme a linha de base

Se já havia recebível reconhecido: o pagamento não gera novo acréscimo de PL; apenas altera a composição dos ativos.

**Solvência após**

SOLVÊNCIA_APÓS = ATIVOS_TOTAIS_APÓS / PASSIVOS_TOTAIS

`ATIVOS_TOTAIS_APÓS` deve ser reconstruído a partir da linha de base. Se um recebível de R$ 100.000,00 já integrava os ativos antes do pagamento, a entrada em caixa não pode ser somada novamente aos ativos totais.

**Cobertura de despesas**

COBERTURA_MESES = ATIVOS_LÍQUIDOS / DESPESAS_ESSENCIAIS_MENSAIS

**Serviço da dívida sobre renda**

DSR = SERVIÇO_MENSAL_DA_DÍVIDA / RENDA_LÍQUIDA_MENSAL

O DSR não cai apenas porque o dinheiro entrou na conta. Ele muda se a intervenção alterar efetivamente as parcelas ou a renda.

**Fluxo livre**

FLUXO_LIVRE = RENDA_LÍQUIDA - DESPESAS_ESSENCIAIS - SERVIÇO_MENSAL_DA_DÍVIDA

## 4. Sete cenários de destinação

1. preservar integralmente por período de diagnóstico;
2. separar reserva e despesas previsíveis antes de decidir;
3. quitar dívida seletivamente;
4. amortizar dívida com simulação do credor;
5. usar parte como entrada em proposta global;
6. combinar reserva com pagamento;
7. simular rateio proporcional quando houver critério jurídico ou negocial que o justifique.

Nenhum cenário é automaticamente o melhor.

### Gate jurídico-financeiro antes da execução

Esses cenários podem ser **simulados financeiramente**, mas a execução não é automaticamente livre quando houver processo de repactuação, negociação global, acordo homologado, garantia, patrimônio controvertido ou outra dependência jurídica material.

Use três estados:
- **VERDE:** nenhuma dependência jurídica material identificada; confirmar contrato, custo e liquidez;
- **AMARELO:** simular e validar juridicamente antes de executar;
- **VERMELHO:** não orientar execução financeira unilateral enquanto persistir ordem, garantia ou controvérsia material.

Quitação ou amortização seletiva em contexto de repactuação não deve ser apresentada como autorização automática. O planejador mede o efeito econômico; a executabilidade jurídica pertence à análise especializada.

## 5. Sustentabilidade

Um cenário que reduz dívida mas mantém **FLUXO_LIVRE < 0** pode apenas adiar a crise.

Se a liquidez remanescente for usada para cobrir déficit:

MESES_ATÉ_EXAUSTÃO = LIQUIDEZ_REMANESCENTE / |FLUXO_LIVRE_NEGATIVO|

Esse número é uma **estimativa estática de primeira ordem**: supõe déficit constante, sem inflação, rendimento, choque de despesa ou mudança de renda/dívida. Não é previsão nem prazo recomendado de plano.

## 6. Capacidade mensal x capacidade patrimonial

**Capacidade mensal recorrente** depende de renda, despesas e parcelas.

**Capacidade patrimonial extraordinária** decorre do capital disponível.

Não trate R$ 100.000,00 como se fossem renda mensal futura.

## 7. Casos

### Caso 1 — amortização elimina o déficit, mas não cria folga
Renda R$ 8 mil, essenciais R$ 5 mil, dívida mensal cai de R$ 5 mil para R$ 3 mil após aplicação de R$ 60 mil. O fluxo vai de −R$ 2 mil para zero e restam R$ 40 mil líquidos. Exige teste de choque.

### Caso 2 — quitação melhora fluxo e preserva liquidez
Renda R$ 8 mil, essenciais R$ 5 mil, serviço R$ 3,5 mil. **Premissa do caso:** R$ 70 mil quitam integralmente a obrigação que gerava os R$ 3,5 mil mensais. O serviço depois cai a zero; o fluxo passa de −R$ 500 para +R$ 3 mil e restam R$ 30 mil.

### Caso 3 — dívida zerada, liquidez pequena
Renda R$ 6 mil, essenciais R$ 5,5 mil, serviço da dívida antes de R$ 2 mil. **Premissa:** R$ 90 mil quitam integralmente a obrigação que gerava esse serviço. O fluxo passa de −R$ 1,5 mil para +R$ 500, e restam R$ 10 mil de liquidez.

### Caso 4 — capital posterga, mas não resolve
Renda R$ 7 mil, essenciais R$ 5 mil, serviço cai de R$ 4 mil para R$ 2,5 mil após aplicação de R$ 60 mil. O fluxo continua em −R$ 500. Restam R$ 40 mil, capazes de cobrir matematicamente 80 meses desse déficit, mas o problema estrutural persiste.

## 8. Interface com a análise jurídica

O Planejamento Financeiro fornece:

- balanço antes/depois;
- liquidez;
- solvência;
- fluxo;
- saldo e serviço das dívidas;
- cenários;
- sustentabilidade.

Não conclui:

- se a ação de repactuação é cabível;
- se o consumidor deixou de ser juridicamente superendividado;
- qual valor integra o mínimo existencial;
- qual parcela deve obrigatoriamente ser oferecida aos credores.

A análise jurídica pertence ao Projeto **Ações Judiciais**.

## 9. Aderência ao CFP®

**Classificação: aplicação profissional do Projeto apoiada por competências do domínio CFP®.**

**SABER:** estoque x fluxo, liquidez, solvência, serviço da dívida, custo e reserva.  
**FAZER:** construir linha de base, simular cenários, calcular fluxo pós-intervenção e documentar incertezas.  
**DECIDIR:** distinguir melhora patrimonial de solução estrutural e reconhecer quando a conclusão é jurídica.

## 10. Regra profissional

> O recebimento dos R$ 100.000,00 melhora imediatamente a liquidez. O efeito incremental sobre o patrimônio líquido depende de o direito já ter sido ou não reconhecido como ativo antes do pagamento. Só depois de conhecer renda, despesas, dívidas e reserva é possível medir quanto do capital pode ser usado sem transformar uma melhora patrimonial em nova fragilidade financeira.

**Última revisão:** 21/09/2026.
