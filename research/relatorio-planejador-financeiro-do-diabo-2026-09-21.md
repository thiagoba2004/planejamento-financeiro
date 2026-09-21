# RELATÓRIO DO PLANEJADOR FINANCEIRO DO DIABO

## Auditoria adversarial integral do Site Planejamento Financeiro

**Data:** 21 de setembro de 2026  
**Estratégia:** EA-000004-000023  
**Escopo:** todos os 30 HTMLs públicos identificados, seus Markdown canônicos correspondentes, fontes centrais, fórmulas, casos, navegação, Fale Conosco e coerência entre as unidades.

## 1. Conclusão executiva

A conclusão principal é semelhante, mas não idêntica, à auditoria adversarial do Projeto Ações Judiciais:

**o Site Planejamento Financeiro possui boa arquitetura de raciocínio e várias salvaguardas corretas, mas ainda não está suficientemente resistente a um leitor profissional que trate cada fórmula, rótulo e sequência como prescrição técnica.**

Não encontrei uma falha única capaz de invalidar o Site inteiro. Encontrei, porém, quatro classes de risco que merecem correção:

1. **condições omitidas em fórmulas aparentemente universais**;
2. **fronteira insuficientemente explícita entre planejamento financeiro e atividades reguladas/especializadas**;
3. **efeito de halo CFP®**, no qual conteúdos profissionais do Projeto podem parecer objetivos oficiais do exame sem mapeamento direto;
4. **ruptura da fonte da verdade**, porque diversos Markdown “canônicos” são muito mais pobres que o HTML efetivamente publicado.

A auditoria técnica de navegação resistiu bem: foram identificados 30 HTMLs públicos, sem ausência de `<title>` ou `<h1>`, sem destinos internos inexistentes na varredura estática e sem vazamento dos códigos de governança pesquisados.

**Estado final da auditoria: ACHADOS REQUEREM CORREÇÃO.**

---

## 2. ACHADO DE ALTA PRIORIDADE — Markdown canônico e HTML público não representam a mesma verdade

O próprio AGENTS define:

> Markdown = fonte textual canônica  
> HTML = publicação

Mas várias páginas centrais contradizem materialmente essa regra.

Exemplos objetivos:

- `cfp/index.md`: cerca de 160 caracteres; o HTML contém estrutura do exame, oito módulos, Módulo II, data do 54º Exame e links oficiais;
- `fontes/index.md`: cerca de 500 caracteres; o HTML contém extensa biblioteca institucional;
- `metricas/index.md`: cerca de 170 caracteres; o HTML contém as métricas que o leitor efetivamente usa;
- `gestao-financeira/index.md`: cerca de 420 caracteres; o HTML contém todo o catálogo temático;
- `casos/index.md`: pouco mais de 1.000 caracteres; o HTML reúne um corpus de casos muito maior;
- `ferramentas/index.md`: pouco mais de 1.200 caracteres; o HTML contém a biblioteca real de ferramentas.

### Risco

Uma auditoria do Markdown pode aprovar um texto que não é o texto público. Uma regeneração futura a partir do Markdown pode apagar conteúdo material. E a ideia de “fonte canônica” deixa de ter sentido operacional.

### Correção necessária

Instituir **paridade semântica obrigatória Markdown ↔ HTML**. O layout pode divergir; o conteúdo técnico, as condicionantes, fórmulas, avisos, fontes e estados de atualização não.

---

## 3. ACHADO DE ALTA PRIORIDADE — O Fale Conosco possui versões incompatíveis do próprio estado

O Markdown canônico ainda afirma que o backend permanece indisponível até configuração e teste end-to-end.

Entretanto:

- o `PROJECT_STATE.json` registra `E2E_VERIFICADO`;
- há teste real concluído em 20/09/2026;
- o HTML possui os IDs reais de Forminit e EmailJS;
- o formulário é exibido por JavaScript quando a configuração está presente;
- o HTML estático conserva a frase “O formulário está temporariamente indisponível”, escondida em execução.

### Risco

O JavaScript mascara texto editorial obsoleto, e três fontes de verdade descrevem estados diferentes.

### Correção

Atualizar Markdown e HTML estático para o estado real e deixar o fallback técnico como fallback, não como narrativa principal.

---

## 4. ACHADO DE ALTA PRIORIDADE — Lacuna LGPD no Fale Conosco

O canal permite enviar:

- nome ou pseudônimo;
- e-mail;
- assunto e mensagem;
- URL;
- até três anexos, com até 25 MB no total.

