# Auditoria de Home, tipografia e responsividade — 22/09/2026

## Evidência da regressão
Antes da correção:
- `h1`: `clamp(2.5rem,7vw,5rem)`;
- `.home-hero h1`: `clamp(3.1rem,9vw,6.5rem)`;
- mobile `h1`: até `3.9rem`;
- `.home-main`: flex em linha com Hero e nota institucional;
- captura fornecida mostrou a nota projetada para fora da viewport.

## Estado após a correção
- `h1`: `clamp(1.55rem,3vw,1.9rem)`;
- `.home-hero h1`: `clamp(1.75rem,3.5vw,2.1rem)`;
- mobile `h1`: `1.6rem`;
- mobile Home `h1`: `1.75rem`;
- `h2`: `clamp(1.25rem,2.4vw,1.5rem)`;
- `h3`: `1.08rem`;
- Home usa `flex-direction: column`;
- imagens/vetores/vídeos limitados a `max-width:100%`;
- nota redundante de independência institucional removida da Home e preservada no contexto CFP®;
- Home, CFP®, Conhecimentos e índice de Artigos: exatamente um `h1` por página;
- nenhuma dessas páginas usa `style=""` inline para ampliar títulos;
- valores antigos de 5rem e 6,5rem não permanecem no CSS.

## Síntese institucional vigente
“Formação baseada no CFP®, conectando conhecimento técnico, cálculos, casos, ferramentas e publicações para desenvolver diagnóstico, julgamento e tomada de decisão profissional.”

## Gate responsivo
A folha de estilos agora codifica:
- cards em coluna única no mobile;
- Home em coluna;
- títulos moderados;
- exceção de overflow somente em componentes deliberadamente roláveis.

A inspeção HTTP externa do ambiente não conseguiu abrir o domínio `github.io`; por isso, a prova de publicação é o pipeline oficial do GitHub Pages.

## Deploy
GitHub Pages run `35747406857`: **success** em todas as etapas, incluindo Build public-only artifact, Upload Pages artifact e Deploy to GitHub Pages.
