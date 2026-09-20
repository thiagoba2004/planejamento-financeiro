# Fase 01/06 — Escopo patrimonial e interface jurídica

**Estratégia:** EA-000004-000006 — Patrimônio, avaliação econômica e liquidez na partilha  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Objetivo

Construir a camada econômica do patrimônio afetado pela ruptura conjugal sem substituir a análise jurídica da partilha.

O Planejamento Financeiro responde:
- quanto vale economicamente cada ativo/passivo em uma data-base;
- qual o valor líquido após passivos diretamente vinculados;
- quão líquido é o item;
- quais custos de conversão podem reduzir o valor disponível;
- qual a concentração patrimonial por classe;
- quais cenários econômicos decorrem de classificações jurídicas diferentes;
- quais ativos sustentam ou não necessidades de caixa, moradia e objetivos.

O Planejamento Financeiro **não responde**:
- se o bem é comunicável;
- qual é a meação;
- quem é juridicamente responsável por determinada dívida;
- se uma pretensão de partilha será acolhida;
- qual marco temporal deve prevalecer juridicamente;
- se determinada transferência patrimonial é juridicamente exigível.

## 2. Classes patrimoniais cobertas

1. caixa e contas;
2. investimentos financeiros;
3. imóveis;
4. veículos e outros bens móveis relevantes;
5. bens financiados;
6. FGTS e direitos semelhantes;
7. previdência aberta e fechada, sempre preservando a classificação jurídica recebida;
8. quotas, ações e participações empresariais;
9. ativos digitais e criptoativos;
10. créditos e recebíveis;
11. frutos, aluguéis e rendimentos patrimoniais;
12. benfeitorias economicamente identificáveis;
13. passivos e garantias;
14. outros direitos com valor econômico verificável.

## 3. Dupla classificação obrigatória

Cada item deve carregar dois eixos separados.

### Eixo jurídico — recebido do PRJ-000003

- `CONFIRMADO_COMUNICAVEL`;
- `CONFIRMADO_PARTICULAR`;
- `CONTROVERTIDO`;
- `NAO_ANALISADO`.

Quando necessário, conservar ainda:
- percentual juridicamente confirmado;
- regime de bens;
- data jurídica relevante;
- fundamento/documento de origem.

### Eixo financeiro — produzido pelo PRJ-000004

- `LIQUIDO_IMEDIATO`;
- `LIQUIDO_CURTO_PRAZO`;
- `ILIQUIDO_NEGOCIAVEL`;
- `INDIVISIVEL_OU_COMPLEXO`;
- `CONDICIONADO_A_EVENTO`;
- `VALOR_NAO_MENSURADO`.

Um item pode ser juridicamente comunicável e financeiramente ilíquido. Também pode ser juridicamente particular e ainda ser relevante para a capacidade financeira individual de uma das partes.

## 4. Tratamento econômico por status jurídico

| Status jurídico | Tratamento financeiro permitido |
|---|---|
| CONFIRMADO_COMUNICAVEL | pode integrar cenários comuns conforme percentual juridicamente confirmado |
| CONFIRMADO_PARTICULAR | integra patrimônio individual, não o bolo comum |
| CONTROVERTIDO | somente em cenários explícitos alternativos |
| NAO_ANALISADO | inventariar, mas não atribuir a qualquer parte nem tratar como disponível para partilha |

## 5. Valor patrimonial

Para cada ativo:

```text
VALOR_LIQUIDO_ESTIMADO =
VALOR_BRUTO
− PASSIVO_DIRETAMENTE_VINCULADO
− CUSTOS_DE_CONVERSAO_ESTIMADOS
− TRIBUTOS/CUSTOS APENAS QUANDO TECNICAMENTE FUNDAMENTADOS
```

A fórmula é econômica. Ela não define valor jurídico de meação.

## 6. Dimensões de análise

Cada item será analisado em pelo menos seis dimensões:

1. **existência** — o ativo/passivo está comprovado?
2. **valor** — há valor mensurável e data-base?
3. **passivo vinculado** — existe dívida diretamente associada?
4. **liquidez** — quanto tempo e custo para converter em caixa?
5. **indivisibilidade/complexidade** — pode ser fracionado sem perda relevante?
6. **dependência jurídica** — o uso do valor depende de definição ainda controvertida?

## 7. Perguntas de escopo

### Identificação
1. Quais ativos e passivos existem?
2. Qual o titular formal de cada item?
3. Qual a documentação comprobatória?
4. Qual a data-base apropriada para a análise econômica?

### Valor
5. Há cotação observável?
6. Há necessidade de avaliação técnica?
7. O valor registrado contabilmente difere do valor econômico?
8. Existe passivo vinculado?
9. Há custo de venda, resgate, transferência ou encerramento?

### Liquidez
10. O ativo pode ser convertido em caixa imediatamente?
11. Existe carência, bloqueio ou prazo operacional?
12. A venda exige mercado específico?
13. O ativo é indivisível?
14. A liquidação destrói valor econômico relevante?

### Dependência jurídica
15. O item é confirmado comunicável, particular, controvertido ou não analisado?
16. Há percentual juridicamente confirmado?
17. O uso do ativo depende de decisão judicial, anuência de terceiro ou credor?
18. O passivo está juridicamente atribuído ou ainda controvertido?

### Concentração
19. Quanto do patrimônio está concentrado em imóveis?
20. Quanto está em ativos financeiros?
21. Quanto está em empresa/participação societária?
22. Quanto está condicionado a controvérsia?
23. Quanto está efetivamente líquido?

### Transição
24. Que ativos podem financiar despesas de transição?
25. Que ativos não devem ser usados para isso?
26. A venda de um ativo compromete moradia, trabalho ou renda?
27. A liquidação antecipada gera perda ou penalidade?

### Cenários
28. Como muda o patrimônio líquido de A e B se determinado item for comunicável?
29. Como muda se for particular?
30. Como muda se o percentual for diferente?
31. O equilíbrio nominal da partilha produz desequilíbrio de liquidez?
32. Uma parte ficaria com ativos ilíquidos e a outra com caixa?
33. Há concentração excessiva em um único ativo após o cenário?
34. Há necessidade de compensação financeira para equilibrar liquidez?
35. A compensação exigiria dívida nova?
36. Qual cenário preserva melhor liquidez sem assumir conclusão jurídica?

## 8. Interface com outras estratégias

Esta estratégia fornecerá:
- valor econômico líquido → moradia, investimentos e reconstrução;
- grau de liquidez → orçamento de transição;
- passivos vinculados → dívidas/crédito;
- eventos de venda/transferência → tributação;
- participações empresariais → estratégia empresarial.

## 9. Gate

Gate satisfeito:
- classes patrimoniais cobertas;
- fronteira jurídica/financeira definida;
- dupla classificação obrigatória estabelecida;
- fórmula econômica de valor líquido definida;
- seis dimensões de análise registradas;
- 36 perguntas de escopo persistidas;
- interfaces com estratégias subsequentes mapeadas.