O aviso para evitar dados desnecessários é positivo, mas não substitui transparência sobre tratamento de dados.

### Risco

Um visitante pode anexar extratos, contratos, documentos fiscais, informações sobre patrimônio, dados familiares, documentos judiciais ou dados de terceiros — justamente materiais potencialmente sensíveis em um Site de planejamento financeiro.

### Correção

Criar **Aviso de Privacidade / Tratamento de Dados** abrangendo ao menos finalidades, categorias de dados, canal do controlador/responsável, provedores utilizados, retenção, exclusão, anexos, direitos do titular, segurança/minimização e compartilhamentos necessários.

---

## 5. ACHADO DE ALTA PRIORIDADE — “R$ 100 mil líquidos” foi transformado em “integralmente livres/disponíveis”

O cenário fornecido ao Projeto confirmou que os R$ 100.000,00 já eram **líquidos**.

Em várias páginas, essa premissa evoluiu para:

> “líquidos e integralmente disponíveis”

São conceitos diferentes.

**Líquido** pode significar valor após retenções/descontos considerados no cenário.

**Disponível em caixa** significa que o dinheiro foi recebido.

**Livre para alocação** exigiria ainda confirmar ausência de destinações obrigatórias, obrigações já assumidas, restrições contratuais, processuais ou jurídicas e necessidades de curto prazo.

### Risco

A palavra “integralmente” pode ser lida como conclusão jurídica/econômica de que nenhum valor está vinculado, o que o próprio guia de superendividamento não pode assegurar.

### Correção

Usar algo como:

> “R$ 100.000,00 recebidos em caixa e líquidos das retenções consideradas no cenário; a disponibilidade econômica para alocação e eventual disponibilidade jurídica devem ser verificadas separadamente.”

---

## 6. ACHADO DE ALTA PRIORIDADE — “Patrimônio líquido + R$ 100 mil” não é universalmente verdadeiro no momento do recebimento

Três unidades repetem, em substância:

`PATRIMÔNIO_LÍQUIDO_APÓS = PATRIMÔNIO_LÍQUIDO_ANTES + 100.000`

Isso é verdadeiro **se o balanço anterior ainda não reconhecia nenhum direito/recebível referente à indenização**.

Mas, se o direito já estava reconhecido como ativo — por exemplo, crédito líquido decorrente de acordo, sentença ou outro direito suficientemente mensurável — o recebimento pode apenas converter **contas a receber → caixa**, elevando liquidez sem aumentar novamente o patrimônio líquido.

### Risco

O Site pode contar duas vezes a mesma criação de riqueza: uma quando reconhece o direito e outra quando o dinheiro entra.

### Correção

Separar:

- **efeito sobre caixa/ativos líquidos:** +R$ 100 mil no recebimento, conforme a linha de base;
- **efeito sobre patrimônio líquido:** +R$ 100 mil apenas se o ativo correspondente não estiver previamente reconhecido e não houver contrapartida/passivo.

Esse ponto deve ser corrigido em:
- `indenizacao-trabalhista-capital-liquido`;
- `indenizacao-superendividamento`;
- `plano-financeiro-integrado-pos-indenizacao`.

---

## 7. ACHADO DE ALTA PRIORIDADE — Fórmula do gap de objetivos mistura datas sem trazê-las para a mesma base

A unidade de objetivos usa:

`GAP_OBJETIVO = VALOR_ALVO - RECURSOS_JA_DESTINADOS - APORTES_FUTUROS_PROJETADOS`

A fórmula parece intuitiva, mas só é matematicamente coerente se todos os valores estiverem expressos na **mesma data-base e na mesma unidade monetária real/nominal**.

R$ 100 mil hoje, R$ 20 mil aportados daqui a cinco anos e um objetivo de R$ 300 mil em dez anos não podem ser simplesmente somados/subtraídos sem capitalização, desconto e definição de inflação.

### Correção

Escolher uma metodologia:

- levar ativos e aportes ao valor futuro na data do objetivo; ou
- trazer o objetivo e fluxos a valor presente.

Declarar retorno líquido, inflação, momento dos aportes, tributação/custos quando materiais e se o cálculo é nominal ou real.

---

## 8. ACHADO DE ALTA PRIORIDADE — Perímetro regulatório da atuação está insuficientemente explícito

O Site usa expressões como:

