# Johnny-Five

Linguagem: Johnny-Five
~~~~
Nome: Sara Silva da Silva - saremedss - 20131011110185;
      Jonathan Cardoso F. de Moura - johnny99tech - 20141011110131;
      Jules Brendo - ;
~~~~
## Resumo

> * Propósito da linguagem: Johnny-Five é a plataforma JavaScript Robotics & IoT . Lançado pela Bocoup em 2012, Johnny-Five é mantido por uma comunidade de desenvolvedores de software apaixonado e engenheiros de hardware. Mais de 75 desenvolvedores contribuíram para a construção de um ecossistema robusto, extensível e componível. Como muitos dos projetos de construção com a Johnny-Five envolvem conexão física e hardware, também fornecemos extensa documentação e exemplos (com diagramas) de como conectar e depurar componentes no site da Johnny-Five.

> * Paradgima da linguagem (procedural, orientado a objetos, funcional, etc): Johnny-Five é uma estrutura de programação JavaScript Arduino de código aberto para robótica. Estrutura para controlar componentes de hardware através de uma variedade de microprocessadores populares e plataformas de sistema em um chip usando JavaScript. Johnny-Five traz paradigmas e técnicas familiares de programação JavaScript para o mundo real, com uma API idiomática, orientada a objetos, semelhante a jQuery, que torna o processo de mover um braço robótico como o de animar um elemento em uma página da web. Com o suporte incorporado para placas compatíveis com protocolo Firmata e um conjunto de outros IO-Plugins, o Johnny-Five faz o trabalho de abstrair a comunicação de modo que os componentes se comportem o mesmo independentemente da plataforma que está sendo usada.

> * Data de criação: Lançado pela Bocoup em 2012 por Rick Waldron.

> * Principal mantenedor (Oracle, Microsoft, Google, etc): Bocoup.

## Instalação e uso

> * Descrever de forma resumida como instalar, demonstrando os comandos (ver Markdown sobre códigos): instalar o johnny-five: npm install johnny-five;


> * Descrever de forma resumida como usar (compilar e executar), demonstrando os comandos (ver Markdown sobre códigos)
```
"Olá Mundo" com um simples LED piscando; O seguinte demonstra como fazer isso com o quadro Johnny-Five.

var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);
  led.blink(500);
});
```

## Sintaxe básica

/*Descrever sintaxe básica da linguagem contendo explicação e exemplo para:*/

> *  Variáveis e constantes - inicialização e comandos de atribuição : As variáveis são declaradas com a palavra chave var, como segue:
      ```   
      var i;
      var sum;
      ```
      Também é possível declarar varias variáveis com a mesma palavra chave var:
      ```
      var i, sum;
      ```
      E pode-se combinar a declaração da variável com sua inicialização:
      ```
      var i = 0, j = 0, k = 0;
      var nome = "Fulano";
      ```
      Antes de usar uma variável em um programa JavaScript, deve declará-la.
      
      > > Tipos
      Os tipos em JavaScript podem ser divididos em duas categorias: tipo primitivo e de objeto.
      Os tipo primitivos incluem números, strings e valores booleanos.
      Os valores especiais null e undefined são valores primitivos mas não são números, nem string e nem booleanos.
      Qualquer valor em JavaScript que não seja número, string, booleano, null ou undefined é um objeto.
      O typeof é um operador unário colocado antes de seu operando, o qual pode ser de qualquer tipo. Seu valor é uma string que             especifica o tipo do operando.
      ```   
      typeof "foo"; // 'string'
      typeof 123;   // 'number'
      ```   
      > > Números
      Ao contrário de muitas linguagens, JavaScript não faz distinção entre valores inteiros e valores em ponto flutuante. Todos os números em JavaScript são representados como valores em ponto flutuante.
      Literais inteiros:
      0
      1
      100
      Literais em ponto flutuante:

      3.14
      100.09
      0.33333
      
      > > Strings
      Para incluir uma string literal em um programa JavaScript, basta colocar os caracteres da string dentro de um par combinado de aspas simples ou duplas.

      "" string de cumprimento zero
      'testing'
      "other testing"
      Para concatenar strings utilizamos o operador +.
      ```
      var msg = "Hello " + "word"; // "Hello word"
      msg = "Welcome to my blog, " + name;
      ```
      A propriedade length determina o tamanho da string.
      ```
      "palavra".length // 7
      ```
      > > Booleanos
      Os valores booleanos são representados por true e false.
      null e undefined
      A palavra chave null indica a ausência de um valor.
      Mas também há um segundo valor que indica ausência de valor: undefined.
      O valor indefinido (undefined) representa uma ausência mais profunda, é o valor de variáveis que não foram inicializadas.

      > > Conversão
      A linguagem é muito flexível quanto aos tipos de valores que exige.

      As variáveis em JavaScript são não tipadas. Você pode atribuir um valor de qualquer tipo a uma variável e, posteriormente, atribuir um valor de tipo diferente para a mesma variável.

      JavaScript converte valores de um tipo para outro de forma livre.

      Se um programa espera uma string, por exemplo, e você fornece um número, ele converte o número em string automaticamente.

      Se você usa um valor não booleano onde é esperado um booleano, JavaScript converte adequadamente.


> *  Operadores relacionais e lógicos:
      
> *  Operadores aritméticos
> *  Estruturas de controle condicional
> *  Estruturas de repetição
> *  Vetores, matrizes e strings
> *  Funções

## Sintaxe OO

/*Descrever sintaxe orientada a objetos da linguagem contendo explicação e exemplo para:*/
> Sintaxe orientada a objetos da linguagem contendo explicação:

> *  Classes
> *  Objetos
> *  Atributos (visibilidade: privado e público, escopo: classe e objeto)
> *  Métodos (visibilidade: privado e público, escopo: classe e objeto)
> *  Construtores
> *  Herança
> *  Polimorfismo
> *  Sobrecarga

> > Descrever sintaxe básica de exceções:

> *  Categorias de exeções
> *  Captura e lançamento de exceções
> *  Criar novas exeções

## Sintaxe Funcional

> Descrever sintaxe básica do paradigma da linguagem contendo explicação e exemplo.





