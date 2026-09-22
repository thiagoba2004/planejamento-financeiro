# Auditoria de Interface — Planejamento Financeiro

**Projeto:** PRJ-000004 — Planejamento Financeiro  
**Estratégia:** EA-000004-000043 — Auditoria e harmonização semântica da interface do Site Planejamento Financeiro  
**Data:** 22/09/2026

## Síntese

O padrão geral foi aplicado preservando a identidade própria do Planejamento Financeiro: **verde-petróleo, verde profundo, turquesa, âmbar e superfícies claras**, com tipografia sans-serif e componentes arredondados.

O Site já possuía uma separação avançada entre `action-button`, `nav-button`, `secondary-link` e cards. A auditoria concentrou-se em consolidar essa arquitetura, retirar o estilo genérico legado e aprofundar a hierarquia cromática da ação primária.

## Correções aplicadas

- **ação primária real:** `action-button` em verde-petróleo `#0c555a`, texto branco;
- **hover/foco da ação primária:** verde profundo `#073d41`;
- **navegação destacada:** `nav-button` contornado, preservando turquesa como realce;
- **retorno simples:** `secondary-link`;
- regra CSS genérica `.button`: removida;
- tokens semânticos `--action-primary`, `--action-primary-hover` e `--action-primary-text` adicionados;
- três links de retorno em unidades temáticas foram rebaixados de CTA destacado para link secundário;
- cards clicáveis continuam em superfície verde-azulada clara; cards informativos continuam brancos e estáticos.

## Auditoria integral

Foram verificados **40 arquivos HTML públicos**.

Resultado:
- exatamente um `<h1>` em 40/40;
- zero `<style>` ou atributos `style=`;
- zero âncoras com classe genérica `button`;
- zero botões com classe genérica `button`;
- zero âncoras com `action-button`;
- todos os botões reais usam `action-button`;
- menu global presente em 40/40;
- **152 cards clicáveis** e **380 cards informativos** preservam a distinção semântica e cromática;
- **25 navegações destacadas** usam `nav-button`;
- **22 links secundários** usam `secondary-link`;
- dois botões reais auditados: envio do formulário e cópia de protocolo.

CSS:
- ação primária usa verde-petróleo e hover/foco usa verde profundo;
- turquesa permanece realce de navegação/cards, sem ocupar o papel da ação primária;
- card clicável e card informativo permanecem visualmente distintos;
- menu horizontal rolável até 880 px confirmado;
- chaves CSS balanceadas.

## Especificidade preservada

O Planejamento Financeiro não recebeu botões vermelhos, azul-marinho ou estética editorial do Classe e Massas/Ações Judiciais. A regra compartilhada é funcional — **ação ≠ navegação ≠ card** — enquanto a expressão cromática permanece própria do projeto.

## Gate

**APROVADO NO CÓDIGO.**

A próxima etapa é confirmar o pipeline do GitHub Pages e fechar a estratégia.