- selecionar classes;
- recomendar alterações;
- implementar;
- rebalancear;
- reavaliar suitability;
- manter, ajustar, substituir ou reforçar seguros/proteções.

Como material educacional, essas expressões fazem sentido. Como orientação sobre atuação profissional, precisam de uma fronteira mais precisa.

A certificação CFP® não deve ser apresentada como se, por si só, concedesse autorização para toda atividade regulada.

No mercado de valores mobiliários, a Resolução CVM nº 19 disciplina a atividade de consultoria de valores mobiliários, enquanto a Resolução CVM nº 30 impõe deveres de suitability aos participantes abrangidos pela norma. No mercado de seguros, a intermediação de contratos por corretor depende de habilitação e registro perante a Susep.

### Risco

O aluno pode aprender a técnica financeira correta e concluir que toda recomendação ou implementação está automaticamente dentro de sua autorização profissional.

### Correção

Criar uma seção canônica **“Perímetro profissional e atividades reguladas”**, diferenciando:

- educação financeira;
- planejamento financeiro;
- análise e modelagem;
- recomendação individualizada de valores mobiliários, quando caracterizar atividade regulada;
- distribuição/intermediação;
- corretagem de seguros;
- atuação jurídica, contábil, atuarial e tributária.

A regra deve ser funcional: depende da atividade efetivamente exercida, não apenas do título profissional.

Fontes centrais:
- CVM — Resolução 19: https://conteudo.cvm.gov.br/legislacao/resolucoes/resol019.html
- CVM — Resolução 30: https://conteudo.cvm.gov.br/legislacao/resolucoes/resol030.html
- Susep — cadastro/atuação de corretores: https://www.gov.br/susep/pt-br/arquivos/arquivos-licenciamento/corretor-de-seguros/perguntas-frequentes

---

## 9. ACHADO DE ALTA/MÉDIA PRIORIDADE — “Halo CFP®”: formação do Projeto pode parecer conteúdo oficial do exame

O Projeto é cuidadoso em alguns textos. O dossiê de superendividamento, por exemplo, informa que determinados conteúdos específicos permanecem em grau de evidência inferior até leitura direta da fonte oficial.

Mas, ao longo do Site, multiplicam-se seções como:

- “Para a prova CFP®”;
- “Para a formação CFP®”;
- “A unidade mobiliza...”.

O conteúdo é frequentemente pertinente à profissão, mas nem sempre está demonstrado como objetivo literal do programa vigente.

### Risco

O leitor pode confundir:
1. objetivo oficial da prova;
2. conceito geral pertencente a um domínio do CFP®;
3. aplicação profissional desenvolvida pelo próprio Site.

### Correção

Criar três rótulos públicos:

- **Mapeado diretamente no programa vigente**;
- **Competência/conceito do domínio CFP®**;
- **Aplicação profissional do Projeto — não apresentada como objetivo literal da prova**.

A página CFP® também deve expor de forma mais completa as fontes oficiais vigentes: programa, perfil de competências, fórmulas, orientações, Manual de Certificação, Guia de Melhores Práticas e Código de Ética.

---

## 10. ACHADO DE PRIORIDADE MÉDIA — Dois modelos incompatíveis de “perfil de risco”

Uma unidade trabalha com **três dimensões**:

- capacidade;
- disposição;
- necessidade de risco.

Outra usa **cinco dimensões**:

- capacidade;
- necessidade;
- tolerância;
- horizonte;
- liquidez.

Não é errado modelar risco com várias dimensões, mas o Site não explica por que os modelos mudam nem qual deles é canônico.

Além disso, a Resolução CVM nº 30 verifica, no mínimo, adequação a:
- objetivos;
- situação financeira;
- conhecimento necessário para compreender riscos.

### Correção

Criar um modelo canônico distinguindo:

**dimensões pessoais de risco**
- capacidade;
- tolerância/disposição;
- necessidade de risco;

**restrições do plano**
- horizonte;
- liquidez;
- concentração;
- obrigações;

**suitability regulatório, quando aplicável**
- objetivos;
- situação financeira;
- conhecimento/experiência e demais elementos da norma.

---

## 11. ACHADO DE PRIORIDADE MÉDIA — Fórmula da reserva pode produzir dupla contagem

A página de liquidez define:

`RESERVA_ALVO = E × H`

e depois:

`CAPITAL_REMANESCENTE = C - I0 - P12 - LACUNA_RESERVA`

