# Johnny-Five

Linguagem: Johnny-Five
~~~~
Nome: Sara Silva da Silva - saremedss - 20131011110185;
      Jonathan Cardoso F. de Moura - johnny99tech - 20141011110131;
      
~~~~
## Resumo

> * Propósito da linguagem

Johnny-Five é a plataforma JavaScript Robotics & IoT . Lançado pela Bocoup em 2012, Johnny-Five é mantido por uma comunidade de desenvolvedores de software apaixonado e engenheiros de hardware. Mais de 75 desenvolvedores contribuíram para a construção de um ecossistema robusto, extensível e componível. Como muitos dos projetos de construção com a Johnny-Five envolvem conexão física e hardware, também fornecemos extensa documentação e exemplos (com diagramas) de como conectar e depurar componentes no site da Johnny-Five.

> * Paradgima da linguagem (procedural, orientado a objetos, funcional, etc)

Johnny-Five é uma estrutura de programação JavaScript Arduino de código aberto para robótica. Estrutura para controlar componentes de hardware através de uma variedade de microprocessadores populares e plataformas de sistema em um chip usando JavaScript. Johnny-Five traz paradigmas e técnicas familiares de programação JavaScript para o mundo real, com uma API idiomática, orientada a objetos, semelhante a jQuery, que torna o processo de mover um braço robótico como o de animar um elemento em uma página da web. o Johnny-Five faz o trabalho de abstrair a comunicação de modo que os componentes se comportem o mesmo independentemente da plataforma que está sendo usada.

> * Data de criação: Lançado pela Bocoup em 2012 por Rick Waldron.

> * Principal mantenedor (Oracle, Microsoft, Google, etc): Bocoup.

## Instalação e uso

> * Instalação

Usando o Node.js, utilizaremos: 
```
npm install johnny-five --save;
```

> * Compilando e executando os comandos

No codigo abaixo temos o codigo necessário para o "Olá Mundo" que é com um simples LED piscando. Em um arquivo OLAMUNDO.js 

```
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);
  led.blink(500);
});
```
 
