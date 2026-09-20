# Fase 03/06 — Métodos de avaliação econômica

**Estratégia:** EA-000004-000006 — Patrimônio, avaliação econômica e liquidez na partilha  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## 1. Princípio

Não existe um único “valor do patrimônio”.

Para cada item devem ser distinguidos, quando relevantes:
- valor documental/contábil;
- valor de mercado;
- valor de resgate;
- valor de liquidação;
- valor líquido após passivos e custos;
- valor econômico em cenário.

O método escolhido deve corresponder ao uso da informação.

## 2. Data-base

Todo valuation deve registrar uma data-base.

Regras:
- ativos comparados entre si devem preferencialmente usar a mesma data-base;
- quando não for possível, registrar a defasagem;
- ativos voláteis exigem referência temporal mais precisa;
- saldo devedor e valor do ativo devem ser reconciliados para períodos compatíveis;
- não misturar valor histórico de aquisição com valor econômico atual sem identificação.

## 3. Matriz de métodos por classe

### Caixa e depósitos
**Método:** saldo comprovado na data-base.  
**Ajustes:** indisponibilidade, bloqueio ou titularidade não devem ser ignorados.  
**Erro a evitar:** tratar limite de conta/cartão como ativo.

### Investimentos com cotação ou valor de posição
**Método:** posição/valor de mercado ou de resgate fornecido pela instituição na data-base.  
**Ajustes:** custos, carência, tributação e liquidez apenas quando documentados.  
**Erro a evitar:** usar valor aplicado histórico como valor atual.

### Renda fixa sem cotação simples
**Método:** valor de resgate/posição informado pela instituição ou valuation tecnicamente verificável.  
**Erro a evitar:** projetar taxa futura como se já fosse valor disponível.

### Imóveis
**Métodos possíveis:**
- avaliação técnica;
- comparação com transações/ofertas comparáveis devidamente ajustadas;
- múltiplas referências independentes quando não houver laudo.

**Registrar:** localização, área, padrão, estado, ocupação, gravames, data-base e fonte.

**Erro a evitar:** usar preço pedido de um único anúncio como “valor de mercado”.

### Imóvel financiado
Separar:
- valor bruto de mercado;
- saldo para liquidação/financiamento;
- custos de conversão fundamentados;
- valor líquido estimado.

```text
VALOR_LIQUIDO =
VALOR_BRUTO
− SALDO_PASSIVO_VINCULADO
− CUSTOS_DE_CONVERSAO_FUNDAMENTADOS
```

### Veículos
**Método:** referência pública de mercado + ajuste documentado por estado, versão, quilometragem, sinistro, gravame ou condição comercial.

**Erro a evitar:** usar referência genérica sem identificar modelo/versão/data.

### FGTS e direitos vinculados
**Método econômico:** saldo comprovado por período/competência.  
**Tratamento de liquidez:** separado do valor patrimonial; não presumir disponibilidade para saque.  
**Classificação jurídica:** importada do PRJ-000003.

### Previdência
**Método econômico:** saldo de resgate, reserva ou benefício informado pelo plano conforme a natureza do produto.  
**Erro a evitar:** equiparar todo plano a investimento líquido disponível.

### Participações societárias
O Planejamento Financeiro deve distinguir:
- valor contábil;
- patrimônio líquido ajustado;
- valor econômico estimado;
- fluxo/renda distribuída;
- valor de haveres quando houver determinação jurídica/pericial própria.

Métodos financeiros possíveis dependem de dados e finalidade, podendo incluir:
- patrimônio líquido ajustado;
- múltiplos comparáveis;
- fluxo de caixa descontado, quando tecnicamente cabível;
- avaliação independente.

**Limite:** método judicial de apuração de haveres não é escolhido pelo PRJ-000004. Se houver método juridicamente determinado, ele prevalece para o cenário correspondente.

### Ativos digitais
**Método:** quantidade comprovada × cotação na data/hora-base, com identificação da fonte.  
**Ajustes:** custos de conversão e custódia quando documentados.  
**Erro a evitar:** estimar quantidade a partir de valor declarado antigo.

### Recebíveis
**Método:** valor nominal quando recebimento é imediato e certo; caso contrário, cenário de valor presente ou haircut somente com premissas documentadas.

**Erro a evitar:** tratar crédito litigioso ou incerto pelo valor nominal como caixa.

### Bens móveis relevantes
**Método:** referência de mercado, cotação de revenda, avaliação especializada ou valor residual justificável.

**Erro a evitar:** confundir custo de reposição com valor de venda.

### Dívidas
**Método:** saldo para liquidação ou saldo contratual reconciliado na data-base.  
Registrar:
- principal;
- encargos;
- vencimento;
- garantia;
- custo de liquidação, quando houver.

## 4. Custos de conversão

Nunca inserir percentual genérico de venda.

Custos possíveis:
- corretagem;
- comissão;
- emolumentos;
- tributos;
- multa;
- deságio;
- despesas de regularização;
- custo de encerramento;
- custo operacional.

Só entram no valor líquido quando:
1. são aplicáveis ao cenário;
2. possuem base técnica/documental;
3. não estão sendo contados em outra etapa.

## 5. Moeda estrangeira

Registrar:
- moeda original;
- valor original;
- taxa de conversão;
- fonte da taxa;
- data da taxa;
- valor convertido.

Não misturar câmbios de datas diferentes sem explicitação.

## 6. Intervalo de valor

Quando não houver precisão razoável, preferir:
- valor mínimo plausível;
- valor central;
- valor máximo plausível;

em vez de produzir falsa exatidão.

O intervalo deve resultar de fontes ou premissas explicitadas.

## 7. Confiança do valuation

- `ALTA` — valor diretamente observável/confirmado na data-base;
- `MEDIA` — estimativa apoiada em múltiplas referências ou método consistente;
- `BAIXA` — dado incompleto ou alta dispersão;
- `NAO_AVALIADO`.

Confiança econômica não altera status jurídico.

## 8. Fixture de validação

Exemplo puramente metodológico:

| Item | Valor bruto | Passivo vinculado | Custos fundamentados | Valor líquido |
|---|---:|---:|---:|---:|
| Imóvel | R$ 600.000 | R$ 220.000 | R$ 20.000 | R$ 360.000 |
| Veículo | R$ 90.000 | R$ 30.000 | R$ 2.000 | R$ 58.000 |
| Investimento | R$ 80.000 | R$ 0 | R$ 0 | R$ 80.000 |

```text
PATRIMONIO_BRUTO = 770.000
PASSIVOS_VINCULADOS = 250.000
CUSTOS_FUNDAMENTADOS = 22.000
PATRIMONIO_LIQUIDO_ESTIMADO = 498.000
```

A soma serve apenas para validar a mecânica. A alocação entre partes continua dependente do status jurídico de cada item.

## 9. Gate

Gate satisfeito:
- data-base obrigatória;
- métodos definidos por classe;
- custos de conversão sem percentuais arbitrários;
- tratamento de moeda/recebíveis/empresas documentado;
- níveis de confiança definidos;
- fixture aritmético validado.
