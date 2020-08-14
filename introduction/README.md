# Introdução
 
Esta seção descreve rapidamente o que é JavaScript, como é montada a estrutura do repositório e quais as formas de estar rodando JavaScript no seu computador. Se você é iniciante, comece por aqui, esta é uma seção importante :wink:
 
## O que é JavaScript
 
Após a invenção do [World Wide Web](https://webfoundation.org/about/vision/history-of-the-web/?gclid=Cj0KCQjw7Nj5BRCZARIsABwxDKLr6aDFzY-jvRgXLV3VegeCy5Q4_CO9RnAcBgxrrQziAxEyOyxZbbAaAsVMEALw_wcB) e sua popularização, a internet começou a ser utilizada por vários tipos de pessoas, com as mais diversas intenções. Porém, a internet ainda era um lugar estático, as páginas eram feitas somente com [HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML) e [CSS](https://developer.mozilla.org/pt-BR/docs/Web/CSS), não existia interação.
 
Foi neste contexto que, em 1995, surgiu JavaScript, para trazer interação e tornar as páginas dinâmicas. Ela é uma linguagem de programação interpretada, de script e de alto nível. Possui tipagem dinâmica fraca e é multi paradigma (orientado a objetos, estruturada, funcional e  protótipos). Foi implementado inicialmente para funcionar nos navegadores, sendo atualmente a principal linguagem front-end, mas também vêm dominado outras áreas ao longo da última década, como o lado do servidor com [Node.js](https://nodejs.org/en/) e desenvolvimento mobile com [ReactNative](https://reactnative.dev/).
 
Por mais que faça menção ao [Java](https://www.java.com/pt_BR/about/whatis_java.jsp?bucket_value=desktop-chrome84-linux&in_query=no) em seu nome, isto se trata somente de uma estratégia de marketing, pois Java era muito famoso na época, mas as duas linguagens não tem relação. Por outro lado, JavaScript tem sido regulamentada pela [Ecma Internacional](https://www.ecma-international.org/), originando uma nova linguagem denominada [ECMAScript](https://www.ecma-international.org/ecma-262/7.0/#). Porém, na prática, ECMAScript e JavaScript são a mesma linguagem, com nomes diferentes por motivos históricos, então se você encontrar por alguém falando sobre ECMAScript 2016, ECMAScript 2015... Nada mais são que novas especificações para o JavaScript, com novas funcionalidades.
 
## Como usar este repositório
 
Este repositório é separado por pastas, cada uma destinada a explicar um tópico diferente acerca da linguagem, você pode ter um acesso mais rápido a todo o conteúdo disponível no sumário do README do repositório. O conteúdo foi criado de forma cronológica, seguindo a ordem do sumário, ou seja, cada tópico necessita dos conhecimentos do tópico anterior, e foi criado na premissa que você não possui os conhecimentos dos tópicos a frente. Desta forma os iniciantes não se sentem perdidos e sempre estão aprendendo. Caso deseje revisar, existem os arquivos de códigos comentados, que são mais diretos e podem ser executados.
 
Cada pasta possui dois tipos de arquivos, seu próprio README, com a explicação do tópico da pasta, e os arquivos de código exemplo. Os READMEs contam uma estória onde somos deuses em um universo que a menor parte da matéria são pequenas partículas que assumem dois estados, 0 e 1, e nós temos que inventar um conjunto de regras para poder trabalhar com elas e comandar nosso universo. Nestas histórias procuro demonstrar a necessidade da existência do tópico tratado, assim como um pouco de como elas funcionam por baixo dos panos. Ao longo da estória, posto vários links para você se aprofundar mais. Já os arquivos de códigos são bem mais diretos, eles contêm os códigos demonstrados nos READMEs, comentários acerca do que está sendo feito e podem ser executados.
 
## Como executar um código JavaScript
 
Como não irei contar que você já saiba HTML, como executar o código JavaScript no navegador será um tópico futuro. Além do mais, este repositório visa explanar exclusivamente sobre JavaScript. Então será demonstrado como o código pode ser executado em seu computador.
 
Primerio, é necessário instalar o [Node.js](https://nodejs.org/en/). Para isso, acesse o link anterior e siga as instruções. Para windows, basicamente tudo o que você terá que fazer baixar e executar um executável. No linux é necessário executar alguns comandos no terminal.
 
Após a instalação do Node, tudo o que você precisa fazer é abrir o terminal na pasta onde possui o arquivo JavaScript que deseja executar e rodar o seguinte comando:
 
``` bash
node nomeDoArquivo.js
```
 
Caso use o VSCode e deseje mais facilidade, você pode instalar o plugin *Code Runner*. Nele você consegue executar os arquivos com um único clique dentro do VSCode.
 
Se não deseja utilizar JavaScript tão cedo e só queira realizar algum teste, ver como a linguagem funciona ou brincar um pouco, pode estar utilizando algum ambiente web para isto, eu gosto do *[repl.it](https://repl.it/)*.
 
> Caso use outro ambiente, você pode contribuir com formas de executar um código JavaScript nele.
 
## Observações
 
> A partir de agora irei me referir ao JavaScript por sua sigla JS. É cansativo escrever o nome por extenso o tempo todo hehe.
