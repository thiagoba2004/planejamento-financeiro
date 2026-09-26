# AGENTS.md — PLANEJAMENTO FINANCEIRO

**project_code:** `PRJ-000004`  
**project_sequence:** `000004`  
**project_alias:** `PF`  
**project_name:** `Planejamento Financeiro`  
**project_id legado:** `planejamento-financeiro`  
**generated_from_kernel:** `1.8`  
**generator_release:** `1.23`  
**repository:** `thiagoba2004/planejamento-financeiro`  
**modules:** `research`, `publication`, `web-site`, `contact-protocol`, `software`, `data`, `professional-education`, `publication`, `software`, `data`, `professional-education`

## 1. Missão

Qualificar profissionais com base no CFP®, integrando preparação para a prova e desenvolvimento de competências para atuação profissional no mercado.

O projeto não deve confundir aprovação em exame com competência profissional. Todo tema deve responder três perguntas: **o que saber, o que saber fazer e o que ser capaz de decidir**.

## 2. Entrada de qualquer pedido

```text
REGISTRAR EM REQUEST_LOG.jsonl
↓
CONFIRMAR TECNICAMENTE O REGISTRO
↓
INFORMAR “PEDIDO REGISTRADO.”
↓
INFORMAR QUE IRÁ LER O PROMPT, ANALISAR E TOMAR AS PROVIDÊNCIAS
↓
EXECUTAR
```

### Ponte bidirecional com o Coordenador Geral

Antes de tratar pedidos com **possível repercussão transversal**, **dúvida de pertencimento/roteamento**, possível vínculo com a **governança global** ou sinais de **candidato a novo Projeto**, consultar, quando a Biblioteca estiver acessível:

`/Governanca-Geral-Modelos-IA/00_BOOTSTRAP_COORDENADOR_GERAL.md`

Regras:

- pedidos inequivocamente locais e já abrangidos por este Projeto seguem diretamente este `AGENTS.md`, sem consulta obrigatória ao Bootstrap;
- a consulta ao Bootstrap é condicional e serve para classificar/rotear, não para substituir a governança local;
- evitar loop de roteamento: Bootstrap → Projeto é entrada normal; Projeto → Bootstrap ocorre apenas diante de dúvida, repercussão transversal ou governança global;
- se a Biblioteca/Bootstrap não estiver acessível na sessão, não inventar seu conteúdo; registrar a limitação quando material e prosseguir pela governança local comprovada;
- conversas classificadas como casuais/efêmeras pelo Coordenador Geral não devem ser artificialmente absorvidas por este Projeto.

### Arquitetura universal de ambientes v2

Este Projeto adota a arquitetura global de seis planos: **G** (identidade), **A** (superfície), **E** (executor), **C** (contexto/memória), **K** (fontes de conhecimento) e **P** (persistência/publicação).

Fonte global: `thiagoba2004/governanca-geral-modelos-ia/ARQUITETURA_UNIVERSAL_AMBIENTES_EXECUCAO_PERSISTENCIA.md`.

Regras locais:

- Projeto ChatGPT não é sinônimo deste Projeto de Governança;
- o modo de memória do Projeto ChatGPT é uma propriedade individual e não possui padrão global; o estado atual deste Projeto é **C2 — memória padrão**;
- memória exclusiva reduz contaminação contextual, mas não elimina alucinações nem prevalece sobre fontes persistentes;
- no estado atual C2, Work pode ser usado dentro do Projeto conforme disponibilidade; se o Projeto for alterado para C3, Work ficará indisponível dentro dessa fronteira e exigirá handoff;
- fontes anexadas ao Projeto ChatGPT formam **Core Context curado**, não o repositório integral;
- Biblioteca e nuvens conectadas são fontes operacionais;
- GitHub deste Projeto é a fonte versionada canônica de estado, regras e histórico;
- filesystem local/Notebook é working copy/cache e nunca deve ser a única cópia necessária à continuidade;
- Codex deve devolver alterações relevantes ao repositório;
- o handoff para Work/Codex transfere somente o contexto necessário, com sensibilidade e destino canônico definidos.

