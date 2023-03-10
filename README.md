# Estudo-short-sintax

## Operador ternário

<p>
- A condição seria o que vamos comparar para o if determinar se é falso ou verdadeiro

- No if normal, esta parte fica entre parentes, no ternário não há esta necessidade

- O ponto de interrogação funciona como uma pergunta “é verdadeiro?” e caso for, entre na condição seguinte dele executando aquela lógica

- Os dois pontos (:) representa um ‘se for falso’, e caso seja, executa aquela lógica em seguida dele

Então vamos fazer uma comparação:
</p>

````
// if comum
if(1 == 2) {
    console.log('verdadeiro');
} else {
    console.log('falso');
}
````

````
// if ternário

condição ? valor se verdadeiro : valor se falso

1 == 2 ? console.log('veradeiro') : console.log('falso');

// A mesma comparação escrita das duas formas, perceba que a execução de ‘falso’ será dada nas duas estruturas
// Uma vez que a primeira parte do if ternário representa a condição 1 do if comum, já a segunda parte representa o else
````

## Arrow function

<p>
- São funções anônimas com sintaxe mais enxuta, que facilitam tanto na escrita quanto na leitura do código

- Não utilizamos nem a palavra function e as vezes nem return, tudo está implícito

- Temos a presença de um novo elemento o =>, que faz parte da sintaxe dessas funções

- São sempre funções anônimas, ou seja, elas não tem um nome para serem invocadas em algum lugar do código
</p>

````
//Sintaxe da arrow function`

(parâmetro1, parâmetro2, parâmetroN) => {
    return expressão;
}
````

````
// Chamada de block body, pois há um corpo para a lógica da função e um return explícito ou esta abaixo, que é chamada de concise body, pois o retorno é implicito e não há corpo:

(parâmetro1, parâmetro2, parâmetroN) => expressão;
````

````
//Uma mesma função no ES5 seria assim:

function(parâmetro1, parâmetro2, parâmetroN) {
    return expressão;
}
````

<p>
- Basicamente passamos os parâmetros entre parenteses, e utilizamos o símbolo =>

- Depois deste símbolo há a expressão que será resolvida com os parâmetros escolhidos

- E o resultado da expressão pode ser retornado para uma variável, por exemplo


Vejamos agora alguns exemplos de utilização da arrow function:
</p>

````
// Com vários argumentos

// arrow function vários parâmetros
var x = 10;
var y = 5;

var soma = (num1, num2) => num1 + num2;

console.log(soma(x, y)); // 15
````

````
// Com um argumento

// arrow function um parâmetro
var frase = 'Estou vendo como criar arrow functions!';

var fraseToArray = (frase) => frase.split(' ');

console.log(fraseToArray(frase)); // (6) ["Estou", "vendo", "como", "criar", "arrow", "functions!"]
````

````
// Sem argumento

// arrow function sem parâmetro
var semParam= () => console.log('Teste arrow function');

semParam(); // Teste arrow function
````