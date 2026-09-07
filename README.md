# DesenvolvimentoWeb_20262

Repositório de Aula da AA de Desenvolvimento Web e Aplicativos.

Este README funciona como um **guia de consulta rápida** com todas as tags HTML e propriedades CSS já trabalhadas em aula, nos projetos guiados e nos trabalhos, na ordem em que foram aparecendo no curso. Use `Ctrl+F` para encontrar rapidamente uma tag ou propriedade.

## Estrutura do repositório

- `aulas/` — exemplos e exercícios feitos durante as aulas (aula2 a aula6)
- `projetos-guiados/` — projetos conduzidos passo a passo em sala
- `trabalhos/` — trabalhos avaliativos entregues pelos alunos

---

## Aula 2 — HTML Básico

Arquivos: [aulas/aula2/index.html](aulas/aula2/index.html), [trabalhos/trabalho1/trabalho1.html](trabalhos/trabalho1/trabalho1.html)

### Estrutura do documento

| Tag | Para que serve |
|---|---|
| `<!DOCTYPE html>` | Declara que o documento é HTML5 |
| `<html lang="pt-br">` | Elemento raiz; `lang` indica o idioma da página |
| `<head>` | Metadados da página (não aparece no corpo visível) |
| `<meta charset="UTF-8">` | Define a codificação de caracteres (acentos, ç, etc.) |
| `<title>` | Título exibido na aba do navegador |
| `<body>` | Conteúdo visível da página |
| `<!-- comentário -->` | Comentário HTML, não aparece na página |

### Textos e títulos

| Tag | Para que serve |
|---|---|
| `<h1>` a `<h6>` | Títulos e subtítulos, do mais (h1) ao menos importante (h6) |
| `<p>` | Parágrafo de texto |
| `<hr />` | Linha horizontal divisória |
| `<br />` | Quebra de linha |

### Listas

| Tag | Para que serve |
|---|---|
| `<ul>` | Lista **não ordenada** (marcadores/bullets) |
| `<ol>` | Lista **ordenada** (numerada) |
| `<li>` | Item de lista, usado dentro de `<ul>` ou `<ol>` |

### Links e imagens

| Tag/Atributo | Para que serve |
|---|---|
| `<a href="...">` | Link/âncora para outra página ou seção |
| `target="_blank"` | Abre o link em uma **nova aba** |
| `target="_self"` | Abre o link na **mesma aba** (padrão) |
| `<a name="topo"></a>` / `<a href="#topo">` | Âncora interna, cria um link para um ponto da própria página |
| `<img src="..." alt="..." width="" height="" />` | Insere uma imagem; `alt` é o texto alternativo (acessibilidade/SEO), `width`/`height` controlam o tamanho |

### Tabelas (usadas também como estrutura/layout na Aula 2/3)

| Tag | Para que serve |
|---|---|
| `<table>` | Cria a tabela |
| `<tr>` | Linha da tabela (*table row*) |
| `<th>` | Célula de cabeçalho (*table header*, texto em negrito e centralizado por padrão) |
| `<td>` | Célula de dado (*table data*) |
| `cellpadding="20"` | Espaçamento interno das células (atributo antigo, hoje se prefere `padding` via CSS) |

---

## Aula 3 — CSS Externo, Inline e Seletores

Arquivos: [aulas/aula3/resenha.html](aulas/aula3/resenha.html), [aulas/aula3/css/style-header.css](aulas/aula3/css/style-header.css), [aulas/aula3/css/style-body.css](aulas/aula3/css/style-body.css)

### As 3 formas de aplicar CSS

1. **Inline**: direto na tag, via atributo `style="..."` — ex: `<h1 style="color: blueviolet;">`
2. **Interno**: dentro de `<style>` no `<head>` do próprio HTML (ver Aula 4)
3. **Externo**: em um arquivo `.css` separado, ligado via `<link rel="stylesheet" href="css/arquivo.css" />`

### Seletores CSS

