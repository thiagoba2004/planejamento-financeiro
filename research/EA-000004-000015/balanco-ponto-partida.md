# Fase 04/06 — Incorporação ao balanço e ponto de partida financeiro

**Estratégia:** EA-000004-000015 — Recebimento da indenização: documentação, tratamento declaratório e incorporação do capital líquido  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Regra de incorporação

O cenário confirma:

CAPITAL_LIQUIDO_RECEBIDO = R$ 100.000,00
DISPONIBILIDADE = INTEGRAL
RENDA_RECORRENTE = NÃO

O valor entra no planejamento como **ativo financeiro líquido extraordinário**.

## 2. Efeito incremental certo

Sem inventar o patrimônio anterior:

CAIXA_APÓS = CAIXA_ANTES + R$ 100.000,00

e, inexistindo passivo criado pelo próprio recebimento:

PATRIMÔNIO_LÍQUIDO_APÓS = PATRIMÔNIO_LÍQUIDO_ANTES + R$ 100.000,00

A fórmula registra apenas o efeito incremental do evento.

## 3. O que permanece desconhecido

| Variável | Estado |
|---|---|
| patrimônio financeiro anterior | DADO_AUSENTE |
| imóveis e outros ativos | DADO_AUSENTE |
| dívidas | DADO_AUSENTE |
| renda recorrente mensal | DADO_AUSENTE |
| despesas essenciais | DADO_AUSENTE |
| reserva prévia | DADO_AUSENTE |
| capacidade mensal de poupança | DADO_AUSENTE |
| objetivos | DADO_AUSENTE |
| perfil de risco | DADO_AUSENTE |
| dependentes | DADO_AUSENTE |

A ausência desses dados não impede registrar o evento, mas impede definir a alocação final.

## 4. Balanço incremental

### Antes do recebimento

ATIVOS = DADO_AUSENTE  
PASSIVOS = DADO_AUSENTE  
PATRIMÔNIO LÍQUIDO = DADO_AUSENTE

### Evento

+ R$ 100.000,00 em caixa líquido disponível

### Depois do recebimento

ATIVOS_FINANCEIROS_APÓS = ATIVOS_FINANCEIROS_ANTES + R$ 100.000,00

PATRIMÔNIO_LÍQUIDO_APÓS = PATRIMÔNIO_LÍQUIDO_ANTES + R$ 100.000,00

## 5. Não transformar capital em renda

É proibido tratar R$ 100.000,00 ÷ 12 como se fosse salário ou renda mensal recorrente.

Retiradas mensais do capital:
- reduzem patrimônio;
- podem ser planejadas;
- não transformam a origem em renda recorrente.

## 6. Primeira segmentação financeira

Ainda sem definir percentuais, o capital deverá futuramente ser testado contra cinco funções:

1. **liquidez e reserva**;
2. **dívidas**, se existirem;
3. **investimentos**;
4. **objetivos e proteção**;
5. **uso discricionário consciente**.

Nenhuma função recebe percentual automático nesta fase.

## 7. Métricas que só serão calculadas após novos dados

MESES_DE_RESERVA = RESERVA_LÍQUIDA / DESPESA_ESSENCIAL_MENSAL

COMPROMETIMENTO_DE_RENDA = SERVIÇO_MENSAL_DA_DÍVIDA / RENDA_LÍQUIDA_MENSAL

PESO_DA_INDENIZAÇÃO = 100.000 / PATRIMÔNIO_FINANCEIRO_APÓS

Essas métricas permanecem DADO_AUSENTE enquanto faltarem os denominadores.

## 8. Interface com as estratégias seguintes

### EA-000004-000016 — Liquidez
Recebe R$ 100.000,00 líquidos e a necessidade de dimensionar reserva.

### EA-000004-000017 — Dívidas
Recebe o capital disponível e um inventário de dívidas ainda ausente. Se não houver dívidas, pode ser marcada NAO_APLICAVEL_NO_CASO.

### EA-000004-000018 — Investimentos
Recebe capital extraordinário, mas não pode aplicar 100% antes de dimensionar liquidez e objetivos.

### EA-000004-000019 — Objetivos e proteção
Recebe capital disponível e mapa de objetivos ainda ausente.

### EA-000004-000020 — Comportamento
Recebe evento extraordinário e avalia risco de decisões impulsivas.

### EA-000004-000021 — Plano integrado
Receberá apenas resultados confirmados das anteriores.

## 9. Linha de base canônica

ORIGEM = INDENIZAÇÃO POR DANO MORAL TRABALHISTA
CAPITAL LÍQUIDO = R$ 100.000,00
LIQUIDEZ = INTEGRAL
RENDA RECORRENTE = NÃO
TRIBUTAÇÃO DA ORIGEM = NÃO INCIDE IR, SEGUNDO REGRA ATUAL
DECLARAÇÃO = ISENTO/NÃO TRIBUTÁVEL, COM REVALIDAÇÃO OPERACIONAL NO EXERCÍCIO APLICÁVEL
DESTINO DO CAPITAL = NÃO DEFINIDO

## 10. Gate da Fase 04

**SATISFEITO.**

Foram persistidos:
- efeito incremental de R$ 100.000,00;
- regra de incorporação ao balanço;
- variáveis desconhecidas;
- fórmulas sem dados artificiais;
- interfaces com as seis estratégias seguintes.

## 11. Próxima fase

**Fase 05/06 — Casos, comunicação e competências CFP®.**