O `EXECUTION_ENVIRONMENT_PROFILE.json` schema v2 registra a política local.

## 3. Fonte da verdade

1. `AGENTS.md`;
2. materiais oficiais da Planejar identificados em `PLANEJAR_SOURCES.md` e `SOURCE_REGISTRY.jsonl`;
3. `REQUEST_LOG.jsonl`;
4. `STRATEGY_LOG.jsonl`;
5. `PROJECT_STATE.json`;
6. `ROADMAP.md` e planos de fases;
7. fontes técnicas primárias e institucionais verificadas;
8. arquivos Markdown canônicos;
9. histórico Git comprovado;
10. somente depois, memória/conversa.

### 3.1. Materiais da Planejar

Todo material disponibilizado oficialmente pela Planejar e pertinente ao CFP® é fonte canônica do projeto.

“Canônico” não significa necessariamente “copiado integralmente para o repositório”. Para cada material, registrar quando possível: título, URL/identificador, tipo, versão/data, data de consulta, status de vigência e relação com competências. Reprodução integral pública somente quando houver permissão compatível.

## 4. Estratégias e fases

Toda Estratégia Autônoma deve possuir `strategy_code` e `strategy_name` antes da execução substantiva.

Padrões:
```text
EA-000004-EEEEEE
F-000004-EEEEEE-FFF
```

Toda estratégia deve ter Plano de Fases integralmente numerado.

## 5. Resposta de continuidade

```text
PROJETO: PRJ-000004 — Planejamento Financeiro
ALIAS: PF
ESTRATÉGIA AUTÔNOMA: <código> — <nome>
FASE: <número>/<total> [<código>] — <nome>
ESTADO: <estado comprovado>
ONDE PARAMOS: <ponto exato comprovado>
PRÓXIMO PASSO LÓGICO: <próximo passo comprovado>
```

## 6. Persistência e verificação

```text
PRODUZIR → SALVAR → VERIFICAR → ATUALIZAR ESTADO → CONTINUAR
```

Nunca afirmar atualização de programa, regra de certificação, conteúdo oficial, cálculo validado, publicação ou implantação sem confirmação técnica.

## 7. Módulo research

- priorizar Planejar e demais fontes institucionais/primárias adequadas;
- distinguir fonte canônica, fonte complementar, interpretação e hipótese;
- registrar data de consulta e versão quando o conteúdo puder mudar;
- não reconstruir critérios de prova ou certificação de memória quando a fonte oficial puder ser consultada;
- para Notícias e Observatório, separar cadência de busca de gatilho de publicação;
- monitorar por padrão apenas temas já cobertos pelo Site, salvo decisão expressa de expansão;
- registrar janela temporal, descritores, fontes prioritárias, data de corte e critérios de relevância em monitoramento recorrente;
- no Observatório, aplicar ciclo de horizon scanning: detectar → filtrar → priorizar → avaliar → disseminar → acompanhar;
- usar lógica de evidência viva quando conclusões puderem mudar, com data da última busca, versão/data da síntese e registro do que mudou.

## 8. Módulo professional-education

Todo tópico formativo deve separar **aderência ao CFP®** de **aplicação profissional**.

Na camada pública, usar obrigatoriamente uma das três categorias de aderência:
- mapeado diretamente no programa/material oficial vigente;
- competência ou conceito do domínio CFP®;
- aplicação profissional desenvolvida pelo Projeto.

A sobreposição entre preparação para o exame e prática é desejável quando comprovada; a inferência de conteúdo de prova é proibida.

Cada unidade deve declarar:
- **SABER:** conceitos, regras e fundamentos;
- **FAZER:** cálculos, diagnóstico, comunicação, elaboração ou execução;
- **DECIDIR:** julgamento profissional, escolhas, prioridades e limites;
- **FONTE:** material canônico que sustenta o conteúdo;
- **AVALIAÇÃO:** como comprovar domínio.

Questões objetivas não bastam para competências de comunicação, ética, diagnóstico ou julgamento: usar também casos práticos.

## 9. Módulo data