Para execução é necessária apenas a chamada do arquivo, e no [Arduino](http://www.obomprogramador.com/2014/11/arduino-etilico-2-vinganca-do-javascript.html) por exemplo ele irá acender a led:

```
node OLAMUNDO.js
```

[Video acerca do OLAMUNDO.js](http://morvanabonin.org/introducao-arduino-com-node-js-utilizando-johnny-five/)

[Um pouco mais sobre o Arduino](http://www.techtudo.com.br/noticias/noticia/2013/10/o-que-e-um-arduino-e-o-que-pode-ser-feito-com-ele.html)

## Sintaxe básica


> *  Variáveis e constantes

inicialização e comandos de atribuição : As variáveis são declaradas com a palavra chave var, como segue:
~~~~

var i, sum;
~~~~      

E pode-se combinar a declaração da variável com sua inicialização:
~~~~

var i = 0, j = 0, k = 0;
var nome = "Fulano";
const my_fav = 7;
~~~~

>> Tipos
Os tipos podem ser divididos em duas categorias: tipo primitivo e de objeto.

      >>> Os tipos primitivos
Incluem números, strings e valores booleanos. Os valores especiais null e undefined são valores primitivos mas não são números, nem string e nem booleanos.

      >>>Objetos
Qualquer valor que não seja número, string, booleano, null ou undefined é um objeto.
~~~~  
      var meuCarro = new Object();
      meuCarro.fabricacao = "Ford";
      meuCarro.ano = 1969;
~~~~

>> Números


Ao contrário de muitas linguagens, JavaScript não faz distinção entre valores inteiros e valores em ponto flutuante. Todos os números em JavaScript são representados como valores em ponto flutuante.  
~~~~

Literais inteiros:
@@ -86,9 86,9 @@ Nome: Sara Silva da Silva - saremedss - 20131011110185;
100.09
0.33333
~~~~ 

>> Strings

Para incluir uma string literal em um programa JavaScript, basta colocar os caracteres da string dentro de um par combinado de aspas simples ou duplas.
~~~~

"" string de cumprimento zero
@@ -107,33 107,26 @@ A propriedade length determina o tamanho da string.
"palavra".length // 7
~~~~

>> Booleanos

Os valores booleanos são representados por true e false.
>> null e undefined


A palavra chave null indica a ausência de um valor.    
Mas também há um segundo valor que indica ausência de valor: undefined.   
O valor indefinido (undefined) representa uma ausência mais profunda, é o valor de variáveis que não foram inicializadas.

>> Conversão

A linguagem é muito flexível quanto aos tipos de valores que exige.
As variáveis em JavaScript são não tipadas. Você pode atribuir um valor de qualquer tipo a uma variável e, posteriormente, atribuir um valor de tipo diferente para a mesma variável.
JavaScript converte valores de um tipo para outro de forma livre.
Se um programa espera uma string, por exemplo, e você fornece um número, ele converte o número em string automaticamente.
Se você usa um valor não booleano onde é esperado um booleano, JavaScript converte adequadamente.

>* Operadores relacionais e lógicos:
>> Relacionais: Os Operadores Relacionais são:
~~~~

A propriedade length determina o tamanho da string.
==  igual a
!=  diferente de
~~~~      

>> Lógicos: 
~~~~

/* &&: e *\

a==3 && b<10 // retorna verdadeiro
a!=3 && b==5 // retorna falso
      
/* ||: ou *\

a==3 || b<10 // retorna verdadeiro
a!=3 || b==5 // retorna verdadeiro
a==1 || b==3 // retorna falso

/* !: não *\ 

! (a==3) // retorna falso
! (a!=3) // retorna verdadeiro
~~~~


> * Operadores aritméticos
>> Condicional - if / else
~~~~

css
@@ -172,7 170,7 @@ A propriedade length determina o tamanho da string.
// executa este bloco else
}
~~~~       

>> Operador Condicional Ternário

É possível obter resultados semelhantes usando o operador condicional ternário condition ? expr1 : expr2.
resultado = (a > b) ? "a é maior que b" : "b é maior que a";
@@ -187,7 185,7 @@ A propriedade length determina o tamanho da string.
}

>> Condicional - switch
~~~~   

@@ -203,10 201,12 @@ A propriedade length determina o tamanho da string.
}
~~~~

> * Estruturas de controle condicional

Agora que você já sabe as estruturas condicionais if, else if e else, podemos apimentar um pouco mais seu código com algumas condições mais complexas.
>> If (se)

Para utilizar a estrutura if, precisamos da palavra if  ( pelo menos uma condição entre parênteses )  { quantas ações forem necessárias entre colchetes }.
~~~~

@@ -219,7 219,7 @@ A propriedade length determina o tamanho da string.
alert('Vou nadar!');
}      
~~~~

>> If … else
Também pode ocorrer de você ter uma ação contrária para ser executada, caso sua ação principal não seja verdadeira, por exemplo:
Se o sol sair hoje, vou nadar; caso contrário, vou ler.
Nesse caso temos duas ações dependendo de uma condição, uma das duas terá que ser executada.

~~~~

@@ -237,10 237,11 @@ A propriedade length determina o tamanho da string.
alert('Vou ler');
}
~~~~

>> If … else if … else

Outro fato que vai ocorrer constantemente em suas aplicações Javascript, é o fato de existir mais de uma condição, por exemplo:
Se eu acordar de madrugada, vou ler; se acordar de manhã, vou estudar; se acordar tarde vou assistir filme.
Nesse caso podemos utilizar um else if ( outra condição ):
~~~~

// Variáveis booleanas
@@ -258,16 259,16 @@ A propriedade length determina o tamanho da string.
}
~~~~

> * Estruturas de repetição
>> for
~~~~    

for (var i = 0; i < 5; i) {
// Will execute 5 times
}
~~~~

> * Vetores, matrizes e strings
>> Arrays
Em JavaScript, arrays são um tipo especial de objeto que representam um conjunto ordenado de valores numerados.
~~~~

@@ -297,8 298,6 @@ Uma função é um objeto que tem código executável associado. Uma função po
~~~~

## Sintaxe OO

> *  Classes
No Javascript utilizamos uma função para criar a classe.
~~~~

@@ -347,28 346,31 @@ Para passar parâmetros para o construtor da classe.
~~~~
### Sintaxe básica de exceções:

> * Categorias de exceções
>> throw

Use a declaração throw para lançar uma exceção. Quando você lança uma exceção, você especifica a expressão contendo o valor a ser lançado:
~~~~

throw true;       // tipo booleano
throw {toString: function() { return "Eu sou um objeto!"; } };
~~~~
>> try...catch

Declaração: coloca um bloco de declarações em try, e especifica uma ou mais respostas para uma exceção lançada. Se uma exceção é lançada, a declaração try...catch pegá-a.
~~~~

try {
throw "myException"; // lança  uma exceção
}
catch (e) {
// declarações de lidar com as exceções
logMyErrors(e); // passar a exceção para o manipulador de erro
}

~~~~
> * Captura e lançamento de exceções

> * Criar novas exeções

## Sintaxe Funcional
> Descrever sintaxe básica do paradigma da linguagem contendo explicação e exemplo.
  ### Sintaxe básica de exceções:
  
 > * Categorias de exceções
 >> throw
 
 +Use a declaração throw para lançar uma exceção. Quando você lança uma exceção, você especifica a expressão contendo o valor a ser lançado:
 ~~~~
 
        throw true;       // tipo booleano
        throw {toString: function() { return "Eu sou um objeto!"; } };
 ~~~~
 
 >> try...catch
 
Declaração: coloca um bloco de declarações em try, e especifica uma ou mais respostas para uma exceção lançada. Se uma exceção é lançada, a declaração try...catch pegá-a.
 ~~~~
 
        try {
          throw "myException"; // lança  uma exceção
        }
        catch (e) {
          // declarações de lidar com as exceções
          logMyErrors(e); // passar a exceção para o manipulador de erro
        } 
~~~~

 > * Captura e lançamento de exceções
  
 > * Criar novas exeções
  
## Sintaxe Funcional
> * Descrever sintaxe básica do paradigma da linguagem contendo explicação e exemplo.
### Sintaxe básica de exceções:

> * Categorias de exceções
    >>TypeError
    >> RangeError
    >> EvalError
      
      ```css
       try {
          myroutine(); // pode lançar três tipos de exceções
      } catch (e if e instanceof TypeError) {
          // declarações para manipular exceções TypeError
      } catch (e if e instanceof RangeError) {
          // declarações para manipular exceções RangeError
      } catch (e if e instanceof EvalError) {
          // declarações para manipular exceções EvalError
      } catch (e) {
          // declarações para manipular quaisquer exceções não especificadas
          logMyErrors(e); // passa o objeto de exceção para o manipulador de erro
      }
      ```
      
> *  Captura e lançamento de exceções
      > > throw
Use a declaração throw para lançar uma exceção. Quando você lança uma exceção, você especifica a expressão contendo o valor a ser lançado:
      ```
      throw true;       // tipo booleano
      throw {toString: function() { return "Eu sou um objeto!"; } };
      ```
    
      > > try...catch
A declaração try...catch coloca um bloco de declarações em try, e especifica uma ou mais respostas para uma exceção lançada. Se uma exceção é lançada, a declaração try...catch pegá-a.
      ```
      try {
        throw "myException"; // lança  uma exceção
      }
      catch (e) {
        // declarações de lidar com as exceções
        logMyErrors(e); // passar a exceção para o manipulador de erro
      }
      ```
> *  Criar novas exeções
```css
      function MeuErro(mensagem, solucao, localizacao) {  
          return new Error(messagem + " Solution:" + solucao +  " Location:" + localizacao);
      }

      throw MeuErro('Tem um erro', 'colocar a variável a fora do for', index.js:1:6);
```
## Sintaxe Funcional

> * Sintaxe básica do paradigma da linguagem

A noção de paradigmas de programação é uma forma de classificar as linguagens de programação de acordo com o estilo de programação  de computadores. Características de várias linguagens de programação determinam quais paradigmas elas pertencem; Alguns paradigmas estão preocupados principalmente com a maneira que o código é organizado, como o agrupamento de código em unidades, juntamente com o estado que é modificado pelo código. No entanto, outros estão preocupados principalmente com o estilo de sintaxe e gramática.

O principal de outros paradigmas é o imperativo, e até pode ser usada na forma procedural (obviamente de forma estruturada).

O Johnny-five é convertido para o Javascript que tambem é conhecido por também ser orientada a objeto através de protótipos, mas como toda linguagem moderna, usa cada vez mais os paradigmas funcionais, tendo uma forte influência em programação orientada a eventos. Onde a linguagem usa tipagem dinâmica é usada como script. Costuma rodar de forma interpretada, mas fundo é compilada.

[Exemplo de pulso de LED que enfraquece um LED dentro e fora repetidamente. Requer LED no pino que suporta PWM](http://johnny-five.io/examples/led-pulse/)

```css
      node eg/led-pulse.js
```

```css
      var five = require("johnny-five");
      var board = new five.Board();

      board.on("ready", function() {

        // Create a standard `led` component
        // on a valid pwm pin
        var led = new five.Led(11);

        led.pulse();

        // Stop and turn off the led pulse loop after
        // 10 seconds (shown in ms)
        this.wait(10000, function() {

          // stop() terminates the interval
          // off() shuts the led off
          led.stop().off();
        });
      });
```
