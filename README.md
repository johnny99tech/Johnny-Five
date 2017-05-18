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
      Os tipos em JavaScript podem ser divididos em duas categorias: tipo primitivo e de objeto.~~~
      Os tipo primitivos incluem números, strings e valores booleanos.~~~
      Os valores especiais null e undefined são valores primitivos mas não são números, nem string e nem booleanos.~~~
      Qualquer valor em JavaScript que não seja número, string, booleano, null ou undefined é um objeto.~~~
      O typeof é um operador unário colocado antes de seu operando, o qual pode ser de qualquer tipo. Seu valor é uma string que             especifica o tipo do operando.~~~
      ~~~
      ```   
      typeof "foo"; // 'string'
      typeof 123;   // 'number'
      ```   
> > Números
      ~~~
      Ao contrário de muitas linguagens, JavaScript não faz distinção entre valores inteiros e valores em ponto flutuante. Todos os números em JavaScript são representados como valores em ponto flutuante.
      ~~~
      ``` 
      Literais inteiros:
      0
      1
      100
      Literais em ponto flutuante:

      3.14
      100.09
      0.33333
      ``` 
> > Strings
      ~~~
      Para incluir uma string literal em um programa JavaScript, basta colocar os caracteres da string dentro de um par combinado de aspas simples ou duplas.~~~

      "" string de cumprimento zero
      'testing'
      "other testing"
      Para concatenar strings utilizamos o operador +.
      ~~~
      ```
      var msg = "Hello " + "word"; // "Hello word"
      msg = "Welcome to my blog, " + name;
      ```
      ~~~
      A propriedade length determina o tamanho da string.
      ~~~
      ```
      "palavra".length // 7
      ```
      ~~~
> > Booleanos
      ~~~
      Os valores booleanos são representados por true e false.~~~
      >> null e undefined~~~
      A palavra chave null indica a ausência de um valor.~~~
      Mas também há um segundo valor que indica ausência de valor: undefined.~~~
      O valor indefinido (undefined) representa uma ausência mais profunda, é o valor de variáveis que não foram inicializadas.~~~

> > Conversão
      ~~~
      A linguagem é muito flexível quanto aos tipos de valores que exige.

      As variáveis em JavaScript são não tipadas. Você pode atribuir um valor de qualquer tipo a uma variável e, posteriormente, atribuir um valor de tipo diferente para a mesma variável.

      JavaScript converte valores de um tipo para outro de forma livre.

      Se um programa espera uma string, por exemplo, e você fornece um número, ele converte o número em string automaticamente.

      Se você usa um valor não booleano onde é esperado um booleano, JavaScript converte adequadamente.


> *  Operadores relacionais e lógicos:
      > > Relacionais: Os Operadores Relacionais são:
      ```css
            >	maior que
            <=	menor ou igual
            <	menor que
            <=	menor ou igual
            ==	igual a
            !=	diferente de
      ```
      
      > > Lógicos: && 
      
      ```css
      a==3 && b<10 // retorna verdadeiro
      a!=3 && b==5 // retorna falso
      || -
      a==3 || b<10 // retorna verdadeiro
      a!=3 || b==5 // retorna verdadeiro
      a==1 || b==3 // retorna falso
      ! -
      ! (a==3) // retorna falso
      ! (a!=3) // retorna verdadeiro
      ```
      
> *  Operadores aritméticos
      > > Condicional - if / else
      ```css
      if (n == 1) {
          // executa este bloco if
      } else if () {
          // executa este bloco else if
      } else {
          // executa este bloco else
      }
      ```
      
      > > Operador Condicional Ternário
      É possível obter resultados semelhantes usando o operador condicional ternário condition ? expr1 : expr2.
      resultado = (a > b) ? "a é maior que b" : "b é maior que a";
      O código acima é equivalente ao de baixo:
      ```css
      if (a > b) {
          resultado = "a é maior que b";
      } else {
          resultado = "b é maior que a";
      }
      ```

      >> Condicional - switch
      ```css
      switch(action) {
          case 'draw':
              drawit();
              break;
          case 'eat':
              eatit();
              break;
          default:
              donothing();
      }
      ```

