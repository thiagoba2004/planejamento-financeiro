# Arquitetura Pública — Planejamento Financeiro

## Menu global

Início · CFP® · Conhecimentos · Casos · Ferramentas · Publicações · Fontes · Fale Conosco

## Princípio arquitetural

O Menu global representa **áreas estáveis e transversais do Site**. Módulos, temas, métricas ou seções internas de uma unidade não sobem automaticamente para o primeiro nível.

## Função de cada área

- **Início:** apresentação institucional enxuta; não funciona como catálogo dos Menus.
- **CFP®:** exame, certificação, estrutura vigente e materiais oficiais.
- **Conhecimentos:** porta de entrada para as áreas de conhecimento do projeto.
  - **Gestão Financeira:** subárea de Conhecimentos.
    - **Superendividamento das Pessoas Físicas:** unidade formativa.
- **Casos:** biblioteca transversal para treino de diagnóstico, decisão, comunicação e julgamento profissional.
- **Ferramentas:** biblioteca de instrumentos executáveis e quadros de apoio.
  - **Métricas e indicadores:** subárea de Ferramentas.
  - **Escada de intervenção:** ferramenta de apoio à decisão.
  - evolução prevista: calculadoras, checklists, roteiros, templates e árvores de decisão.
- **Publicações:** hub editorial transversal em `/publicacoes/`, com **Notícias** (o que mudou), **Artigos** (como interpretar e problematizar) e **Observatório** (como o estado cumulativo do conhecimento se conecta, evolui e exige revalidação).
- **Fontes:** Planejar, Banco Central e demais referências institucionais.
- **Fale Conosco:** canal protocolado de contato.
- **Privacidade:** rota pública de transparência sobre tratamento de dados, acessível pelo Fale Conosco, recibo e rodapé/Mapa; não integra o menu global.
- **Mapa do Site:** índice estrutural acessível pelo rodapé, fora do menu global.

## Regra de interação

- `<button>` executa ação;
- `<a href>` navega;
- ação primária usa padrão visual `action-button`;
- navegação em formato de chamada usa `nav-button`;
- links secundários usam `secondary-link`;
- card clicável deve ser um `<a class="resource-card">` e exibir sinal de navegação;
- card meramente informativo deve permanecer estático, sem hover que sugira clique.

## Identidade visual

Paleta exclusiva:
- verde-petróleo `#0c555a`;
- verde profundo `#073d41`;
- fundo frio `#f3f8f7`;
- turquesa `#14787d`;
- âmbar `#c88a2b`.

Tipografia:
- títulos: Trebuchet MS / sans-serif;
- corpo e navegação: Arial/Helvetica.

A identidade deve comunicar clareza, formação, cálculo e decisão, sem reproduzir a aparência do Classe e Massas ou do Ações Judiciais.


## Paridade editorial e rastreabilidade

- Markdown é fonte canônica substantiva; HTML é artefato público.
- Toda informação técnica, fórmula, condição, limite, fonte, data/status e aviso profissional presente no HTML deve existir também no Markdown correspondente.
- A página pública pode resumir detalhes de governança interna, mas não pode inventar conteúdo técnico ausente da fonte canônica.
- Regras perecíveis (exame, tributação, limites regulatórios, FGC, SFH, previdência) devem expor data de verificação quando material.
- Fontes sensíveis devem permitir identificar órgão/autoria, documento, versão/data, status e link recuperável.
- Divergência material Markdown–HTML bloqueia publicação.


## Arquitetura editorial transversal — implementada em 22/09/2026

- Modo de navegação: `EDITORIAL_HUB`.
- Rótulo global: **Publicações**.
- Rotas públicas: `/publicacoes/`, `/publicacoes/noticias/`, `/publicacoes/artigos/` e `/publicacoes/observatorio/`.
- Conhecimentos, Casos e Ferramentas continuam como áreas estáveis; as novas camadas não as duplicam.
- O Mapa do Site expõe as três subáreas públicas.


## Padrão Coleção → Detalhe — 22/09/2026

- `/publicacoes/noticias/`, `/publicacoes/artigos/` e `/publicacoes/observatorio/` são páginas de **coleção/índice**.
- Cada item publicado possui página individual própria na mesma subpasta.
- O título do item é o hiperlink principal; data, tema e resumo curto orientam a escolha.
- Sinais ainda em monitoramento podem aparecer resumidos sem serem tratados como publicação autônoma.
- Markdown e HTML seguem a mesma granularidade.


## Arquitetura pública do Observatório — 22/09/2026

- índice público organizado por **temas do Observatório**;
- metadado público principal: **Atualizado em DD/MM/AAAA**;
- identificadores técnicos de versão ficam fora da UI;
- cada tema financeiro organiza síntese, premissas/evidências, implicações, interdependências, mudanças, questões em aberto, fontes e conteúdos relacionados;
- monitoramento e gatilhos permanecem na governança interna.
