# **CHAKRA UI**

## **Install npm**

Para iniciar chakra primero se debe instalar la libreria.

 ``` JavaScript
npm i @chakra-ui/react @emotion/react @emotion/styled framer-motion
```
## **Lineas dentro del codigo**

Para implementar Chakra se debe acceder a la carpeta index.js dentro de las carpetas de front.

Aqui estara renderisado el componente App que contiene todo el jsx del codigo.

Luego de instalar se debe colocar el componente Provider por fuera de App, de esta forma se renderisara Chakra.

 ``` JavaScript
// 1. Primero importar react
import React from "react";
// 2. El componente App creado
import App from "./App";
// 3. ReactDom es le que se encarga de creaer y apuntar al componente root (App)
import ReactDOM from "react-dom/client";
// 4. Importamos el provider `ChakraProvider`
import { ChakraProvider } from '@chakra-ui/react'

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(
    <ChakraProvider>
      <App />
    </ChakraProvider>
);
// 5. Tuki
```

## **Componentes** y sus **props** para dar estilos

El css se le asigna por las props

 ``` html
 <Componentes props="" />
```

En este link estan todas las props que se les puede asignar a los componentes https://chakra-ui.com/docs/styled-system/style-props

