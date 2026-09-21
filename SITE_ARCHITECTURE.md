# Arquitetura Pública — Planejamento Financeiro

## Menu global

Início · CFP® · Conhecimentos · Casos · Ferramentas · Fontes · Fale Conosco

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
- **Fontes:** Planejar, Banco Central e demais referências institucionais.
- **Fale Conosco:** canal protocolado de contato.
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
