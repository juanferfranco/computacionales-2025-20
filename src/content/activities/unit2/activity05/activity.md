##### Punteros

Un puntero es una variable que almacena la dirección de memoria de otra variable. Observa el siguiente programa escrito en C++:

``` cpp
int a = 10;
int* p;
p = &a;
*p = 20;
```

El programa anterior modifica el contenido de la variable **a** por medio de la variable **p**. **p** es un puntero porque almacena la dirección de memoria de la variable **a**. En este caso el valor de la variable **a** será 20 luego de ejecutar *p = 20;. 

Ahora analiza con detenimiento:

- ¿Cómo se **declara** un puntero en C++? 

``` cpp
int* p;
```

**p** es una variable que almacenará la dirección de otra variable. Dicha variable almacenará número enteros.

- ¿Cómo se **define** (nota que antes preguntamos cómo se **declara**) un puntero en C++? 

``` cpp
p = &a;. 
```

Definir el puntero es **inicializar** el valor del puntero, es decir, guardar la dirección de una variable. En este caso p contendrá la dirección de a o podemos decir que p apunta a **a**

- ¿Cómo se almacena en C++ la dirección de memoria de una variable? Con el operador **&**. 

``` cpp
p = &a;
```

- ¿Cómo se escribe el contenido de la variable a la que apunta un puntero? Con el operador *. 

``` cpp
*p = 20;
```

En este caso como **p** contiene la dirección de **a**. Por tanto, se está modificando el valor 
de la variable **a** por medio de **p**.

Ahora vas a usar un puntero para leer la posición de memoria a la que este apunta, 
es decir, vas a leer por medio del puntero la variable cuya dirección está almacenada en él.

``` cpp
int a = 10;
int b = 5;
int *p;
p = &a;
b = *p;
```

En este caso: 

``` cpp
b = *p;
```

el código anterior hace que el valor de b cambie de 5 a 10 porque p apunta a **a** y con *p a la derecha del igual estás leyendo el contenido de la variable apuntada.


:::caution[📤 Bitácora]
Convierte estos programas a ensamblador y realiza la simulación paso a paso.
Recuerda la metodología: predice, ejecuta, observa y reflexiona.

``` cpp
int a = 10;
int* p;
p = &a;
*p = 20;
```

``` cpp
int a = 10;
int b = 5;
int *p;
p = &a;
b = *p;
```
:::