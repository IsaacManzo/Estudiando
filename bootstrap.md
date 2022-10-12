# **Bootstrap**

## **¿Qué es bootstrap?**

Bootstrap es un **framework** de **css**, utiliza plantillas **html** prediseñadas y con estilos prediseñados. Solo se debe copiar el codigo y el componente sera creado dentro de nuestra app.

# **Grid/Grilla**

Bootstrap esta conformado por **grillas**, estas grillas ocupan un ancho respectivo de la pagina. Para entender mejor este concepto hay que pensar en que una grilla puede ser fraccionada hasta **12** veces. Dependiendo que caracteristica le agregemos a cada **row**, seran las cantidad de **columns** que va a tener ese componente.

Existen 6 rows distintas con sus medidas, cada row tiene sus **columnas** maximas y sus **pixeles** respectivos, al disminuir sus pixeles esta row se rompe. Las rows se indican por medidas **xxl**, **xl**, **lg**, **md**, **sm**, **xs**.

**Depende de nosotros saber cual usar dependiendo para que pantalla se va a ver nuestra app, ya sea celular, notebook, tablet, etc**.

### **col-xxl-1** / 12 espacios / 1400px

![No cargo la imagen](https://media.discordapp.net/attachments/991322622660976670/1029757232268722216/unknown.png)

### **col-xl-2** / 6 espacios / 1200px

![No cargo la imagen](https://media.discordapp.net/attachments/991322622660976670/1029758903820484668/unknown.png)

### **col-lg-3**  / 4 espacios / 992px

![No cargo la imagen](https://media.discordapp.net/attachments/991322622660976670/1029759518831284274/unknown.png)

### **col-md-4** / 3 espacios / 768px

![No cargo la imagen](https://media.discordapp.net/attachments/991322622660976670/1029759770976063579/unknown.png)

### **col-sm-6** / 2 espacios / 576px

![No cargo la imagen](https://media.discordapp.net/attachments/991322622660976670/1029760207234007080/unknown.png)

### **col-xs-12** / 1 espacios / 576px

![No cargo la imagen](https://media.discordapp.net/attachments/991322622660976670/1029760308409020596/unknown.png?width=449&height=702)

## **Como asignar estos valores**

A cada componente que creemos le debemos asignar su respectiva medida, para esto hay que asignarlo al className.

Con **fluid** le asignaremos siempre el 100% de la pantalla.

 ``` html
 <div className="container" >Content</div>
 <div className="container-sm" >Content</div>
 <div className="container-md" >Content</div>
 <div className="container-lg" >Content</div>
 <div className="container-xl" >Content</div>
 <div className="container-xxl" >Content</div>
 <div className="container-fluid" >Content</div>
```

![No cargo la imagen](https://media.discordapp.net/attachments/991322622660976670/1029765821662244864/unknown.png)

### **Asignar mas de un valor**

Nosotros podemos asignar mas de una propiedad de tamaño, esto se hace para que el contenedor sea lo mas responsive posible para cada tamaño de pantalla donde se vera el front de nuestra app. Para esto tendremos que pasarle el tamaño y luego la cantida de columnas (siempre respetando el maximo de 12).

 ``` html
 <div className="container-lg-8 container-md-6" >Content</div>
 <div className="container-lg-4 container-md-6" >Content</div>
```

En pantallas lg se veran dos columnas, una de 8 y otra de 4, en cambio, en pantallas de md se veran dos columnas de 6.

### **Centrar cosas**

Podemos centrar contenedores para donde nosotros querramos, para esto debemos asignarle estos valores a cada row.

![No cargo la imagen](https://cdn.discordapp.com/attachments/991322622660976670/1029774487480180757/unknown.png)

1) className="row justify-content-**start**"
2) className="row justify-content-**center**"
3) className="row justify-content-**end**"
4) className="row justify-content-**around**"
5) className="row justify-content-**between**"
6) className="row justify-content-**evenly**"

### **Eliminar o asignar el padding**

Para eliminar el padding de un contenedor, ya sea en el eje x o en el eje y, se usa la propiedad **gx-n o gy-n**.

 ``` html
 <div className="container gx-1" >Content</div>
 <div className="container gy-1" >Content</div>
```

# **Buttons/Botonoes**
