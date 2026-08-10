# Clayton Rennan — Engenheiro Civil

Site institucional de página única (estática) para **Clayton Rennan**, engenheiro civil — projetos estruturais, laudos técnicos e acompanhamento de obra.

## Estrutura

| Arquivo        | Função                                                |
| -------------- | ----------------------------------------------------- |
| `index.html`   | Página principal (Tailwind via CDN + Material Symbols) |
| `404.html`     | Página de erro 404 no mesmo visual                    |
| `vercel.json`  | Configuração do deploy (headers, clean URLs)          |
| `robots.txt`   | Permissão de indexação + aponta para o sitemap        |
| `sitemap.xml`  | Sitemap (URL principal)                               |
| `favicon.svg`  | Favicon do site                                       |

## Deploy na Vercel

**Opção 1 — CLI:**

```bash
npm i -g vercel
vercel        # preview
vercel --prod # produção
```

**Opção 2 — Git (GitHub/GitLab/Bitbucket):** importe o repositório em [vercel.com/new](https://vercel.com/new). Sem build command, sem output directory — é um site estático puro.

## Importante antes de publicar

- Troque o domínio de placeholder `claytonrennan.vercel.app` em `robots.txt`, `sitemap.xml` e nas meta tags `canonical`/`og:url` do `index.html` pelo domínio real (ex.: `claytonrennan.com.br`) depois que conectar na Vercel.
- A data do `sitemap.xml` (`lastmod`) pode ser atualizada a cada publicação.
- O Tailwind via CDN (`cdn.tailwindcss.com`) mostra um aviso de desenvolvimento no console — para produção ideal é buildar com o Tailwind CLI. Para este site de página única funciona normalmente.
