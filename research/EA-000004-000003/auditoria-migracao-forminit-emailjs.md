# Auditoria — Migração do Fale Conosco para Forminit + EmailJS

**Data:** 20/09/2026  
**Estratégia:** EA-000004-000003

## Confirmado

- FormSubmit removido da camada pública;
- SDK Forminit presente;
- SDK EmailJS presente;
- protocolo só é liberado no fluxo após retorno de sucesso do Forminit;
- confirmação por e-mail é posterior ao recebimento confirmado;
- página de recibo distingue e-mail enviado, falha no e-mail e ausência de e-mail;
- formulário permanece oculto enquanto os quatro identificadores reais não estiverem configurados;
- e-mail institucional direto permanece disponível;
- deploy GitHub Pages 35527384732 concluído com sucesso.

## Bloqueio externo

Faltam credenciais/identificadores públicos obtidos nos painéis autenticados:

- Forminit Form ID próprio do projeto;
- EmailJS Service ID;
- EmailJS Template ID;
- EmailJS Public Key.

Sem esses dados não é possível executar teste end-to-end real. O estado correto é **BACKEND_NAO_CONFIGURADO**, não “operacional”.
