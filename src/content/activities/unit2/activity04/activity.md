#### Convierte un ciclo while en un ciclo for

**Enunciado**: considera el siguiente programa: 

``` c
//Adds 1+...+100.
 int i=1;
 int sum=0;
 
 while(i <=100){
    sum+= i;
    i++;
 }
 ```

Una traducción a ensamblador es como sigue: 

``` asm
// Adds1+...+100.
 @i // i refers to some memory location.
 M=1 // i=1
 @sum // sum refers to some memory location.
 M=0 // sum=0
 (LOOP)
 @i
 D=M // D=i
 @100
 D=D-A // D=i-100
 @END
 D;JGT // If(i-100)>0 gotoEND
 @i
 D=M // D=i
 @sum
 M=D+M // sum=sum+i
 @i
 M=M+1 // i=i+1
 @LOOP
 0;JMP // GotoLOOP
 (END)
 @END
 0;JMP // Infinite loop
```

Vamos a transformar este programa a su equivalente usando un ciclo for:

 ``` cpp
//Adds 1+...+100.
int sum=0;
for(int i = 1; i <=100; i++){
    sum+= i;
}
 ```

- Analiza los programas con while y for asegúrate de entender por qué son equivalentes.
- Convierte la versión del for a ensamblador.
- No olvides comprobar el funcionamiento de los programas en ensamblador en el simulador.
- Compara las versiones en ensamblador del while y del for. ¿Qué puedes concluir?

:::caution[📤 Bitácora] 
Escribe en tu bitácora el programa en ensamblador y las conclusiones que has sacado de la comparación entre los dos programas.
:::