- distinguir dado, premissa, cálculo e interpretação;
- registrar fórmulas, unidades, períodos e arredondamentos relevantes;
- preservar exemplos reproduzíveis;
- não preencher dado ausente silenciosamente;
- validar cálculos críticos e casos numéricos antes de publicar.

## 10. Módulo publication

Para conteúdo textual/editorial publicável, o padrão é:

```text
Markdown (.md) = fonte textual canônica
HTML (.html) = publicação
JSON (.json) = somente quando houver função estruturada real
```

**JSON não é terceiro artefato obrigatório.** Não criar `.json` apenas para duplicar texto, título, resumo, seções, caminhos ou metadados que já estejam adequadamente preservados no Markdown e no HTML.

JSON/JSONL deve ser mantido quando houver finalidade objetiva de máquina, como:
- estado e governança;
- registros append-only;
- configuração;
- datasets, fixtures, catálogos, taxonomias ou schemas;
- dados consumidos por cálculo, script, automação, API, busca estruturada, filtro ou validação;
- interoperabilidade comprovada entre projetos.

Antes de criar um JSON, identificar expressamente **qual processo o consome** e **qual dado estruturado ele preserva que o Markdown não atende adequadamente**. Sem finalidade concreta, não criar.

Alterações editoriais devem ser sincronizadas entre Markdown e HTML. JSON existente só precisa ser atualizado quando sua função estruturada exigir.

Quando forem publicados conteúdos editoriais transversais:
- **Notícias** tratam fatos e mudanças verificáveis em CFP®, regulação, dados, mercados, práticas e temas já cobertos, com fonte e data;
- **Artigos** tratam análise crítica/autoral, distinguindo evidência, inferência, opinião técnica, implicações e limites profissionais;
- **Observatório** trata pesquisa cumulativa, mudanças regulatórias/metodológicas/científicas, sinais, relações e lacunas;
- cada conteúdo possui função editorial primária e deve evitar duplicação com Conhecimentos, Casos, Ferramentas ou Fontes;
- buscas semanais, mensais, trimestrais, semestrais e anuais podem coexistir, mas publicação depende de materialidade.

### 10.2. Paridade semântica obrigatória

Markdown é a fonte textual canônica e deve ser suficiente para reconstruir o conteúdo substantivo do HTML público. Aparência, componentes e microcopy de interface podem variar; conteúdo técnico, fórmulas, condições, limitações, fontes, datas de verificação, status e avisos profissionais não podem existir apenas no HTML.

Antes de publicar, comparar semanticamente cada par Markdown–HTML alterado. Divergência material bloqueia o deploy.

### 10.3. Auditoria adversarial quantitativa

Nenhuma fórmula, métrica, sequência, cenário ou recomendação é considerada auditada apenas porque a aritmética está correta. Verificar também: data-base, unidade, horizonte, sobreposição de variáveis, valor do dinheiro no tempo, denominadores-limite, qualidade dos dados, premissas implícitas, perímetro regulatório, natureza da fonte, aderência efetiva ao CFP® e coerência com as demais unidades.

### 10.1. Separação entre governança interna e Site Público

O Site Público é orientado ao aluno, profissional e leitor externo. A governança permanece no repositório e **não deve ser exibida na interface pública**.

É proibido publicar na UI, rodapé, cabeçalho, cards, tabelas ou metadados destinados ao navegador:

- códigos internos de projeto, estratégia, fase, pedido, evento, competência, caso ou fonte (`PRJ-*`, `EA-*`, `F-*`, `REQ-*`, `EVT-*`, `PF-COMP-*`, `PF-CASO-*`, `SRC-*`);
- números de fase, gates, estados editoriais/técnicos e status de workflow;
- versões de kernel/gerador, IDs de deployment, run, commit, branch ou arquivos de governança;
- nomes como `PROJECT_STATE`, `REQUEST_LOG`, `STRATEGY_LOG`, `AGENTS` ou equivalentes;
- rótulos metodológicos internos como graus A/B/P, códigos A1–A4 ou códigos de métricas, quando não forem necessários à compreensão do leitor.

Na camada pública, converter conceitos úteis para linguagem natural, por exemplo:

