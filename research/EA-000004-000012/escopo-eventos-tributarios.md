# Fase 01/06 — Escopo tributário e eventos relevantes

**Estratégia:** EA-000004-000012 — Tributação, declarações e custos de transferência  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## Regra central

Tributo não é atributo automático do bem. Ele nasce de um **evento juridicamente caracterizado**, em uma **data**, sob determinada **jurisdição**.

A ordem de trabalho é:

1. identificar o evento;
2. importar a natureza jurídica confirmada;
3. identificar competência tributária;
4. localizar fonte vigente;
5. definir contribuinte/responsável;
6. identificar base de cálculo;
7. verificar alíquota, isenção ou redução;
8. identificar prazo e obrigação declaratória;
9. calcular custo líquido;
10. documentar incerteza.

## Eventos que entram na triagem

- atribuição de bem em partilha;
- atribuição por valor fiscal diferente do valor histórico;
- excesso de meação/quinhão;
- compensação financeira;
- venda posterior;
- permuta;
- transferência de imóvel;
- transferência de investimento;
- resgate/liquidação;
- rendimentos produzidos durante a transição;
- alteração de dependência;
- pensão alimentícia formalmente fixada/paga;
- mudança de titularidade cadastral;
- registro/averbação/escritura;
- emolumentos e taxas.

## Estados tributários

- `NAO_ANALISADO`;
- `POTENCIAL_INCIDENCIA`;
- `INCIDENCIA_CONFIRMADA`;
- `NAO_INCIDENCIA_CONFIRMADA`;
- `ISENCAO_A_VALIDAR`;
- `OBRIGACAO_DECLARATORIA`;
- `JURISDICAO_PENDENTE`;
- `CONTADOR_TRIBUTARISTA_REQUERIDO`.

## Trava temporal

Regras anuais da DIRPF devem ser vinculadas ao exercício.

Em 20/09/2026:
- a referência oficial disponível é o IRPF exercício 2026, ano-calendário 2025;
- fatos ocorridos em 2026 devem ser revalidados nas regras do exercício 2027 quando publicadas;
- não copiar automaticamente limites, deduções ou campos da declaração de 2026 para 2027.

## Perguntas de diagnóstico

1. Qual evento econômico ocorrerá?
2. Em que data?
3. Qual é a natureza jurídica confirmada?
4. Há onerosidade, gratuidade ou mera divisão do patrimônio comum?
5. Qual bem/direito está envolvido?
6. Onde o imóvel está situado?
7. Qual era o custo/valor declarado?
8. Qual valor será atribuído na transferência?
9. Existe ganho acumulado?
10. Há excesso de meação/quinhão?
11. Existe torna/compensação?
12. Quem recebe e quem paga?
13. Existe venda posterior prevista?
14. Que declaração anual refletirá o evento?
15. Há dependentes ou pensão formal que alterem a declaração?
16. Existe cartório/registro/averbação necessário?
17. Qual fonte oficial vigente se aplica?
18. Há benefício fiscal, isenção ou redução a validar?
19. O caso exige contador ou advogado tributarista?
20. Qual custo líquido muda a decisão financeira?

## Gate

Satisfeito. Escopo, eventos, estados tributários, ordem de análise, trava temporal e perguntas foram persistidos.
