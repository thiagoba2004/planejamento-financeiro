# AGENTS.md — PLANEJAMENTO FINANCEIRO

**project_code:** `PRJ-000004`  
**project_sequence:** `000004`  
**project_alias:** `PF`  
**project_name:** `Planejamento Financeiro`  
**project_id legado:** `planejamento-financeiro`  
**generated_from_kernel:** `1.4`  
**generator_release:** `1.9`  
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

## 11. Módulo web-site

O Site é uma arquitetura pública multipágina. Não pode ser reduzido a uma Home com cards e uma página longa.

**Menu global obrigatório:** Início · CFP® · Gestão Financeira · Casos · Ferramentas · Métricas · Fontes · Fale Conosco.

Regras obrigatórias:
- o mesmo menu global aparece em todas as páginas;
- a página corrente usa `aria-current="page"`;
- no mobile, o menu permanece acessível em linha horizontal rolável;
- a Home é institucional e enxuta; não contém catálogo dos Menus nem “Explore o Site”;
- toda página pública possui no rodapé o hiperlink **Mapa do Site**;
- `mapa-do-site/` reflete as rotas públicas reais;
- páginas centrais de Menu possuem conteúdo útil, não placeholders;
- a interface pública não exibe códigos, estados e metadados de governança interna;
- `SITE_ARCHITECTURE.md` é a fonte da arquitetura;
- `SITE_STYLE_GUIDE.md` é a fonte da identidade visual;
- mudanças estruturais exigem auditoria desktop/mobile, links, overflow e navegação.

**Identidade visual:** deve ser exclusiva deste projeto. Reutilizar a estrutura do Classe e Massas não autoriza reutilizar sua paleta, tipografia ou composição.

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

**Estado atual:** `MIGRACAO_TECNICA_PENDENTE` de FormSubmit para Forminit + EmailJS.

## 11. Módulo software

Distinguir `IMPLEMENTADO`, `TESTADO`, `VERSIONADO`, `IMPLANTADO` e `VERIFICADO EM EXECUÇÃO`. Site no repositório não equivale a site publicado.

## 14. Regra específica do CFP®

O projeto deve manter uma matriz rastreável entre:
1. fonte oficial vigente;
2. domínio/competência;
3. conteúdo de estudo;
4. exercício ou caso;
5. aplicação profissional;
6. revisão/atualização.

Quando programa, regulamento ou material oficial mudar, identificar o impacto nas unidades dependentes antes de marcá-las como atualizadas.

## 15. Interoperabilidade com PRJ-000003

O superendividamento também pode ser estudado em Ações Judiciais. Este projeto trata prioritariamente do fenômeno financeiro, diagnóstico, prevenção, recuperação e competências profissionais. Questões jurídicas podem ser referenciadas, mas não devem transformar este projeto em fonte jurídica primária.

## 16. Fechamento

Antes de declarar etapa concluída, verificar fontes, cálculos, coerência entre prova/prática, persistência, versionamento, publicação quando aplicável e próximo passo lógico.

> **Nunca obrigar o usuário a pagar novamente, com tempo, energia ou recursos, por falha de memória, persistência, continuidade, planejamento ou verificação do Modelo de IA.**
