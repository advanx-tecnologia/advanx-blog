# Blog Advanx — IA e Captação para Advogados

Blog estático gerado com **Hugo + PaperMod**, hospedado no GitHub Pages.

🌐 **URL:** https://blog.advanx.com.br

---

## Como publicar um novo artigo

### Opção 1 — Editar direto no GitHub (mais fácil)

1. Acesse a pasta [`content/posts/`](./content/posts/)
2. Clique em **"Add file" → "Create new file"**
3. Nome do arquivo: `meu-artigo.md`
4. Cole o conteúdo com o formato abaixo
5. Clique em **"Commit changes"** → deploy automático em ~2 min

### Opção 2 — Git local

```bash
# Clone o repositório
git clone https://github.com/advanx-tecnologia/advanx-blog.git
cd advanx-blog

# Crie o arquivo do artigo
# (substitua o nome do slug pelo tema do artigo)
nano content/posts/meu-artigo.md

# Publique
git add .
git commit -m "post: Título do artigo"
git push origin main
# GitHub Actions faz o deploy automático
```

---

## Formato do artigo (frontmatter obrigatório)

```markdown
---
title: "Título do Artigo Aqui"
date: 2026-05-20
description: "Resumo do artigo para SEO e listagem (1-2 frases)."
slug: "url-do-artigo"
tags:
  - "IA para advogados"
  - "captação de clientes"
draft: false
---

Conteúdo do artigo começa aqui.

## Subtítulo

Parágrafo normal. Use **negrito** e *itálico* normalmente.

## Outro Subtítulo

- Item de lista
- Outro item

> Citação ou destaque importante
```

---

## Campos do frontmatter

| Campo | Obrigatório | Descrição |
|-------|-------------|-----------|
| `title` | ✅ | Título do artigo (aparece na página e no Google) |
| `date` | ✅ | Data de publicação (formato AAAA-MM-DD) |
| `description` | ✅ | Resumo para SEO (aparecer no Google) |
| `slug` | ✅ | URL do artigo (sem espaços, sem acentos) |
| `tags` | recomendado | Categorias/tópicos do artigo |
| `draft` | ✅ | `false` = publicado, `true` = rascunho |
| `image` | opcional | URL da imagem de capa |

---

## Dicas de SEO

- **title**: inclua a palavra-chave principal (ex: "IA para advogados")
- **description**: 120-160 caracteres, descreva o conteúdo
- **slug**: use a palavra-chave principal na URL
- **tags**: escolha 3-5 tags relevantes
- Artigos com 800+ palavras rankeiam melhor

---

## Estrutura do repositório

```
content/
  posts/           ← seus artigos ficam aqui
    exemplo.md
static/
  CNAME            ← domínio blog.advanx.com.br
hugo.toml          ← configurações do blog
themes/
  PaperMod/        ← tema (não editar)
.github/
  workflows/
    deploy.yml     ← GitHub Actions (deploy automático)
```

---

## Deploy automático

Cada `git push` na branch `main` dispara o GitHub Actions:
1. Instala Hugo
2. Faz o build do site
3. Publica no GitHub Pages

Tempo médio: **~2 minutos** após o push.

Acompanhe em: [Actions](https://github.com/advanx-tecnologia/advanx-blog/actions)

---

## Adicionar imagem de capa

```markdown
---
image: "https://lhbwfbquxkutcyqazpnw.supabase.co/storage/v1/object/public/images/blog/minha-imagem.webp"
---
```

Ou use imagens externas (Unsplash, etc.) pelo link direto.

---

## Contato e suporte

Site principal: [advanx.com.br](https://advanx.com.br)
