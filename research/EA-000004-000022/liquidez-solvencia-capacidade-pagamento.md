# Fase 02/06 — Liquidez, solvência e capacidade de pagamento

**Estratégia:** EA-000004-000022 — Impacto financeiro da indenização trabalhista no diagnóstico e no plano de superendividamento  
**Data:** 21/09/2026  
**Estado:** CONCLUÍDA

## 1. Objetivo

Demonstrar quais métricas mudam imediatamente com o recebimento de R$ 100.000,00 líquidos e quais permanecem inalteradas até que o capital seja efetivamente destinado a dívidas ou despesas.

A metodologia reutiliza o dicionário de métricas da EA-000004-000001 e a linha de base da Fase 01 desta estratégia.

## 2. Regra central

A indenização é um **choque positivo de estoque**, não um aumento automático de renda mensal.

Isso produz uma assimetria:

| Dimensão | Efeito direto |
|---|---|
| caixa/liquidez | aumenta |
| ativos totais | aumenta |
| patrimônio líquido | aumenta |
| solvência patrimonial | melhora, se houver passivo positivo |
| renda recorrente | não muda |
| serviço mensal da dívida | não muda |
| fluxo livre mensal | não muda |
| comprometimento mensal da renda | não muda |

## 3. Patrimônio líquido

    PL_ANTES = ATIVOS_ANTES - PASSIVOS_ANTES
    PL_DEPOIS = PL_ANTES + 100.000

O incremento é conhecido mesmo sem conhecer o PL absoluto.

## 4. Solvência

Para passivos totais positivos:

    SOLVENCIA_ANTES = ATIVOS_ANTES / PASSIVOS_TOTAIS
    SOLVENCIA_DEPOIS = (ATIVOS_ANTES + 100.000) / PASSIVOS_TOTAIS

Logo:

    DELTA_SOLVENCIA = 100.000 / PASSIVOS_TOTAIS

O recebimento melhora a razão de solvência, mas o valor exato é não calculável sem passivos totais.

Se PASSIVOS_TOTAIS = 0:
- registrar SEM_PASSIVO;
- não reportar razão infinita.

## 5. Liquidez corrente

Se os R$ 100.000,00 permanecem em ativo de curto prazo:

    LIQUIDEZ_CORRENTE_ANTES
    = ATIVOS_CP_ANTES / PASSIVOS_CP

    LIQUIDEZ_CORRENTE_DEPOIS
    = (ATIVOS_CP_ANTES + 100.000) / PASSIVOS_CP

Para PASSIVOS_CP > 0:

    DELTA_LIQUIDEZ_CORRENTE
    = 100.000 / PASSIVOS_CP

A melhora de liquidez pode ser grande e ainda coexistir com fluxo mensal deficitário.

## 6. Cobertura de despesas essenciais

    COBERTURA_MESES_ANTES
    = ATIVOS_LIQUIDOS_ANTES / DESPESAS_ESSENCIAIS_MENSAIS

    COBERTURA_MESES_DEPOIS
    = (ATIVOS_LIQUIDOS_ANTES + 100.000)
      / DESPESAS_ESSENCIAIS_MENSAIS

Para despesas essenciais positivas:

    DELTA_COBERTURA_MESES
    = 100.000 / DESPESAS_ESSENCIAIS_MENSAIS

Essa métrica indica amortecedor de liquidez, não quantidade juridicamente "protegida".

## 7. Serviço da dívida sobre renda

    DSR = SERVICO_MENSAL_DA_DIVIDA / RENDA_LIQUIDA_MENSAL

No instante do recebimento:

    DSR_DEPOIS = DSR_ANTES

porque a indenização:
- não aumenta a renda recorrente;
- não reduz automaticamente as parcelas.

O índice só muda se houver amortização, quitação, renegociação ou mudança de renda.

## 8. Fluxo livre mensal

    FLUXO_LIVRE
    = RENDA_LIQUIDA
    - DESPESAS_ESSENCIAIS
    - SERVICO_MENSAL_DA_DIVIDA

