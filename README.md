# Acervo.digital

Galeria pública e minimalista para preservação e compartilhamento de peças digitais.

## Estrutura Atual

- `index.html` — galeria principal
- `1/index.html` — item 001
- `2/index.html` — item 002
- `3/index.html` — item 003
- `transparencia/index.html` — transparência e contato
- `assets/` — arquivos de mídia e imagens sociais

## Publicação De Novos Itens

1. Crie uma nova pasta com URL curta, como `4/`.
2. Adicione `4/index.html` usando o mesmo padrão dos itens existentes.
3. Coloque os arquivos de mídia em `assets/` (ex.: `publicacao_04.png`).
4. Gere ou adicione a imagem social (ex.: `social_04.png`).
5. Atualize `index.html` com número, resumo, autor e link para `4/`.

## Compartilhamento Social

Cada item pode usar uma imagem social específica no `og:image`, separada da peça original, para evitar cortes ruins em cards de redes sociais.

## Navegação Entre Itens

Nas páginas de item, a navegação entre publicações funciona de duas formas:

- botões laterais sobre a imagem (anterior e próximo)
- atalhos de teclado (`ArrowLeft` e `ArrowRight`)

## Deploy

O deploy é automatizado pelo workflow em `.github/workflows/deploy.yml`.

## Transparência E Contato

A página pública de transparência e contato está em `transparencia/index.html`.
Contato principal: `contato@acervo.digital`.

