# Stack do Fale Conosco — Planejamento Financeiro

## Estado

**FORMINIT + EMAILJS CONFIGURADOS / TESTE E2E PENDENTE**

O FormSubmit foi removido da camada pública. O frontend já usa a stack canônica Forminit + EmailJS.

## Padrão canônico aprovado

- e-mail institucional: `planejamentofinanceiro2012@gmail.com`;
- prefixo de protocolo: `PF-`;
- recebimento e anexos: **Forminit**;
- confirmação do protocolo ao remetente: **EmailJS**;
- referência funcional: Fale Conosco do Site Classe e Massas.

## Regra de recebimento

1. gerar protocolo no cliente;
2. enviar protocolo e conteúdo ao Forminit;
3. somente após resposta de sucesso do Forminit considerar a submissão recebida;
4. se houver e-mail de retorno, acionar EmailJS;
5. redirecionar para página de confirmação com o protocolo;
6. distinguir sucesso do protocolo de eventual falha no e-mail.

## Configuração exigida antes do teste

- Forminit próprio do projeto criado;
- `FORM_ID`: `7wcs1ehfwsf`;
- Authentication mode: `Public`;
- Self-email notification: `Active`;
- configurar EmailJS para envio ao e-mail informado pelo visitante;
- registrar `SERVICE_ID`, `TEMPLATE_ID` e chave pública quando aplicável;
- não reutilizar FORM_ID do Classe e Massas sem comprovar isolamento.

## Gate end-to-end

O canal só pode ser declarado operacional depois de teste real que comprove:
- recebimento no backend;
- protocolo idêntico na submissão e na confirmação;
- chegada do protocolo ao e-mail de retorno;
- comportamento sem e-mail;
- falha do e-mail sem invalidação do protocolo;
- anexos, se publicados.


## Bloqueio externo comprovado

O frontend já segue a lógica Forminit + EmailJS. A ativação pública depende de configuração autenticada nos painéis dos provedores:

- Forminit próprio já criado em modo Public, com `FORM_ID 7wcs1ehfwsf`;
- Self-email notification ativada;
- criar ou validar serviço/template EmailJS e obter Service ID, Template ID e Public Key;
- inserir os quatro identificadores no frontend;
- executar teste end-to-end real.

Enquanto os identificadores do EmailJS não existirem, o formulário permanece oculto e o e-mail institucional direto continua disponível.


## Forminit do Planejamento Financeiro criado

Em 20/09/2026, foi criado o formulário isolado do projeto:

- nome: **Fale Conosco — Planejamento Financeiro**;
- Form ID: `7wcs1ehfwsf`;
- Authentication mode: **Public**;
- Self-email notification: **Active**.

O próximo componente pendente da stack é o EmailJS para envio do protocolo ao remetente.


## EmailJS Service e Public Key configurados

Em 20/09/2026, foram configurados no projeto Planejamento Financeiro:

- serviço: **Gmail — Planejamento Financeiro**;
- Service ID: `service_i1a5brn`;
- conta institucional: `planejamentofinanceiro2012@gmail.com`;
- Public Key: `pUNgfjly-neqGcOJE`.

A Public Key é um identificador público de cliente usado pelo SDK do EmailJS no navegador. A Private Key não deve ser versionada nem inserida no frontend.

Permanece pendente:
- criar o template de confirmação de protocolo;
- obter o Template ID;
- inserir o Template ID no frontend;
- executar o teste end-to-end real.


## Correção — template já existente

O usuário informou que o template de confirmação do Planejamento Financeiro **já havia sido criado**.

Portanto, não há pendência de criação de template. Falta apenas obter/registrar o **Template ID** desse template já existente e inseri-lo no frontend antes do teste end-to-end.


## EmailJS Template ID configurado

Em 20/09/2026, foi confirmado o template **Confirmação de Protocolo - Planejamento Financeiro**:

- Template ID: `template_hcfqltz`;
- Service ID: `service_i1a5brn`;
- Public Key: `pUNgfjly-neqGcOJE`;
- Forminit Form ID: `7wcs1ehfwsf`.

A configuração técnica necessária para o fluxo está completa. O próximo gate é o teste end-to-end real.


## Teste real de 20/09/2026

Evidências:
- protocolo público: `PF-20260920-172057-2A2C86`;
- registro técnico Forminit: `rS2g1N0yKZb08RwK`;
- EmailJS History: `email_f0nKUDSMlsaED3hqEQNKnsLk`;
- resultado EmailJS: **OK**;
- destinatário: `thiagoba2004@yahoo.com.br`;
- confirmação recebida efetivamente na Caixa de Entrada do Yahoo Mail;
- mesmo protocolo preservado entre Site, Forminit e EmailJS.

### Estado final

`E2E_VERIFICADO`

### Dívida não bloqueante

O e-mail exibe a marca “Email sent via EmailJS.com”; avaliar remoção futura apenas se houver suporte do plano/provedor e se for desejável para identidade visual.


## Privacidade e minimização — atualização 21/09/2026

- rota pública: `privacidade/index.html`;
- o Fale Conosco e a página de recibo apontam para o Aviso de Privacidade;
- o formulário pode receber nome/pseudônimo, e-mail, assunto, URL, mensagem e até três anexos;
- anexos são opcionais e o Site orienta minimização/anonimização;
- o workflow do GitHub Pages inclui explicitamente `privacidade/**`;
- o estado operacional do canal permanece `E2E_VERIFICADO`.