| Seletor | Exemplo | Atinge |
|---|---|---|
| Elemento (tag) | `p { }`, `h2 { }`, `table { }` | Todas as tags daquele tipo |
| Classe | `.paragrafo { }`, `.borda { }` | Todos os elementos com `class="paragrafo"` |
| ID | `#subtitulo { }` | O elemento único com `id="subtitulo"` |
| Universal | `* { }` | Todos os elementos da página |

Atributos usados nas tags para "conectar" com o CSS: `class="..."` (pode repetir na página) e `id="..."` (deve ser único).

### Propriedades de texto e cor

| Propriedade | Para que serve |
|---|---|
| `color` | Cor do texto |
| `background-color` | Cor de fundo |
| `text-align` | Alinhamento do texto (`center`, `justify`, `left`, `right`) |
| `letter-spacing` | Espaçamento entre letras |
| `font-family` | Fonte (com fontes alternativas separadas por vírgula) |

### Box model (introdução)

| Propriedade | Para que serve |
|---|---|
| `border` | Borda (largura, estilo e cor, ex: `1px solid orangered`) |
| `border-radius` | Arredonda os cantos da borda |
| `box-sizing: border-box` | Faz `padding` e `border` serem **incluídos** na largura/altura definidas (evita que somem "por fora") |
| `padding` | Espaçamento **interno**, entre o conteúdo e a borda |
| `margin` | Espaçamento **externo**, entre o elemento e os vizinhos |
| `width` | Largura do elemento |
| `opacity` | Transparência (0 a 1) |
| `display: inline-block` | Elemento se comporta como texto (fica na linha) mas aceita `width`/`height`/`margin` como um bloco |

> Dica: `padding`/`margin` aceitam de 1 a 4 valores: `padding: 20px 10px 20px 0px;` segue a ordem **topo, direita, baixo, esquerda** (sentido horário).

---

## Aula 4 — Formulários, CSS Interno e `position`

Arquivos: [aulas/aula4/aula4.html](aulas/aula4/aula4.html), [aulas/aula4/inquerito-operario.html](aulas/aula4/inquerito-operario.html), [aulas/aula4/posicionamento.html](aulas/aula4/posicionamento.html), [aulas/aula4/css/styles.css](aulas/aula4/css/styles.css)

### Formulários

| Tag/Atributo | Para que serve |
|---|---|
| `<form action="..." method="get\|post">` | Cria o formulário; `action` é o destino do envio, `method` define como os dados viajam (`GET` na URL, `POST` no corpo da requisição) |
| `enctype="multipart/form-data"` | Necessário quando o formulário envia **arquivos** |
| `<label for="id-do-campo">` | Rótulo de um campo; `for` conecta ao `id` do input, tornando-o clicável e acessível |
| `<fieldset>` | Agrupa campos relacionados dentro de uma borda |
| `<legend>` | Título/legenda de um `<fieldset>` |
| `<small>` | Texto pequeno, usado para dicas de preenchimento |
| `<code>` | Texto em formato de código (fonte monoespaçada) |

### Tipos de `<input>`

| `type` | Para que serve |
|---|---|
| `text` | Texto simples de uma linha |
| `password` | Texto oculto (senha) |
| `email` | Texto validado como e-mail |
| `number` | Número (aceita `min`, `max`, `step`) |
| `date` | Seletor de data |
| `checkbox` | Caixa de marcação (múltipla escolha) |
| `radio` | Botão de opção única dentro do mesmo `name` |
| `file` | Upload de arquivo (`accept` filtra o tipo aceito) |
| `submit` | Botão que envia o formulário |
| `reset` | Botão que limpa o formulário |

### Atributos de `<input>`/`<select>`/`<textarea>`

| Atributo | Para que serve |
|---|---|
| `name` | Nome do campo, usado como chave ao enviar os dados |
| `id` | Identificador único, usado por `<label for="">` e CSS |
| `value` | Valor pré-preenchido (ou o valor enviado, no caso de `radio`/`checkbox`) |
| `placeholder` | Texto de exemplo exibido quando o campo está vazio |
| `required` | Torna o preenchimento obrigatório |
| `disabled` | Desabilita o campo (não é enviado no formulário) |
| `list="id-do-datalist"` + `<datalist>` | Cria sugestões de autocompletar para um `<input>` |
| `<select>` / `<option value="">` | Caixa de seleção com opções |
| `<textarea rows="4">` | Campo de texto multilinha |

