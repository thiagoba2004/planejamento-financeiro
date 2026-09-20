# Guia de Identidade Visual — Planejamento Financeiro

## Princípio

A identidade deve transmitir clareza, formação, organização, cálculo e tomada de decisão. A arquitetura pode reutilizar padrões funcionais de outros Sites, mas a aparência não pode ser copiada.

## Design tokens

- fundo principal: verde muito claro `#f3f8f7`;
- superfície: branco `#ffffff`;
- superfície suave: `#e5f1ef`;
- texto: verde-carvão `#183234`;
- primária: verde-petróleo `#0c555a`;
- primária profunda: `#073d41`;
- interação: turquesa `#14787d`;
- acento: âmbar `#c88a2b`;
- linha/borda: `#c9d9d7`.

## Tipografia

- títulos: Trebuchet MS / Arial;
- corpo e navegação: Arial / Helvetica.

## Componentes

- cards contemporâneos com cantos arredondados;
- métricas em painéis simples;
- tabelas didáticas;
- linguagem visual distinta do Ações Judiciais.

## Semântica visual de interação

A aparência deve ajudar o visitante a antecipar o que acontecerá:

- **ação:** botão preenchido (`action-button`), reservado a operações como enviar ou copiar;
- **navegação destacada:** CTA contornado (`nav-button`) com indicação direcional;
- **link secundário:** texto sublinhado (`secondary-link`);
- **card clicável:** `<a class="resource-card">`, identificado por fundo verde-azulado claro, borda/realce turquesa e resposta de hover;
- **card informativo:** `<article class="resource-card">`, branco e neutro, estático e sem hover que prometa clique.

Nunca trocar `button` por `a` ou vice-versa apenas para obter determinada aparência.

## Home

Institucional e enxuta. Não contém catálogo dos Menus nem bloco “Explore o Site”.

## Mobile

Menu global horizontal rolável, item atual identificável, cards em coluna única e ausência de overflow geral.

## Diferenciação

Não reutilizar a paleta, tipografia ou linguagem editorial do Classe e Massas ou do Ações Judiciais.