- nomenclaturas internas antigas como `TRILHA_PROVA` devem ser convertidas para a taxonomia pública de aderência ao CFP®;
- `TRILHA_PRATICA` ou equivalentes → “Na prática profissional”, quando útil;
- códigos de casos → “Caso 1”, “Caso 2” etc.;
- códigos de competências → apenas o nome da competência;
- códigos de métricas → nome e fórmula em linguagem comum.

Pode permanecer público quando útil ao leitor:

- conteúdo material;
- data de atualização;
- fontes oficiais;
- fórmulas;
- exemplos e casos;
- critérios de avaliação em linguagem natural;
- avisos de limites profissionais.

Antes de cada publicação, executar varredura de vazamento de governança. A presença de marcador interno na camada pública bloqueia o deploy.

## 11. Módulo web-site

O Site é uma arquitetura pública multipágina. Não pode ser reduzido a uma Home com cards e uma página longa.

**Menu global obrigatório vigente:** Início · CFP® · Conhecimentos · Casos · Ferramentas · Fontes · Fale Conosco.

**Arquitetura editorial planejada:** `EDITORIAL_HUB` com rótulo **Publicações**, contendo Notícias, Artigos e Observatório. O hub só entra no menu público após existir conteúdo real nas páginas centrais, rotas auditadas e workflow do GitHub Pages atualizado.

**Menu futuro após o gate de conteúdo:** Início · CFP® · Conhecimentos · Casos · Ferramentas · Fontes · Publicações · Fale Conosco.

Regras obrigatórias:
- o mesmo menu global aparece em todas as páginas;
- a página corrente usa `aria-current="page"`;
- no mobile, o menu permanece acessível em linha horizontal rolável;
- a Home é institucional e enxuta; não contém catálogo dos Menus nem “Explore o Site”;
- toda página pública possui no rodapé o hiperlink **Mapa do Site**;
- `mapa-do-site/` reflete as rotas públicas reais;
- páginas centrais de Menu possuem conteúdo útil, não placeholders;
- Publicações não substitui áreas estáveis: Notícias = mudança factual; Artigos = análise autoral; Observatório = síntese sistêmica cumulativa;
- as rotas planejadas são `/publicacoes/`, `/publicacoes/noticias/`, `/publicacoes/artigos/` e `/publicacoes/observatorio/`;
- o Mapa do Site deve expor as três subáreas quando públicas, mesmo agrupadas sob o hub;
- Notícias devem apontar para a unidade formativa afetada quando houver; Artigos e Observatório usam referências cruzadas e não duplicação;
- Menus de primeiro nível representam áreas estáveis e transversais; módulos, temas e seções internas não devem subir automaticamente ao Menu global;
- `Conhecimentos` agrega áreas como Gestão Financeira; `Métricas e indicadores` integra `Ferramentas`;
- a interface pública não exibe códigos, estados e metadados de governança interna;
- `SITE_ARCHITECTURE.md` é a fonte da arquitetura;
- `SITE_STYLE_GUIDE.md` é a fonte da identidade visual;
- mudanças estruturais exigem auditoria desktop/mobile, links, overflow e navegação;
- toda nova rota pública deve ser incluída explicitamente no workflow de GitHub Pages (`paths`, diretório `_site` e cópia para o artefato) antes de considerar o deploy concluído;
- auditoria de publicação deve verificar não apenas a existência no repositório, mas a presença da rota no artefato público.

**Identidade visual:** deve ser exclusiva deste projeto. Reutilizar a estrutura do Classe e Massas não autoriza reutilizar sua paleta, tipografia ou composição.

### 11.1. Semântica de interação

- `<button>` é reservado a ações;
- `<a href>` é reservado a navegação;
- ação primária usa `action-button`, com verde-petróleo `#0c555a` e hover/foco verde profundo `#073d41`;
- navegação destacada usa `nav-button`;
- link secundário ou retorno simples usa `secondary-link`;
- a classe genérica `.button` é vedada na superfície pública por misturar funções distintas;
- `a.resource-card` deve ser diferenciado por cor e pode responder a hover;
- `article.resource-card` é informativo, deve permanecer cromaticamente neutro e não pode ter comportamento visual que sugira clique;
- o texto de cada CTA deve descrever destino ou ação de modo específico;
- não usar textos redundantes como `Acessar →` em cards; a distinção entre card clicável e informativo deve ser cromática e comportamental.

