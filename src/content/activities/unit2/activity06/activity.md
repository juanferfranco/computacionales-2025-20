#### Experimenta con arreglos

Los arreglos son colecciones de datos en la memoria. 

Considera el siguiente programa

``` cpp

int arr[] = {1,2,3,4,5,6,7,8,9,10};
int sum = 0;

for (int j = 0; j < 10; j++) {
    sum = sum + arr[j];
}

```

:::caution[📤 Bitácora]
- Implementa el programa anterior en lenguaje ensamblador aplicando el concepto de punteros.  
- Considera que los datos del arreglo están almacenados **desde** la dirección 16. Inicializa 
el arreglo en lenguaje ensamblador.  
- Simula paso a paso el programa en ensamblador. Recuerda la metodología: predice, ejecuta, observa y reflexiona.  
- Construye tu programa PASO A PASO mediante pruebas. Indica qué característica vas 
a implementar con cada prueba y cómo la probaste.
- Muestra el programa final y cómo lo probaste. 
:::