No efeito direto:

    FLUXO_LIVRE_DEPOIS = FLUXO_LIVRE_ANTES

Portanto, o consumidor pode receber R$ 100.000,00 e continuar com:

    FLUXO_LIVRE < 0

A liquidez nova pode financiar esse déficit por algum tempo, mas isso não o torna sustentável.

## 9. Tempo de sobrevivência de um déficit

Se o fluxo livre mensal for negativo e o capital fosse usado apenas para cobri-lo:

    MESES_DE_COBERTURA_DO_DEFICIT
    = 100.000 / ABS(FLUXO_LIVRE_MENSAL)

Essa métrica é apenas uma medida de consumo do capital.

Ela **não** significa:
- reserva recomendada;
- prazo sustentável de plano;
- capacidade recorrente;
- mínimo existencial;
- solução do superendividamento.

## 10. Capacidade de pagamento mensal × capacidade patrimonial

### Capacidade mensal recorrente

Depende de:

    RENDA_RECORRENTE
    - DESPESAS_ESSENCIAIS
    - OUTRAS_OBRIGACOES
    - MARGEM_DE_SEGURANCA

Não é criada pela indenização.

### Capacidade patrimonial extraordinária

O capital máximo bruto disponível no evento é:

    CAPITAL_EXTRAORDINARIO_BRUTO_DISPONIVEL = 100.000

Mas o valor economicamente utilizável para credores só pode ser definido depois de considerar:
- reserva já existente;
- lacuna de reserva;
- despesas previsíveis;
- riscos de renda;
- necessidades dependentes;
- custos de transição;
- consequências de cada dívida.

Logo:

    CAPITAL_SUSTENTAVEL_PARA_DIVIDAS
    = NÃO_CALCULÁVEL NESTA FASE

## 11. Três estados possíveis após o recebimento

### Estado A — melhora patrimonial e melhora de liquidez, fluxo ainda negativo

O capital posterga a crise, mas não resolve a causa.

### Estado B — melhora patrimonial e possibilidade de reestruturação

Parte do capital pode reduzir estoque e/ou serviço da dívida, com potencial de tornar o fluxo sustentável.

### Estado C — ativos passam a ser suficientes para extinguir passivos

Mesmo nesse caso:
- a decisão de quitar tudo não é automática;
- é necessário preservar liquidez e testar obrigações excluídas/contestadas;
- a conclusão jurídica sobre superendividamento pertence ao PRJ-000003.

## 12. Métricas que serão entregues à estratégia jurídica

| Métrica | Estado atual |
|---|---|
| incremento patrimonial | +R$ 100.000,00 |
| incremento de liquidez | +R$ 100.000,00 |
| solvência após | fórmula disponível; valor não calculável |
| liquidez corrente após | fórmula disponível; valor não calculável |
| cobertura de despesas | fórmula disponível; valor não calculável |
| DSR | não muda diretamente; valor não calculável |
| fluxo livre | não muda diretamente; valor não calculável |
| capital sustentável para dívidas | NÃO_CALCULÁVEL |

## 13. Erros proibidos

- somar R$ 100.000,00 à renda anual ou mensal;
- considerar que patrimônio positivo resolve fluxo negativo;
- chamar todo o capital de "capacidade de pagamento";
- usar os R$ 100.000,00 para quitar dívidas antes de dimensionar liquidez;
- tratar melhora de solvência como conclusão jurídica de ausência de superendividamento;
- transformar meses de cobertura de déficit em prazo recomendado de plano.

## 14. Gate da Fase 02

**SATISFEITO.**

Foram definidos:
- efeitos sobre liquidez e solvência;
- invariância inicial de DSR e fluxo livre;
- fórmula de consumo do capital em déficit;
- separação entre capacidade mensal e patrimonial;
- métricas de interoperabilidade com o PRJ-000003.

## 15. Próxima fase

**Fase 03/06 — Cenários de destinação do capital no superendividamento.**
