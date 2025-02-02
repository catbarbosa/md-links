# Markdown Links

## Índice

* [1. Sobre](#1-sobre)
* [2. Pré-requisitos](#2-pré-requisitos)
* [3. Como instalar](#3-como-instalar)
* [4. Como utilizar](#4-como-utilizar)
* [5. Ferramentas utilizadas](#5-ferramestas-utilizadas)

***

## 1. Sobre

Uma biblioteca em JavaScript Vanilla, com o objetivo de extrai links de url em um arquivo _markdown_. O modo de utiliza-la detalhamente está sendo descrito abaixo, mas poderá ser executada diretamente pelo terminal ou importado com `require` no seu código.
O retorno da função é uma `Promise` que devolve um `Array` e `Objects` contendo as seguintes informações:

`href`: URL encontrada.

`text`: Texto dentro do markdown.

`status`: Status da requisição.

## 2. Pré-requisitos

Para utilizar a biblioteca é necessário ter instalado:

* _Node.js_


### Ubuntu ou macOS

```sh

 sudo apt-get install nodejs

```

ou clique [aqui](https://nodejs.org/en/download/) para fazer o download.

Para maiores informações segue a [Documentação do Node.js](https://nodejs.org/pt-br/about/).

## 3. Como instalar

Para instalar a biblioteca utilize o seguinte comando no terminal:

```sh
$ npm install -g catbarbosa/md-links
```

## 4. Como utilizar

A partir do terminal:

```sh

$ md-links <endereço-do-arquivo>

```

Por exemplo:

```sh

$ md-links ./documents/example.md
http://exemplo.com - Link de exemplo
http://google.com/ - Google

```

Caso nenhum link seja encontrado:

```sh

$ md-links ./documents/example.md
No matches found

```

Outro exemplo:

```js
const links = require("md-links");


mdLinks("./example.md")
  .then(links => {
    // => [{ href, text }]
  })
  .catch(console.error);

```

## 5. Ferramentas utilizadas

Para desenvolver esta biblioteca, foram utilizadas as seguintes ferramentas:

* JavaScript
* GIT
* GitHub
* Node js
* Jest
* Visual Studio Code
* Trello

***

```js
const mdLinks = require("md-links");

mdLinks("./example.md")
  .then(links => {
    // => [{ href, text }]
  })
  .catch(console.error);
  ```