# Fase 03/06 — Cenários de destinação do capital no superendividamento

**Estratégia:** EA-000004-000022 — Impacto financeiro da indenização trabalhista no diagnóstico e no plano de superendividamento  
**Data:** 21/09/2026  
**Estado:** CONCLUÍDA

## 1. Objetivo

Comparar usos possíveis dos R$ 100.000,00 sem presumir obrigação jurídica de escolher qualquer cenário e sem inventar saldos, parcelas, renda ou despesas.

## 2. Variáveis

K = 100.000 — capital extraordinário líquido  
R = lacuna de reserva necessária — DADO_AUSENTE  
E = despesas previsíveis — DADO_AUSENTE  
D = saldo total elegível das dívidas — DADO_AUSENTE  
Q_i = saldo para quitação da dívida i  
P_i = parcela mensal da dívida i  
A = valor efetivamente aplicado a dívidas  
L = liquidez remanescente

Regra básica: **L = K - A**.

Nenhum cenário pode usar o mesmo real simultaneamente como reserva e pagamento de dívida.

## 3. Cenário A — preservação integral temporária

A = 0  
L = 100.000

Efeito imediato:
- dívida: inalterada;
- serviço mensal: inalterado;
- fluxo livre: inalterado;
- liquidez: máxima entre os cenários;
- tempo para diagnóstico: maior.

É cenário de referência, não recomendação automática.

## 4. Cenário B — reserva/despesas primeiro, saldo decisório depois

CAPITAL_DECISORIO = máximo entre zero e 100.000 - R - E.

Somente o capital decisório pode ser comparado com quitação/amortização sem destruir funções de liquidez já reconhecidas.

Como R e E são DADO_AUSENTE, o capital decisório é atualmente **NÃO_CALCULÁVEL**.

## 5. Cenário C — quitação seletiva

Para uma dívida i:

A = Q_i  
L = 100.000 - Q_i

A quitação só pode ser analisada com saldo real para quitação, CET, parcela eliminada, garantia, atraso e demais consequências.

O serviço mensal novo só cai pela parcela efetivamente eliminada.

## 6. Cenário D — amortização seletiva

A = VALOR_AMORTIZADO  
L = 100.000 - A

Não presumir o efeito. É necessário obter do credor simulação com nova parcela, novo prazo, custo total e redução de encargos.

## 7. Cenário E — entrada extraordinária em proposta global

A = ENTRADA_GLOBAL  
L = 100.000 - A

Financeiramente, avaliar:
- redução do estoque;
- novo serviço mensal total;
- custo total do plano;
- liquidez remanescente;
- fluxo livre posterior.

Admissibilidade jurídica e distribuição entre credores pertencem à **EA-000003-000007**.

## 8. Cenário F — combinação reserva + pagamento

A = 100.000 - R - E - COLCHAO_ADICIONAL, com piso zero.

Esse cenário evita tratar todo o capital como disponível para dívida.

O colchão adicional depende de risco de renda, dependentes e incertezas; não recebe percentual arbitrário.

## 9. Cenário G — pagamento proporcional hipotético

Se houver critério jurídico ou negocial que autorize distribuição proporcional:

PESO_i = SALDO_i / SOMA_SALDOS_ELEGIVEIS  
PAGAMENTO_i = A × PESO_i

Essa proporcionalidade não é regra jurídica criada pelo Planejamento Financeiro. É apenas ferramenta matemática.

## 10. Métricas comuns

Para cada cenário registrar:
- liquidez remanescente;
- saldo total das dívidas após;
- serviço mensal das dívidas após;
- fluxo livre após;
- cobertura de despesas após;
- custo total remanescente;
- garantias liberadas ou mantidas;
- data-base.

## 11. Teste de sustentabilidade

Cenário que reduz dívida, mas mantém **FLUXO_LIVRE_APOS < 0**, não resolve por si a causa estrutural.

Cenário que elimina muitas dívidas, mas deixa **LIQUIDEZ_REMANESCENTE = 0**, precisa ser testado contra despesas essenciais, renda instável e choques previsíveis.

## 12. Matriz qualitativa

| Cenário | Liquidez | Estoque da dívida | Parcela mensal | Risco de recaída |
|---|---|---|---|---|
| preservar integral | alta | igual | igual | depende do déficit |
| reservar e depois decidir | preservada | inicialmente igual | inicialmente igual | menor se reserva adequada |
| quitar seletivamente | cai | reduz | pode reduzir muito | depende da dívida e fluxo |
| amortizar | cai | reduz | depende da simulação | depende do efeito contratual |
| entrada global | cai | reduz conforme plano | depende do plano | depende da sustentabilidade |
| combinação | intermediária | reduz | pode reduzir | testável |
| proporcional hipotético | cai | reduz distribuído | depende dos contratos | testável |

## 13. Travas

- nenhuma dívida presumida;
- nenhum percentual fixo de reserva;
- nenhum percentual fixo a credores;
- nenhuma equivalência entre capital recebido e capacidade de pagamento integral;
- nenhum cenário recebe rótulo de melhor sem dados;
- plano jurídico não é desenhado pelo planejador financeiro.

## 14. Entrega à estratégia jurídica

A EA-000003-000007 recebe catálogo de cenários, fórmulas, variáveis ausentes, efeitos econômicos esperados e alertas de sustentabilidade.

Ela decidirá quais cenários são juridicamente admissíveis, necessários ou irrelevantes.

## 15. Gate da Fase 03

**SATISFEITO.**

Foram modelados sete cenários sem dados fictícios, com fórmulas, métricas comuns, trava contra dupla contagem e interface jurídica explícita.

## 16. Próxima fase

**Fase 04/06 — Sustentabilidade do plano após uso do capital.**
