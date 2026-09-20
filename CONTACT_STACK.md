# Stack do Fale Conosco — Planejamento Financeiro

## Estado

**MIGRAÇÃO TÉCNICA PENDENTE**

A implementação pública atual usa **FormSubmit** e foi classificada como não conforme após a revisão do padrão.

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

- criar Forminit próprio do projeto, com roteamento ao e-mail institucional;
- registrar `FORM_ID`;
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
