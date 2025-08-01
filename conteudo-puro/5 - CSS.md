# Capítulo 5: CSS - Folhas de Estilo em Cascata

## Introdução

O CSS (Cascading Style Sheets) é uma linguagem de estilo utilizada para definir a apresentação de documentos HTML. Ele permite controlar o layout, as cores, as fontes, o espaçamento, entre outras características visuais dos elementos de uma página web.

---

## Formas de Aplicar CSS

Existem **três formas principais** de aplicar CSS a um documento HTML:

### 1. CSS Inline

Aplica-se diretamente no atributo `style` de um elemento HTML.

```html
<p style="color: red;">Texto em vermelho</p>
```

### 2. CSS Incorporado (Internal)

Define-se dentro da tag `<style>` no `<head>` do documento HTML.

```html
<head>
  <style>
    p {
      color: blue;
    }
  </style>
</head>
```

### 3. CSS Externo (External)

Define-se em um arquivo `.css` separado, que é importado com a tag `<link>`:

```html
<link rel="stylesheet" href="estilo.css">
```

Essa é a forma mais recomendada para projetos maiores e reutilização de estilos.

---

## Conceito de Herança no CSS

O CSS trabalha com **herança**, o que significa que algumas propriedades aplicadas a um elemento pai podem ser herdadas pelos filhos. Isso reduz a repetição de código e permite aplicar estilos de forma mais eficiente.

**Exemplo:**

```css
body {
  font-family: Arial;
}
```

Todos os textos dentro do `body` herdarão a fonte Arial, a menos que seja sobrescrito localmente.

---

## Seletores CSS

### 1. Seletor de Tipo

Seleciona elementos HTML pelo nome da tag.

```css
p {
  color: green;
}
```

### 2. Seletor de Classe

Seleciona elementos com a classe especificada. Usa `.` antes do nome da classe.

```css
.caixa {
  border: 1px solid black;
}
```

> **Nota:** Um mesmo elemento pode ter **múltiplas classes**.

```html
<div class="card destaque sombra"></div>
```

### 3. Seletor de ID

Seleciona um único elemento com o ID especificado. Usa `#`.

```css
#cabecalho {
  background-color: gray;
}
```

> **Dica de boas práticas:** Use nomes **semânticos** nas classes e IDs, que representem o **propósito** do elemento, e não a sua aparência. Por exemplo, prefira `.menu-principal` em vez de `.menu-vermelho`, pois isso facilita mudanças no estilo sem quebrar a semântica do código.

---

## Agrupamento de Seletores

Permite aplicar o mesmo estilo a vários seletores de uma vez, separados por vírgula.

```css
h1, h2, h3 {
  font-weight: bold;
}
```

---

## Seletores Hierárquicos

### 1. Seletores Descendentes

Aplicam estilos a elementos que estão **em qualquer nível abaixo** de outro.

```css
div p {
  color: purple;
}
```

O seletor acima afeta todos os `<p>` que estão dentro de um `<div>`, mesmo que não sejam filhos diretos.

### 2. Seletores de Filhos Diretos

Afetam apenas elementos que são **filhos imediatos** do elemento pai.

```css
ul > li {
  list-style-type: square;
}
```

---

## Comentários em CSS

Comentários são úteis para explicar trechos do código e são ignorados pelo navegador.

```css
/* Este é um comentário em CSS */
```

---

## Cores no CSS

### 1. Cor de Fundo

```css
body {
  background-color: #f0f0f0;
}
```

### 2. Cor do Texto

```css
p {
  color: rgb(100, 100, 100);
}
```

### 3. Notações de Cores

* **RGB:** `rgb(255, 0, 0)`
* **Hexadecimal:** `#ff0000`
* **Hexadecimal Abreviada:** `#f00` (equivalente a `#ff0000`)

### 4. Ferramentas para Descobrir Códigos de Cor

Ferramentas úceis:

* [Coolors](https://coolors.co/)
* [ColorHexa](https://www.colorhexa.com/)
* Ferramenta de seletor de cores do **Chrome DevTools**

---

## Formatação de Texto

### Propriedades mais comuns:

| Propriedade       | Descrição                                     |
| ----------------- | --------------------------------------------- |
| `color`           | Define a cor do texto                         |
| `font-size`       | Define o tamanho da fonte                     |
| `font-family`     | Define a fonte principal e alternativas       |
| `font-style`      | Define o estilo (normal, italic, etc.)        |
| `font-weight`     | Define o peso da fonte (normal, bold, etc.)   |
| `font`            | Atalho para definir várias propriedades       |
| `text-decoration` | Define sublinhado, tachado, etc.              |
| `text-align`      | Alinha o texto (left, center, right, justify) |

### Exemplo:

```css
h1 {
  font-family: Arial, sans-serif;
  font-size: 32px;
  font-weight: bold;
  text-align: center;
}
```

### Formatação em Relação ao Pai

Tamanhos relativos, como `%` ou `em`, são interpretados com base no elemento pai:

```css
p {
  font-size: 1.2em; /* 1.2x o tamanho da fonte do elemento pai */
}
```

---

## Inspeção de Elementos no Chrome

O navegador Google Chrome oferece uma ferramenta chamada **DevTools**, que permite:

* Visualizar e modificar o CSS aplicado a qualquer elemento;
* Ver a hierarquia dos elementos no DOM;
* Testar estilos em tempo real;
* Verificar a cascata e herança dos estilos.

Para acessar: **clique com o botão direito → Inspecionar** ou use `Ctrl + Shift + I`.

---

## Conclusão

O CSS é essencial para tornar páginas HTML visualmente atrativas e organizadas. Com o domínio de seletores, cores, formatação e boas práticas semânticas, é possível criar experiências visuais responsivas e acessíveis para os usuários.

---

## Referências

* W3C. [Cascading Style Sheets (CSS)](https://www.w3.org/Style/CSS/)
* MDN Web Docs. [CSS: Cascading Style Sheets](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
* Google Chrome Developers. [Chrome DevTools](https://developer.chrome.com/docs/devtools/)
* CSS Tricks. [A Complete Guide to CSS Selectors](https://css-tricks.com/almanac/selectors/)
* Livro: "HTML and CSS: Design and Build Websites" - Jon Duckett
