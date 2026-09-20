# Carteira de Estratégias — Consequências Financeiras do Divórcio Litigioso

**Projeto:** PRJ-000004 — Planejamento Financeiro  
**Interface jurídica:** PRJ-000003 / EA-000003-000005  
**Data:** 20/09/2026

## Objetivo

Dar conta, de forma modular e rastreável, das consequências financeiras possíveis de uma ação de divórcio litigioso cumulada com partilha de bens, guarda, convivência e alimentos.

## Arquitetura da carteira

1. **EA-000004-000005 — Diagnóstico financeiro da ruptura e orçamento de transição** — fundacional.
2. **EA-000004-000006 — Patrimônio, avaliação econômica e liquidez na partilha**.
3. **EA-000004-000007 — Moradia, financiamento e reorganização residencial**.
4. **EA-000004-000008 — Filhos: alimentos, educação, saúde e logística de convivência**.
5. **EA-000004-000009 — Dívidas, crédito, garantias e contas conjuntas**.
6. **EA-000004-000010 — Investimentos e reorganização de carteiras** — condicional à existência de investimentos relevantes.
7. **EA-000004-000011 — Seguros, previdência e proteção financeira** — condicional à existência/necessidade desses instrumentos.
8. **EA-000004-000012 — Tributação, declarações e custos de transferência**.
9. **EA-000004-000013 — Empresas, participações societárias e continuidade de renda** — condicional à existência de empresa, participação ou renda empresarial.
10. **EA-000004-000014 — Reconstrução financeira e plano integrado pós-divórcio** — integradora.

## Dependências

```text
PRJ-000003 / EA-000003-000005
        ↓ premissas jurídicas confirmadas
EA-000004-000005 — diagnóstico-base
        ↓
EA-000004-000006 ... EA-000004-000013
        ↓ resultados aplicáveis
EA-000004-000014 — plano integrado pós-divórcio
```

## Limite profissional

O Planejamento Financeiro:
- não decide comunicabilidade de bens;
- não fixa alimentos;
- não define guarda ou convivência;
- não substitui advogado, contador, perito, atuário ou avaliador quando a matéria exigir;
- transforma fatos, documentos e resultados jurídicos confirmados em dados, cenários e decisões financeiras.

## Regra de cenários

Enquanto uma questão jurídica estiver pendente, utilizar cenários condicionais identificados como hipóteses, nunca como direitos adquiridos ou resultados processuais previstos.
