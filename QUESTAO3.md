# Questão 3

## Operações com strings

Nessa questão, manipularemos a string "JavaScript é baseada em ECMA Script" de três formas.

Num primeiro caso, digamos que um aluno quer verificar se a palavra "Script" está nessa string. Como faremos isso? Bem,
o JS tem um método que faz exatamente isso: verifica se uma palavra esta numa string. É o método includes(). Você coloca
essa string numa variável, digamos, "baseadaEm", coloca o resultado do método includes aplicado à variável "baseadaEm"
em uma outra variável, "resultado", e voilà, você tem a resposta para a sua pergunta. Vejamos isso em prática:

```js
let baseadaEm = "JavaScript é baseada em ECMA Script";
let resultado = baseadaEm.includes("Script");
return resultado;
```

O que será retornado pode ser true or false. Nesse caso, será true.

No segundo caso, outro aluno quer remover a palavra "Javascript" e criar uma nova string, sem a palavra "Javascript".
Há três métodos que fazem isso: slice(), substring() e substr().

No método slice(), você atribui dois argumentos: o índice que você quer que inicie o recorte e o índice de final do
recorte. Assim como numa range, o índice final não é inclusivo, é aberto, matematicamente falando.

```js
let baseadaEm = "JavaScript é baseada em ECMA Script";
let resultado = baseadaEm.slice(11, 35);
//"é baseada em ECMA Script"
return resultado;
```

Se você não passar o segundo argumento para o método slice(), ele vai considerar o último indice da string como o índice
final do recorte.

O método substring(), os argumentos funcionam da mesma forma que no split(), com uma diferença: Se você passar os 
argumentosao contrário, vai funcionar de qualquer jeito no método substring(), ele sempre pega o número maior como índice
final do recorte. Se você fizer isso no método slice(), tudo o que você vai ter é uma string vazia como resposta.

```js
let baseadaEm = "JavaScript é baseada em ECMA Script";

let resultado1 = baseadaEm.substring(11, 35);
//"é baseada em ECMA Script"

let resultado2 = baseadaEm.substring(35, 11);
//"é baseada em ECMA Script"

let resultado3 = baseadaEm.slice(35, 11);
//""

return resultado1;
```

Por último, o método substr() funciona de uma forma bem diferente dos outros métodos. Pegue o índice inicial do recorte.
Esse é o primeiro parâmetro. Até aí, tudo bem. Porém, o segundo parâmetro é a quantidade de caracteres que você quer
que o recorte tenha. Vejamos o código:

```js
let baseadaEm = "JavaScript é baseada em ECMA Script";
let resultado = baseadaEm.substr(11, 24);
//"é baseada em ECMA Script"
return resultado;
```

No terceiro e último caso, um terceiro aluno quer trocar a palavra "baseada" pela expressão "tem origem". Para isso,
precisamos do método replace(). Ele troca a primeira instância de um trecho numa string por outro trecho passado por
você. Vejamos o exemplo:

```js
let baseadaEm = "JavaScript é baseada em ECMA Script";
let temOrigemEm = baseadaEm.replace("baseada", "tem origem");
return temOrigemEm;
```

Do jeito que foi escrito acima, o texto modificado está na variável "temOrigemEm".
