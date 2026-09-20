# Fase 03/06 — Matriz evento–tributo–declaração–documento

**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

| Evento | Possível efeito | Fonte/competência | Documento mínimo | Estado inicial |
|---|---|---|---|---|
| Bem atribuído pelo mesmo valor constante na DIRPF | sem ganho positivo nessa diferença, mas atualização patrimonial/declaratória pode ser necessária | Receita Federal | decisão/escritura + última DIRPF + documento do bem | A VALIDAR |
| Bem atribuído por valor superior ao declarado | possível IR sobre ganho de capital | Receita Federal | decisão transitada/escritura + custo fiscal + valor atribuído | POTENCIAL_INCIDENCIA |
| Venda posterior do bem | possível ganho de capital | Receita Federal | aquisição + venda + despesas/custos admissíveis | POTENCIAL_INCIDENCIA |
| Excesso gratuito de meação | possível ITD/ITCMD | Estado competente | partilha + valores + prova de ausência de compensação | JURISDICAO_PENDENTE |
| Excesso oneroso envolvendo imóvel | possível ITIV/ITBI | Município do imóvel | partilha + torna/compensação + matrícula + valores | JURISDICAO_PENDENTE |
| Transferência/registro de imóvel | emolumentos/taxas | cartório/TJ competente | título + matrícula + valor do ato | A CALCULAR |
| Transferência de investimento | custo/tributação depende da operação | federal/instituição | extrato + custo + natureza da operação | NAO_ANALISADO |
| Resgate de investimento/previdência | tributação depende do produto/regime | federal/instituição | informe + regulamento + histórico | NAO_ANALISADO |
| Rendimentos de bem durante transição | tributação/declaratório | Receita Federal | informes/extratos + titularidade jurídica | A VALIDAR |
| Alteração de dependente | efeito na DIRPF | Receita Federal | guarda/condição + CPF + rendimentos do dependente | OBRIGACAO_DECLARATORIA |
| Pensão alimentícia | efeito tributário/declaratório conforme regra do exercício | Receita Federal | decisão/acordo/escritura + comprovantes | A VALIDAR |

## 1. Transferência em partilha e ganho de capital federal

Regra de diagnóstico:

```text
ganho potencial
= valor de transferência adotado
− custo/valor fiscal aplicável
```

Se não houver diferença positiva, não há ganho positivo nessa operação específica.

Se houver diferença:
- verificar GCAP;
- verificar alíquota vigente;
- verificar isenções/reduções;
- identificar contribuinte e prazo;
- transportar corretamente o evento para a DIRPF correspondente.

## 2. Exemplo federal simplificado

Premissas fictícias:
- imóvel declarado: R$ 300.000;
- valor atribuído na partilha: R$ 500.000;
- diferença: R$ 200.000.

Antes de qualquer isenção/redução específica:

```text
ganho potencial = 500.000 − 300.000 = R$ 200.000
```

Na faixa geral de ganho até R$ 5 milhões, a alíquota federal vigente é 15%:

```text
IR ilustrativo = 200.000 × 15% = R$ 30.000
```

Esse exemplo:
- não decide qual valor jurídico deve ser usado;
- não considera redução/isenção específica;
- não considera tributo estadual/municipal;
- não substitui GCAP/contador.

## 3. Custo líquido do evento

```text
custo líquido de transação
= tributos confirmados
+ emolumentos/taxas
+ custos profissionais diretamente atribuíveis
+ custos operacionais
```

Não incluir imposto apenas “por prudência” sem hipótese identificada; usar cenário separado.

## Gate

Satisfeito. Matriz, documentos, estados, cálculo federal ilustrativo e fórmula de custo líquido foram documentados.
