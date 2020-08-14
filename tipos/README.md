# Tipos de dados

Imagine que somos deuses em um universo repleto de dígitos, sendo eles 0 ou 1, cada dígito é denominado de bit e estão a disposição para serem utilizados como bem entendermos, além disso, podemos trocar o estado de um bit 0 para 1 e vice versa.  

Para facilitar, decidimos agrupar esses bits de 8 em 8 e damos o nome a este conjunto de byte. Agora temos um universo repleto de bytes, porém, estes ainda não passam de um amontoado de 0s e 1s (00100110) que podem assumir 256 combinações diferentes. É necessário atribuir alguma função a eles, para que possam virar IAs, aplicativos, jogos, robôs... 

Mas antes de atribuir alguma função a eles, é necessário que eles signifiquem algo. Para isso, nos o agrupamos  e demos um nome a cada agrupamento.

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