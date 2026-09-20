# Stack do Fale Conosco — Planejamento Financeiro

## Estado

**FORMINIT CONFIGURADO / EMAILJS PENDENTE**

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
