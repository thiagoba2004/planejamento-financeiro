# DECISIONS — PRJ-000004 — Planejamento Financeiro

## DEC-000001 — 20/09/2026 — Dupla finalidade
O projeto deve preparar para a prova CFP® e para a prática profissional, sem tratar uma finalidade como substituta da outra.

## DEC-000002 — 20/09/2026 — Fontes da Planejar como canônicas
Todo material oficial pertinente disponibilizado pela Planejar integra o corpus canônico por referência e metadados. Reprodução integral pública depende de permissão/licença compatível.

## DEC-000003 — 20/09/2026 — Unidade formativa por competência
Cada unidade deve registrar SABER, FAZER, DECIDIR, FONTE e AVALIAÇÃO.

## DEC-000004 — 20/09/2026 — Separação prova/prática
Todo tema deve identificar explicitamente TRILHA_PROVA e TRILHA_PRATICA quando ambas existirem.

## DEC-000005 — 20/09/2026 — Autonomia diante do projeto jurídico
Questões jurídicas do superendividamento podem ser referenciadas no PRJ-000003, sem transferir ao Planejamento Financeiro a função de fonte jurídica primária.

## DEC-000006 — 20/09/2026 — Graus de verificação de fontes externas canônicas

Quando uma fonte externa oficial é canônica, mas sua interface impede a extração direta do arquivo, o projeto distingue:
- **GRAU A:** conteúdo verificado diretamente na fonte canônica;
- **GRAU B:** fonte oficial identificada/vigente e conteúdo triangulado por reprodução independente coerente;
- **GRAU C:** fonte apenas identificada, sem verificação material suficiente.

Fontes não oficiais usadas no Grau B são **corroboração**, nunca substituem a fonte canônica e devem ser registradas como `CORROBORACAO_NAO_CANONICA`.

Uma limitação técnica de acesso não autoriza inventar conteúdo nem atribuir ao documento oficial uma citação que só foi observada no espelho.



## DEC-20260920-CONTACT-STACK — Stack canônica do Fale Conosco

**Decisão:** a expressão “seguir o mesmo padrão do Fale Conosco do Classe e Massas” inclui a stack técnica **Forminit + EmailJS**.

A implementação FormSubmit criada anteriormente é classificada como divergência técnica. Ela não deve ser tratada como solução final nem receber estado E2E_VERIFICADO.

**Migração obrigatória:** configurar Forminit isolado para `planejamentofinanceiro2012@gmail.com`, configurar EmailJS para confirmação ao remetente e testar o fluxo completo antes do fechamento.
