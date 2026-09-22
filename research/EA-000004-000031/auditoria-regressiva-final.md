# EA-000004-000031 — Auditoria regressiva final

**Data de corte:** 21/09/2026  
**Objeto:** integração das superveniências jurídicas do Projeto Ações Judiciais no Planejamento Financeiro.

## 1. Superfície publicada auditada

O artefato exato do GitHub Pages foi obtido do workflow de deploy e auditado localmente.

- workflow run: `35676806642`;
- commit público: `efffbd4f604a28eafd81ebad321095d428129408`;
- conclusão do workflow: `success`;
- artifact id: `10673705963`;
- artifact digest: `sha256:8a12811d7695d7e11096f092d5b6697d6e5f8fafc5ed57e5964bdb8b73867955`;
- páginas HTML no artefato: **33**.

## 2. Integridade global

- referências `href` auditadas: **808**;
- verificações de âncoras internas/cruzadas: **267**;
- links internos quebrados: **0**;
- âncoras quebradas: **0**;
- vazamentos de governança interna: **0**;
- páginas com estrutura `<main>` anômala: **0**.

## 3. Paridade semântica das alterações

Foram reconfirmadas no Markdown canônico e no HTML publicado as seguintes integrações:

### Unidade econômica e separação de fato
- Separação de fato e base das métricas;
- Separação de fato sem divórcio formal;
- Patrimônio pendente de definição;
- Renda do outro responsável e transferências;
- Unidade econômica antes do divórcio formal.

### Gate jurídico-financeiro
- Gate jurídico-financeiro antes da execução;
- Gate jurídico antes de executar;
- Gate jurídico-financeiro do plano.

### Contingência em ruptura familiar protegida
- Contingência financeira em ruptura protegida;
- Mudança urgente e sobreposição de moradia;
- Alimentos provisórios/provisionais: quatro estados;
- Contingência financeira em contexto de medida protetiva.

### Integração transversal
- Casos integrados — superveniências jurídicas e planejamento financeiro;
- Gate jurídico-financeiro na biblioteca de Ferramentas.

Todas as verificações retornaram **OK** no Markdown e no artefato HTML correspondente.

## 4. Fontes jurídicas de controle

Foram registrados no `SOURCE_REGISTRY.jsonl`:
- `PF-SRC-000088` — Lei nº 15.411/2026;
- `PF-SRC-000089` — Lei nº 15.412/2026;
- `PF-SRC-000090` — Lei nº 14.713/2023.

As normas funcionam no Projeto Planejamento Financeiro apenas como premissas jurídicas externas e gatilhos de atualização do plano. O planejador não diagnostica violência, não decide medidas protetivas e não substitui análise jurídica.

## 5. Resultado das estratégias derivadas

- **EA-000004-000032:** concluída — separação de fato e unidade econômica;
- **EA-000004-000033:** concluída — gate jurídico-financeiro no superendividamento e capital indenizatório;
- **EA-000004-000034:** concluída — contingência financeira em ruptura familiar com medidas protetivas.

## 6. Testes conceituais finais

Passaram sem regressão material detectada:
1. estado civil não é usado como sinônimo automático de unidade econômica;
2. renda do outro cônjuge não é automaticamente incorporada à renda do cliente;
3. transferências, pagamentos diretos e rateios são classificados separadamente;
4. patrimônio ainda sujeito a definição jurídica permanece contingente/cenário;
5. bens financiados separam valor bruto, saldo devedor, valor líquido e participação atribuível;
6. dívida juridicamente fora da repactuação continua no fluxo financeiro;
7. quitação/amortização seletiva distingue simulação de execução;
8. reserva financeira prudente não é apresentada como blindagem jurídica;
9. alimentos confirmados são distinguidos de pedidos, pagamentos voluntários e cenários;
10. contingência financeira não autoriza ocultação/dissipação patrimonial;
11. conteúdos jurídicos permanecem classificados como condições externas, sem falsa atribuição ao programa CFP®.

## 7. Conclusão

A auditoria regressiva não detectou regressão material residual. A integração AJ → PF está tecnicamente apta ao fechamento.
