# Capítulo 3: Encoding de Caracteres e seu Papel no HTML

## O que é encoding (codificação de caracteres)?

**Encoding**, ou codificação de caracteres, é o processo de converter caracteres (como letras, números e símbolos) em bytes que podem ser armazenados, transmitidos e interpretados por computadores.

Como computadores só entendem números, cada caractere precisa ser representado por um número binário. O encoding define **como associar esses números a caracteres específicos**.

### Exemplos de codificações:

* **ASCII**: Codificação básica com 128 caracteres, usada nos EUA.
* **ISO-8859-1 (Latin-1)**: Ampliação do ASCII com acentos e caracteres europeus.
* **UTF-8**: Codificação moderna e padrão atual da web. Representa qualquer caractere Unicode de forma eficiente.
* **UTF-16**: Mais usada em sistemas como Windows e linguagens como Java, mas menos comum na web.

## Por que encoding é importante no HTML?

Quando uma página HTML é exibida, o navegador precisa saber **qual codificação foi usada para interpretar corretamente os caracteres**. Sem isso, você verá símbolos estranhos no lugar de letras acentuadas, cedilha, emojis etc.

Exemplo de problema:

```html
<!-- Sem encoding ou encoding errado -->
Ol&#225; Mundo! <!-- esperado: Olá Mundo -->
```

### Como informar a codificação no HTML

A codificação usada deve ser especificada no `<head>` da página, com a meta tag `charset`. A forma mais comum e recomendada hoje é:

```html
<meta charset="UTF-8">
```

Essa linha informa ao navegador que a codificação da página é **UTF-8**, compatível com praticamente todos os idiomas e símbolos modernos.

## Por que usar UTF-8?

* É compatível com o padrão **Unicode**, que representa quase todos os idiomas do mundo.
* Suporta emojis, símbolos matemáticos, caracteres especiais e mais.
* É eficiente: letras comuns (ex: A-Z) ocupam apenas 1 byte.
* É o encoding padrão do HTML5.
* Evita problemas de compatibilidade entre sistemas, navegadores e editores de texto.

## Exemplo prático completo

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Exemplo de Encoding</title>
</head>
<body>
  <p>Olá, mundo! Você está aprendendo sobre encoding de caracteres.</p>
</body>
</html>
```

## Encoding em arquivos HTML

Além de declarar o encoding no HTML, é importante que o **arquivo em si seja salvo com o mesmo encoding**. Isso depende do editor de texto ou IDE que você usa.

Por exemplo, ao usar o VS Code, você pode definir o encoding do arquivo para UTF-8 clicando no canto inferior direito onde aparece "UTF-8" ou usando a opção "Salvar com encoding...".

## Encoding em URLs e formulários

Encoding também aparece em outros contextos da web:

* **URLs**: caracteres especiais são codificados (ex: espaço = `%20`, acento = `%C3%A1`)
* **Formulários**: o navegador precisa saber qual encoding usar para enviar os dados corretamente

Exemplo de URL com encoding:

```
https://exemplo.com/pesquisa?q=ol%C3%A1+amigo
```

## Conclusão

Entender encoding é essencial para criar páginas web confiáveis, que funcionam corretamente em qualquer idioma e sistema. Ao adotar **UTF-8** como padrão e configurá-lo corretamente tanto no HTML quanto no editor, você evita problemas comuns com caracteres corrompidos, símbolos estranhos ou falhas em formulários.

Encoding não é só um detalhe técnico — é o que garante que **as palavras cheguem ao leitor como foram escritas**.
