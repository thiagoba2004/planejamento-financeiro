# Protocolo Canônico de Métricas e Fórmulas

**Projeto:** PRJ-000004 — Planejamento Financeiro  
**Última revisão:** 21/09/2026.

## Regra geral

Nenhuma métrica é interpretada sem ficha mínima:
1. finalidade;
2. origem: fonte externa ou metodologia do Site;
3. fórmula;
4. unidade;
5. data-base;
6. horizonte/período;
7. definição do numerador e denominador;
8. tratamento de zero, valor negativo e dado ausente;
9. premissas;
10. interpretação;
11. limitações;
12. teste de dupla contagem;
13. necessidade de equivalência temporal.

## Métricas centrais

### Patrimônio líquido
**Fórmula:** ativos totais − passivos totais.  
**Unidade:** moeda na mesma data-base.  
**Limite:** o recebimento de caixa não aumenta novamente o PL se o direito correspondente já estava reconhecido como ativo.

### Cobertura de despesas
**Fórmula:** ativos líquidos elegíveis ÷ despesas essenciais mensais.  
**Unidade:** meses.  
**Limites:** numerador deve excluir ativos indisponíveis e não duplicar caixa reservado para outra obrigação.

### Serviço da dívida / renda
**Fórmula:** serviço planejado da dívida ÷ renda líquida recorrente.  
**Unidade:** %.  
**Limite:** pagamento mínimo contratual de cartão/rotativo não é automaticamente serviço sustentável.

### Fluxo livre
**Fórmula:** renda líquida recorrente − despesas essenciais − serviço planejado da dívida − demais obrigações recorrentes confirmadas.  
**Unidade:** moeda/tempo.

### Solvência
**Fórmula:** ativos totais ÷ passivos totais.  
**Unidade:** razão.  
**Limite:** se passivos = 0, registrar “sem passivos / razão não aplicável”; não dividir por zero.

### Runway estática
**Fórmula:** liquidez elegível ÷ déficit mensal absoluto.  
**Unidade:** meses.  
**Rótulo obrigatório:** estimativa estática de primeira ordem, não previsão.  
**Premissas:** déficit constante, sem inflação, rendimento, choque ou mudança de renda/dívida.

### Gap de objetivo
Objetivo, recursos atuais e aportes futuros devem estar na **mesma data-base**. Usar valor presente ou valor futuro, declarando inflação, retorno líquido, custos/tributação materiais e momento dos aportes.

### Gap de proteção
Não somar capital à vista e fluxos futuros sem equivalência temporal. Usar ativos efetivamente disponíveis para o risco e trazer necessidades, coberturas e benefícios à mesma base ou modelar por período.

## Casos quantitativos

Todo caso publicado deve permitir reprodução por terceiro com:
**inputs → data-base → fórmula → intervenção → resultado → interpretação → limitações**.
