# Plano de Fases — EA-000004-000030

## Estratégia
**EA-000004-000030 — Auditoria regressiva pós-correção do Site Planejamento Financeiro**

## Objetivo
Verificar se o ciclo corretivo do Relatório do Planejador Financeiro do Diabo introduziu regressões, deixou inconsistências residuais ou publicou conteúdo divergente do repositório, com foco em conteúdo servido, paridade Markdown–HTML, fórmulas, CFP®, perímetro profissional, privacidade e navegação.

## FASE 01/05 [F-000004-000030-001] — Estado publicado e inventário de superfície
Confirmar o deployment vigente, inventariar a superfície pública e selecionar páginas críticas para verificação externa.
**Gate:** estado público e corpus regressivo definidos.

## FASE 02/05 [F-000004-000030-002] — Verificação HTTP do conteúdo servido
Abrir diretamente as rotas públicas críticas e confirmar que as correções materialmente importantes estão efetivamente servidas.
**Gate:** amostra crítica pública verificada fora do repositório.

## FASE 03/05 [F-000004-000030-003] — Regressão semântica e quantitativa
Testar reaparecimento de fórmulas antigas, premissas inválidas, divergências de risco/suitability, heurísticas sem rótulo, halo CFP® e estados incompatíveis.
**Gate:** matriz de regressões concluída.

## FASE 04/05 [F-000004-000030-004] — Navegação, privacidade e integridade editorial
Revalidar links internos, rotas novas, ausência de vazamento de governança e coerência entre Home, CFP®, Conhecimentos, Mapa, Fale Conosco e Privacidade.
**Gate:** superfície editorial e institucional sem regressões materiais.

## FASE 05/05 [F-000004-000030-005] — Relatório regressivo e estado
Consolidar achados, corrigir regressões se existirem, registrar o resultado e atualizar o estado do Projeto.
**Gate:** relatório persistido e estratégia encerrada.
