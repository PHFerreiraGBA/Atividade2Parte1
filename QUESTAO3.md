# Questão 3

## Operações com strings

Nessa questão, manipularemos a string "JavaScript é baseada em ECMA Script" de três formas.

Num primeiro caso, digamos que um aluno quer verificar se a palavra "Script" está nessa string. Como faremos isso? Bem,
o JS tem um método que faz exatamente isso: verifica se uma palavra esta numa string. É o método includes(). Você coloca
essa string numa variável, digamos, "baseadaEm", coloca o resultado do método includes aplicado à variável "baseadaEm"
em uma outra variável, "resultado", e voilà, você tem a resposta para a sua pergunta. Vejamos isso em prática:

```js
let baseadaEm = "JavaScript é baseada em ECMA Script"
let resultado = baseadaEm.includes("Script")
return resultado
```

O que será retornado pode ser true or false. Nesse caso, será true.

No segundo caso, outro aluno quer remover a palavra "Javascript" e criar uma nova string, sem a palavra "Javascript".
Para fazer isso, o aluno irá usar o método 
