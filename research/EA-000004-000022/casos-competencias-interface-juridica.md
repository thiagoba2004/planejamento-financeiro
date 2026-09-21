# Fase 05/06 — Casos, competências CFP® e interface jurídica

**Estratégia:** EA-000004-000022 — Impacto financeiro da indenização trabalhista no diagnóstico e no plano de superendividamento  
**Data:** 21/09/2026  
**Estado:** CONCLUÍDA

## 1. Regra dos casos

Todos os números abaixo, exceto o capital-base de R$ 100.000,00, são **hipóteses didáticas**. Não descrevem o caso-base e não substituem dados reais.

## 2. Caso 1 — amortização melhora o fluxo, mas sem folga

Premissas didáticas:
- renda líquida: R$ 8.000/mês;
- despesas essenciais: R$ 5.000/mês;
- serviço da dívida antes: R$ 5.000/mês;
- dívida total: R$ 180.000;
- aplicação do capital: R$ 60.000;
- simulação real do credor reduz serviço para R$ 3.000/mês;
- liquidez remanescente: R$ 40.000.

Antes:

**FLUXO_LIVRE = 8.000 − 5.000 − 5.000 = −R$ 2.000**

Depois:

**FLUXO_LIVRE = 8.000 − 5.000 − 3.000 = R$ 0**

Cobertura da liquidez remanescente:

**40.000 / 5.000 = 8 meses**

Leitura: a intervenção elimina o déficit no cenário-base, mas não cria margem para choques. Exige stress test.

## 3. Caso 2 — quitação integral com fluxo positivo

Premissas:
- renda: R$ 8.000;
- essenciais: R$ 5.000;
- serviço da dívida: R$ 3.500;
- saldo para quitação: R$ 70.000;
- quitação integral: R$ 70.000;
- liquidez remanescente: R$ 30.000.

Antes:

**FLUXO_LIVRE = −R$ 500**

Depois:

**FLUXO_LIVRE = +R$ 3.000**

Cobertura:

**30.000 / 5.000 = 6 meses**

Leitura financeira: o cenário melhora simultaneamente fluxo e estoque e preserva liquidez relevante. A conclusão jurídica sobre necessidade de repactuação continua pertencendo ao PRJ-000003.

## 4. Caso 3 — dívida eliminada, liquidez muito menor

Premissas:
- renda: R$ 6.000;
- essenciais: R$ 5.500;
- serviço da dívida: R$ 2.000;
- saldo para quitação: R$ 90.000;
- quitação integral: R$ 90.000;
- liquidez remanescente: R$ 10.000.

Antes:

**FLUXO_LIVRE = −R$ 1.500**

Depois:

**FLUXO_LIVRE = +R$ 500**

Cobertura:

**10.000 / 5.500 ≈ 1,82 mês**

Leitura: quitar tudo melhora o fluxo, mas deixa pouco amortecedor. A decisão não pode usar apenas “dívida zerada” como métrica de sucesso.

## 5. Caso 4 — redução de dívida sem resolver déficit

Premissas:
- renda: R$ 7.000;
- essenciais: R$ 5.000;
- serviço antes: R$ 4.000;
- dívida: R$ 200.000;
- aplicação: R$ 60.000;
- serviço após simulação: R$ 2.500;
- liquidez remanescente: R$ 40.000.

Antes:

**FLUXO_LIVRE = −R$ 2.000**

Depois:

**FLUXO_LIVRE = −R$ 500**

Se nada mudar:

**40.000 / 500 = 80 meses** de cobertura matemática do déficit.

Leitura: o capital posterga a exaustão, mas o déficit permanece estrutural. Os 80 meses não são prazo recomendado de plano.

## 6. Caso 5 — capital maior que a dívida não encerra a análise

Premissas:
- saldo total para quitação: R$ 80.000;
- capital: R$ 100.000;
- despesas essenciais, reserva anterior e risco de renda: ainda não conhecidos.

Uma quitação deixaria R$ 20.000.

Leitura:
- matematicamente, o capital cobre o saldo;
- financeiramente, ainda é preciso testar liquidez e sustentabilidade;
- juridicamente, a EA-000003-000007 avaliará se a impossibilidade manifesta de pagamento persiste.

## 7. Caso 6 — capital muito inferior ao estoque

Premissas:
- saldo total elegível: R$ 300.000;
- capital: R$ 100.000;
- fluxo mensal continua deficitário.

Mesmo aplicando integralmente o capital, restariam R$ 200.000 de estoque, antes de considerar encargos e condições de negociação.

Leitura: a melhora patrimonial é relevante, mas não demonstra solução estrutural.

## 8. Competências CFP®

### SABER
- diferenciar estoque e fluxo;
- interpretar patrimônio líquido, solvência, liquidez e serviço da dívida;
- compreender CET e saldo para quitação;
- distinguir reserva de capital para pagamento;
- reconhecer limites jurídicos da atuação financeira.

### FAZER
- construir linha de base antes/depois;
- reconciliar dívidas;
- simular quitação/amortização;
- calcular fluxo livre e cobertura;
- testar exaustão do capital;
- documentar premissas e incertezas.

### DECIDIR
- quando preservar liquidez antes de pagar;
- quando uma intervenção apenas posterga déficit;
- quando exigir simulação do credor;
- quando a análise é NÃO AVALIÁVEL;
- quando encaminhar conclusão jurídica ao PRJ-000003.

## 9. Protocolo de entrega ao jurídico

Para cada cenário, entregar:

1. data-base;
2. valor da indenização ainda disponível;
3. renda recorrente;
4. despesas essenciais;
5. dívida elegível e não elegível separadas;
6. saldo para quitação;
7. serviço mensal antes/depois;
8. liquidez antes/depois;
9. fluxo livre antes/depois;
10. prazo de exaustão se houver déficit;
11. premissas;
12. dados ausentes;
13. cenários alternativos.

Não escrever no relatório financeiro:
- “a ação é cabível”;
- “o consumidor deixou de ser superendividado”;
- “esse valor é mínimo existencial”;
- “o credor tem direito a X”.

## 10. Gate da Fase 05

**SATISFEITO.**

Foram produzidos seis casos progressivos, cálculos reproduzíveis, competências SABER/FAZER/DECIDIR e protocolo formal de interoperabilidade jurídica.

## 11. Próxima fase

**Fase 06/06 — Publicação, auditoria e atualização.**
