# Express
Express es el framework web mas popular de Node, y es la libreria subyacente para un gran numero de otros frameworks populares. 
<!-- Basicamente se usa para poder levantar un servidor, hacer pedidos y enviar datos a la api -->

### **Proporciona**

* Escritura de manjadores de peticiones con diferentes verbos HTTP en diferente caminos URL (Rutas).

* Integracion de motores de renderizacion "vistas" para generar respuestas mediante la introduccion de datos en plantillas.

* Establecer ajustes en aplicaciones web como que puerto usar para conectar, y la localizabion de las plantillas que se utilizan para renderizar la respuesta.

* Añadir procesamientos de peticiones "middleware" adicional en cualquier punto dentro de la tuberia de manejo de la peticion.

### Como levantar un servidor con express

``` JavaScript

var express = require('express'); // 1.
var app = express();// 2.

app.get('/', function(req, res) { // 3.
  res.send('Hola Mundo!');
});

app.listen(3000, function() { // 4.
  console.log('Aplicación ejemplo, escuchando el puerto 3000!');
});
```

1) En la primer linea se requiere express para poder ser utilizado en nuestra app.

2) Luego definimos nuestra aplicacion, a una variable le asignamos express y le heredamos los metodos para el enrutamiento de las peticiones HTTP.

3) El metodo get() se ejecutara cuando el path sea "/", esto significara que desde el cliente quieren acceder a la pagina home de la web, get entendera que esto esta sucediendo, su funcion pasada por segundo parametro recivira el request (req) desde el cliente y luego enviara una respuesta (res) con el metodo .send(), en este caso un string.

4) El metodo .listen() se ejecuta y crea el servidor escuchado en su respectivo puerto, en este caso el 3000. Si esto sucede de forma correcta entonces en la web deberiamos poder ver el console.log con el mensaje de confirmacion.

## Verbs POST, GET, PUT and DELETE

Primero debemos entender que hay ciertas cosas imporantes para tener en cuenta, como cuales son los verbos mas comunes requeridos hoy en dia.

* Create - Crea un nuevo recurso
* Read - Lee/recive un recruso from server
* Update - Actualiza un recurso
* Delete - Deletea/borra un recurso

<<<<<<< HEAD
#### Request

El req o request es la consulta que esta haciendo el cliente, es decir, desde el path esta pidiendo algo, por ejemplo, si vos queres acceder a tu perfil en facebook, lo que vas a hacer es desde la url entrar a tu usuario, http://facebook.com/MiUsuario. El back end de nuestra app se encargara de responder con la solicitud.

#### Response

El response es el metodo que se usa para enviar lo que el request quiere, por ejemplo, res.(MiUsuario).

### POST

=======
#### POST: