# Auditoria da integração editorial — 22/09/2026

## Escopo

Integração pública de **Publicações → Notícias / Artigos / Observatório** no Site Planejamento Financeiro.

## Resultado

- páginas HTML auditadas: **37**;
- páginas com item **Publicações** no menu global: **37/37**;
- links internos (`href`) verificados: **900**;
- links internos quebrados: **0**;
- marcadores internos de governança expostos na camada pública: **0**;
- pares Markdown/HTML criados para Hub, Notícias, Artigos e Observatório: **4/4**;
- JSON editorial espelho criado: **não** — política de JSON condicional preservada;
- Mapa do Site atualizado: **sim**;
- `SITE_ARCHITECTURE.md` atualizado: **sim**;
- workflow inclui `publicacoes/**` e copia as quatro rotas públicas: **sim**.

## Deploy

- commit público final: `564775f06979052de485134f958011bece91aa11`;
- GitHub Actions run: `35729180230`;
- job `deploy`: **success**;
- Checkout: success;
- Build public-only artifact: success;
- Setup Pages: success;
- Upload Pages artifact: success;
- Deploy to GitHub Pages: success.

## Observação de verificação

A tentativa de leitura HTTP independente das novas URLs pelo mecanismo externo disponível nesta sessão não conseguiu acessar o domínio GitHub Pages. Por isso, a comprovação de publicação adotada neste fechamento é o pipeline oficial do próprio repositório, cujo build, upload do artefato e etapa **Deploy to GitHub Pages** concluíram com sucesso.

## Gate de não redundância

Satisfeito:
- Notícias = mudança temporal/factual;
- Artigos = análise e argumentação;
- Observatório = conhecimento cumulativo, sinais, interdependências, lacunas e revalidação;
- Conhecimentos, Casos e Ferramentas = conteúdo estável e operacional.