## 12. Módulo contact-protocol

O Fale Conosco adota o padrão técnico de referência do Classe e Massas:

```text
Forminit = recebimento/aceite da submissão e anexos
EmailJS  = confirmação do protocolo ao e-mail informado
```

Regras:
- e-mail institucional: `planejamentofinanceiro2012@gmail.com`;
- prefixo: `PF-`;
- `CONTACT_STACK.md` documenta a configuração e o estado;
- FormSubmit não é stack canônica e a implementação atual deve ser migrada;
- é proibido substituir Forminit/EmailJS por outro provedor sem decisão expressa e persistida;
- o protocolo pode ser preparado antes do envio, mas só é **confirmado** após sucesso do Forminit;
- EmailJS só é acionado após recebimento confirmado;
- falha no EmailJS não invalida um protocolo já aceito pelo Forminit;
- a página de confirmação usa `noindex,nofollow` e oferece **Copiar protocolo**;
- cada projeto deve ter Forminit próprio ou isolamento de roteamento comprovado;
- o canal só é declarado operacional após teste end-to-end real de recebimento + protocolo + e-mail.

**Estado atual:** `E2E_VERIFICADO` com Forminit + EmailJS.

## 13. Módulo software

Distinguir `IMPLEMENTADO`, `TESTADO`, `VERSIONADO`, `IMPLANTADO` e `VERIFICADO EM EXECUÇÃO`. Site no repositório não equivale a site publicado.

## 14. Regra específica do CFP®

Toda afirmação de aderência ao CFP® deve ser classificada, em linguagem pública, como uma destas três categorias:
1. **mapeado diretamente no programa/material oficial vigente**;
2. **competência ou conceito pertencente ao domínio CFP®**;
3. **aplicação profissional desenvolvida pelo Projeto**, sem afirmar que seja objetivo literal da prova.

O Site é projeto independente e não representa institucionalmente Planejar ou FPSB. Em caso de divergência, prevalecem os materiais oficiais vigentes.

### 14.1. Processo profissional e perímetro regulatório

Conteúdo profissional deve distinguir educação financeira, planejamento financeiro, análise/modelagem e atividades reguladas ou especializadas. A certificação CFP® não deve ser tratada como autorização automática para consultoria de valores mobiliários, distribuição, corretagem de seguros, advocacia, contabilidade, atuária ou atividade tributária especializada. O enquadramento depende da atividade efetivamente exercida e das regras aplicáveis.

O projeto deve manter uma matriz rastreável entre:
1. fonte oficial vigente;
2. domínio/competência;
3. conteúdo de estudo;
4. exercício ou caso;
5. aplicação profissional;
6. revisão/atualização.

Quando programa, regulamento ou material oficial mudar, identificar o impacto nas unidades dependentes antes de marcá-las como atualizadas.

## 15. Interoperabilidade com PRJ-000003

Temas com dimensão jurídica também podem ser estudados no PRJ-000003 — Ações Judiciais. O superendividamento e o divórcio litigioso são exemplos atuais. Este projeto trata prioritariamente de diagnóstico, cálculo, cenários, decisão financeira e competências profissionais. O PRJ-000003 é a fonte da verdade para conclusões jurídicas. No tema divórcio, direito à partilha, regime de bens, guarda, convivência e fixação de alimentos entram aqui apenas como premissas/cenários jurídicos confirmados; o Planejamento Financeiro não decide esses direitos.

### 15.1. Programa financeiro do divórcio litigioso

A carteira EA-000004-000005 a EA-000004-000014 cobre, respectivamente:
1. diagnóstico e orçamento de transição;
2. patrimônio, avaliação e liquidez;
3. moradia;
4. filhos e despesas de cuidado;
5. dívidas, crédito e garantias;
6. investimentos;
7. seguros, previdência e proteção;
8. tributação e custos de transferência;
9. empresas/participações e continuidade de renda;
10. reconstrução financeira integrada.

A EA-000004-000005 é fundacional. A EA-000004-000014 é integradora. Estratégias condicionais podem ser marcadas NÃO APLICÁVEL após triagem documentada.

## 16. Fechamento

Antes de declarar etapa concluída, verificar fontes, cálculos, coerência entre prova/prática, persistência, versionamento, publicação quando aplicável e próximo passo lógico.

> **Nunca obrigar o usuário a pagar novamente, com tempo, energia ou recursos, por falha de memória, persistência, continuidade, planejamento ou verificação do Modelo de IA.**


## Padrão editorial Coleção → Detalhe

Para Notícias, Artigos e Observatório públicos, a página da seção é um índice/arquivo. Cada conteúdo integral deve possuir página própria; o título do item é o hiperlink principal, acompanhado de metadados e resumo curto. É proibido acumular múltiplos conteúdos integrais na página de índice quando os itens têm autonomia editorial.


## 13. Escala tipográfica responsiva

- Títulos devem ser apenas moderadamente maiores que o texto corrente; evitar escala de display como padrão.
- No Site Planejamento Financeiro, a faixa canônica de `h1` é aproximadamente `1,55rem–1,90rem`, com Home em `1,75rem–2,10rem`; no mobile, `h1` fica em torno de `1,60rem` e o título da Home em torno de `1,75rem`.
- `h2` fica aproximadamente em `1,25rem–1,50rem` e `h3` em torno de `1,08rem`.
- A Home deve empilhar seus blocos estruturais no mobile e não pode produzir overflow horizontal geral.
- Toda alteração de CSS estrutural exige teste das páginas Início, CFP®, Conhecimentos e de pelo menos uma página de conteúdo em larguras móveis representativas.


## 14. Estados editoriais internos não são conteúdo público

- Rótulos como **“Em monitoramento”**, “fila editorial”, “pendente”, “gatilho de revisão”, “critério editorial”, “triagem” e equivalentes pertencem à governança interna.
- Itens ainda não aprovados como notícia, artigo ou unidade do Observatório não devem aparecer no Site Público como pré-publicação.
- O Site Público exibe somente conteúdo editorial já publicado e informações substantivas úteis ao leitor.
- Monitoramento, horizon scanning, gatilhos e critérios de materialidade permanecem em arquivos internos de pesquisa/governança.
- A auditoria de publicação deve procurar e bloquear a exposição desses estados internos.


## 15. Arquitetura pública do Observatório

- Não expor no Site identificadores técnicos de versão como `Snapshot 0.1`, `v0.1` ou equivalentes, salvo significado público comprovado.
- Cada tema do Observatório deve exibir **Atualizado em DD/MM/AAAA**.
- O índice do Observatório apresenta **temas**, não versões técnicas.
- Para o Observatório de Planejamento Financeiro, a unidade temática deve organizar, quando aplicável: **Em síntese; Evidências e premissas atuais; Implicações para o planejamento; Mapa de interdependências; O que mudou desde a última atualização; Questões em aberto; Fontes principais; Conteúdos relacionados**.
- “Questões em aberto” descreve lacunas substantivas e pode ser pública; monitoramento, fila editorial e gatilhos permanecem internos.


### Padrão transversal do botão ENVIAR MENSAGEM

- todo botão público **ENVIAR MENSAGEM** deve incluir `submit-button`;
- `submit-button` é sempre oval/pílula (`border-radius:999px`), nunca retangular;
- no Planejamento Financeiro, a cor permanece verde-petróleo;
- não aplicar essa forma automaticamente a todos os demais botões.

## Pauta editorial interna

O arquivo `governanca/PAUTA_EDITORIAL.md` é o **backlog editorial interno** do projeto para possíveis Artigos futuros.

Regras obrigatórias:

