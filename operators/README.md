# Operadores

Agora que conseguimos separar e classificar conjuntos de bits, eles viraram números, string, booleanos, null e undefined. Esta foi nossa primeira grande invenção, e por conta dela podemos nos comunicar com outros, dar nomes, enviar mensagens, atribuir valores, informar se algo é verdadeiro ou falso e informar sobre a existência de algum valor. 

Isto é bom, mas de longe suficiente. Para conseguir extrair a verdadeira utilidade dessa invenção é preciso conseguir operar com eles. Realizar operações matemáticas, criar e modificar textos e realizar testes lógicos são algumas coisas que deveríamos poder fazer. Chegou a hora de inventarmos então, os operadores.

# Matematicos

Os primeiros operadores que criamos foram os matemáticos. Com eles, é possível realizar as operações matemáticas necessárias para a grande maioria das situações. Para isso, desenvolvemos 5 operadores: soma `+`, subtração `-`, multiplicação `*`, divisão `/` e resto `%`.

Para utilizá-los, basta colocar o operador no meio dos dois números que deseja realizar a operação e o resultado será o número a esquerda com o efeito do operador utilizando o número a direita.

``` javascript
10 + 5
// Saída: 10
10 - 5
// Saída: 5
10 * 5
// Saída: 50
10 / 5
// Saída 2
10 % 5
// Saída: 0
```

Também seria muito bom se fosse possível utilizar mais de um operador por linha.

``` javascript
10 + 5 - 5
// Saída: 10
10 + 5 * 5
// Saída: 35
```

Porém, temos que criar algumas regras acerca de quando tiver mais de um operador por linha. A primeira delas é qual operador deve ser executado primeiro. Aqui temos dois níveis de operadores, no exemplo acima, tanto faz executar a soma ou a subtração primeiro, ambas as formas resultarão no mesmo valor e o mesmo ocorre se fosse multiplicação no lugar da soma e divisão no lugar da subtração, a ordem não mudaria. Porém, quando há multiplicação ou divisão e soma ou subtração na mesma linha, as coisas podem ficar diferentes.

Caso a primeira conta realizada fosse a soma, e posteriormente a multiplicação, no exemplo acima, o resultado seria 75, porém se a multiplicação ocorrer primeiro, o resultado seria 35. Então precisamos definir uma **precedência** acerca de qual operador deve ser executado primeiro, e a decisão é de que os operadores de multiplicação, divisão e resto serão executados primeiro, posteriormente, os de soma e subtração.

Mas temos um problema, existem situações onde podemos querer realizar uma soma ou uma subtração primeiro e depois realizar outra operação, como a de multiplicação, por exemplo. Precisamos definir uma estratégia para isto... Que tal cercar entre `()` o que queremos que seja executado primeiro?

``` javascript
(10 + 5) * 5
// Saída: 75
```

Por último, temos que definir uma regra básica, a sequência em que as operações serão realizadas. Por exemplo, em uma conta com operações de mesmo nível, como `10 + 5 - 5` qual conta é realizada primeiro? Estamos somando 0 de 10 ou subtraindo 5 de 15? Isto é importante não só para contas maiores e complexas, como para definir um comportamento de como as coisas funcionam.

Vamos definir então que a ordem de execução das operações é a mesma da que lemos, da esquerda para a direita, portanto, `10 + 5 - 5` é igual a `(10 + 5) - 5`. Respondendo a pergunta anterior então, estamos subtraindo 5 de 15.

## Textuais

Os próximos operadores que temos que criar são os de texto. Estes são mais simples, existe basicamente uma operação que possa ser feito entre duas strings, a de concatenação. Isso diz respeito a transformar duas strings diferentes em uma única string.

``` javascript
 "Nanadaime" + " Hokage"
 // Saída: Nanadaime Hokage
```

Agora vamos retomar a discussão a respeito das *template strings*, que são as strings escritas entre com os *backtraces*. Imagine que queiramos escrever operações matemáticas dentro de uma string, como faríamos? Até o momento não temos formas de realizar este procedimento. Além disso, as *template strings* serão muito úteis em várias outras situações que encontraremos no futuro. Mas como elas nos ajudam a escrever expressões matemáticas dentro da string? da seguinte forma.

``` javascript
 `O resultado é ${10 + 5}!`
 // Saída: O resultado é 15!
```

