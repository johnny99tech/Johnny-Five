# Johnny-Five

Linguagem: Johnny-Five
~~~~
Nome: Sara Silva da Silva - saremedss - 20131011110185;
      Jonathan Cardoso F. de Moura - johnny99tech - 20141011110131;
      
~~~~
## Resumo

> Propósito da linguagem

Johnny-Five é a plataforma JavaScript Robotics & IoT . Lançado pela Bocoup em 2012, Johnny-Five é mantido por uma comunidade de desenvolvedores de software apaixonado e engenheiros de hardware. Mais de 75 desenvolvedores contribuíram para a construção de um ecossistema robusto, extensível e componível. Como muitos dos projetos de construção com a Johnny-Five envolvem conexão física e hardware, também fornecemos extensa documentação e exemplos (com diagramas) de como conectar e depurar componentes no site da Johnny-Five.

> Paradgima da linguagem (procedural, orientado a objetos, funcional, etc)

Johnny-Five é uma estrutura de programação JavaScript Arduino de código aberto para robótica. Estrutura para controlar componentes de hardware através de uma variedade de microprocessadores populares e plataformas de sistema em um chip usando JavaScript. Johnny-Five traz paradigmas e técnicas familiares de programação JavaScript para o mundo real, com uma API idiomática, orientada a objetos, semelhante a jQuery, que torna o processo de mover um braço robótico como o de animar um elemento em uma página da web. o Johnny-Five faz o trabalho de abstrair a comunicação de modo que os componentes se comportem o mesmo independentemente da plataforma que está sendo usada.

> Data de criação: Lançado pela Bocoup em 2012 por Rick Waldron.

> Principal mantenedor (Oracle, Microsoft, Google, etc): Bocoup.

## Instalação e uso

> Instalação

Usando o Node.js, utilizaremos: 
```
npm install johnny-five --save;
```

> Compilando e executando os comandos

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


> Variáveis e constantes

inicialização e comandos de atribuição : As variáveis são declaradas com a palavra chave var, como segue:
~~~~

var i, sum;
~~~~      

E pode-se combinar a declaração da variável com sua inicialização:
~~~~

      var i = 0, j = 0, k = 0;
      var nome = "Sara";
      var nome = "Johnny";
~~~~

> Tipos

Os tipos podem ser divididos em duas categorias: tipo primitivo e de objeto.

>> Tipos primitivos

Incluem números, strings e valores booleanos. Os valores especiais null e undefined são valores primitivos mas não são números, nem string e nem booleanos.

>> Objetos

Por definição com suas características e finalidades, sendo essa função um protótipo desse objeto, ou ainda o método construtor de uma classe.
Ex: Cadeira possui tamanho, cor, material de que é feita, se tem rodas, se é giratória etc..
~~~~  

      //nomeObjeto.nomePropriedadevar 
      
      var meuCarro = new Object();
      meuCarro.fabricacao = "Ford";
      meuCarro.ano = 1969;
      
      car = {type:"Fiat", model:"500", color:"white"};
      
      //onde meuCarro é o Objeto
      //fabricacao e ano são os propriedades do Objeto
~~~~

>> Números

Ao contrário de muitas linguagens, JavaScript não faz distinção entre valores inteiros e valores em ponto flutuante. Todos os números são representados como valores em ponto flutuante.
~~~~
        
      var inteiro = 100;
~~~~ 

>> Strings

Para incluir uma string literal em um programa JavaScript, basta colocar os caracteres da string dentro de um par combinado de aspas simples ou duplas.
~~~~

      var txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
~~~~

>> Booleanos

Os valores booleanos são representados por true e false.
~~~~

      var x = false;
      var y = true;
~~~~

>> null e undefined

-valor undefined
      Utilizado quando uma variável não teve valor atribuído.
-valor null
      valor primitivo que representa a ausência intencional de um valor de objeto.

A palavra chave null indica a ausência de um valor.    
Mas também há um segundo valor que indica ausência de valor: undefined.   
O valor indefinido (undefined) representa uma ausência mais profunda, é o valor de variáveis que não foram inicializadas.
~~~~

      var y; //undefined
      var x = null; //null
     
~~~~
>> Conversão

A linguagem é muito flexível quanto aos tipos de valores que exige.
Você pode atribuir um valor de qualquer tipo a uma variável e, posteriormente, atribuir um valor de tipo diferente para a mesma variável.
~~~~

      O método Date toString () faz o mesmo.
      Date().toString() 

      parseFloat() - Converte uma string em float.
      parseInt() - Converte uma string em inteiro.
~~~~

> Operadores relacionais e lógicos:
>> Relacionais:
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

> Operadores aritméticos

