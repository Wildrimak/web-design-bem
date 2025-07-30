# Capítulo 3: Semântica e Estrutura no HTML

## HTML como linguagem semântica

O HTML não serve apenas para exibir conteúdo na tela. Ele também é um meio de **transmitir significado** para os navegadores, leitores de tela e, principalmente, **motores de busca** (como o Google). Essa capacidade de descrever o conteúdo através das tags é chamada de **semântica**.

Uma estrutura HTML bem semântica ajuda a:

- Melhorar o SEO (Search Engine Optimization)
- Tornar o conteúdo acessível para leitores de tela
- Facilitar a manutenção e leitura do código

## Títulos e hierarquia semântica

Os elementos de título, de `<h1>` a `<h6>`, têm um papel importante na definição da **hierarquia do conteúdo**. Eles não definem apenas **tamanho de fonte**, mas sim **nível de importância**:

- `<h1>`: título principal da página ou seção
- `<h2>`: subtítulo direto de um `<h1>`
- ...
- `<h6>`: o menor nível hierárquico

Exemplo:

```html
<h1>Documentação do Projeto</h1>
  <h2>Instalação</h2>
  <h2>Uso</h2>
    <h3>Modo Interativo</h3>
    <h3>Modo Automático</h3>
```

Essa estrutura é essencial para que mecanismos de busca entendam o que é mais relevante em uma página.

## Parágrafos e quebras de linha

O elemento `<p>` representa um **parágrafo de texto**. Diferente de linguagens como Markdown ou editores de texto, **quebras de linha no código-fonte HTML não são exibidas como quebras visuais no navegador**.

Exemplo:

```html
<p>Este é um parágrafo.
Mesmo que esteja quebrado aqui,
o navegador vai exibir tudo como um único bloco.</p>
```

### Quebra manual de linha com `<br>`

Se for necessário forçar uma quebra de linha dentro de um parágrafo ou outro elemento, usa-se a tag `<br>`:

```html
<p>Nome: João<br>Idade: 30 anos</p>
```

Entretanto, recomenda-se usar **CSS para controlar a aparência e espaçamento**, em vez de inserir múltiplos `<br>` para formatar.

## Comentários no HTML

Comentários servem para inserir **anotações no código que não serão exibidas na página**. Úteis para documentação ou explicações:

```html
<!-- Este é um comentário em HTML -->
```

## Ênfase e significado textual

HTML também fornece elementos para dar **ênfase ou destacar significados** específicos dentro do texto:

- `<em>`: ênfase (lida com entonação em leitores de tela)
- `<strong>`: importância (geralmente aparece em negrito)
- `<mark>`: destaque contextual (como se fosse marca-texto)

Exemplo:

```html
<p>Este produto está <strong>em promoção</strong> apenas hoje!</p>
<p>Gostaria de <em>ressaltar</em> a importância deste ponto.</p>
<p>Use o comando <mark>npm start</mark> para iniciar.</p>
```

## Imagens no HTML

O elemento `<img>` é usado para **inserir imagens** em uma página:

```html
<img src="imagens/logo.png" alt="Logo da empresa" width="200" height="100">
```

### Atributos importantes:

- `src`: caminho da imagem (relativo ou absoluto)
- `alt`: texto alternativo (importante para SEO e acessibilidade)
- `width` e `height`: dimensões da imagem (em pixels ou %)

### Organização e caminhos

Boas práticas para organizar imagens em um projeto:

```
projeto/
├── index.html
├── imagens/
│   ├── logo.png
│   └── banner.jpg
```

Usar caminhos relativos como `imagens/logo.png` facilita a portabilidade do projeto.

### Suporte dos navegadores

Todos os navegadores modernos suportam os formatos mais comuns:

- **JPEG/JPG**: fotos, compressão com perdas
- **PNG**: transparência, compressão sem perdas
- **GIF**: animações simples
- **WEBP/AVIF**: formatos modernos, mais eficientes (requerem fallback em navegadores antigos)

## Links e navegação

Para criar links, usamos a tag `<a>` com o atributo `href`:

```html
<a href="https://exemplo.com">Visite nosso site</a>
```

### Atributo `target`

Controla como o link será aberto:

- `_self`: abre na mesma aba (padrão)
- `_blank`: abre em nova aba

```html
<a href="https://exemplo.com" target="_blank">Abrir em nova aba</a>
```

## Estrutura de seções e divisões

O HTML oferece várias tags para estruturar visualmente e semanticamente a página:

- `<header>`: cabeçalho da página ou seção
- `<footer>`: rodapé
- `<article>`: conteúdo independente (como uma notícia)
- `<section>`: bloco de conteúdo temático
- `<aside>`: conteúdo lateral, como uma barra de navegação
- `<div>`: contêiner genérico (sem significado semântico)

### Uso de `id`

Para estilização com CSS ou interações com JavaScript, podemos usar o atributo `id`:

```html
<section id="sobre">
  <h2>Sobre o Projeto</h2>
</section>
```

Cada `id` deve ser único por página.

## Conclusão

A semântica no HTML vai muito além da aparência. Ela estrutura o conteúdo de forma que máquinas e humanos possam entendê-lo claramente. Com o uso adequado de títulos, parágrafos, marcações textuais e elementos de estrutura, você cria páginas mais acessíveis, fáceis de manter e melhor ranqueadas pelos mecanismos de busca.

