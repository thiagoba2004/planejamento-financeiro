# Fase 02/06 — Universo de investimentos e qualidade dos dados

**Estratégia:** EA-000004-000018 — Investimentos e alocação do capital extraordinário
**Data:** 21/09/2026
**Estado:** CONCLUÍDA

## 1. Objetivo

Mapear classes de investimento que podem ser analisadas futuramente, classificando risco, liquidez, custos, tributação, garantias, complexidade e adequação ao objetivo.

Esta fase não seleciona produtos nem recomenda alocação.

## 2. Critérios obrigatórios

Todo investimento candidato deve ser descrito por emissor/devedor, classe, prazo, liquidez, carência, riscos de mercado/crédito/liquidez/inflação/câmbio, concentração, possibilidade de perda, garantias, tributação, custos, complexidade, documentação oficial, aderência ao objetivo, aderência ao perfil e data de verificação.

## 3. Renda fixa soberana

### Tesouro Selic
Pode cumprir funções de liquidez, reserva ou parcela defensiva, conforme regras operacionais. Avaliar risco soberano, marcação a mercado, tributação, custos e liquidez real.

### Tesouro Prefixado
Pode servir a objetivo com horizonte compatível. Risco relevante: sensibilidade a juros e possível perda em venda antes do vencimento.

### Tesouro IPCA+
Pode servir a objetivos reais de prazo compatível. Avaliar duration, oscilação antes do vencimento e risco de venda antecipada.

Fontes-base: PF-SRC-000068 e PF-SRC-000075.

## 4. Títulos bancários

Incluem CDB/RDB e outros instrumentos bancários, observadas as características específicas.

Avaliar emissor, prazo, carência, liquidez, indexador, taxa, FGC quando aplicável, concentração por instituição/conglomerado e tributação.

FGC não é sinônimo de risco zero e não cobre todo produto financeiro.

Fontes: PF-SRC-000046, PF-SRC-000066 e PF-SRC-000067.

## 5. Crédito privado não bancário

Exemplos: debêntures, CRI, CRA e outros títulos privados permitidos ao investidor.

Avaliar risco de crédito, garantias, covenants, duration, liquidez secundária, concentração por emissor/setor, documentação da oferta, tributação e inexistência de presunção de FGC.

Fonte: PF-SRC-000078.

## 6. Fundos de investimento

Classes possíveis: renda fixa, multimercado, ações e cambial.

Avaliar política de investimento, benchmark, risco da carteira, taxas, cotização, liquidação, tributação, regime de responsabilidade, volatilidade e estratégia.

Fundo não é automaticamente diversificado nem líquido apenas por ser fundo.

Fonte: PF-SRC-000070.

## 7. ETFs

Podem oferecer exposição diversificada a índices de ações, renda fixa e outros segmentos permitidos.

Avaliar índice subjacente, metodologia, taxa, spread, liquidez, aderência ao índice, moeda e risco da classe subjacente.

Fonte: PF-SRC-000077.

## 8. Ações

São participação no capital de empresas e possuem retorno incerto, volatilidade, risco específico da companhia e risco setorial.

Ações individuais elevam risco de concentração quando comparadas a exposições amplas diversificadas.

Fonte: PF-SRC-000076.

## 9. Fundos imobiliários

Podem gerar exposição a imóveis, direitos e títulos imobiliários conforme a política do fundo. Avaliar risco de mercado, risco imobiliário, vacância/crédito, liquidez e custos.

Não tratar rendimento distribuído como renda garantida.

Fonte: PF-SRC-000079.

## 10. Exposição internacional

Pode ser obtida por veículos disponíveis ao investidor brasileiro, como fundos ou ETFs com ativos externos, conforme produto.

Avaliar risco cambial, jurisdição, índice/estratégia, custos, tributação, liquidez e concentração geográfica.

Não incluir apenas sob o rótulo genérico de diversificação: a exposição deve ter função no portfólio.

## 11. Previdência e proteção

PGBL, VGBL e previdência complementar não entram automaticamente na carteira desta fase.

A análise completa de tributação, sucessão, custos, portabilidade, horizonte, seguros e proteção pertence à EA-000004-000019.

## 12. Ativos de alta complexidade

Derivativos, criptoativos, produtos estruturados, alavancagem e instrumentos de maior complexidade não são componentes padrão.

Só podem ser analisados após objetivo específico, conhecimento comprovado, capacidade de perda, entendimento do risco, suitability e função clara no portfólio.

## 13. Matriz de qualidade do dado

Classificações permitidas:
- FONTE_OFICIAL_ATUAL;
- DOCUMENTO_DO_PRODUTO;
- DADO_DA_INSTITUICAO;
- DADO_DO_CLIENTE_COMPROVADO;
- DADO_DO_CLIENTE_DECLARADO;
- ESTIMATIVA;
- DADO_AUSENTE.

Nenhuma taxa anunciada deve entrar no plano sem data, prazo, emissor, indexador, condição de resgate e fonte.

## 14. Matriz resumida do universo

| Classe | Liquidez | Risco dominante | Garantia | Uso depende de |
|---|---|---|---|---|
| Tesouro Selic | alta conforme operação | juros/soberano | Tesouro Nacional | liquidez/horizonte |
| Prefixado/IPCA+ | depende da venda | juros/duration | Tesouro Nacional | data do objetivo |
| CDB e bancários | contratual | crédito/liquidez | FGC quando elegível | emissor/prazo |
| crédito privado | variável | crédito/mercado | não presumir | análise de emissor |
| fundos | regulamento | carteira/gestão | sem FGC | política/custos |
| ETFs | mercado | índice/mercado | sem FGC | objetivo/índice |
| ações | mercado | empresa/mercado | sem FGC | horizonte/risco |
| FII | mercado | imobiliário/liquidez | sem FGC | horizonte/risco |

A tabela é classificatória, não ranking.

## 15. Gate da Fase 02

**SATISFEITO.**

Foram mapeados critérios comuns, classes, riscos, limitações, fronteira com previdência/proteção, regra para ativos complexos e classificação da qualidade dos dados.

## 16. Próxima fase

**Fase 03/06 — Política de alocação e cenários.**