>> Condicional - if / else
~~~~
      
      var n = 0;
      if(n != 0){
            console.log("par");
      }
      else{
            console.log("impar");	
      }
~~~~       

>> Operador Condicional Ternário

É possível obter resultados semelhantes usando o operador condicional ternário.
~~~~

      (a > b) ? "a é maior que b" : "b é maior que a";
~~~~

>> Condicional - switch
~~~~   
      
      var n = 0;
      if(n != 0){
            console.log("par");
      }
      else{
            console.log("impar");	
      }
~~~~

> Estruturas de controle condicional

Agora que você já sabe as estruturas condicionais if, else if e else, podemos apimentar um pouco mais seu código com algumas condições mais complexas.

>> If … else if … else

É o fato de existir mais de uma condição, por exemplo:
Se eu acordar de madrugada, vou ler; se acordar de manhã, vou estudar; se acordar tarde vou assistir filme.
Nesse caso podemos utilizar um else if ( outra condição ):

> Estruturas de repetição

>> For
~~~~    

      for (var i = 0; i < 5; i++) {
            // Will execute 5 times
      }
~~~~

>> Arrays

Em JavaScript, arrays são um tipo especial de objeto que representam um conjunto ordenado de valores numerados. Uma função é um objeto que tem código executável associado.  
~~~~
      
      var cars = [
            "Saab",
            "Volvo",
            "BMW"
      ];

      var pessoa = ["John", "Doe", 46];
~~~~

## Sintaxe OO

> Classes

Utiliza uma função para criar a classe. Para passar parâmetros para o construtor da classe.
~~~~

      class Rectangle {
        constructor(height, width) {
          this.height = height;
          this.width = width;
        }
      }
~~~~
### Sintaxe básica de exceções:

> Categorias de exceções

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
> Captura e lançamento de exceções

> Criar novas exeções

## Sintaxe Funcional

> Descrever sintaxe básica do paradigma da linguagem contendo explicação e exemplo.

### Sintaxe básica de exceções:
  
> Categorias de exceções

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

> Captura e lançamento de exceções
  
> Criar novas exceções
  
## Sintaxe Funcional

> Descrever sintaxe básica do paradigma da linguagem contendo explicação e exemplo.

### Sintaxe básica de exceções:

> Categorias de exceções

>> TypeError
>> RangeError
>> EvalError
~~~~

      css
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
~~~~
      
> Captura e lançamento de exceções

>> throw

Use a declaração throw para lançar uma exceção. Quando você lança uma exceção, você especifica a expressão contendo o valor a ser lançado:
~~~~

      throw true;       // tipo booleano
      throw {toString: function() { return "Eu sou um objeto!"; } };
~~~~
    
>> try...catch

A declaração try...catch coloca um bloco de declarações em try, e especifica uma ou mais respostas para uma exceção lançada. Se uma exceção é lançada, a declaração try...catch pegá-a.
~~~~

      try {
        throw "myException"; // lança  uma exceção
      }
      catch (e) {
        // declarações de lidar com as exceções
        logMyErrors(e); // passar a exceção para o manipulador de erro
      }
~~~~
> *Criar novas exeções
~~~~

      css
      function MeuErro(mensagem, solucao, localizacao) {  
          return new Error(messagem + " Solution:" + solucao +  " Location:" + localizacao);
      }

      throw MeuErro('Tem um erro', 'colocar a variável a fora do for', index.js:1:6);
~~~~


## Sintaxe Funcional

> Sintaxe básica do paradigma da linguagem

A noção de paradigmas de programação é uma forma de classificar as linguagens de programação de acordo com o estilo de programação  de computadores. Características de várias linguagens de programação determinam quais paradigmas elas pertencem; Alguns paradigmas estão preocupados principalmente com a maneira que o código é organizado, como o agrupamento de código em unidades, juntamente com o estado que é modificado pelo código. No entanto, outros estão preocupados principalmente com o estilo de sintaxe e gramática.

O principal de outros paradigmas é o imperativo, e até pode ser usada na forma procedural (obviamente de forma estruturada).

O Johnny-five é convertido para o Javascript que tambem é conhecido por também ser orientada a objeto através de protótipos, mas como toda linguagem moderna, usa cada vez mais os paradigmas funcionais, tendo uma forte influência em programação orientada a eventos. Onde a linguagem usa tipagem dinâmica é usada como script. Costuma rodar de forma interpretada, mas fundo é compilada.

[Exemplo de pulso de LED que enfraquece um LED dentro e fora repetidamente. Requer LED no pino que suporta PWM](http://johnny-five.io/examples/led-pulse/)
~~~~

      css
      node eg/led-pulse.js

      css
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
~~~~
