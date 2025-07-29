# Capítulo 2: Entendendo o HTML e a Evolução para o HTML5

## O que é HTML?

HTML, sigla para **HyperText Markup Language**, é a linguagem padrão usada para criar páginas da web.  
Ela estrutura o conteúdo por meio de "marcadores" (tags), que definem elementos como títulos, parágrafos, imagens, links, listas e muito mais.

Por exemplo, um título é definido com `<h1>` e um parágrafo com `<p>`.  
O HTML não é uma linguagem de programação — ele apenas organiza e apresenta informações de forma compreensível para os navegadores.

## A evolução até o HTML5

Desde sua criação nos anos 1990, o HTML passou por várias versões.  
Até meados dos anos 2000, a versão mais usada era o **HTML4**, lançado em 1997. Essa versão focava mais na estrutura do conteúdo, mas deixava a interatividade e a apresentação para linguagens externas como JavaScript e CSS.

Com o crescimento de vídeos, jogos, aplicativos e o uso da web em celulares, tornou-se evidente a necessidade de uma linguagem mais moderna. Foi assim que surgiu o **HTML5**.

## O que é HTML5?

O **HTML5** é a quinta e mais recente versão da linguagem HTML.  
Ele foi criado com os seguintes objetivos principais:

- Tornar o código mais semântico (com tags que explicam o conteúdo)
- Remover a dependência de plugins externos (como Flash)
- Melhorar a acessibilidade e SEO
- Suportar dispositivos móveis e aplicações ricas (como jogos e vídeos)
- Tornar a web mais interativa e poderosa

O HTML5 não é apenas um conjunto de novas tags, mas também um conjunto de **novas APIs e funcionalidades** que ampliam o que é possível fazer com uma página da web.

## Novidades do HTML5 em relação ao HTML4

O HTML5 trouxe diversas melhorias e inovações em comparação ao HTML4. Abaixo, destacamos as principais:

### 1. Tags semânticas

O HTML5 introduziu novas tags que descrevem o papel de cada parte da página.  
Antes, usávamos `<div>` para quase tudo. Agora, temos:

- `<header>` — Cabeçalho da página ou seção  
- `<footer>` — Rodapé  
- `<nav>` — Menu de navegação  
- `<section>` — Seção temática  
- `<article>` — Conteúdo independente (ex: post, notícia)  
- `<aside>` — Conteúdo complementar  
- `<main>` — Conteúdo principal da página  

Essas tags melhoram a clareza do código, o SEO e a acessibilidade.

### 2. Suporte nativo a mídia (áudio e vídeo)

O HTML5 permite incluir **áudio e vídeo diretamente no HTML**, sem necessidade de plugins como Flash:

```html
<video src="video.mp4" controls></video>
<audio src="audio.mp3" controls></audio>
```

### 3. Novos tipos de input

Formulários agora suportam novos tipos de entrada, melhorando a validação e a experiência do usuário:

* `email`
* `url`
* `tel`
* `date`, `time`, `datetime-local`
* `range`, `color`
* `search`

Exemplo:

```html
<input type="email" required>
<input type="range" min="0" max="100">
```

### 4. Elemento `<canvas>` para gráficos e jogos

O `<canvas>` permite desenhar gráficos 2D via JavaScript, sendo muito usado para jogos, visualizações e editores de imagem.

```html
<canvas id="meuCanvas" width="300" height="150"></canvas>
```

### 5. Armazenamento local

O HTML5 introduziu formas de **armazenar dados no navegador**, sem usar cookies:

* `localStorage` — dados persistem mesmo após fechar o navegador
* `sessionStorage` — dados válidos apenas durante a sessão atual

Exemplo com JavaScript:

```javascript
localStorage.setItem('nome', 'João');
let nome = localStorage.getItem('nome');
```

### 6. Novas APIs

O HTML5 trouxe diversas APIs poderosas que permitem criar aplicações mais ricas e interativas:

* **Geolocation API** — Acessa localização do usuário
* **Drag and Drop API** — Arrastar e soltar elementos
* **Web Storage API** — Armazenamento local
* **WebSockets API** — Comunicação em tempo real
* **Web Workers API** — Execução de scripts em segundo plano

### 7. Compatibilidade com dispositivos móveis

O HTML5 foi projetado com foco em **responsividade e adaptação**, facilitando o desenvolvimento para smartphones e tablets.

### 8. Fim de elementos obsoletos

O HTML5 removeu ou desaconselhou o uso de tags que misturam conteúdo com apresentação, como:

* `<center>`
* `<font>`
* `<big>`, `<small>`
* `<strike>`, `<u>`

Esses estilos devem ser aplicados via CSS.

---

## Conclusão

O HTML5 representa um grande avanço na forma como desenvolvemos para a web.
Ele é mais **semântico**, **interativo** e **moderno**, refletindo as necessidades da web atual, onde o conteúdo deve ser acessível, adaptável e rico em funcionalidades — tudo isso sem depender de tecnologias externas.

Com o HTML5, a web se torna uma verdadeira **plataforma de aplicações**, abrindo caminho para experiências cada vez mais completas e acessíveis diretamente do navegador.
