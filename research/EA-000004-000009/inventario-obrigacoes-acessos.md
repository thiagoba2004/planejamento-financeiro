# Fase 01/06 — Inventário de obrigações e acessos

**Estratégia:** EA-000004-000009 — Dívidas, crédito, garantias e contas conjuntas  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## Objetivo

Construir um inventário operacional de obrigações financeiras e acessos após a ruptura, separando quatro dimensões:

1. **quem figura formalmente no contrato ou relacionamento**;
2. **quem paga hoje**;
3. **qual é o impacto financeiro**;
4. **qual é a classificação jurídica aplicável ou ainda pendente**.

O planejamento financeiro não presume responsabilidade jurídica apenas porque determinada dívida foi contraída durante a relação.

## Escopo do inventário

### Empréstimos e financiamentos
- credor;
- modalidade;
- devedor(es) formal(is);
- coobrigado/garantidor formal;
- saldo devedor;
- prestação;
- vencimento;
- taxa/CET quando disponível;
- prazo;
- garantia;
- débito automático;
- conta de pagamento;
- status de adimplência;
- data-base.

### Cartões
- titular;
- cartões adicionais;
- fatura atual;
- compras parceladas futuras;
- limite total;
- limite disponível;
- débito automático;
- assinaturas recorrentes;
- carteiras digitais vinculadas;
- status de bloqueio/cancelamento quando aplicável.

### Contas e relacionamentos
- instituição;
- tipo de conta;
- titularidade formal;
- forma de movimentação contratual;
- cartões vinculados;
- Pix e outros meios de pagamento;
- débitos automáticos;
- autorizações recorrentes;
- procuradores/representantes, quando houver;
- dispositivos e canais próprios utilizados.

### Garantias
- tipo;
- obrigação garantida;
- bem ou direito vinculado;
- garantidor formal;
- valor/limite;
- documentos;
- status jurídico;
- risco financeiro em caso de inadimplência.

## Instrumentos de descoberta

### SCR
O Relatório de Empréstimos e Financiamentos do Banco Central é útil para conhecer compromissos de crédito reportados pelas instituições e apoiar a reconciliação com contratos/extratos.

### CCS
O Cadastro de Clientes do Sistema Financeiro ajuda a localizar relacionamentos com instituições financeiras. Ele identifica vínculos, mas não substitui extratos nem informa saldos/movimentações.

### Documentos primários
- contratos;
- faturas;
- extratos;
- boletos;
- demonstrativos de evolução;
- propostas/renegociações;
- termos de garantia;
- comprovantes de pagamento.

## Acessos e segurança operacional

O inventário deve registrar apenas os acessos do próprio cliente ou formalmente autorizados.

Verificar:
- senha pessoal;
- biometria;
- dispositivo confiável;
- token;
- cartão físico;
- cartão virtual;
- carteira digital;
- chave Pix;
- e-mail/telefone de recuperação;
- assinaturas/recorrências;
- procurações/autorizados formais.

Nunca orientar acesso indevido a conta, aparelho, senha ou credencial de terceiro.

## Estados do dado

- `COMPROVADO`;
- `INFORMADO_NAO_COMPROVADO`;
- `DIVERGENTE`;
- `DADO_AUSENTE`;
- `CONTROVERTIDO`;
- `JURIDICO_CONFIRMADO`.

## Perguntas de diagnóstico

1. Quais dívidas constam nos contratos e quais aparecem no SCR?
2. Há diferença entre saldo contratual e saldo informado?
3. Quem é devedor formal, coobrigado ou garantidor?
4. Quem está pagando cada obrigação hoje?
5. Qual conta recebe débitos automáticos?
6. Há cartão adicional ou autorização recorrente ainda ativa?
7. Há conta conjunta ou relacionamento compartilhado?
8. Existem limites de crédito não utilizados?
9. Há compras parceladas futuras?
10. Há garantia patrimonial vinculada?
11. Algum bem em partilha garante dívida?
12. Existe atraso ou risco de vencimento imediato?
13. Há acesso digital que precisa ser regularizado pelo próprio titular?
14. Há relacionamento bancário identificado no CCS ainda não documentado?
15. Que pontos dependem de conclusão jurídica?

## Gate

Satisfeito. Escopo, perguntas, fontes de descoberta, segurança operacional, estados de dado e limites profissionais foram persistidos.
