# Operadores

Agora que conseguimos separar e classificar conjuntos de bits, eles viraram números, string, booleanos, null e undefined. Esta foi nossa primeira grande invenção, e por conta dela podemos nos comunicar com outros, dar nomes, enviar mensagens, atribuir valores, informar se algo é verdadeiro ou falso e informar sobre a existência de algum valor. 

Isto é bom, mas de longe suficiente. Para conseguir extrair a verdadeira utilidade dessa invenção é preciso conseguir operar com eles. Realizar operações matemáticas, criar e modificar textos e realizar testes lógicos são algumas coisas que deveríamos poder fazer. Chegou a hora de inventarmos então, os operadores.

# Matematicos

Os primeiros operadores que criamos foram os matemáticos. Com eles, é possível realizar as operações matemáticas necessárias para a grande maioria das situações. Para isso, desenvolvemos 5 operadores: soma `+`, subtração `-`, multiplicação `*`, divisão `/` e resto `%`.

Para utiliza-los, basta colocar o operador no meio dos dois números que deseja realizar a operação e o resultado será o número a esquerda com o efeito do operador utilizando o número a direita.

``` javascript
10 + 5
// Saida: 10
10 - 5
// Saida: 5
10 * 5
// Saida: 50
10 / 5
// Saida 2
10 % 5
// Saída: 0
```

Também seria muito bom se fosse possível utilizar mais de um operador por linha.

``` javascript
10 + 5 - 5
// Saida: 10
10 + 5 * 5
// Saida: 35
```

Porém, temos que criar algumas regras a cerca de quando tiver mais de um operador por linha. A primeira delas é qual operador deve ser executado primeiro. Aqui temos dois níveis de operadores, no exemplo acima, tanto faz executar a soma ou a subtração primeiro, ambas as formas resultarão no mesmo valor e o mesmo ocorre se fosse multiplicação no lugar da soma e divisão no lugar da subtração, a ordem não mudaria. Porém, quando há multiplicação ou divisão e soma ou subtração na mesma linha, as coisas podem ficar diferentes.

Caso a primeira conta realizada fosse a soma, e posteriormente a multiplicação, no exemplo acima, o resultado seria 75, porém se a multiplicação ocorrer primeiro, o resultado seria 35. Então precisamos definir uma **precedência** acerca de qual operador deve ser executado primeiro, e a decisão é de que os operadores de multiplicação, divisão e resto serão executados primeiro, posteriormente, os de soma e subtração.

Mas temos um problema, existêm situações onde podemos querer realizar uma soma ou uma subtração primeiro e depois realizar outra operação, como a de multiplicação, por exemplo. Precisamos definir uma estratégia para isto... Que tal cercarmos entre `()` o que queremos que seja executado primeiro?

``` javascript
(10 + 5) * 5
// Saída: 75
```

Por último, temos que definir uma regra básica, a sequência em que as operações serão realizadas. Por exemplo, em uma conta com operações de mesmo nível, como `10 + 5 - 5` qual conta é realizada primeiro? Estamos somando 0 de 10 ou subtraindo 5 de 15? Isto é importante não só para contas maiores e complexas, como para definir um comportamento de como as coisas funcionam.

Vamos definir então que a ordem de execução das operações é a mesma da que lemos, da esquerda para a direita, portanto, `10 + 5 - 5` é igual a `(10 + 5) - 5`. Respondendo a pergunta anterior então, estamos subtraindo 5 de 15.