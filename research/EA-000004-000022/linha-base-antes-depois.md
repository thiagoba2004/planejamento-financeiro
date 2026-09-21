# Fase 01/06 — Linha de base antes e depois da indenização

**Estratégia:** EA-000004-000022 — Impacto financeiro da indenização trabalhista no diagnóstico e no plano de superendividamento  
**Data:** 21/09/2026  
**Estado:** CONCLUÍDA

## 1. Objetivo

Criar uma fotografia financeira imediatamente anterior e imediatamente posterior ao recebimento de **R$ 100.000,00 líquidos e integralmente disponíveis**, sem confundir o capital extraordinário com renda recorrente e sem inventar dívidas, renda, despesas ou reservas.

## 2. Premissas confirmadas

    ORIGEM = INDENIZAÇÃO POR DANO MORAL TRABALHISTA
    CAPITAL_LIQUIDO_RECEBIDO = R$ 100.000,00
    DISPONIBILIDADE = INTEGRAL
    RENDA_RECORRENTE_GERADA_PELO_RECEBIMENTO = NÃO

## 3. Linha de base — imediatamente antes

| Variável | Estado |
|---|---|
| ativos financeiros líquidos | DADO_AUSENTE |
| demais ativos | DADO_AUSENTE |
| passivos totais | DADO_AUSENTE |
| passivos de curto prazo | DADO_AUSENTE |
| saldo para quitação das dívidas | DADO_AUSENTE |
| renda líquida mensal | DADO_AUSENTE |
| despesas essenciais mensais | DADO_AUSENTE |
| serviço mensal das dívidas | DADO_AUSENTE |
| reserva prévia | DADO_AUSENTE |
| patrimônio líquido | NÃO_CALCULÁVEL |
| fluxo livre mensal | NÃO_CALCULÁVEL |
| cobertura de despesas por ativos líquidos | NÃO_CALCULÁVEL |
| solvência | NÃO_CALCULÁVEL |

## 4. Efeito incremental certo do recebimento

    ATIVOS_LIQUIDOS_DEPOIS = ATIVOS_LIQUIDOS_ANTES + 100.000
    ATIVOS_TOTAIS_DEPOIS = ATIVOS_TOTAIS_ANTES + 100.000
    PASSIVOS_TOTAIS_DEPOIS = PASSIVOS_TOTAIS_ANTES
    PATRIMONIO_LIQUIDO_DEPOIS = PATRIMONIO_LIQUIDO_ANTES + 100.000

Essas fórmulas só descrevem o efeito incremental do evento.

## 5. O que não muda automaticamente

O recebimento, isoladamente, não altera renda líquida mensal recorrente, despesas essenciais mensais, valor contratual das parcelas, CET das dívidas, prazo contratual, garantias, existência de atrasos ou número de credores.

Portanto:

    RENDA_LIQUIDA_MENSAL_DEPOIS = RENDA_LIQUIDA_MENSAL_ANTES
    SERVICO_MENSAL_DA_DIVIDA_DEPOIS = SERVICO_MENSAL_DA_DIVIDA_ANTES

até que haja uso efetivo do capital para modificar as dívidas ou outro fato econômico.

## 6. Métricas antes e imediatamente depois

### Patrimônio líquido
    PL_ANTES = ATIVOS_ANTES - PASSIVOS_ANTES
    PL_DEPOIS = PL_ANTES + 100.000

### Solvência
    SOLVENCIA_ANTES = ATIVOS_ANTES / PASSIVOS_ANTES
    SOLVENCIA_DEPOIS = (ATIVOS_ANTES + 100.000) / PASSIVOS_ANTES

### Liquidez corrente
Se os R$ 100.000,00 forem classificados como ativo de curto prazo:

    LIQUIDEZ_CORRENTE_DEPOIS = (ATIVOS_CP_ANTES + 100.000) / PASSIVOS_CP

### Cobertura de despesas
    COBERTURA_MESES_DEPOIS = (ATIVOS_LIQUIDOS_ANTES + 100.000) / DESPESAS_ESSENCIAIS_MENSAIS

### Serviço da dívida sobre renda
    DSR_DEPOIS = SERVICO_MENSAL_DA_DIVIDA / RENDA_LIQUIDA_MENSAL

**O recebimento sozinho não reduz esse índice**, porque nem a parcela nem a renda recorrente mudam até haver intervenção.

### Fluxo livre mensal
    FLUXO_LIVRE_DEPOIS = RENDA_LIQUIDA - DESPESAS_ESSENCIAIS - SERVICO_MENSAL_DA_DIVIDA

**O recebimento sozinho não transforma déficit mensal em superávit mensal.** Ele cria um estoque de liquidez capaz de financiar transição ou reestruturação, mas um déficit estrutural pode continuar existindo.

## 7. Distinção crítica: estoque × fluxo

A indenização modifica imediatamente o **estoque patrimonial**. Ela não modifica automaticamente o **fluxo recorrente**.

Assim:
- um consumidor pode ficar mais solvente e continuar com fluxo mensal negativo;
- pode ganhar liquidez e ainda enfrentar parcelas incompatíveis com renda;
- pode usar o capital para quitar dívidas e depois voltar a déficit se a causa estrutural permanecer;
- pode preservar parte do capital como reserva e utilizar outra parte para reorganização.

## 8. Linha de base pós-evento

    CAPITAL_EXTRAORDINARIO = 100.000
    PL_INCREMENTAL = +100.000
    LIQUIDEZ_INCREMENTAL = +100.000
    RENDA_RECORRENTE_INCREMENTAL = 0
    DESPESA_RECORRENTE_INCREMENTAL = 0
    SERVICO_DA_DIVIDA_INCREMENTAL = 0

Os três últimos permanecem zero **apenas como efeito direto do recebimento**, não como valores absolutos do caso.

## 9. Dados necessários para avançar

1. ativos líquidos antes do recebimento;
2. outros ativos;
3. passivos totais;
4. passivos de curto prazo;
5. saldo para quitação de cada dívida;
6. parcelas mensais;
7. renda líquida mensal;
8. despesas essenciais mensais;
9. despesas não essenciais recorrentes;
10. reserva anterior;
11. atrasos;
12. garantias;
13. custo das dívidas;
14. objetivos de curto prazo;
15. riscos de renda;
16. dependentes e necessidades especiais.

## 10. Interface jurídica

A estratégia financeira não conclui se o consumidor continua juridicamente superendividado, se os R$ 100.000,00 integram integralmente a capacidade de pagamento, qual valor deve ser preservado como mínimo existencial, se existe dever jurídico de informar ou se o plano deve ser revisto.

Ela fornece números e cenários à EA-000003-000007.

## 11. Gate da Fase 01

**SATISFEITO.**

Foram produzidos fotografia antes/depois, efeito incremental certo, separação entre estoque e fluxo, métricas reproduzíveis, lista de dados ausentes e limites da interface jurídica.

## 12. Próxima fase

**Fase 02/06 — Liquidez, solvência e capacidade de pagamento.**
