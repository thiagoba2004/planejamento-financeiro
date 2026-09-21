# Auditoria final de publicação — EA-000004-000017

**Estratégia:** EA-000004-000017 — Dívidas, crédito e prioridade de uso do capital indenizatório  
**Fase:** 06/06 — Publicação, auditoria e atualização  
**Data:** 21/09/2026  
**Estado:** APROVADA

## 1. Artefatos publicados

- `temas/dividas-capital-indenizatorio.md`
- `temas/dividas-capital-indenizatorio.html`
- `research/EA-000004-000017/casos-competencias-cfp.md`

Integrações públicas:
- Conhecimentos;
- Gestão Financeira;
- Casos;
- Ferramentas;
- Fontes;
- Mapa do Site.

## 2. Auditoria estrutural do site público

Foram verificados **24 arquivos HTML**.

Resultado consolidado:
- links `href` em elementos `<a>`: **513**;
- links internos: **434**;
- links externos: **79**;
- links internos quebrados: **0**;
- vazamentos de arquivos de governança: **0**;
- ocorrências do padrão proibido `ACESSAR →` / `ACESSAR ->`: **0**;
- páginas com quantidade divergente do menu global de 7 itens: **0**.

A auditoria foi executada em três blocos de oito HTMLs por limite operacional do conector, preservando o universo integral de 24 arquivos.

## 3. Âncoras da nova unidade

Âncoras exigidas e encontradas:

- `#inventario`
- `#cet`
- `#cenarios`
- `#prioridade`
- `#oportunidade`
- `#casos`
- `#cfp`
- `#fontes`

Âncoras ausentes: **0**.

## 4. Conteúdo e metodologia

Verificado que:
- o cenário-base mantém existência de dívidas como `DADO_AUSENTE`;
- ausência de informação não é convertida em saldo zero;
- casos didáticos estão identificados como hipóteses próprias;
- CET, saldo de quitação, fluxo, garantia e custo de oportunidade permanecem separados;
- não há regra universal de “quitar toda dívida”;
- reserva, despesas previsíveis e liquidez precedem a liberação de capital decisório;
- não foi criado JSON narrativo.

## 5. Fontes institucionais

A unidade pública referencia:
- Banco Central — Relatório de Empréstimos e Financiamentos (SCR);
- Resolução CMN nº 4.881/2020 — CET;
- Banco Central — Liquidação antecipada.

As fontes estão registradas em `SOURCE_REGISTRY.jsonl` como PF-SRC-000071 a PF-SRC-000073.

## 6. Deploy

- workflow: **Deploy public site to GitHub Pages**;
- run: **35587960672**;
- conclusão: **success**;
- commit público: `927706553da34967772e77959f9b1f49e5d922cb`;
- URL pública: https://thiagoba2004.github.io/planejamento-financeiro/temas/dividas-capital-indenizatorio.html

## 7. Gate da Fase 06

**SATISFEITO.**

A EA-000004-000017 pode ser encerrada em 6/6 fases e o portfólio pode avançar para a EA-000004-000018 — Investimentos e alocação do capital extraordinário.
