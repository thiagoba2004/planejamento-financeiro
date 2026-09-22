# Decisão de arquitetura editorial — EA-000004-000035

## Decisão

Adotar **EDITORIAL_HUB** no Site Planejamento Financeiro.

### Rótulo do hub
**Publicações**

### Estrutura planejada
- Publicações
  - Notícias
  - Artigos
  - Observatório

### Rotas planejadas
- `/publicacoes/`
- `/publicacoes/noticias/`
- `/publicacoes/artigos/`
- `/publicacoes/observatorio/`

## Justificativa

1. O menu atual possui sete áreas estáveis e legíveis.
2. Notícias, Artigos e Observatório atravessam todos os domínios e não devem competir com CFP®, Conhecimentos, Casos e Ferramentas.
3. O hub aumenta o primeiro nível em apenas um item.
4. **Publicações** acomoda atualização factual, análise autoral e produtos do Observatório sem reduzir semanticamente nenhuma subárea.
5. O hub terá página própria e conteúdo real.
6. As três subáreas aparecerão no Mapa do Site.
7. A implementação pública só ocorre depois de conteúdo suficiente e auditoria das rotas/workflow.

## Menu futuro, após o gate de conteúdo

Início · CFP® · Conhecimentos · Casos · Ferramentas · Fontes · **Publicações** · Fale Conosco

## Relações editoriais

- notícia → aponta para conteúdo formativo afetado;
- artigo → desenvolve análise crítica e implicações;
- observatório → mantém sínteses cumulativas, sinais e lacunas;
- Conhecimentos/Casos/Ferramentas permanecem as áreas estáveis de formação e aplicação.

## Gate da Fase 02

**SATISFEITO.** Modo de navegação, rótulo, rotas e regra de não redundância definidos. A alteração pública aguarda as estratégias filhas.