### CSS interno (`<style>` no `<head>`)

Além do CSS externo (link) e inline (atributo `style`), o CSS pode ser escrito dentro de uma tag `<style>` no `<head>` — útil para páginas de exemplo isoladas, como [posicionamento.html](aulas/aula4/posicionamento.html).

### A propriedade `position`

| Valor | Comportamento |
|---|---|
| `static` | Padrão. Segue o fluxo normal; `top/right/bottom/left` não têm efeito |
| `relative` | Mantém o espaço original, mas pode ser deslocado com `top/right/bottom/left` a partir dele mesmo |
| `absolute` | Sai do fluxo normal; posiciona-se em relação ao ancestral mais próximo que **não** seja `static` |
| `fixed` | Sai do fluxo; fica fixo em relação à **janela do navegador**, mesmo durante o scroll |
| `sticky` | Híbrido: comporta-se como `relative` até atingir o limite definido (ex: `top: 0`), aí "gruda" como `fixed` |

Outras propriedades usadas junto com `position`: `top`, `right`, `bottom`, `left`, `z-index` (ordem de sobreposição entre elementos).

---

## Aula 5 — Responsividade (Mobile-First e Media Queries)

Arquivos: [aulas/aula5/inquerito-operario.html](aulas/aula5/inquerito-operario.html), [aulas/aula5/css/styles.css](aulas/aula5/css/styles.css)

### Conceitos

- **Mobile-first**: o CSS "base" (sem media query) é escrito para telas pequenas; regras dentro de `@media (min-width: ...)` vão **adicionando/ajustando** o layout conforme a tela cresce.
- **Viewport**: sem a meta tag de viewport, o celular renderiza a página como se fosse desktop e depois encolhe tudo.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Media queries usadas

| Media query | Quando se aplica |
|---|---|
| `@media (min-width: 600px)` | A partir da largura de tablet |
| `@media (min-width: 992px)` | A partir da largura de desktop |
| `@media (orientation: landscape)` | Dispositivo em modo paisagem (deitado) |
| `@media (max-width: 600px)` | Até a largura definida (usado em [trabalho2](projetos-guiados/projeto-guiado-1/css/styles.css) para inverter o layout em telas pequenas) |

### Flexbox (introduzido para reorganizar formulários)

| Propriedade | Para que serve |
|---|---|
| `display: flex` | Ativa o modelo flexbox no contêiner |
| `flex-direction` | Direção dos itens: `row` (linha) ou `column` (coluna) |
| `flex-wrap: wrap` | Permite que os itens quebrem para a próxima linha quando não cabem |
| `justify-content` | Alinhamento dos itens no eixo principal (`flex-end`, `center`, etc.) |
| `align-items` | Alinhamento dos itens no eixo transversal (`center`, etc.) |
| `gap` | Espaçamento entre os itens flex/grid |
| `flex: 1` | Faz o item crescer para dividir o espaço disponível igualmente |
| `flex-shrink: 0` | Impede que o item encolha |

### CSS Grid (responsividade "intrínseca")

| Propriedade | Para que serve |
|---|---|
| `display: grid` | Ativa o modelo grid no contêiner |
| `grid-template-columns` | Define as colunas do grid (ex: `1fr 1fr` = duas colunas iguais) |
| `repeat(auto-fit, minmax(200px, 1fr))` | Cria quantas colunas de no mínimo `200px` couberem no espaço disponível — se auto-ajusta sem precisar de media query |

### Outras propriedades desta aula

