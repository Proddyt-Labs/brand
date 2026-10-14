# Proddyt brand

Identidade visual compartilhada por todos os sites Proddyt (Proddyt, Proddyt Labs, Proddyt Studio).
Página de referência: https://proddyt-labs.github.io/brand/

## Conteúdo

| Arquivo | O que é |
|---|---|
| `tokens.css` | Variáveis de cor, fonte e raio. Tema claro padrão; escuro por `prefers-color-scheme` ou `[data-theme="dark"]`; frente por `[data-brand]` |
| `base.css` | Estilos base e componentes `p-*` (header, logo, botão, card, chip, footer, ícone de app) |
| `theme.js` | Botão de tema: qualquer `<button data-theme-toggle>`; escolha salva em `localStorage` (`proddyt-theme`) |
| `marks/*.svg` | Símbolo `/·/` de cada frente (`proddyt`, `labs`, `studio`) |
| `marks/apps/*.png` | Ícones 256px dos 12 apps do Studio (fonte: `switch-tools/icons`) |
| `index.html` | Página de referência (também é o teste visual da marca) |

## Usar num site

```html
<html lang="pt-BR" data-brand="labs">
<head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600;700&family=IBM+Plex+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Proddyt-Labs/brand@1/tokens.css">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Proddyt-Labs/brand@1/base.css">
  <script src="https://cdn.jsdelivr.net/gh/Proddyt-Labs/brand@1/theme.js"></script>
</head>
```

Sites linkam `@1`: o jsDelivr resolve pra última tag `v1.x.x`.

## Publicar uma mudança

1. Edite e confira o `index.html` localmente nos 2 temas.
2. Push na `main` → workflow `Publish`: republica a página (GitHub Pages), cria a tag `v1.<run>.0` e purga o cache do jsDelivr. Sites atualizam em minutos, sem commit neles.
3. Mudança que quebra site: troque `MAJOR` pra `2` no workflow e migre cada site pra `@2`.

Spec e decisão: Second Brain `ORGANIZATIONS/PRODDYT/MARCA.md`.
