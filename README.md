# AURA-OS — Site

Site estatico do projeto AURA-OS: guias de compra, produtos digitais e
politica de privacidade.

## Estrutura

- `index.html`        — home com a lista de guias
- `blog.html`         — todos os guias
- `store.html`        — produtos digitais
- `buy-*.html`        — paginas de venda
- `posts/*.html`      — guias individuais
- `privacy.html`      — politica de privacidade
- `sitemap.xml`       — sitemap
- `robots.txt`        — robots
- `feed.xml`          — RSS 2.0

## Como e gerado

Todo o conteudo e gerado a partir de `~/.aura-os/scripts/`:

```bash
python3 product_research.py       # coleta produtos
python3 blog_batch.py 18          # gera os guias (LLM)
python3 product_builder.py guide  # produto digital + PDF
python3 site_builder.py --base-url https://teles-eliandro.github.io/aura-os
python3 store_builder.py build    # paginas de venda
```

Nao edite os HTML a mao — eles sao sobrescritos.

## Afiliados

Links de afiliado usam `rel="nofollow sponsored"`, conforme exigido pelo
Google. O disclosure da Amazon Associates aparece no rodape de cada pagina.

## Deploy

GitHub Pages, branch `main`, raiz do repositorio.
