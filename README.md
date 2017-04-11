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
