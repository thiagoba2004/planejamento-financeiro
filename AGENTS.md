# AGENTS.md — PLANEJAMENTO FINANCEIRO

**project_code:** `PRJ-000004`  
**project_sequence:** `000004`  
**project_alias:** `PF`  
**project_name:** `Planejamento Financeiro`  
**project_id legado:** `planejamento-financeiro`  
**generated_from_kernel:** `1.4`  
**generator_release:** `1.8`  
**repository:** `thiagoba2004/planejamento-financeiro`  
**modules:** `research`, `publication`, `software`, `data`, `professional-education`

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
- não reconstruir critérios de prova ou certificação de memória quando a fonte oficial puder ser consultada.

## 8. Módulo professional-education

Todo tópico formativo deve separar:

```text
TRILHA_PROVA
TRILHA_PRATICA
```

A sobreposição é desejável quando real; a confusão é proibida.

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

Todo texto editorial/publicável deve manter:

```text
Markdown (.md) = fonte textual canônica
HTML (.html) = publicação
JSON (.json) = representação estruturada
```

Alterações materiais devem ser sincronizadas nos três artefatos.

### 10.1. Separação entre governança interna e Site Público

O Site Público é orientado ao aluno, profissional e leitor externo. A governança permanece no repositório e **não deve ser exibida na interface pública**.

É proibido publicar na UI, rodapé, cabeçalho, cards, tabelas ou metadados destinados ao navegador:

- códigos internos de projeto, estratégia, fase, pedido, evento, competência, caso ou fonte (`PRJ-*`, `EA-*`, `F-*`, `REQ-*`, `EVT-*`, `PF-COMP-*`, `PF-CASO-*`, `SRC-*`);
- números de fase, gates, estados editoriais/técnicos e status de workflow;
- versões de kernel/gerador, IDs de deployment, run, commit, branch ou arquivos de governança;
- nomes como `PROJECT_STATE`, `REQUEST_LOG`, `STRATEGY_LOG`, `AGENTS` ou equivalentes;
- rótulos metodológicos internos como graus A/B/P, códigos A1–A4 ou códigos de métricas, quando não forem necessários à compreensão do leitor.

Na camada pública, converter conceitos úteis para linguagem natural, por exemplo:

- `TRILHA_PROVA` → “Para a prova CFP®”;
- `TRILHA_PRATICA` → “Na prática profissional”;
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

### 10.2. Arquitetura pública e identidade visual

O Site Público adota arquitetura multipágina, inspirada no padrão estrutural do Classe e Massas, mas com identidade própria.

**Menu global obrigatório:** Início · CFP® · Gestão Financeira · Casos · Ferramentas · Métricas · Fontes.

Regras:
- o menu global deve aparecer em todas as páginas públicas;
- no mobile, o menu permanece em uma linha horizontal rolável, sempre acessível;
- a página atual deve possuir destaque por `aria-current="page"`;
- cada área central deve conter conteúdo útil, não placeholders;
- a homepage deve apresentar a arquitetura do Site e conduzir às áreas;
- o Site não pode ser reduzido a uma homepage e uma unidade longa.

**Identidade exclusiva Planejamento Financeiro:**
- verde-petróleo como cor estrutural;
- branco frio e verde muito claro como superfícies;
- turquesa como interação;
- âmbar como acento;
- tipografia predominantemente sans-serif;
- cards contemporâneos com cantos arredondados;
- não reutilizar a paleta nem a aparência do Classe e Massas ou do Ações Judiciais.

Os tokens visuais vigentes estão em `assets/style.css`.

### 10.3. Início, Mapa do Site e Fale Conosco

1. A página **Início** é institucional e enxuta. É proibido transformá-la em catálogo, índice ou explicação dos Menus.
2. O catálogo de navegação deve ficar na página **Mapa do Site**.
3. Toda página pública deve possuir, no rodapé, hiperlink denominado exatamente **Mapa do Site**.
4. **Fale Conosco** integra obrigatoriamente o menu global.
5. O Fale Conosco deve disponibilizar o e-mail institucional `planejamentofinanceiro2012@gmail.com` e formulário protocolado.
6. O protocolo público usa prefixo `PF-`, data/hora e componente aleatório.
7. Se o visitante informar e-mail, o formulário deve solicitar o envio automático do protocolo ao endereço informado.
8. O protocolo só identifica a comunicação; não significa análise, aceite ou resposta.
9. Mudanças no provedor do formulário devem preservar geração de protocolo, confirmação visual e tentativa de confirmação por e-mail.
10. A página de confirmação deve ser `noindex,nofollow`.

## 11. Módulo software

Distinguir `IMPLEMENTADO`, `TESTADO`, `VERSIONADO`, `IMPLANTADO` e `VERIFICADO EM EXECUÇÃO`. Site no repositório não equivale a site publicado.

## 12. Regra específica do CFP®

O projeto deve manter uma matriz rastreável entre:
1. fonte oficial vigente;
2. domínio/competência;
3. conteúdo de estudo;
4. exercício ou caso;
5. aplicação profissional;
6. revisão/atualização.

Quando programa, regulamento ou material oficial mudar, identificar o impacto nas unidades dependentes antes de marcá-las como atualizadas.

## 13. Interoperabilidade com PRJ-000003

O superendividamento também pode ser estudado em Ações Judiciais. Este projeto trata prioritariamente do fenômeno financeiro, diagnóstico, prevenção, recuperação e competências profissionais. Questões jurídicas podem ser referenciadas, mas não devem transformar este projeto em fonte jurídica primária.

## 14. Fechamento

Antes de declarar etapa concluída, verificar fontes, cálculos, coerência entre prova/prática, persistência, versionamento, publicação quando aplicável e próximo passo lógico.

> **Nunca obrigar o usuário a pagar novamente, com tempo, energia ou recursos, por falha de memória, persistência, continuidade, planejamento ou verificação do Modelo de IA.**