Mas:
- `E × H` já representa meses de despesas essenciais;
- `P12` pode conter despesas dos próximos 12 meses que se sobrepõem a essas mesmas despesas;
- `I0` pode ser caixa operacional que também integra a reserva disponível.

### Risco

A metodologia pode reservar o mesmo gasto duas vezes.

### Correção

Definir buckets mutuamente exclusivos ou uma reconciliação explícita:
- caixa operacional;
- despesas extraordinárias/previsíveis não incluídas no custo mensal essencial;
- reserva de emergência;
- demais compromissos.

E indicar claramente quando uma despesa já incluída em `E` não deve reaparecer em `P12`.

---

## 12. ACHADO DE PRIORIDADE MÉDIA — Gap de proteção mistura capital e fluxos sem equivalência temporal

A fórmula usada é, em essência:

`GAP_PROTECAO = NECESSIDADE_BRUTA - ATIVOS_LIQUIDOS - COBERTURAS - BENEFICIOS`

Problemas possíveis:
- ativos líquidos podem já estar comprometidos com reserva ou objetivos;
- benefício mensal futuro não é diretamente equivalente a capital à vista;
- coberturas e benefícios têm prazos, elegibilidade e eventos de pagamento distintos;
- alguns valores podem ser tributados ou sujeitos a condições.

### Correção

Usar apenas **ativos efetivamente disponíveis para o risco analisado** e converter fluxos futuros a uma base temporal comparável, ou construir um mapa de necessidades por período em vez de uma única soma.

---

## 13. ACHADO DE PRIORIDADE MÉDIA — Métricas internas aparecem como se fossem quase universais

A página Métricas lista:

- solvência = ativos/passivos;
- cobertura de despesas = ativos líquidos/despesas essenciais;
- comprometimento = serviço da dívida/renda líquida;
- fluxo livre etc.

São indicadores úteis. O problema é a falta de uma ficha metodológica dizendo:

- se a métrica é padrão externo ou metodologia própria do Site;
- unidade;
- horizonte;
- data-base;
- tratamento de renda variável;
- tratamento de denominador zero ou negativo;
- comportamento quando passivos são zero;
- interpretação e limites.

### Exemplo

`ATIVOS / PASSIVOS` não produz um número operacionalmente útil quando passivos = 0. O Site precisa dizer como representar esse caso em vez de deixar a divisão implícita.

### Correção

Criar um **Protocolo Canônico de Métricas**, com ficha para cada indicador.

---

## 14. ACHADO DE PRIORIDADE MÉDIA — “Serviço da dívida” pode ser subestimado pelo uso de pagamentos mínimos

Uma unidade define serviço mensal da dívida como:

> soma das parcelas e pagamentos mínimos confirmados no mês.

Para crédito rotativo, pagamento mínimo de cartão pode ser apenas requisito mínimo contratual e não representar serviço sustentável da dívida nem amortização adequada do principal.

### Correção

Separar:
- **caixa mínimo contratual do mês**;
- **serviço planejado da dívida**;
- **valor necessário para evitar/encerrar financiamento rotativo**, quando aplicável.

---

## 15. ACHADO DE PRIORIDADE MÉDIA — Alguns casos não são totalmente reproduzíveis

Os casos de `indenizacao-superendividamento` apresentam resultados de fluxo corretos sob hipóteses implícitas, mas nem sempre registram todos os inputs.

Exemplo: “quitação de R$ 70 mil” leva o serviço mensal de R$ 3,5 mil a zero, mas o texto não diz expressamente que os R$ 70 mil quitam integralmente a obrigação que gerava todo o serviço mensal.

Outro caso informa fluxo antes/depois sem declarar claramente o serviço mensal inicial.

### Correção

Todo caso quantitativo deve ter um quadro de inputs completo:
- renda;
- essenciais;
- dívida/serviço antes;
- saldo;
- desembolso;
- serviço depois;
- liquidez restante;
- fórmula;
- resultado.

---

## 16. ACHADO DE PRIORIDADE MÉDIA — “80 meses até exaustão” é uma runway estática, não uma projeção

A fórmula:

`MESES_ATÉ_EXAUSTÃO = LIQUIDEZ_REMANESCENTE / |FLUXO_LIVRE_NEGATIVO|`

é aritmeticamente correta no caso simples.

Mas pressupõe:
- déficit constante;
- nenhum retorno sobre o capital;
- nenhuma inflação;
- nenhuma despesa extraordinária;
- nenhuma mudança de renda ou dívida;
- saídas uniformes.