Ou seja, o que estiver dentro de `${}` será computado e seu resultado irá virar uma string. Outra funcionalidade muito boa das *template strings*, é que não é necessários ficar utilizando o `\n`, toda vez que se desejar quebrar uma linha, é possível fazer isso de forma muito mais fluida, como representado a seguir.

``` javascript
 `Tu te tornas eternamente responsável
  por aquilo que cativas!`
  /*
  Saída:
  Tu te tornas eternamente responsável
  por aquilo que cativas!
  */
```

Basta pular uma linha dentro da *template strings* escrevendo, que a quebra de linha já é automaticamente identificada.

## Comparação

Ok, poder realizar operações matemáticas, concatenar strings e até realizar operações matemáticas dentro de strings é muito bom. Dá para fazer inúmeras coisas somente com essas invenções, porém, ainda faltam alguns temas a serem abordados. 

Imagine agora que tenhamos duas expressões matemáticas complicadas, que não sabemos a resposta, e queremos saber se uma é maior, menor ou igual a outra, ou até mesmo se elas são diferentes entre si. Ou seja, caso eu queira comparar dois valores, como eu posso fazer? Hmm, está na hora então de inventar os operadores de comparação.

Estes valores estão diretamente ligados com o tipo booleano, e é aqui que eles brilham. Cada comparador ira testar uma condição entre as duas operações matemáticas e retornara `true` caso seja verdadeiro e  `false` caso seja falso, como visto a seguir. E as operadores são `<` menor que, `>` maior que, `!=` diferente, `==` igual e `===`;

``` javascript
 8 < 7
 // Saída: false
 8 > 7
 // Saída: true
 8 != 7
 // Saída: true
 8 == 7
 // Saída: false
 8 === 7 
 // Saída: false
```

Seria interessante se também poderiamos usar estes operadores para strings, assim poderiamos realizar comparações entre string para qualquer que seja o fim. Só que aqui a comparação ocorre através de uma lógica diferente, pois é um tipo diferente.

> Para entender como funciona, você tem que lembrar que cada caractere tem um valor descrito em um [dicionário](pt.wikipedia.org/wiki/ASCII), que oferece uma combinação de bits para cada um deles. Essa combinação também pode ser interpretada como um número, oferecendo um valor para cada digito. 

A lógica é a seguinte, quando usamos os operadores `<`ou `>`, irá ser checado o primeiro caractere da string, a depender do valor de ambos, a string como um todo será maior ou menor que a outra, idependente de quantos caracteres tenha a seguir. Caso os valores sejam iguais, será checado o segundo dígito, e assim por diante.

``` javascript
'abc' < 'z'
// Saída: true
'abc' > 'z'
// Saída: false
```

Quado se realizar uma comparação com os operadores `==`, `===` ou `!=`. Será checado se todos os dígitos são iguais, caso sejam, as strings são iguais, caso contrário, não. Assim, podemos conferir a seguir, que definitivamente pera e maçã não são a mesma coisa.

``` javascript
'pêra' == 'maça'
// Saída: false
'pêra' === 'maça'
// Saída: false
'pêra' != 'maça'
// Saída: true
```

A esta altura, talvez você esteja se perguntando, *mas qual a diferença entre o `==` e o `===`?* Bem, esta é uma das exentricidades da nossa criação. Exploraremos mais sobre este tópico no próximo capítulo, mas já adiantando, observe o seguinte cenário.

``` javascript
'42' == 42
// Saída: true
```

Hmm... Ok, isto não deveria ocorrer, pois, além ambos serem de tipos completamente diferentes e sequer ser possível realizar esta comparação, o dígito 4 ou 2 em uma string tem valores numéricos diferentes de 42. Como eu faço então para poder realizar uma checagem mais precisa e livre deste tipo de erro? Utilizando justamente o `===`. Ele além checa primeiramente o tipo, se forem diferentes, a comparação já retorna `false` automaticamente.

``` javascript
'42' === 42
// Saída: false
```

Outro detalhe interessante a cerca de comparações, é que o único valor que não é igual a ele mesmo é o `NaN`. Isto ocorre por que ele é o resultado de uma expressão matemática sem sentido e que não existe resposta na atualidade, como `0/0`. E aparentemente, uma coisa estranha é diferente de outra coisa estranha, pois ambas são estranhas e não há conhecimento disponível para sequer conseguir compara-las.

``` javascript
NaN == NaN
// Saída: false
```