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