O texto diz que não é prazo recomendado, o que ajuda, mas ainda precisa chamá-la de **estimativa estática de primeira ordem**, não previsão.

---

## 17. ACHADO DE PRIORIDADE MÉDIA — Cronogramas 7/30/90/180/365 dias podem parecer padrão CFP®

Várias unidades usam cronogramas semelhantes:
- 0–7 dias;
- 30 dias;
- 90 dias;
- 180 dias;
- 365 dias.

Eles são pedagogicamente úteis, mas não estão identificados de forma uniforme como **heurística operacional do Projeto**.

### Risco

O aluno pode memorizar os prazos como exigência profissional, regulatória ou do CFP®.

### Correção

Rotular: “sequenciamento didático/adaptável do Site; não constitui prazo universal da Planejar, FPSB ou regulador, salvo quando outra fonte indicar prazo específico.”

---

## 18. ACHADO DE PRIORIDADE MÉDIA — O plano integrado coloca “proteção” como bucket de capital apesar de o seguro ser despesa recorrente

O plano pós-indenização reconcilia:

> continuidade + reserva + dívidas + objetivos/proteção + investimentos + uso discricionário

Mas outra página explica corretamente que prêmio de seguro mensal/anual precisa ser sustentável pela **renda recorrente**, não pelo capital extraordinário.

### Contradição

“Proteção” pode significar:
- prêmio recorrente;
- custo inicial;
- capital destinado a autosseguro;
- objetivo patrimonial.

Essas coisas não devem ser agrupadas sem explicação.

### Correção

Separar:
- **capital de proteção** eventualmente reservado;
- **prêmios recorrentes**, tratados no fluxo;
- custos pontuais de contratação, quando existirem.

---

## 19. ACHADO DE PRIORIDADE MÉDIA — Fórmula de valuation empresarial é simplificada demais para ser apresentada sem rótulo

A página empresarial usa:

`valor da firma = VP dos fluxos operacionais + VP do valor terminal`

e depois:

`valor do capital próprio = valor da firma - dívida líquida`

Essa ponte é coerente para metodologias do tipo **FCFF → Enterprise Value**, com os ajustes apropriados.

Mas não é fórmula universal de DCF:
- FCFE conduz diretamente ao equity value;
- ativos não operacionais, caixa excedente, participações, passivos contingentes e outros ajustes podem alterar a ponte;
- classes de participação, acordos e iliquidez podem impedir que `equity value × percentual` represente valor realizável.

### Correção

Rotular o exemplo como **ponte simplificada FCFF → valor da firma → capital próprio** e listar os principais ajustes.

---

## 20. ACHADO DE PRIORIDADE MÉDIA — Fórmula de “renda empresarial média ajustada” é conceitualmente ambígua

O texto define:

`média de pagamentos recorrentes documentados - itens extraordinários`

Se a média já foi construída apenas com **pagamentos recorrentes**, itens extraordinários já deveriam estar fora da base.

### Correção

Definir:
1. pagamentos totais ao sócio no período;
2. classificar recorrentes e extraordinários;
3. normalizar pró-labore/distribuições;
4. calcular média apenas da base sustentável.

---

## 21. ACHADO ESTRUTURAL — O Site ensina muitas técnicas, mas pouco do processo completo de planejamento financeiro

A arquitetura enfatiza:
- métricas;
- casos;
- ferramentas;
- temas;
- decisões.

Mas o processo profissional completo não aparece como eixo público forte.

Os padrões globais da FPSB organizam a profissão em **Knowing | Doing | Being** e descrevem o processo de planejamento como colaborativo e iterativo, começando por estabelecer/definir a relação, escopo, competências e conflitos de interesse.

### Lacuna

O Site ensina muito bem “o que calcular”, mas poderia ensinar melhor:
- relação e escopo;
- responsabilidades;
- conflitos de interesse;
- qualidade/consentimento dos dados;
- formulação da recomendação;
- apresentação;
- implementação e limites de implementação;
- monitoramento;
- documentação;
- ética.

### Correção

Criar uma unidade central **Processo de Planejamento Financeiro** e fazer as unidades aplicadas apontarem para ela.

Fontes:
- FPSB — Financial Planning Process: https://fpsb.org/about-financial-planning/financial-planning-process/
- FPSB — Standards for the Profession: https://fpsb.org/standards-for-the-profession/

---

## 22. ACHADO DE PRIORIDADE MÉDIA — Falta declaração pública clara de independência institucional