| Propriedade | Para que serve |
|---|---|
| `transition` | Anima suavemente a mudança de uma propriedade (ex: cor ao passar o mouse) |
| `:hover` | Pseudo-classe aplicada quando o mouse está sobre o elemento |
| `:focus` | Pseudo-classe aplicada quando o campo está selecionado/focado |
| `:active` | Pseudo-classe aplicada durante o clique |
| `:disabled` | Estilo para elementos desabilitados |
| `:last-child` | Seleciona o último filho de um contêiner |
| `[type="text"]` | Seletor de atributo — atinge inputs com aquele `type` específico |
| `content` (em `::before`) | Insere conteúdo textual/gerado via CSS, sem precisar mexer no HTML |
| `accent-color` | Muda a cor padrão de checkboxes/radios do navegador |
| `cursor` | Tipo de cursor do mouse (`pointer`, `not-allowed`, etc.) |
| `box-shadow` | Sombra ao redor do elemento |
| `line-height` | Altura da linha de texto |
| `text-transform: uppercase` | Transforma o texto em maiúsculas via CSS |
| `resize: vertical` | Permite redimensionar um `<textarea>` só na vertical |
| `rgba(0,0,0,0.05)` | Cor com transparência (canal alfa) |

---

## Projeto Guiado 1

Arquivo: [projetos-guiados/projeto-guiado-1/projeto-guiado-1.html](projetos-guiados/projeto-guiado-1/projeto-guiado-1.html)

Reaplica os conceitos de formulário + flexbox + media query da Aula 5 em um novo exercício guiado em sala, consolidando `fieldset`, tipos de `input`, e o padrão mobile-first com `@media (max-width: 600px)`.

---

## Trabalho 1 — HTML Básico

Arquivo: [trabalhos/trabalho1/trabalho1.html](trabalhos/trabalho1/trabalho1.html)

Exercício de fixação da Aula 2: imagem com `alt` descritivo, parágrafo e lista não ordenada — sem uso de CSS.

## Trabalho 2 — Menu, `position` e alinhamento sem `flex`/`grid`

Arquivos: [trabalhos/trabalho2/trabalho2.html](trabalhos/trabalho2/trabalho2.html), [trabalhos/trabalho2/css/styles.css](trabalhos/trabalho2/css/styles.css)

Além das tags/propriedades já vistas, este trabalho mostra como **centralizar e distribuir imagens em grade sem `display: flex` e sem `display: grid`**, aproveitando que `<img>` é um elemento `inline` por padrão:

| Propriedade | Para que serve |
|---|---|
| `text-align: center` no contêiner (`div`) | Centraliza os elementos inline (como `<img>`) dentro dele — a mesma técnica usada em `footer p` |
| `margin: 0 20px` na `<img>` | Cria o espaçamento entre as imagens, simulando uma grade |
| `vertical-align: middle` | Alinha as imagens entre si na mesma linha |
| `overflow: hidden` | Esconde o conteúdo que ultrapassa os limites do elemento (usado no menu sticky) |

Também reforça `position: sticky` (menu do topo) e `position: absolute` (links do menu alinhados à direita).

---

## Resumo — todas as propriedades CSS vistas até agora

`color` · `background-color` · `background-position` · `background-size` · `text-align` · `letter-spacing` · `font-family` · `font-size` · `font-weight` · `font-style` · `text-transform` · `text-decoration` · `line-height` · `border` · `border-radius` · `border-bottom` / `border-top` · `box-sizing` · `padding` · `margin` · `width` · `height` · `max-width` · `min-width` · `opacity` · `display` (`inline-block`, `flex`, `grid`, `none`) · `position` (`static`, `relative`, `absolute`, `fixed`, `sticky`) · `top` / `right` / `bottom` / `left` · `z-index` · `overflow` · `flex-direction` · `flex-wrap` · `flex` · `flex-shrink` · `justify-content` · `align-items` · `gap` · `grid-template-columns` · `transition` · `transform` · `box-shadow` · `cursor` · `accent-color` · `resize` · `vertical-align`

## Resumo — todas as tags HTML vistas até agora

`html` · `head` · `meta` · `title` · `link` · `style` · `body` · `h1`–`h6` · `p` · `hr` · `br` · `ul` · `ol` · `li` · `a` · `img` · `table` · `tr` · `th` · `td` · `div` · `span` · `section` · `header` · `footer` · `main` · `em` · `strong` · `code` · `form` · `label` · `fieldset` · `legend` · `input` · `select` · `option` · `datalist` · `textarea` · `small`

---

*Guia mantido conforme o conteúdo avança em aula. Sinta-se à vontade para consultar os arquivos linkados para ver cada tag/propriedade em contexto real.*
