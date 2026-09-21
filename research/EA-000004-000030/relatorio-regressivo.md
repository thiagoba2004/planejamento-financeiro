# Relatório — Auditoria Regressiva Pós-Correção

**Projeto:** PRJ-000004 — Planejamento Financeiro  
**Estratégia:** EA-000004-000030  
**Data:** 21/09/2026  
**Origem:** ciclo corretivo do Relatório do Planejador Financeiro do Diabo.

## 1. Objetivo

Testar se o ciclo corretivo introduziu regressões, deixou divergências entre Markdown e HTML ou publicou conteúdo diferente do estado esperado do repositório.

## 2. Verificação externa e artefato de publicação

A leitura HTTP direta do domínio `thiagoba2004.github.io` não foi possível nos dois mecanismos externos disponíveis nesta sessão:

- navegador de pesquisa: domínio `github.io` não acessível pela ferramenta;
- ambiente de execução: resolução DNS externa indisponível.

Essa limitação não foi confundida com indisponibilidade do Site.

A auditoria utilizou o **artefato exato produzido pelo GitHub Pages**.

### Artefato inicial auditado
- run: `35643562008`;
- artifact ID: `10658379653`;
- digest: `sha256:ffb60320cbb7db77196cc1263b492aae743876b294ce978ec85cc25e259106cd`;
- commit: `7b0669e5074a5106eebda87fdb668fe96d529c33`.

O pacote continha **33 HTMLs públicos + 1 CSS**.

## 3. Achados regressivos

A primeira varredura do artefato confirmou:

- 0 links internos quebrados;
- 0 âncoras quebradas;
- 0 páginas sem `<title>`;
- 0 páginas sem `<h1>`;
- 0 resíduos das fórmulas e expressões adversariais pesquisadas;
- rotas de Privacidade, Processo de Planejamento Financeiro e Perímetro Profissional presentes;
- Fale Conosco alinhado ao estado E2E;
- cronogramas operacionais pesquisados devidamente rotulados como heurísticas.

Entretanto, foi encontrada uma regressão de **paridade semântica CFP®** em cinco HTMLs.

O Markdown dessas unidades já possuía classificação explícita, mas o HTML não apresentava o rótulo público `Classificação:` de forma padronizada:

1. `temas/dividas-credito-garantias-contas-conjuntas.html`;
2. `temas/empresas-participacoes-societarias-renda.html`;
3. `temas/investimentos-capital-extraordinario.html`;
4. `temas/investimentos-reorganizacao-carteiras.html`;
5. `temas/seguros-previdencia-protecao-financeira.html`.

Em três casos a categoria material aparecia sem o rótulo; em dois casos a categoria explícita não estava publicada.

## 4. Correções aplicadas

As cinco páginas foram corrigidas para declarar explicitamente a categoria de aderência ao CFP®.

Nenhum conteúdo novo foi inventado: o HTML foi alinhado às classificações que já existiam nos respectivos Markdown canônicos.

## 5. Novo deployment

O ajuste regressivo final está no commit público:

`be331d70ee3623e640af492910ab1bd2a57fd548`

GitHub Pages run:

**35645234961 — success**

Todas as etapas foram concluídas com sucesso, inclusive:
- Build public-only artifact;
- Upload Pages artifact;
- Deploy to GitHub Pages.

### Artefato final auditado
- artifact ID: `10659862746`;
- digest: `sha256:1d79283f8b6e19241309af077cec291611a413877a0de5de08dd2c4b31fb655d`;
- 33 HTMLs + 1 CSS.

## 6. Reauditoria do artefato final

Resultado da varredura integral do pacote implantado:

- **33 HTMLs públicos**;
- **0 problemas de title**;
- **0 problemas de H1**;
- **0 links internos inexistentes**;
- **0 âncoras internas ou de destino quebradas**;
- **0 vazamentos dos códigos internos pesquisados**;
- **0 resíduos de “integralmente disponíveis”**;
- **0 estado editorial antigo do Fale Conosco**;
- **0 “Perfil de risco em três/cinco dimensões”**;
- **0 headings CFP® legados pesquisados**;
- **0 fórmulas pesquisadas de PL + R$ 100 mil sem condicionante**;
- **0 gaps antigos pesquisados sem equivalência temporal**;
- **0 unidades temáticas com seção Aderência ao CFP® sem classificação explícita**;
- **0 cronogramas pesquisados com janelas 7/30/90/180/365 ou equivalentes sem rótulo de heurística**.

Checagens positivas:
- Aviso de Privacidade: presente;
- link de Privacidade no Fale Conosco: presente;
- link de Privacidade no recibo: presente;
- Privacidade no Mapa do Site: presente;
- Processo de Planejamento Financeiro: presente;
- Perímetro Profissional: presente;
- estado E2E do Fale Conosco: presente;
- independência institucional na área CFP®: presente.

## 7. Conclusão

A auditoria regressiva foi útil porque detectou uma inconsistência que a auditoria corretiva anterior não havia capturado: **cinco HTMLs não reproduziam integralmente a classificação CFP® que já existia no Markdown canônico**.

Após a correção e novo deployment:

**ESTADO FINAL: AUDITORIA REGRESSIVA APROVADA — NENHUMA REGRESSÃO MATERIAL RESIDUAL DETECTADA NO ARTEFATO FINAL.**