> *  Estruturas de controle condicional
      Agora que você já sabe as estruturas condicionais if, else if e else, podemos apimentar um pouco mais seu código com algumas condições mais complexas.
      > > If (se)
      Para utilizar a estrutura if, precisamos da palavra if + ( pelo menos uma condição entre parênteses ) + { quantas ações forem necessárias entre colchetes }.
      ~~~~
      ```css
      // Variável booleana verdadeira
      var sol = true;

      // Condição
      if ( sol ) {
            // Ação
            alert('Vou nadar!');
      }
      ```
      ~~~~
      
      > > If … else
      
      ~~~~
      Também pode ocorrer de você ter uma ação contrária para ser executada, caso sua ação principal não seja verdadeira, por exemplo:
      Se o sol sair hoje, vou nadar; caso contrário, vou ler.
      Nesse caso temos duas ações dependendo de uma condição, uma das duas terá que ser executada.
      Para suprir essa necessidade, completamos a estrutura condicional if com else (senão):
      ~~~~
      ```css
      // Variável booleana falsa
      var sol = false;

      // Condição
      if ( sol ) {
            alert('Vou nadar');
      } else {
            alert('Vou ler');
      }
      ```
      ~~~~
      >> If … else if … else
      ~~~~
      Outro fato que vai ocorrer constantemente em suas aplicações Javascript, é o fato de existir mais de uma condição, por exemplo:
      Se eu acordar de madrugada, vou ler; se acordar de manhã, vou estudar; se acordar tarde vou assistir filme.
      Nesse caso podemos utilizar um else if ( outra condição ):
      ~~~~
      ```
      // Variáveis booleanas
      var madrugada = false;
      var cedo = true;
      var tarde = false;

      // Condição
      if ( madrugada ) {
            alert('Vou ler');
      } else if ( cedo ) {
            alert('Vou estudar');
      } else {
            alert('Vou assistir filme');
      }
      ```
      ~~~~
      
> *  Estruturas de repetição
      >> for
      ~~~~
      ```
      for (var i = 0; i < 5; i++) {
          // Will execute 5 times
      }
      ```
      ~~~~
> *  Vetores, matrizes e strings
      > > Arrays
      Em JavaScript, arrays são um tipo especial de objeto que representam um conjunto ordenado de valores numerados.
      ~~~~
      ```
      var a = new Array();
      a[0] = "dog";
      a[1] = "cat";
      a[2] = "hen";
      a.length // 3
      ```
      ~~~~
      Uma forma mais conveniente de utilização de um array, na verdade a mais usada:
      ~~~~
      ```
      var a = ["dog", "cat", "hen"];
      a.length // 3
      ```
      ~~~~
      
> *  Funções
      ~~~~
      Uma função é um objeto que tem código executável associado. Uma função pode ser chamada para executar esse código executável e retornar um valor calculado.
      ~~~~
      ```
      function add(x, y) {
          var total = x + y;
          return total;
      }
      ```
      ~~~~
      
## Sintaxe OO

/*Descrever sintaxe orientada a objetos da linguagem contendo explicação e exemplo para:*/

> *  Classes
      ~~~~
      No Javascript utilizamos uma função para criar a classe.
      ~~~~
      ```
      function listButton() {
      }
      ```
      ~~~~
      Para criar propriedades podemos usar a palavra var ou this. Se utilizarmos a palavra var o atributo vai ficar privado e se utilizarmos a palavra this o atributo vai ficar publico.
      ~~~~
      ```
      function MyClasse() {
          var nome;

          this.idade;
      }


      function document_OnLoad() {
          oMyClasse = new MyClasse();

          oMyClasse.idade = '10';
      }
      ```
      ~~~~
      Para passar parâmetros para o construtor da classe.
      
      ```
      function MyClasse(value) {
          this.idade = value;
      }

      function document_OnLoad() {
          oMyClasse = new MyClasse('10');
      }

      ```
      
> *  Objetos
      ~~~~   
> *  Atributos (visibilidade: privado e público, escopo: classe e objeto)
> *  Métodos (visibilidade: privado e público, escopo: classe e objeto)
> *  Construtores
> *  Herança
> *  Polimorfismo
> *  Sobrecarga

### Sintaxe básica de exceções:

> *  Categorias de exceções
      > > throw
      Use a declaração throw para lançar uma exceção. Quando você lança uma exceção, você especifica a expressão contendo o valor a ser lançado:
      ```
      throw true;       // tipo booleano
      throw {toString: function() { return "Eu sou um objeto!"; } };
      ```
      > > try...catch
      Declaração try...catch
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
> *  Captura e lançamento de exceções

> *  Criar novas exeções

## Sintaxe Funcional
> Descrever sintaxe básica do paradigma da linguagem contendo explicação e exemplo.
