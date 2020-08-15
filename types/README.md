# Tipos de dados
 
Imagine que somos deuses em um universo repleto de minúsculas partículas. Estas partículas têm uma particularidade muito interessante, elas conseguem assumir dois estados. Em um dos estados ela está aparentemente inativa, o chamaremos de 0. Em seu outro estado ela está ativa, o chamaremos de 1. Para facilitar, vamos dar o nome desta partícula de bit. Os bits estão a disposição para serem utilizados como bem entendermos, além disso, podemos trocar o estado de um bit 0 para 1 e vice versa. 
 
Para facilitar mais, decidimos agrupar esses bits de 8 em 8 e damos o nome a este conjunto de byte. Agora temos um universo repleto de bytes, porém, estes ainda não passam de um amontoado de 0s e 1s (00100110) que podem assumir 256 combinações diferentes. É necessário atribuir alguma função a eles, para que possam virar o que quer que imaginemos.
 
Mas antes de atribuir alguma função a eles, é necessário que eles signifiquem algo. Para isso, nós o agrupamos  e demos um nome a cada agrupamento.
 
## Números
 
Os números são agrupamentos de 8 bytes, ou 64 bits, onde seu 1° bit informa se o número é negativo ou positivo e os demais 63 bits são usandos para calcular o valor do número ([saiba mais](https://en.wikipedia.org/wiki/Double-precision_floating-point_format)). Os números podem seguir o seguinte formato:
 
``` JavaScript
 42       // Inteiro positivo
 3.14     // Número de ponto flutuante
-42       // Números negativos
 14e9     // Notação científica
 Infinity // Representação de infinito
-Infinity // Representação de infinito negativo
 NaN      // "Not a Number" Representação de valores não numéricos
```

## Strings

As strings existem para podermos nos comunicar com outros através de textos. Cada parte de uma string (ou cada caractere) é um agrupamento de 16 bits ou 2 bytes, podendo assumir 2 elevado a 16 combinações diferentes. Cada combinação representa um elemento em uma espécie de dicionário criado, por outros de nós, chamado [unicode](https://home.unicode.org/). Acabou que eles se empolgaram um pouco e existem hoje mais elementos do que combinações que podemos representar utilizando 2 bytes. As strings seguem o seguinte formato:

``` JavaScript
 "Olá mundo!" // Dentro de aspas duplas
 'Olá mundo'  // Dentro de aspas simples
 `Olá mundo`  // Backticks
```

É possível utilizar alguns caracteres especiais dentro das string, por exemplo, o `\n` é utilizado para quebrar a linha.

``` JavaScript
 "Olá\nmundo!" // Caractere especial
/*
 Saída:
 Olá
 Mundo!
*/
```

Nestas situações, o caractere `\` indica que o caractere a seguir é especial e torna possível que algo ocorra. Mas o contrário também é possível, caso  você use o `\` e o próximo caractere seja especial, ele perde seu efeito e se torna um caractere normal. O próprio `\` se inclui nisto.

``` JavaScript
 "Olá\"\\n\"mundo!" // Cancelando caractere especial
/* 
 Saída: 
 Olá "\n" mundo"
*/
```

String escritas com aspas simples ou duplas são basicamente a mesma coisa, a unica diferença é que dentro das aspas simples você pode usar livremente as aspas duplas e vice-versa.

``` JavaScript
 "''" // Aspas simples dentro das duplas
 '""' // Aspas duplsa dentro das simples
 /*
  Saída:
  ''
  ""
 */
```

Já as strings escritas com `` são chamadas de *template strings*, pois dentro delas é possível fazer algumas coisas interessantes, mas voltaremos a isso mais tarde.

## Booleanos

Booleanos são nada mais que um único byte responsável por armazenar dois valores, verdadeiro e falso.

``` JavaScript
 true  // Verdadeiro
 false // Falso
```

## Null e undefined

É necessário algum valor para representar quando algo está vazio. Então criamos dois tipos para isso, null e undefined. Existema algumas diferenças entre esses dois valores, mas por hora podemos dizer o seguinte. Ao olhar para um punhado de bytes e não conseguir identificar nenhum estrutura, ou seja, ele não é um número, string ou booleano, então ele é undefined, pois seu tipo e valor estão indefinidos. O null, por outro lado, é um tipo, e seu valor é null, ou seja, é um conjunto de bytes estruturados de forma a nos informar que não há nada ali, seu valor não é indefinido pois nós sabemos o que tem ali, e não há nada.

As diferenças entre null e undefined e sua utilização é mais entendivel quando visto na prática, e nós o faremos, em exemplos práticos no futuro.