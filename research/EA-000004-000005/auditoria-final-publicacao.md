# Auditoria final de publicação — Diagnóstico financeiro da ruptura

**Projeto:** Planejamento Financeiro  
**Estratégia:** EA-000004-000005 — Diagnóstico financeiro da ruptura e orçamento de transição  
**Data:** 20/09/2026  
**Fase:** 06/06 — Publicação, auditoria e atualização

## 1. Conteúdo produzido

A estratégia produziu:
- delimitação com 42 perguntas de diagnóstico;
- inventário de dados e linha de base;
- template tabular da linha de base;
- metodologia de fluxo e cenários de 30, 90 e 365 dias;
- template de cenários;
- calendário de eventos;
- teste numérico reproduzível;
- metodologia de liquidez e reserva de transição;
- template de fontes de liquidez;
- calendário de obrigações;
- quatro casos progressivos;
- matriz de competências;
- unidade pública em Markdown + HTML + JSON.

## 2. Integração pública

A nova unidade foi integrada em:
- Conhecimentos;
- Casos;
- Ferramentas;
- Mapa do Site.

A Home permaneceu institucional e sem catálogo.

## 3. Workflow

O workflow do GitHub Pages já possuía cobertura correta:
- gatilho para `temas/**`;
- diretório `_site/temas`;
- cópia `cp temas/*.html _site/temas/`.

Não foi necessária alteração no workflow.

## 4. Auditoria HTML

Páginas HTML auditadas: **13**.  
Referências `href` examinadas: **200**.

Resultados:
- arquivos internos inexistentes: **0**;
- âncoras locais quebradas: **0**;
- âncoras cruzadas verificadas nos novos fluxos: **0 quebras**;
- divergências no Menu global: **0**;
- marcadores de governança interna: **0**;
- ocorrências públicas de “ACESSAR →” ou “ACESSAR ->”: **0**.

Menu global verificado:
**Início · CFP® · Conhecimentos · Casos · Ferramentas · Fontes · Fale Conosco**.

## 5. Semântica de interação

Confirmado:
- ações reais do Fale Conosco usam `action-button`;
- navegação destacada usa `nav-button`;
- links comuns permanecem links;
- cards clicáveis são `a.resource-card`;
- cards informativos são `article.resource-card`;
- diferenciação cromática entre cards clicáveis e informativos permanece vigente.

## 6. Cálculos

O fixture de cenários foi verificado para duas hipóteses:

| Métrica | Cenário A | Cenário B |
|---|---:|---:|
| saídas recorrentes/mês | R$ 7.000 | R$ 7.500 |
| saldo operacional/mês | R$ 1.000 | R$ 500 |
| caixa 30 dias | R$ 9.000 | R$ 8.500 |
| caixa 90 dias | R$ 9.000 | R$ 7.500 |
| caixa 365 dias | R$ 12.000 | R$ 6.000 |

O objetivo do teste é validar a mecânica do modelo, não recomendar qualquer valor real.

## 7. Limites profissionais

A unidade pública preserva expressamente que planejamento financeiro:
- não decide partilha;
- não fixa alimentos;
- não decide guarda/convivência;
- não define responsabilidade jurídica por dívidas;
- não define tributação definitiva;
- não prevê decisão judicial.

O tema “divórcio” é apresentado como caso profissional aplicado, e não como objetivo literal do exame CFP® sem fonte oficial específica.

## 8. Deploy

- commit público: **e8a0f1c756ee9523478f29227fc32506f7b75a39**;
- workflow run: **35541592376**;
- conclusão: **success**.

## 9. Gate final

**SATISFEITO.**

A estratégia possui artefatos sincronizados, cálculos reproduzíveis, integração interprojetos, publicação auditada e deploy confirmado.

**Estado final: CONCLUÍDA.**
