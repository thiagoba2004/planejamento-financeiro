# Fase 02/06 — Documentação de origem e trilha patrimonial

**Estratégia:** EA-000004-000015 — Recebimento da indenização: documentação, tratamento declaratório e incorporação do capital líquido  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Objetivo

Preservar uma trilha documental capaz de demonstrar:
- de onde vieram os R$ 100.000,00;
- por que o recebimento ocorreu;
- qual é a natureza jurídica declarada da verba;
- quando o valor entrou no patrimônio;
- em qual conta entrou;
- como será identificado em futuras declarações e revisões patrimoniais.

A documentação não serve para reabrir a apuração do valor líquido já confirmado.

## 2. Documento jurídico principal

Prioridade máxima:

- sentença;
- acordo judicial;
- acordo extrajudicial homologado;
- termo de conciliação;
- alvará;
- decisão que identifique a verba.

O documento deve permitir localizar, quando aplicável:
- processo;
- partes;
- natureza da verba;
- valor;
- data;
- homologação;
- forma de pagamento.

## 3. Comprovante financeiro

Preservar:
- comprovante do crédito;
- extrato bancário;
- comprovante de transferência;
- identificação do pagador;
- data do crédito;
- valor efetivamente recebido.

Se o pagamento ocorreu em parcelas:
- preservar cada crédito;
- relacionar cada parcela ao documento jurídico;
- consolidar a soma líquida em trilha própria.

## 4. Documentos fiscais

Quando existirem:
- informe de rendimentos;
- comprovante de retenções;
- demonstrativo do processo;
- DARF ou outro comprovante relacionado;
- documento do empregador ou instituição financeira pagadora.

A ausência de um documento fiscal específico não deve ser preenchida por estimativa.

## 5. Honorários e despesas processuais

Mesmo com os R$ 100.000,00 já definidos como capital líquido:
- preservar contrato de honorários;
- recibos;
- comprovantes de pagamento;
- eventuais despesas processuais.

Esses documentos servem para:
- rastreabilidade;
- comprovação histórica;
- eventual necessidade fiscal;
- conciliação entre valor econômico da causa e valor efetivamente incorporado ao patrimônio.

Não subtrair novamente esses valores do capital líquido confirmado.

## 6. Trilha patrimonial mínima

Registrar:

| Campo | Conteúdo esperado |
|---|---|
| origem | indenização trabalhista por dano moral |
| documento jurídico | sentença/acordo/termo aplicável |
| processo | número, se houver |
| data do recebimento | DADO_AUSENTE até informado |
| pagador | empregador |
| conta de entrada | DADO_AUSENTE até informado |
| valor líquido | R$ 100.000,00 |
| comprovante bancário | a preservar |
| documento fiscal | a verificar |
| ano-calendário | depende da data do recebimento |
| destino posterior | ainda não definido |

## 7. Classificação de qualidade documental

### CONFIRMADO
Documento disponível e coerente com o evento.

### DADO_AUSENTE
Documento ou dado ainda não fornecido.

### DIVERGENTE
Documentos apresentam valores, datas ou naturezas incompatíveis.

### A_ESCLARECER
Documento existe, mas sua função ou relação com o evento ainda não está clara.

## 8. Checklist documental

- [ ] sentença/acordo/termo;
- [ ] número do processo, se houver;
- [ ] comprovante do pagamento;
- [ ] extrato bancário;
- [ ] identificação do pagador;
- [ ] data do crédito;
- [ ] informe de rendimentos, se houver;
- [ ] comprovantes de retenção, se houver;
- [ ] contrato/recibo de honorários;
- [ ] documentos de despesas relevantes;
- [ ] cópia da declaração fiscal do ano correspondente após entregue;
- [ ] pasta digital consolidada.

## 9. Organização sugerida

```text
indenizacao-trabalhista/
├── 01-origem-juridica/
├── 02-comprovantes-pagamento/
├── 03-extratos/
├── 04-documentos-fiscais/
├── 05-honorarios-despesas/
└── 06-declaracoes/
```

A organização é uma recomendação operacional; não é exigência jurídica.

## 10. Regra de consistência

A documentação deve permitir responder, no futuro:

> “Por que houve um aumento patrimonial de R$ 100.000,00?”

A resposta deve ser reconstruível sem depender da memória do titular.

## 11. Gate da Fase 02

**SATISFEITO.**

Foram persistidos:
- hierarquia documental;
- trilha patrimonial;
- checklist;
- classificação de qualidade;
- regra de consistência;
- separação entre capital líquido confirmado e documentação histórica.

## 12. Próxima fase

**Fase 03/06 — Tratamento declaratório e registro fiscal.**