O Site usa intensamente a marca CFP® e se apresenta como formação baseada no CFP®.

Não foi localizada, nas páginas centrais auditadas, uma ressalva visível do tipo:

> “Projeto independente; não é página oficial da Planejar nem da FPSB. Em caso de divergência, prevalecem os materiais oficiais vigentes.”

### Risco

Pode haver confusão de autoridade para um leitor externo.

### Correção

Inserir aviso institucional discreto na área CFP® e/ou rodapé metodológico, sem diminuir a utilidade formativa.

---

## 23. ACHADO DE PRIORIDADE MÉDIA — A rastreabilidade pública é menor do que a rastreabilidade interna

O `SOURCE_REGISTRY.jsonl` é robusto e registra emissor, documento, data de consulta, status e notas.

A página Fontes pública é útil, mas expõe sobretudo instituições/links e não entrega ao leitor o mesmo grau de rastreabilidade.

### Correção

Sem publicar logs internos, apresentar junto às afirmações sensíveis:
- órgão/autoria;
- documento;
- versão/data;
- status;
- link;
- data da última conferência.

Especial atenção para:
- regras do exame;
- tributação;
- limites regulatórios;
- FGC;
- SFH;
- previdência;
- regras locais de ITD/ITIV;
- produtos e suitability.

---

## 24. ACHADO DE BAIXA/MÉDIA PRIORIDADE — Conteúdo CFP® altamente perecível precisa de status visível

A página CFP® informa corretamente, na data da auditoria, que o 54º Exame ocorrerá em 18/10/2026 e que a estrutura vigente tem oito módulos.

Mas dados de exame envelhecem muito rápido.

### Correção

Mostrar ao lado da informação:

> “Verificado em 21/09/2026”

e criar rotina para reclassificar automaticamente ou editorialmente uma edição como histórica após a prova.

---

## 25. PONTO DE ATENÇÃO — Tributação da indenização está correta, mas a composição da verba precisa continuar isolada

O Site afirma que não incide IR sobre verba percebida a título de dano moral. Isso está correto para pessoa física e é reconhecido pela própria Receita Federal com base no Tema 370/STJ.

O risco surgiria se um acordo/reclamação tivesse **outras rubricas** misturadas e o leitor tratasse todo o pagamento como dano moral.

### Correção preventiva

Manter a regra:

> a não incidência é da verba efetivamente qualificada como dano moral; outras parcelas de um acordo ou condenação precisam ser classificadas separadamente.

---

# 26. O que resistiu ao Planejador Financeiro do Diabo

A auditoria adversarial também encontrou pontos tecnicamente sólidos.

### Reserva de emergência

A referência de **6 a 12 meses** está corretamente apresentada como estimativa educacional, não como lei universal. O Portal do Investidor/CVM efetivamente informa essa faixa e ressalta que o valor depende do tipo/estabilidade da renda e da composição familiar.

### FGC

Os limites apresentados — **R$ 250 mil por CPF/CNPJ por instituição ou conglomerado** e **R$ 1 milhão em quatro anos** — estão alinhados à informação oficial atual. O Site também faz corretamente a ressalva de que FGC não elimina outros riscos.

### Moradia / SFH

O valor de **R$ 2,25 milhões** citado como limite máximo de avaliação do imóvel no SFH é consistente com a Resolução CMN nº 5.255/2025.

### ITD da Bahia

As alíquotas usadas para doações — 3%, 3,5% e 4%, conforme faixas — estão consistentes com a página oficial da Sefaz/BA para fatos a partir de 27/03/2025, e o Site corretamente restringe o exemplo à Bahia.

### Indenização por dano moral e IR

A não incidência de IR está correta. A Receita registra expressamente a tese vinculante do Tema 370/STJ e inclusive observa a aplicação a dano moral recebido em reclamação trabalhista por pessoa física.

### Previdência

A referência à Lei nº 14.803/2024 está atualizada: a escolha entre regimes progressivo/regressivo pode ocorrer até o benefício ou primeiro resgate, conforme a disciplina legal aplicável.

### Separação estoque × fluxo

A ideia de que capital extraordinário não é renda recorrente está correta e é uma das melhores travas conceituais do Site. A fragilidade encontrada está no momento do reconhecimento patrimonial, não nessa distinção.

### Dívidas

A separação entre CET, saldo devedor, saldo para quitação, parcela e custo total é correta e evita vários erros clássicos.

### Divórcio

