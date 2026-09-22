# EA-000004-000040 — Revisão da Home, tipografia e responsividade

**Status:** EM EXECUÇÃO

## Plano de Fases
1. **Fase 01/04 [F-000004-000040-001] — Diagnóstico visual e de conteúdo** — EM EXECUÇÃO.
2. **Fase 02/04 [F-000004-000040-002] — Correção de Home e escala tipográfica** — PENDENTE.
3. **Fase 03/04 [F-000004-000040-003] — Auditoria responsiva e regressiva** — PENDENTE.
4. **Fase 04/04 [F-000004-000040-004] — Deploy, verificação e fechamento** — PENDENTE.

## Evidência inicial
- `h1`: até 5rem;
- `.home-hero h1`: até 6,5rem;
- `.home-main`: flex em linha contendo hero + nota institucional;
- captura mobile mostra a nota projetada para fora da viewport;
- `SITE_STYLE_GUIDE.md` exige ausência de overflow geral no mobile.

## Gate
Nenhuma página deve depender de títulos desproporcionais nem provocar overflow horizontal geral; a Home deve permanecer institucional, enxuta e representativa do escopo atual.
