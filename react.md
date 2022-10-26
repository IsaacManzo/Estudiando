# **React**

Es una libreria con codigo abierdo de JS, que sirve para construir interfaces de usuario (UI) de forma sencilla y declarativa, a traves de componentes.

### **JSX**

Es una extension de la sintaxis de JS que te permite armar bloques de codigo visuales.

### **Babel**

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

### **Props**

Los componentes son funciones de JS, aceptan inputs arbitrarios (props) y retornan elementos que representan lo que deberia apracere en pantalla.

Los props se pasan como si fueran arbitarios de HTML.

``` JavaScript
let frutas = ["Banana", "Manzana"]
<list frutas = {frutas}>
```

### **Sintaxis para agregar componentes**

<Header />

Estos componentes se deberan ubicar dentro de la constante App,  en el archivo App.js.

``` JavaScript
import //todos los imports comienzan en la linea 1

function App() {
    const { drinks } = menu // menu sera un arr de objetos, en el contendra drinks

    comst driksList = drinks.map((drink) => {
        return (
          <li>
            <strong>{ dirink.name }</strong>
            <strong>{ dirink.name }</strong>
            <strong>{ dirink.name }</strong>
          </l1>  
        )
    })
       return(
        <div>
          <ul>{ drinkList }</ul>
        </div>
       )
}
```

Map() Itera los objetos, y los muestra segun el parametro que elijamos.

## **React router**

Es una tecnologia 100% front-end que permite establecer rutas en nuestra App y lograr que , cuando una URL coincida con el path asociado a un componente, este ultimo se renderice.

``` JavaScript
import "./App.css";
import Register from "./components/Register";
import Login from "./components/Login";
import Home from "./components/Home";

import { Route, Routes } from "react-router";

function App() {
  return (
    <div>
      <Navbar />
      <Routes>
        <Route path="home" element={<Home />}/>
        <Route path="/" element={<Home />} />
        <Route path="register" element={<Register />} />
        <Route path="login" element={<Login />} />
      </Routes>
    </div>
  );
}
```

## **ReactDOM**

Renderiza el codigo que usemos y se muestra reflejado en el browser.

``` JavaScript
import React from "react";
import ReactDOM from "react-dom/client";
import { BrowserRouter } from "react-router-dom";
import App from "./App";

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(
  <BrowserRouter>
    <React.StrictMode>
      <App />
    </React.StrictMode>
  </BrowserRouter>
);
```

### **Fake data o Data**

La fake data se trae en forma de objeto.

Para mostrar esta Data en tu App, se debe colocar en el archivo principal.

``` JavaScript
<ul>
    { fakePlaylist.map ((playlist) => 
      <li>
         <a>{ playlist.name }</a>
      </li>
    )}
</ul>
```

# **Estructura de una App en React**

## **Components y commons:**

Los componentes son aquellos bloques de codigo que qedan estaticos en la pagina y no se modifica su posicion. Como por ejemplo el footer, header, navbar,etc.

Los commons en cambio son bloques de codigo que se usan en varios componentes, y se puede utilizar.Como por ejemplo, un carrito de compras es un componente que contiene productos, osea, commons.

A su vez cada componente va a tener archivos separados con cada uno de ellos. Luego estos seran exportados y importados dentro de la carpeta App. Y asi poder renderizarlo.

## **Eventos:**

Un evento es cualquier accion que el usuario haga dentro del browser, como hacer un click y que retorne algo.
Dentro del componente este evento se debe colocar en forma de prop.

``` JavaScript
function handleSubmit() {
    alert("Apretaste click en este boton")    //se ejecuta la accion
}

<button onClick = { handleSubmit }>Submit</button>
```

## **Estados:**

Para actualizar nuestros componentes en react, usaremos estados. Estos tienen un valor inicial y mutan segun la logica planteada.

``` JavaScript
import {useState} from "react"

const [contador, setContador] = useState(0)

<div>
    <p>Tu cliqueaste { contador } veces</p>
    <button onClick={( => setContador(contador + 1))}>
    Click me
    </button>
</div>
```

Cada vez que se le de un click al boton, al estado se le sumara + 1.
