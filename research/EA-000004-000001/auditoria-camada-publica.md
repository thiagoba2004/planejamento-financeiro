# Auditoria de separação entre Site Público e governança interna

**Data:** 20/09/2026  
**Resultado:** saneamento executado na camada pública.

## Itens removidos do Site Público

- códigos de projeto e estratégia;
- estados editoriais e técnicos;
- graus internos A/B/P;
- códigos de competências;
- códigos de casos;
- códigos de métricas;
- códigos internos de avaliação;
- referências a workflow, deploy e governança.

## Conversões para linguagem pública

- TRILHA_PROVA → “Para a prova CFP®”;
- TRILHA_PRATICA → “Na prática profissional”;
- PF-CASO-* → “Caso 1”, “Caso 2” etc.;
- PF-COMP-* → nome da competência;
- C01–C04 → nome descritivo da métrica;
- A1–A4 → nome natural da forma de avaliação.

## Itens preservados publicamente

- conteúdo financeiro;
- fórmulas;
- exemplos e casos;
- competências em linguagem natural;
- data de atualização;
- fontes oficiais;
- limites profissionais.

## Regra preventiva

O AGENTS.md agora proíbe exposição de governança interna na UI pública e exige varredura antes de cada publicação.

## Verificação final de implantação

- Workflow: `35522801080`.
- Resultado: `completed/success`.
- Build, Setup Pages, Upload e Deploy: `success`.
- Arquivos públicos auditados: `index.html`, `temas/superendividamento-pf.html`.
- Resultado da varredura de marcadores internos: **zero ocorrências**.
