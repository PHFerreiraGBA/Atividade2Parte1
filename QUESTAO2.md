# Questão 2

## Qual a diferença entre JSON.stringify() e JSON.parse()?

De acordo com as documentações da Mozilla ([MDN Web Docs](https://developer.mozilla.org/pt-BR/)), o método JSON.stringify() do JavaScript
converte um objeto JS em um texto JSON. Por exemplo, suponhamos que você armazene um objeto numa variável de nome "pessoa".

```js
let pessoa = {
  nome: "Pedro",
  dataNasc: "2007-02-18",
  profissao: "Estudante"
};
```

Ao criarmos uma nova variável, digamos, "resultado", que guarde o resultado do método stringify, com a variável "pessoa" sendo passada
como argumento...

```js
let resultado = JSON.stringify(pessoa)
```

...a variável "resultado" armazenará o objeto contido na variável "pessoa" como um texto JSON:

```
'{"nome":"Pedro","dataNasc":"2007-02-18","profissao":"Estudante"}'
```

Já o método JSON.parse() pega esses textos JSON e converte de volta a um objeto JS. Outro exemplo: digamos que na outra ponta do código,
por alguma razão, você precise converter a variável "resultado" de volta para objeto. Você pode fazer usando o JSON.parse:

```js
let reconversao = JSON.parse(resultado)
```

Agora, a nova variável "reconversao" contém o mesmo objeto que a variável "pessoa", convertido de um texto JSON desse objeto.

Em resumo, JSON.stringify() converte de objeto JS para texto JSON, enquanto JSON.parse() faz o processo contrário, converte um texto JSON
em um objeto JS.