As páginas, em geral, respeitam bem a fronteira entre cenário financeiro e premissa jurídica. Não encontrei nelas tentativa sistemática de decidir guarda, alimentos, partilha ou responsabilidade jurídica por dívidas.

### Comportamento

A unidade comportamental evita diagnosticar psicologicamente a pessoa e usa perguntas neutras, o que é metodologicamente adequado.

### Arquitetura técnica

Na varredura dos 30 HTMLs:
- 0 páginas sem `<title>`;
- 0 páginas sem `<h1>`;
- 0 destinos internos inexistentes identificados;
- 0 vazamentos dos códigos internos pesquisados.

---

# 27. Resultado página por página

| Página | Resultado adversarial |
|---|---|
| **Início** | sem erro material relevante; falta reforçar independência institucional/metodologia |
| **CFP®** | dados atuais corretos; Markdown quase vazio; ampliar fontes oficiais e provenance do conteúdo de prova |
| **Conhecimentos** | HTML muito mais rico que o Markdown; risco de “halo CFP®” nas aplicações |
| **Casos** | bom acervo, mas HTML praticamente autônomo em relação ao Markdown; padronizar ficha reproduzível |
| **Ferramentas** | útil, porém precisa protocolo canônico de métricas e distinção fonte externa × metodologia própria |
| **Métricas** | fórmulas úteis; faltam unidade, data-base, exceções e denominadores-limite |
| **Fontes** | bom catálogo público, porém inferior ao registro interno em rastreabilidade; MD muito incompleto |
| **Gestão Financeira** | HTML é a verdadeira página; MD não é fonte canônica material |
| **Mapa do Site** | navegação funcional; paridade MD/HTML insuficiente |
| **Fale Conosco** | estado editorial contraditório + lacuna LGPD |
| **Mensagem recebida** | funcional; deve ser abrangida pelo aviso de privacidade/retenção |
| **Superendividamento PF** | estrutura conceitual boa; métricas internas precisam protocolo e conteúdo CFP® precisa gradação pública |
| **Divórcio — transição** | fronteira jurídica boa; cronogramas devem ser rotulados como heurísticos |
| **Patrimônio/partilha** | bom limite jurídico; valuation/cenários devem continuar datados e condicionais |
| **Moradia** | abordagem de custo total robusta; regra SFH atual correta; cronogramas/cenários não são padrões universais |
| **Filhos** | boa prevenção de dupla contagem; cenário familiar consolidado deve continuar sendo ferramenta, não “nova unidade familiar” presumida |
| **Dívidas/crédito/garantias** | boa separação contratual; “serviço da dívida” precisa distinguir pagamento mínimo de serviço sustentável |
| **Investimentos pós-divórcio** | forte conceitualmente; modelo de risco/suitability conflita com outra página e perímetro regulatório precisa ficar explícito |
| **Seguros/previdência** | boa cautela contratual; atuação regulada e equivalência capital × fluxo no gap de proteção precisam refinamento |
| **Tributação/declarações** | uma das páginas mais robustas; boas travas temporal/jurisdicional; preservar validação anual |
| **Empresas/participações** | boas distinções; DCF e renda normalizada estão simplificados demais |
| **Reconstrução pós-divórcio** | boa integração; cronograma é heurístico e deve ser rotulado |
| **Indenização — capital líquido** | IR correto; “líquido/disponível” e +R$100 mil no PL precisam correção |
| **Liquidez/reserva pós-indenização** | boa ideia; fórmula pode duplicar E×H, P12 e I0 |
| **Dívidas e capital indenizatório** | boa disciplina de dados e CET; sem erro crítico encontrado |
| **Indenização × superendividamento** | boa separação estoque/fluxo; +R$100 mil no PL e casos parcialmente implícitos requerem ajuste |
| **Investimentos e capital extraordinário** | boa lógica objetivos→classes; conflito do modelo de perfil + perímetro CVM |
| **Objetivos/aposentadoria/proteção** | gap de objetivos não respeita valor do dinheiro no tempo; gap de proteção mistura capital/fluxos |
| **Finanças comportamentais** | abordagem não moralizante e não diagnóstica resistiu bem; falta integração mais explícita com processo/ética |
| **Plano integrado pós-indenização** | boa reconciliação; PL +100k e bucket “proteção” precisam correção |
| **Template de unidade** | estrutura SABER/FAZER/DECIDIR é boa; deveria acrescentar perímetro regulatório, status da fonte e tipo de aderência ao CFP® |

---

