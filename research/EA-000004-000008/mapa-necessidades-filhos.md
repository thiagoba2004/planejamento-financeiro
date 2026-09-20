# Fase 01/06 — Mapa de necessidades dos filhos

**Estratégia:** EA-000004-000008 — Filhos: alimentos, educação, saúde e logística de convivência  
**Data:** 20/09/2026  
**Estado:** CONCLUÍDA

## Objetivo

Transformar necessidades dos filhos em dados financeiros estruturados, sem fixar alimentos, guarda, residência-base ou convivência.

## Fronteira jurídica

O Planejamento Financeiro pode receber como premissa:
- residência-base confirmada;
- calendário de convivência confirmado;
- alimentos provisórios ou definitivos efetivamente fixados;
- regra confirmada de rateio/reembolso;
- obrigações específicas formalizadas;
- cenários jurídicos explicitamente rotulados quando a matéria ainda estiver pendente.

O Planejamento Financeiro não:
- define necessidade jurídica;
- determina percentual de alimentos;
- escolhe guarda;
- altera convivência;
- presume quem deve pagar determinada despesa;
- converte pedido em obrigação confirmada.

## Mapa de necessidades

### 1. Alimentação
- alimentação doméstica;
- alimentação escolar;
- dietas especiais;
- suplementação quando comprovadamente necessária.

### 2. Moradia
- parcela de custos habitacionais atribuível ao planejamento familiar;
- espaço, mobiliário e adaptações necessárias;
- eventual duplicação de itens entre residências;
- custos adicionais de mudança ou reorganização.

### 3. Educação
- mensalidade;
- matrícula;
- material escolar;
- livros;
- uniforme;
- transporte escolar;
- cursos;
- tecnologia educacional;
- excursões e atividades.

### 4. Saúde
- plano de saúde;
- coparticipação;
- consultas;
- exames;
- medicamentos;
- terapias;
- odontologia;
- óculos/aparelhos;
- necessidades continuadas ou especiais.

### 5. Transporte e logística de convivência
- transporte cotidiano;
- combustível;
- aplicativo/táxi;
- passagens;
- pedágios;
- estacionamento;
- deslocamentos entre residências;
- viagens necessárias à convivência, quando aplicáveis.

### 6. Cuidado
- creche;
- babá/cuidador;
- contraturno;
- apoio especializado;
- acompanhamento por adulto em horários incompatíveis com a jornada dos responsáveis.

### 7. Vestuário e higiene
- roupas;
- calçados;
- itens de higiene;
- itens de uso recorrente ou reposição sazonal.

### 8. Lazer, cultura e esporte
- atividades esportivas;
- cursos artísticos;
- lazer regular;
- eventos;
- equipamentos vinculados à atividade.

### 9. Necessidades especiais
- terapias;
- equipamentos;
- adaptações;
- transporte especializado;
- cuidador;
- medicamentos de uso contínuo;
- qualquer despesa documentada com impacto material.

## Perguntas de diagnóstico

1. Quais despesas existem hoje?
2. Quais são essenciais, recorrentes e comprovadas?
3. Quais variam por residência ou calendário de convivência?
4. Quais são anuais, semestrais, trimestrais ou eventuais?
5. Quais têm histórico suficiente para estimar média?
6. Quais dependem de decisão jurídica ainda não confirmada?
7. Há despesas que aparecem duplicadas nas duas residências?
8. Há custo logístico novo após a ruptura?
9. Existem despesas extraordinárias previsíveis?
10. Há objetivos futuros relevantes — educação, saúde, intercâmbio, equipamentos?
11. Há necessidade especial com tendência de custo crescente?
12. Qual dado faltante muda materialmente o plano?

## Estados do dado

- `COMPROVADO`;
- `INFORMADO_NAO_COMPROVADO`;
- `ESTIMADO_COM_HISTORICO`;
- `CENARIO`;
- `DADO_AUSENTE`;
- `CONTROVERTIDO`.

## Regra contra dupla contagem

Uma mesma despesa não pode:
- ser lançada integralmente em ambos os responsáveis;
- entrar como custo dos filhos e novamente como despesa doméstica sem reconciliação;
- ser tratada simultaneamente como despesa mensal e evento extraordinário;
- aparecer como transferência e como nova renda familiar.

## Gate

Satisfeito. Necessidades, perguntas, estados de dado, dependências e limites profissionais foram persistidos.
