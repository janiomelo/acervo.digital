# Acervo — POC estática

Protótipo mínimo em HTML, CSS e JavaScript puro para testar a ideia do **acervo.digital** no GitHub Pages.

## O que já tem

- visual limpo e minimalista
- imagem em destaque
- título, resumo, créditos e descrição
- botão de compartilhar
- botão de copiar link
- botão para abrir/baixar a imagem
- pronto para publicação estática

## Estrutura

- `index.html` — página única
- `assets/publicacao.webp` — imagem usada na POC

## Como usar

Abra `index.html` no navegador.

## Como publicar no GitHub Pages

1. crie um repositório
2. envie os arquivos desta pasta
3. nas configurações do repositório, habilite o GitHub Pages apontando para a branch principal
4. publique a raiz do projeto

## Como trocar os dados

No final do `index.html`, edite o objeto `item`:

```js
const item = {
  id: '0001',
  title: 'Seu título',
  summary: 'Seu resumo',
  credit: '@perfil',
  platform: 'Instagram',
  description: 'Descrição do item',
  status: 'Ativo, removido, arquivado etc.'
};
```

Se quiser trocar a imagem, substitua `assets/publicacao.webp` e ajuste os caminhos no HTML.

## Próximos passos possíveis

- slug por item
- página de galeria
- metadados Open Graph por item
- transcrição
- coleção e tags
- tema escuro
