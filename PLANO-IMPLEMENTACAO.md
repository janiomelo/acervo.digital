# Plano de implementação

## Contexto atual (confirmado)

- O item `2/index.html` está sem botão/painel `Txt` de transcrição. 

“Eu invento minhas gírias que só eu entendo

Eu agora tô com um tal de “passo mal” que é um equivalente a “que engraçado” “ou estou rindo”

Só que só funciona na minha cabeça
ajaisakak

Passo mal kkkkkk”


- Os itens `1/index.html` e `3/index.html` já têm `Txt` + `Alt`.
- Ainda não há navegação entre itens (anterior/próximo).
- Ainda não há página de erro para rotas inexistentes (`404`).
- Ainda não há alternância de tema claro/escuro no site.

## O que precisa ser feito

- [ ] Adicionar transcrição no item 002 (`2/index.html`)
- [ ] Padronizar os três itens com os mesmos controles (`Txt`, `Alt`, compartilhar)
- [ ] Implementar navegação entre itens (001, 002, 003)
- [ ] Criar página `404.html`
- [ ] Implementar tema claro/escuro com persistência (`localStorage`)
- [ ] Aplicar tema na home, itens e página de transparência
- [ ] Revisar conteúdo sensível no item 001

## Proposta técnica

### 1) Transcrição no item 002

- Incluir botão `Txt` ao lado de `Alt`.
- Incluir painel com a transcrição literal já aprovada.
- Fechamento por `Esc`, clique fora e botão `X`.

### 2) Navegação entre imagens/itens

- Em cada item (`1/`, `2/`, `3/`), adicionar botões:
  - `Anterior`
  - `Próximo`
  - `Voltar para galeria`
- Atalhos de teclado:
  - `ArrowLeft` = anterior
  - `ArrowRight` = próximo
- Ordem de navegação cíclica:
  - 001 -> 002 -> 003 -> 001

### 3) Página 404

- Criar `404.html` na raiz.
- Conteúdo mínimo:
  - título claro: "Página não encontrada"
  - link para home (`/`)
  - link para transparência (`/transparencia/`)
- Layout visual consistente com o restante do projeto.

### 4) Tema claro/escuro

- Criar tokens CSS por variável (`--bg`, `--text`, `--surface`, etc.).
- Definir tema padrão por `prefers-color-scheme`.
- Botão de alternância visível no cabeçalho.
- Persistir escolha em `localStorage`.
- Aplicar em:
  - `index.html`
  - `1/index.html`
  - `2/index.html`
  - `3/index.html`
  - `transparencia/index.html`
  - `404.html`

### 5) Conteúdo explícito (item 001)

Recomendação editorial e de UX para este projeto:

- Não censurar nem ocultar a imagem.
- Não ocultar transcrição por padrão.
- Remover o mecanismo de "revelar conteúdo explícito" (blur em palavras), porque introduz fricção e pode distorcer leitura documental.
- Se você quiser um sinal mínimo, usar somente um aviso discreto, sem bloqueio, por exemplo:
  - "Este item contém linguagem explícita." (resposta minha: quero isso!!!!)

## Dúvidas para decisão (antes da implementação)

- [ ] Navegação entre itens deve ser cíclica (001 -> 003 -> 001) ou linear (sem loop)? - r: com loop
- [ ] O tema padrão deve seguir o sistema (`prefers-color-scheme`) ou iniciar sempre em escuro? R: prefers-color-scheme
- [ ] No item 001, você confirma remover totalmente o ocultamento de palavras explícitas? - R: sim
- [ ] Quer aviso textual discreto de linguagem explícita ou prefere sem aviso algum? - R: quero sim, geral, para texto e imagem. algo mais visual
- [ ] A página `404` deve mostrar somente links utilitários ou também mini-lista de itens recentes? - consegue me surpreender com texto pensando em algo pro projeto? - ou simples e links

## Ordem sugerida de execução

1. Corrigir item 002 com `Txt`.
2. Padronizar navegação entre itens.
3. Criar `404.html`.
4. Implementar tema claro/escuro em todas as páginas.
5. Ajustar política de conteúdo explícito no item 001.
6. Revisão final visual + teste manual de links e compartilhamento.
