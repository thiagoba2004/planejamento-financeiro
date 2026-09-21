# Plano de Fases — EA-000004-000027

## Estratégia
**EA-000004-000027 — Protocolo canônico de métricas, fórmulas e casos reproduzíveis**

## Objetivo
Tornar cada cálculo auditável por data-base, unidade, horizonte, premissas, tratamento de limites e valor do dinheiro no tempo.

## FASE 01/06 [F-000004-000027-001] — Protocolo canônico de métricas
Criar ficha para cada métrica: origem, fórmula, unidade, data-base, horizonte, denominadores-limite, interpretação e limitações.
**Gate:** protocolo persistido.

## FASE 02/06 [F-000004-000027-002] — Objetivos e proteção no tempo
Corrigir gap de objetivos e gap de proteção com equivalência temporal e prevenção de dupla contagem.
**Gate:** fórmulas usam uma única data-base ou mapa temporal explícito.

## FASE 03/06 [F-000004-000027-003] — Dívidas e runway
Separar mínimo contratual de serviço planejado e reclassificar meses até exaustão como estimativa estática de primeira ordem.
**Gate:** linguagem não transforma aproximação em projeção.

## FASE 04/06 [F-000004-000027-004] — Valuation e renda empresarial
Rotular ponte FCFF simplificada, incluir ajustes e corrigir metodologia de renda empresarial sustentável.
**Gate:** fórmulas empresariais não são apresentadas como universais.

## FASE 05/06 [F-000004-000027-005] — Casos quantitativos reproduzíveis
Padronizar inputs → fórmula → intervenção → resultado → interpretação e corrigir hipóteses implícitas.
**Gate:** casos centrais podem ser recalculados por terceiro.

## FASE 06/06 [F-000004-000027-006] — Auditoria matemática
Validar cálculos, limites, unidades, dupla contagem e paridade Markdown/HTML.
**Gate:** auditoria quantitativa aprovada.
