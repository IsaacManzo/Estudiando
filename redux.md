# Redux

## **Configuracion**

### **Setear la Store**

Primero debemos crear una carpeta llamada state dentro de la carpeta front, aqui es donde configuraremos la store.

![No cargo la imagen](https://cdn.discordapp.com/attachments/991322622660976670/1033409316486664332/unknown.png)

Aca se crea una store SUPER basica, lo minimo fundamental para poder enlazarla con React.

``` JavaScript
// 1. Importamos el creador de la store
import { configureStore } from "@redux/toolkit"

// 2. Creamos el reducer
function reducer(state, action){
    return state:
}

// 3. Declaramos la store en una constante y la creamos con configureStore
const store = configureStore({ reducer })

// 4. Exportamos la store
export default store:
```

### **Unir Redux con React**

Dentro del index.js principal del front.

``` JavaScript
import App from ""
// 1. Importamos Provider, sera el que proporciona la conexion entre los controladores,estados y reducers con React 
import { Provider } from "react-redux"

// 2. Importamos la store
import store from "./state/store"

// 3. Declaramos la cosntante app que contendra toda la estructura del front 
const app + (
    // 4. Encerramos a App dentro del Provider para crear la conexion y le indicamos la store a la cual tiene que enlazar
    <Provider store={store}>
     <App />
    </Provider>
)

ReactDOM.render(app, document.geteElementId("root"))
```

### **Creando un action y un reducer**

Dentro de la carpeta state es donde iniciaremos nuestro estados, en este caso el estado es un array con objetos que contiene la fake data de aeropuertos.

``` JavaScript
import { createAction, createReducer } from "@reduxjs/toolkit"

import FakeData from "../utils/fake-data"

export const setAirports = createAction("SET-AIRPOSRTS ")

const initialState = FakeData.getAirports()

const reducer = createReducer(initialState, {
    [setAirports]: (state, action) =>{
        const options = FakeData.getAirports()
        if (action.payload === "All") return options
        return options.filter((opt) => opt.region === action.payload)
    } 
})
```


## **Como esta conformado Redux**

### **Reducer**

Los reducers son como tomar algo de entrada y convertirlo en otra cosa, dependiendo de la accion que recivan.

``` JavaScript
let newState = reducer (state, action)
```

## Palabras clave

### **Action/Action**

Una action es en realidad un objeto que actualiza un evento ocurrido.

### **State/Estado**

Un state es un valor que se desea actualizar, este cambiara dependiendo las acciones que le pasemos.

### **Type/Tipo**

El type recive siempre una accion, type va a indicar siempre que accion se desea ocacionar al state.

### **newState/nuevoEstado**

Este nuevo estado sera el que va a contener al nuevo valor.

``` JavaScript
const counterReducer = (state, action) =>{ // 1.
    const {type} = action // 2.
    if(type === "@counter/incremented"){ // 3. 
    return state +1 // 4.
    }
}

const actionIncremented = { // 5.
    type: "@counter/incremented" // 6.
}

counterReducer = (0, actionIncremented) // 7.
```

## Explicacion linea por linea

### **Reducer**

1) Definimos el reducer, este recibe dos parametros, un state/estado y una action/accion.
2) Que type/tipo de action/accion llego.
3) Un condicional que valida la action/accion.
4) Y por ultimo la actualizacion.

### **Action**

5) Definimos la action/accion, en este caso la de incrementar.
6) Definimos el type/tipo de action/accion.

### **Action y Reducer**

7) El reducer recibe un state/estado (0), pero con es action/accion queremos incrementarlo.

## Agrear mas actions/acciones

A la vez podemos agregar mas acciones, como esta, que dara la action/accion de decrementar el state/estado

``` JavaScript
const actionDecremented = {
    type = "@counter/decremented"
}
```

Para que esta action/accion pueda ser ejecutada, debemos actualizar el reducer, para esto tendremos que agregar un nuevo condicional

``` JavaScript
if(type = "@counter/decremented")
```

## Actualizar el valor de state/estado constantemente

Por ultimo podriamos pasar el nuevo estado por parametro, de esta forma el reducer no siempre va a recibir un 0, sino el state/estado actualizado.

``` JavaScript
const newState = contadorReducer (0, actionIncremented) 
// State/estado ahora vale 1

counterDecremented = (newState, actionDecremented)
```

## El verdadero condicional

De todas formas nunca se utilizan los condicionales if() como en este ejemplo. Sino dos palabras switch()/cambio() y case/caso.

## Palabras clave

### **switch()/cambio**()

El cambio sera la nueva action/accion y type/tipo que se querra cambiar.

### **case/caso**

Sera el caso que se desea comparar, esto es lo que hacia if antes.

``` JavaScript
switch(action, type){ // 1.
    case "@counter/incremented" // 2.
    return state +1 // 3.
    case "@counter/decremented"
    return state -1
    
    default // 4.
    return state
}
```

## Explicacion linea por linea

1) En caso de que la action/accion sea de este tipo.

2) Si la action/accion es esta, entonces ejecuta algo. 

3) En caso de que no se encuentre ninguna action/accion, retorna el state/estado default.

# Funcionamineto


![No cargo la imagen](https://www.freecodecamp.org/news/content/images/2022/06/2.png)

## **Store**

La store es un objeto que reune las actions/acciones y los reducers.

### **Las responsabilidades de store:**

- La responsabilidad de contener el state/estado de la aplicacion

- Permite leer el state/estado de la estado de la aplicacion.

- Permite actualizar el estado de la aplicacion.

Va a ser la store, la que tenga la responsabilidad de llamar a reducer

### **Pasos a seguir**

Arrancamos importando:
``` JavaScript
import { createStore } = from "redux"
```

Luego store toma al reducer:

``` JavaScript
const store = createStore(counterReducer)
```

Luego dispatch() es el que enviara las acciones:

``` JavaScript
store.dispatch({type: "@counter/incremented"})

// o sino

store.dispatch({type: "@counter/decremented"})
```

con getState() obtenemos el state/stado en su estado actual.

``` JavaScript
getState()
```

Vamos a suscribir que cada cambio que tenga la store, vuelva a realizar la aplicacion.

``` JavaScript
const renderApp = () =>{
    ReactDOM.render(
        <App />
        document.getElementById("root")
    )
}

renderApp()
store.subscribe(renderApp)
```