- a pauta é governança interna e **não integra o Site Público**;
- não incluir a pauta, seus estados, prioridades ou itens ainda não publicados em menus, cards, páginas de coleção, Mapa do Site, sitemap, feed ou metadados públicos;
- uma entrada na pauta registra apenas uma hipótese editorial; **não constitui promessa de pesquisa, redação ou publicação**;
- cada item deve registrar, quando possível, identificador, título provisório, pergunta/ângulo, eixo, relação com conteúdo existente, prioridade, estado, densidade e Estratégia Autônoma vinculada;
- antes de pesquisa substantiva, avaliar ao menos relevância, novidade, densidade, disponibilidade de fontes e risco de redundância;
- pauta e Roadmap não são equivalentes: a pauta organiza possibilidades editoriais; o Roadmap e os Planos de Fases governam trabalho efetivamente priorizado;
- quando um item for aprovado para execução, abrir ou vincular Estratégia Autônoma e Plano de Fases antes da pesquisa substantiva;
- quando o artigo for publicado, atualizar o item para `PUBLICADA` e registrar a referência final;
- itens suspensos ou descartados permanecem rastreáveis com motivo suficiente para evitar retrabalho;
- a auditoria de publicação deve verificar que `governanca/PAUTA_EDITORIAL.md` e seus estados internos não vazaram para a camada pública.

Estados canônicos: `IDEIA`, `EM_TRIAGEM`, `APROVADA_PARA_PESQUISA`, `EM_PESQUISA`, `PRONTA_PARA_REDACAO`, `EM_REDACAO`, `PRONTA_PARA_PUBLICACAO`, `PUBLICADA`, `SUSPENSA` e `DESCARTADA`.



## Classificação Universal de Informação

Antes de criar, mover, enviar, fazer upload, commit, publicar ou anexar arquivo persistente, aplicar a política global:

- `/Governanca-Geral-Modelos-IA/CLASSIFICACAO_UNIVERSAL_INFORMACAO.md`;
- `/Governanca-Geral-Modelos-IA/INFORMATION_CLASSIFICATION_POLICY.json`.

Se a Biblioteca não estiver acessível, aplicar obrigatoriamente as regras mínimas abaixo:

1. classificar **sensibilidade**: `S0_PUBLICO`, `S1_INTERNO_NAO_SENSIVEL`, `S2_CONFIDENCIAL`, `S3_ALTAMENTE_SENSIVEL` ou `S4_SEGREDO_CRITICO`;
2. classificar **superfície**: `P0_COFRE_EXTERNO`, `P1_GIT_PRIVADO`, `P2_GIT_PUBLICO_REPOSITORIO` ou `P3_PUBLICO_SITE`;
3. `S2` ou superior nunca pode ser salvo em repositório público nem no Site;
4. documento bruto `S3` permanece em cofre externo por padrão e não deve ser commitado ao Git;
5. `S4` nunca deve ser enviado ao Modelo nem persistido em Git, Biblioteca, chat ou logs;
6. conteúdo só pode descer de classe mediante criação de **derivado sanitizado**; o original mantém sua classificação;
7. mudança de visibilidade do repositório, ativação de Pages ou mudança de destino exige nova classificação.

O arquivo `INFORMATION_HANDLING_PROFILE.json` registra a superfície técnica e os limites deste repositório.

## Índice semântico-factual do acervo

Manter `governanca/KNOWLEDGE_INDEX.jsonl`, gerado por `tools/build_knowledge_index.py`, como camada interna de descoberta. Consultar o índice antes de varreduras manuais amplas e confirmar achados materiais no documento original. O índice não replica texto integral e não substitui fontes CFP®/Planejar ou evidência acadêmica.

## BDTD/IBICT no módulo research

Para endividamento, superendividamento, comportamento financeiro, crédito, consumo, educação financeira e outros temas compatíveis com pós-graduação brasileira, pesquisar sistematicamente a **BDTD/IBICT** como fonte complementar acadêmica. Validar a obra no repositório institucional de origem e por Handle/DOI quando disponível. A BDTD não é fonte canônica do CFP®.

## Inovação e aperfeiçoamento proativos

Manter `IMPROVEMENT_LOG.jsonl`. Oportunidade material de automação, indexação, padronização, fonte adicional, redução de retrabalho ou melhoria de verificabilidade deve ser comunicada e persistida. Sugestão não autoriza expansão silenciosa de escopo. No fechamento de trabalho substancial, executar **innovation check**.