# 28. Prioridade de correção

Minha ordem técnica é:

1. **Paridade Markdown ↔ HTML e fonte da verdade.**
2. **Fale Conosco + LGPD.**
3. **Premissa “líquido/disponível” e reconhecimento patrimonial dos R$ 100 mil.**
4. **Gap de objetivos e demais fórmulas com datas/dupla contagem.**
5. **Perímetro profissional/regulatório — CVM, Susep e especialidades.**
6. **Classificação pública de aderência ao CFP® e eliminação do “halo de prova”.**
7. **Modelo canônico de risco/suitability.**
8. **Protocolo canônico de métricas e casos reproduzíveis.**
9. **Processo de Planejamento Financeiro + ética/conflitos/escopo.**
10. **Rastreabilidade pública e aviso de independência institucional.**

---

# 29. Nova regra metodológica proposta

> **Nenhuma fórmula, métrica, sequência, cenário ou recomendação deve ser considerada auditada apenas porque sua aritmética está correta. A auditoria deve verificar também data-base, unidade, horizonte, sobreposição entre variáveis, valor do dinheiro no tempo, tratamento de denominadores-limite, qualidade dos dados, premissas implícitas, perímetro regulatório, natureza da fonte, aderência real ao CFP® e coerência com as demais unidades do Site.**

E uma segunda regra:

> **Toda afirmação de aderência ao CFP® deve declarar se deriva diretamente do programa/material oficial vigente, se é competência geral do domínio ou se é aplicação profissional desenvolvida pelo próprio Projeto.**

---

# 30. Conclusão do Planejador Financeiro do Diabo

O Site tem uma qualidade importante: ele frequentemente resiste à tentação de oferecer “percentuais mágicos”, carteiras universais e respostas automáticas. Isso é uma virtude real.

O seu ponto fraco atual está em outro nível.

**A metodologia é mais madura do que a governança matemática e regulatória que a sustenta.**

O próximo salto de qualidade não exige colocar mais conteúdo. Exige tornar cada fórmula e cada decisão profissional **auditável nas condições de validade**.

Uma fórmula pode estar certa e ainda ensinar errado se:
- soma valores de datas diferentes;
- conta duas vezes a mesma necessidade;
- trata caixa como criação nova de patrimônio quando o recebível já existia;
- mistura benefício mensal com capital à vista;
- usa “suitability” sem separar dever regulatório de metodologia de planejamento;
- chama aplicação profissional de “CFP®” sem dizer qual é o grau de aderência à fonte oficial.

Por isso, o Relatório conclui:

**ESTADO FINAL: ACHADOS REQUEREM CORREÇÃO.**


# 31. Validação final em fontes oficiais

Em 21/09/2026, os achados mais sensíveis foram novamente confrontados com fontes oficiais ou institucionais vigentes:

- **CVM — Resolução 19:** confirma que consultoria de valores mobiliários envolve orientação, recomendação e aconselhamento profissional, independente e individualizado; a própria norma exclui o planejador financeiro quando sua atuação não envolve essa atividade regulada.
- **CVM — Resolução 30:** permanece como norma de adequação de produtos, serviços e operações ao perfil do cliente.
- **Susep — corretores:** a orientação oficial vigente exige habilitação técnica e registro para atuar como corretor de seguros.
- **FPSB — Financial Planning Process:** confirma processo colaborativo e iterativo, com definição de relação e escopo, competências, conflitos de interesse, coleta de dados, análise, recomendações, implementação e revisão.
- **FGC:** confirma os limites de até R$ 250 mil por CPF/CNPJ por instituição ou conglomerado e teto global de R$ 1 milhão em quatro anos, nas condições do regulamento.
- **Banco Central / SFH:** confirma a elevação do teto do valor do imóvel no SFH para R$ 2,25 milhões.
- **Sefaz/BA — ITD:** confirma as alíquotas de doação de 3%, 3,5% e 4% para os fatos alcançados pela regra atual.
- **Receita Federal — Tema 370/STJ:** confirma a não incidência do IR sobre verba recebida a título de dano moral por pessoa física, inclusive a delimitação referente à reclamação trabalhista.
- **Lei nº 14.803/2024:** confirma a possibilidade de opção pelo regime tributário previdenciário até a obtenção do benefício ou a requisição do primeiro resgate, conforme os requisitos legais.

A validação externa **não altera o estado do relatório**: os achados continuam requerendo correção, e os pontos classificados como sólidos permaneceram confirmados.
