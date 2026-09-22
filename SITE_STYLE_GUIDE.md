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
- corpo e navegação: Arial / Helvetica;
- corpo base próximo de `1rem`;
- `h1`: aproximadamente `1,55rem–1,90rem`; no mobile, cerca de `1,60rem`;
- `h1` da Home: aproximadamente `1,75rem–2,10rem`; no mobile, cerca de `1,75rem`;
- `h2`: aproximadamente `1,25rem–1,50rem`;
- `h3`: aproximadamente `1,08rem`;
- títulos devem estabelecer hierarquia sem assumir escala de display. A regra do Projeto é que fiquem **apenas moderadamente maiores que o texto corrente**.

## Componentes

- cards contemporâneos com cantos arredondados;
- métricas em painéis simples;
- tabelas didáticas;
- linguagem visual distinta do Ações Judiciais.

## Semântica visual de interação

A aparência deve ajudar o visitante a antecipar o que acontecerá:

- **ação primária real:** botão preenchido `action-button` em verde-petróleo `#0c555a`, com texto branco;
- **hover/foco da ação primária:** verde profundo `#073d41`, preservando texto branco;
- **navegação destacada:** CTA contornado `nav-button`, com superfície clara e indicação direcional;
- **link secundário/retorno simples:** texto sublinhado `secondary-link`;
- **card clicável:** `<a class="resource-card">`, identificado por fundo verde-azulado claro, borda/realce turquesa e resposta de hover;
- **card informativo:** `<article class="resource-card">`, branco e neutro, estático e sem hover que prometa clique.

Nunca trocar `button` por `a` ou vice-versa apenas para obter determinada aparência.

A classe genérica `.button` não integra o padrão público: ação, navegação destacada e link secundário possuem classes próprias. O turquesa `#14787d` permanece cor de interação e realce, mas não substitui a variante profunda no hover da ação primária.

## Home

Institucional e enxuta. Não contém catálogo dos Menus nem bloco “Explore o Site”.

- composição principal em uma coluna;
- avisos específicos de CFP®, fontes ou independência institucional devem permanecer nas páginas contextualmente adequadas quando já estiverem disponíveis ali, evitando duplicação desnecessária na Home;
- nenhum bloco lateral pode provocar corte ou overflow no mobile.

## Mobile

Menu global horizontal rolável, item atual identificável, cards em coluna única e ausência de overflow geral.

- testar ao menos larguras de 360 px, 390 px e 412 px;
- conteúdo estrutural da Home deve empilhar verticalmente;
- exceções de overflow ficam restritas a componentes deliberadamente roláveis, como navegação horizontal ou tabelas;
- títulos não podem ocupar a viewport como elemento dominante nem forçar corte lateral.

## Diferenciação

Não reutilizar a paleta, tipografia ou linguagem editorial do Classe e Massas ou do Ações Judiciais.


### Botão ENVIAR MENSAGEM — padrão transversal

O botão real **ENVIAR MENSAGEM** usa a classe adicional `submit-button` e deve ser sempre **oval/pílula**, nunca retangular:

- `border-radius: 999px`;
- mantém a cor primária financeira verde-petróleo;
- a forma é compartilhada com os demais Sites, sem importar suas paletas;
- continua sendo `<button type="submit">`.
