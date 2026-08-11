# Pressell — Deploy na Vercel

Este projeto é 100% estático (HTML + CSS + JS puro), então não precisa de build nem de dependências.

## Estrutura

```
/
├── index.html     ← a página inteira
├── vercel.json    ← configuração da Vercel (headers, cache)
└── README.md
```

## Como publicar

### Opção 1 — Vercel CLI (mais rápido)

```bash
npm i -g vercel
cd pasta-do-projeto
vercel
```

Siga as perguntas no terminal (Enter para aceitar os padrões). No final ele te dá uma URL tipo `https://seu-projeto.vercel.app`.

Para publicar em produção diretamente:

```bash
vercel --prod
```

### Opção 2 — Painel da Vercel (sem terminal)

1. Acesse https://vercel.com/new
2. Clique em **"Deploy" → arraste a pasta do projeto** (ou conecte um repositório Git com esses arquivos)
3. Como é um projeto estático, a Vercel detecta automaticamente — não precisa configurar Build Command nem Output Directory
4. Clique em **Deploy**

### Opção 3 — GitHub + Vercel (recomendado se for atualizar com frequência)

1. Suba esses arquivos (`index.html`, `vercel.json`) para um repositório no GitHub
2. Em https://vercel.com/new, importe o repositório
3. Todo push na branch principal gera um novo deploy automaticamente

## Domínio próprio

Depois de publicado, em **Project Settings → Domains** você pode apontar um domínio próprio (ex: `seusite.com`) para essa página.

## Observações

- O link do Telegram e os links de loja (App Store / Play Store) estão fixos direto no `index.html`, dentro da tag `<script>`. Para trocar, edite as constantes `GROUP_URL`, `PLAY_STORE_URL` e `APP_STORE_URL`.
- Como é HTML puro, funciona em qualquer plano da Vercel, inclusive o gratuito.
