### Ciclo feetch-decode-execute

El siguiente programa está escrito en el lenguaje ensamblador del computador 
Hack. Este computador no es un computador comercial, sino un computador didáctico 
que te permitirá acercarte a los conceptos fundamentales de manera amigable.

``` asm
@1 
D=A 
@2 
D=D+A 
@16 
M=D 
@END
(END) 
0;JMP
```

¿Qué crees que haga este programa? 

Para responder a esta pregunta vamos a analizarlo paso a paso usando un simulador de la CPU Hack que está [aquí](https://nand2tetris.github.io/web-ide/cpu).

Para ejecutar este programa la CPU realiza un **ciclo** constante llamado Fetch-Decode-Execute.

El ciclo Fetch-Decode-Execute describe cómo la CPU ejecuta instrucciones de un programa. Aquí está explicado 
de forma breve y simple:

Fetch (buscar): la CPU obtiene (lee) la siguiente instrucción desde la memoria. El contador de programa (PC) 
indica dónde se encuentra esa instrucción en la memoria ROM.

Decode (decodificar): la CPU interpreta la instrucción que acaba de leer. Esto significa entender qué 
operación debe realizarse y qué datos o recursos necesita.

Execute (ejecutar): la CPU realiza la operación indicada. Por ejemplo, puede ser una operación matemática, 
mover datos entre registros, o acceder a la memoria.

Este ciclo se repite continuamente mientras la computadora esté encendida, procesando instrucciones una 
tras otra. Es la base del funcionamiento de cualquier procesador.

:::note[🧐🧪✍️ Experimento]
Ahora es tu turno. Crea un archivo llamado `program.asm` y copia el código del programa anterior. 
Ejecuta el programa en el simulador de la CPU Hack y observa cómo se comporta.
¿Qué sucede? ¿Qué valor se almacena en la dirección de memoria 16? ¿Por qué crees que es ese valor?
¿Qué instrucciones se ejecutan en cada ciclo Fetch-Decode-Execute?
¿Qué cambios observas en el contenido de la memoria y los registros?
¿Qué instrucciones se ejecutan en cada ciclo Fetch-Decode-Execute?
:::

:::note[🧐🧪✍️ Experimento]
Escribe un programa en lenguaje ensablador que sume los números 5 y 10, y almacene el resultado en la dirección de memoria 20.
Utiliza el simulador de la CPU Hack para ejecutar tu programa y verifica que el resultado es correcto.
:::

:::caution[📤 Bitácora] 
* Reporta tus observaciones para cada experimento en tu bitácora de aprendizaje.
* ¿Qué diferencia hay entre los datos almancenados en la memoria ROM y en la RAM?
:::

