# Fase 03/06 — Aposentadoria e previdência

**Estratégia:** EA-000004-000019 — Objetivos de vida, aposentadoria, seguros e proteção patrimonial
**Data:** 21/09/2026
**Estado:** CONCLUÍDA

## 1. Objetivo

Avaliar como um aporte extraordinário pode reduzir a lacuna de aposentadoria e comparar veículos de acumulação sem presumir que previdência privada seja superior a investimentos ordinários.

## 2. Dados necessários

- idade atual;
- idade/data desejada de aposentadoria;
- expectativa de período de aposentadoria usada no cenário;
- renda desejada em valores reais;
- benefício previdenciário público estimado;
- benefício de previdência fechada, quando houver;
- patrimônio já acumulado;
- contribuições recorrentes;
- capacidade futura de poupança;
- inflação;
- retorno real líquido esperado;
- custos e tributação dos veículos.

No cenário-base, esses dados permanecem DADO_AUSENTE.

## 3. Gap de renda na aposentadoria

GAP_RENDA_MENSAL = RENDA_DESEJADA_REAL - BENEFICIOS_RECORRENTES_CONFIRMADOS

Benefício meramente estimado deve permanecer separado de benefício já adquirido ou documentado.

## 4. Capital necessário

O capital necessário depende de:
- renda-alvo;
- duração do período de aposentadoria;
- retorno real líquido;
- inflação;
- sequência de retornos;
- longevidade;
- tributação;
- margem de segurança.

Não existe multiplicador universal de renda.

Uma formulação genérica é calcular o valor presente dos fluxos reais projetados de aposentadoria, sob premissas explícitas e revisáveis.

## 5. Impacto do aporte extraordinário

Se A for a parcela do capital extraordinário destinada à aposentadoria:

GAP_PATRIMONIAL_APOS = máximo(0 ; GAP_PATRIMONIAL_ANTES - A)

e o impacto sobre aportes futuros deve ser recalculado pelo prazo remanescente.

O aporte único reduz a lacuna patrimonial, mas não substitui automaticamente a necessidade de poupança recorrente.

## 6. Veículos possíveis

### Previdência complementar fechada

Pode ter contribuição do patrocinador e regras específicas de vesting, benefício, portabilidade, resgate e autopatrocínio. O regulamento é fonte central.

Fontes: PF-SRC-000049 e PF-SRC-000050.

### PGBL

É plano de previdência complementar aberta. A fonte oficial SUSEP informa que, observadas as condições fiscais aplicáveis, contribuições podem ser dedutíveis até o limite legal; no resgate/benefício, a base tributável alcança o valor recebido conforme o regime aplicável.

Fontes: PF-SRC-000080 e PF-SRC-000081.

### VGBL

É seguro de pessoas com cobertura por sobrevivência. Não gera a mesma dedução de contribuições do PGBL; no resgate/benefício, a incidência tributária se dá sobre rendimentos conforme o regime aplicável.

Fontes: PF-SRC-000080 e PF-SRC-000081.

### Investimentos fora de previdência

Podem ser apropriados conforme objetivo, horizonte, custos, tributação, liquidez e perfil. Devem ser comparados líquidos de custos e impostos, sem assumir que previdência sempre ganha ou sempre perde.

## 7. Escolha do regime tributário

A Lei nº 14.803/2024 alterou a regra temporal de opção do regime tributário, permitindo a escolha até a obtenção do benefício ou o primeiro resgate, nas hipóteses legais.

Fonte: PF-SRC-000083.

A estratégia não antecipa qual regime será melhor sem conhecer prazo de acumulação, renda futura e forma de recebimento.

## 8. Matriz de comparação

| Critério | Previdência fechada | PGBL | VGBL | Investimento ordinário |
|---|---|---|---|---|
| contribuição patronal | pode existir | não | não | não |
| benefício fiscal de entrada | depende do regime | pode existir | não equivalente | depende do ativo |
| tributação na saída | conforme regras do plano/regime | sobre base aplicável | sobre rendimentos conforme regra | depende do ativo |
| portabilidade | conforme regras | possível entre planos compatíveis | possível entre planos compatíveis | não é o mesmo instituto |
| liquidez | regulamento | regulamento/carência | regulamento/carência | depende do produto |
| custos | regulamento | taxa/fundo/plano | taxa/fundo/plano | depende do produto |
| sucessão/beneficiários | análise específica | análise específica | análise específica | análise jurídica específica |

## 9. Cenários

### Cenário A — aporte único
Parte do capital reduz o gap patrimonial, sem criar contribuição recorrente.

### Cenário B — aporte + contribuição recorrente
O capital extraordinário reduz a lacuna inicial e a renda futura sustenta aportes periódicos.

### Cenário C — sem aporte extraordinário
O capital é preservado para objetivos mais prioritários e a aposentadoria continua financiada por fluxo futuro.

### Cenário D — contribuição patronal relevante
Se houver plano patrocinado, deve-se comparar o valor econômico da contrapartida antes de direcionar recursos a outro veículo.

## 10. Gate da Fase 03

**SATISFEITO.**

Foram documentados gap de renda, gap patrimonial, efeito do aporte extraordinário, comparação entre previdência fechada, PGBL, VGBL e investimentos ordinários e regra tributária atualizada, sem presumir vantagem de veículo.

## 11. Próxima fase

**Fase 04/06 — Seguros e proteção financeira.**
