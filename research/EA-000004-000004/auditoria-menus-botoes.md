# Auditoria de Menus, Botões e Navegação — Planejamento Financeiro

**Data:** 20/09/2026  
**Estratégia:** EA-000004-000004 — Auditoria de Menus, Botões e Navegação

## 1. Escopo

Auditoria das 11 páginas HTML públicas do Site, cobrindo:

- menu global;
- Mapa do Site;
- links internos;
- âncoras;
- botões HTML reais;
- links estilizados como botão;
- cards clicáveis;
- sentido arquitetural de cada Menu;
- coerência entre aparência visual e comportamento.

## 2. Resultado técnico

### Navegação

- 11 páginas HTML públicas auditadas;
- menu global presente e consistente nas páginas;
- 133 links internos verificados;
- 10 links com fragmento/âncora verificados;
- 0 destinos internos quebrados;
- 0 fragmentos inexistentes;
- Mapa do Site acessível pelo rodapé;
- páginas-filhas usam o Menu-pai de forma coerente: Superendividamento marca Gestão Financeira; recibo marca Fale Conosco.

### Elementos de interação

Foram encontrados:

- **2 botões HTML reais**
  - `Enviar mensagem` — submit do formulário;
  - `Copiar protocolo` — ação local no navegador.

- **3 links estilizados como botão**
  - `Estudar os casos na unidade`;
  - `Enviar outra mensagem`;
  - `Voltar para Planejamento Financeiro`.

- **7 cards clicáveis**
  - 3 em CFP®;
  - 3 em Fontes;
  - 1 em Gestão Financeira.

Não foram encontrados botões mortos nem links internos quebrados.

## 3. Botão x hiperlink

A diferença observada pelo usuário é real, mas **não é por si só um erro**.

A regra semântica correta é:

- `<button>` = executa ação;
- `<a href>` = navega para outro destino;
- link pode visualmente parecer botão quando é uma chamada forte para navegação.

O Site atualmente respeita essa regra nos casos auditados.

### Problema de UX

A classe visual genérica `.button` é usada tanto em `<button>` quanto em `<a>`. Isso é tecnicamente válido, mas não comunica claramente ao visitante se ocorrerá uma ação ou uma navegação.

**Recomendação:** manter a semântica HTML correta e diferenciar visualmente:
- ação primária;
- navegação/CTA;
- link secundário.

### Rótulos a melhorar

1. `Estudar os casos na unidade`
   - funciona;
   - “na unidade” é pouco específico;
   - melhor: **Ver casos de Superendividamento**.

2. `Voltar para Planejamento Financeiro`
   - aponta para a Home;
   - o rótulo pode ser interpretado como retorno ao projeto ou à área;
   - melhor, mantendo o destino atual: **Voltar ao início**;
   - alternativa: apontar para Gestão Financeira e usar **Voltar para Gestão Financeira**.

3. `Enviar outra mensagem`
   - coerente com o destino e deve permanecer.

4. `Enviar mensagem`
   - ação real de formulário; correto como `button`.

5. `Copiar protocolo`
   - ação real local; correto como `button`.

## 4. Auditoria dos Menus

### Início — MANTER

Função clara e corretamente enxuta. Não duplica o Mapa do Site.

### CFP® — MANTER

Área autônoma e justificável:
- exame;
- estrutura da certificação;
- programa oficial;
- perfil de competências;
- materiais oficiais.

### Gestão Financeira — REESTRUTURAR NO PRIMEIRO NÍVEL

O conteúdo faz sentido, mas o Menu não escala bem como item global permanente.

O projeto pretende qualificar profissionais **com base no CFP® como um todo**. Gestão Financeira é apenas uma área/módulo. Hoje o primeiro conteúdo publicado pertence a ela, o que fez a arquitetura global nascer excessivamente condicionada à primeira unidade.

**Recomendação:** substituir no menu global por **Conhecimentos** (ou equivalente), com hierarquia:

```text
Conhecimentos
└── Gestão Financeira
    └── Superendividamento das Pessoas Físicas
```

Isso permite incorporar outros domínios do CFP® sem multiplicar o menu principal.

### Casos — MANTER, MAS CONSOLIDAR

Faz sentido como eixo transversal do projeto porque julgamento profissional é parte explícita da missão.

Estado atual:
- contém apenas quatro casos;
- todos derivam da unidade Superendividamento;
- funciona mais como índice temático do que como biblioteca autônoma.

**Recomendação:** manter como Menu, mas evoluir para biblioteca de casos por domínio/competência.

### Ferramentas — MANTER, MAS REDEFINIR

O conceito é útil, porém o conteúdo atual é essencialmente uma **escada de intervenção**. Isso é um método/quadro de decisão, não ainda um conjunto robusto de ferramentas.

Para justificar o Menu, deve reunir elementos executáveis, por exemplo:
- checklists;
- calculadoras;
- planilhas;
- roteiros;
- árvores decisórias;
- templates;
- métricas;
- quadros de comparação.

### Métricas — RETIRAR DO PRIMEIRO NÍVEL

É o Menu menos justificado atualmente.

Razões:
1. suas fórmulas já aparecem dentro da unidade Superendividamento;
2. métrica é naturalmente uma **ferramenta de diagnóstico**, não uma grande área institucional do projeto;
3. como Menu global, aumenta a fragmentação entre conhecimento, ferramenta e aplicação;
4. tende a crescer melhor como biblioteca dentro de Ferramentas.

