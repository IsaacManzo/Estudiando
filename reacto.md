# Reacto

## **Estructura de datos**

Es una forma particular de organizar datos en una computadora para que puedan ser utilizados de manera eficiente. Diferentes tipos de estructuras de datos son adecuados para diferentes tipos de aplicaciones, y algunos son altamente especializados para tareas específicas.

![No cargo la imagen](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d1/Pila.svg/1200px-Pila.svg.png)

Por ejemplo, el historial de google chrome va realizando una pila a medida que el cliente va ingresando a nuevos urls. O cuando vayamos dando rt en twitter, etc.

### **Pila/Stack**

Esta estructura organiza los datos uno arriba del otro, generando una pila, cada vez que se ingrese un nuevo dato, este mismo se coloca por encima de los datos que ya estan en la pila.

## **Big O**

los algoritmos son formas de resolver problemas o ejercicios, intentado realizar la menor cantidad de pasos, con esto lograremos tener un codigo eficiente y mejorar el **tiempo** o el **espacio** del codigo.

### **Categorias**

1) O(1)
2) O(logn)
3) O(n)
4) O(n * logn)
5) O(n^2)
6) O(n^3 n^4)
7) O(2^n)
8) O(n!)

#### **O(1)**

En (o uno) tenemos algo constante que no se ve afectado por el tamaño del input, es decir, el tiempo de ejecucion del algoritmo esta fijo, siempre va as er el mismo.

* Consante.
* No se ve afectada por el tamaño del input.

 ``` JavaScript
let max = 10
```

#### **O(logn)**

En (o logaritmo de n) se da en casos de busqueda binaria, por ejemplo, si queremos buscar un numero. Supongamos que el input es 6, y queremos encontrarlo en un array de numeros, los procedimientos seran comparar si es mayor, igual o menor que el numero root 8, en caso de ser menor entonces pasar al indice **derecho** (1 paso), por ende este sera un nuevo elemento, en este caso numeros, de ser 6 mayor que este elemento/numero entonces se dirigira para la **izquierda** (2 pasos), luego de compararce se encuentra en un nuevo elemento/numero, en este caso el numero 6, asi que el imput es el mismo que el elemento encontrado. Fin del algoritmo.

Para encontrar el elemento/numero 6, a este algoritmo le llevaria 2 pasos.


![texto_alternativo](https://i0.wp.com/somoshackersdelaprogramacion.es/wp-content/uploads/2022/05/image-35.png?resize=407%2C341&ssl=1)

La ventaja de esto es que cada vez que duplicamos la cantidad de pasos, solo se le agrega de a un paso, es decir si ahora quisieramos encontrar algun el numero 4 que esta en la hoja hija del padre 6. Pensar que ya tenemos los pasos para acceder al 6 que son, izquierda y derecha, ahora si se ingresa el input 4 seria, 4 es menor que el root 8 entonces para la **derecha** (1 paso), 4 es mas grande que 3 entonces para la **izquierda** (2 pasos), 4 es menor que 6 entonces para la **derecha** (3 pasos). Fin del algoritmo. 

Para encontrar el elemento/numero 4, a este algoritmo le llevaria 3 pasos.


