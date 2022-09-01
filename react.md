# **React**

Es una libreria con codigo abierdo de JS, que sirve para construir interfaces de usuario (UI) de forma sencilla y declarativa, a traves de componentes.

## **JSX**

Es una extension de la sintaxis de JS que te permite armar bloques de codigo visuales.

## **Babel**

Es un "compilador" o traductor open source que convierte el codigo JSX en codigo JS, de forma que el browser lo pueda interpretar.

# **Como se conforma react**

React esta ligado al HTML mediante un id llamado root, este enlace se ubica en el archivo indes.js de la carpeta donde se ubique el front.

## **Componentes**

Permiten dividir la UI en piezas independientes y a su vez reutilizarlos.
Podriamos crear un componente para el header, boton, footer, etc.

Los componentes pueden referisrse a otros comonentes en su salida.

## **Expresiones en JSX**

En la sintaxis de JSX podemos agregar elementos al DOM de forma mas dinamica.

``` JavaScript
let fruta = ["Banana", "Pera", "Manzana"]

<li>{fruta[0]}</li> 
// "Banana"
<li>{fruta[1]}</li> 
// "Pera"
<li>{fruta[2]}</li> 
// "Manzana"
```

## **Components**

Aca vamos a crear los componentes y luego los importamos donde queramos usarlos.

## **Props**

Los componentes son funciones de JS, aceptan inputs arbitrarios (props) y retornan elementos que representan lo que deberia apracere en pantalla.

Los props se pasan como si fueran arbitarios de HTML.

``` JavaScript
let frutas = ["Banana", "Manzana"]
<list frutas = {frutas}>
```

## **Estilos JSX**

Se puede agregar estilos CSS.

1) Utilizando el atributo className (en archivo indes.css).

2) De manera inline con el atributo style (en archivo de componentes).

### **Sintaxis para agregar componentes**

