#### Explorando la arquitectura del computador Hack

Ahora vamos a analizar juntos el siguiente programa. Este programa tendrá 
todos los conceptos que vamos investigar en la siguiente fase de la unidad 
de manera más profunda. En qué nos enfocaremos:

* Las partes del computador Hack.
* El modelo de programación de la CPU.
* La diferencia entre memoria RAM y registros.
* Los tipos de instrucciones del lenguaje ensamblador.
* Cómo leo el teclado y muestro en pantalla.
* Cómo implemento un bucle.
* Cómo implemento una condición.
* ¿Qué es la ALU y qué operaciones realiza?

En ["este"](https://www.nand2tetris.org/_files/ugd/44046b_7ef1c00a714c46768f08c459a6cab45a.pdf) 
enlace está la documentación del computador Hack.

``` asm
@SCREEN
D=A
@i
M=D
(READKEYBOARD)
@KBD
D=M
@KEYPRESSED
D;JNE
@i
D=M
@SCREEN
D=D-A
@READKEYBOARD
D;JLE
@i
M=M-1
A=M
M=0
@READKEYBOARD
0;JMP

(KEYPRESSED)
@i
D=M
@KBD
D=D-A
@READKEYBOARD
D;JGE
@16
A=M
M=-1
@i
M=M+1
@READKEYBOARD
0;JMP
```

:::note[🧐🧪✍️ Experimento]
Ahora experimenta. Crea un archivo llamado `program.asm` y copia el código del programa anterior. Ejecuta paso a paso el programa en el [simulador](https://nand2tetris.github.io/web-ide/cpu) así:

* Carga el programa en el simulador.
* Antes de ejecutar cada instrucción vas a predecir qué crees que va a suceder. Es muy importante 
que hagas esto, de esta manera tu mismo puedes saber si estás entendiendo el programa.
* Luego, ejecuta la instrucción y observa el resultado.
* Si te equivocas, reflexiona sobre por qué tu predicción no fue correcta.
:::

:::caution[📤 Bitácora] 
Reporta en tu bitácora de aprendizaje:
* Identifica una instrucción que use la ALU y explica qué hace.
* ¿Para qué sirve el registro PC?
* ¿Cuál es la diferencia entre @i y @READKEYBOARD?
* Describe qué se necesita para leer el teclado y mostrar información en la pantalla.
* Identifica un bucle en el programa y explica su funcionamiento.
* Identifica una condición en el programa y explica su funcionamiento.
:::