**Recomendação:** incorporar em:

```text
Ferramentas
├── Métricas e indicadores
├── Calculadoras
├── Checklists
├── Roteiros
└── Árvores de decisão
```

### Fontes — MANTER

Área transversal e autônoma. Justifica-se pela necessidade de vigência, rastreabilidade e atualização do CFP®, dados e referências institucionais.

### Fale Conosco — MANTER

Canal institucional funcional e E2E_VERIFICADO.

### Mapa do Site — MANTER NO RODAPÉ

A decisão de mantê-lo fora do menu global é coerente.

## 5. Sobreposição dentro da unidade Superendividamento

A unidade `temas/superendividamento-pf.html` contém internamente:

- Fontes CFP®;
- Para a prova;
- Na prática;
- Métricas;
- Intervenção;
- Casos;
- Competências;
- Avaliação;
- Fontes.

Isso não é errado: uma unidade formativa deve ser autocontida.

O problema surge quando cada dimensão interna é promovida automaticamente a Menu global. Menus de primeiro nível devem representar **áreas estáveis e transversais do Site**, não todas as seções de uma unidade.

## 6. Arquitetura recomendada

Menu global recomendado:

```text
Início
CFP®
Conhecimentos
Casos
Ferramentas
Fontes
Fale Conosco
```

Estrutura inicial:

```text
Conhecimentos
└── Gestão Financeira
    └── Superendividamento das Pessoas Físicas

Casos
└── Superendividamento
    ├── Caso 1
    ├── Caso 2
    ├── Caso 3
    └── Caso 4

Ferramentas
├── Métricas e indicadores
├── Escada de intervenção
├── Checklists
├── Calculadoras
└── Roteiros
```

## 7. Regras de interação recomendadas

1. usar `button` somente para ações;
2. usar `a` somente para navegação;
3. não trocar semântica apenas para obter aparência visual;
4. diferenciar visualmente CTA de navegação e botão de ação;
5. cards clicáveis devem deixar evidente que são navegáveis;
6. nenhum card não clicável deve usar aparência que sugira link;
7. texto do elemento deve descrever o destino/ação de forma específica;
8. links externos podem receber indicação visual de saída do Site;
9. manter foco visível e estados hover/focus;
10. auditar mobile depois de qualquer mudança de menu.

## 8. Conclusão

### Tecnicamente
A navegação está íntegra: nenhum link/âncora interno quebrado e nenhum botão morto.

### Semanticamente
A distinção HTML entre botão e hyperlink está correta.

### Arquiteturalmente
O menu global precisa de racionalização:
- **Gestão Financeira** está alto demais na hierarquia para um projeto que pretende abranger o CFP®;
- **Métricas** deve deixar o primeiro nível e integrar **Ferramentas**;
- **Casos** e **Ferramentas** justificam-se como eixos transversais, mas precisam evoluir além do recorte da primeira unidade.

Nenhuma alteração pública foi aplicada nesta auditoria. A Fase 03 aguarda decisão sobre as correções propostas.


## 9. Correções aprovadas e implementadas

O usuário aprovou as recomendações estruturais e de interação.

Implementado:
- Menu global: **Início · CFP® · Conhecimentos · Casos · Ferramentas · Fontes · Fale Conosco**;
- nova página `conhecimentos/index.html`;
- Gestão Financeira preservada como subárea de Conhecimentos;
- Métricas preservada como página, mas subordinada a Ferramentas;
- Mapa do Site refeito com hierarquia explícita;
- CTA “Estudar os casos na unidade” alterado para **“Ver casos de Superendividamento”**;
- “Voltar para Planejamento Financeiro” alterado para **“Voltar ao início”**;
- botões de ação passaram a usar `action-button`;
- links de navegação destacados passaram a usar `nav-button`;
- links secundários passaram a usar `secondary-link`;
- cards clicáveis agora têm hover e indicação “Acessar →”;
- cards informativos deixaram de receber hover que sugeria clique;
- rotas antigas foram preservadas para não quebrar URLs publicadas.

A verificação pós-implementação e o deploy público permanecem como último gate da estratégia.


## 10. Verificação final

Após as correções:

- páginas HTML públicas: **12**;
- links internos verificados: **139**;
- âncoras verificadas: **13**;
- destinos internos quebrados: **0**;
- fragmentos quebrados: **0**;
- páginas com Menu global divergente: **0**;
- rótulos antigos remanescentes: **0**;
- botões HTML reais: **2**, ambos com `action-button`;
- CTAs de navegação: **3**, todos com `nav-button`;
- links secundários destacados: **3**, todos com `secondary-link`;
- links legados com classe `button`: **0**;
- cards clicáveis: **10**, com hover e indicação “Acessar →”;
- cards informativos: **16**, sem hover que sugira clique;
- linguagem pública de estado interno (“em configuração”, “em evolução”, “estrutura escalável”): removida;
- deploy GitHub Pages `35537032790`: **success**.

A ferramenta externa de navegação disponível nesta execução não conseguiu abrir o domínio GitHub Pages; por isso, a evidência de publicação utilizada é o pipeline do GitHub Pages e o conteúdo versionado auditado.

## 11. Estado final

`CONCLUIDA`
