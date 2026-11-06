### Objetivos

En este módulo, aprenderás:
- Cuáles son los mensajes HTTP.
- Qué es el modelo cliente-servidor.
- Qué significa el "Error 404".
- Qué es una API y cómo se consume.
- Qué es `jQuery`.
- Qué es AJAX, JSON y XML.

Al finalizar este módulo, podrás poner en práctica tus conocimientos con los ejercicios y el proyecto integrador final (***Weather Channel***).

---

### ¿Qué Es HTTP?

Como vimos al principio del curso, Internet es una red de redes, conectada por miles de nodos que se comunican entre sí.

![imagen-nodos.jpg](https://i.imgur.com/zqVPHXU.jpg)

Para que la transferencia de información sea posible, es preciso que se cumplan ciertas normas; es decir: un protocolo. 

El protocolo usado para transferir información en la web es **HTTP** (siglas en inglés de _Hypertext Transfer Protocol_ o, en castellano, Protocolo de Transferencia de hipertexto).

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">🤓 Según <em>Wikipedia</em>, "HTTP define la sintaxis y la semántica que utilizan los elementos de <em>software</em> de la arquitectura <em>web</em> (clientes, servidores, <em>proxies</em>) para comunicarse".<br></p>


#### Mensajes HTTP

Dentro del protocolo **HTTP** existen 2 tipos de mensajes: por un lado, el pedido que hace el cliente (llamado ***Request***)  y, por el otro, la respuesta que envía el servidor (llamado ***Response***).


#### _Requests_

Dentro de los _Requests_ existen distintos métodos que indican qué tipo de pedido haremos al servidor. Veamos qué verbos usan estos métodos para especificar lo que solicitan: 

  | Verbo | Descripción |
| ----------- | ----------- |
| **GET** | Sirve para obtener datos. |
| **POST** | Le dice al servidor que necesita guardar información. |
| **PUT** | Indica que se quiere editar información. |
| **DELETE** | Sirve para eliminar algo de la base de datos. |

En este módulo nos centraremos en el verbo **GET**.

![imagen](https://i.imgur.com/JrBOsej.jpg)

---

### Modelo Cliente - Servidor

El **Modelo Cliente - Servidor** refiere a la interacción entre el cliente y el servidor.

⚠️ **Importante:** El cliente puede ser uno o varios.

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">👩‍🏫 Un <b>cliente</b> puede ser una computadora, un teléfono celular, una tablet, etc. <b>conectada a Internet</b>.<br>
Un <b>servidor</b>, en cambio,  es una computadora que almacena las páginas <em>Web</em> y que tiene medios para enviarlas a los clientes.
</p>

#### ¿Cómo Funciona Una Página ***Web***?

A grandes rasgos, una página _web_ funciona de la siguiente manera:

- El cliente usa un navegador (como _Chrome_, por ejemplo).
- El cliente realiza una petición al servidor a través de _internet_ (por ejemplo, haciendo _click_ en un _link_).
- El servidor recibe el pedido, elabora la respuesta y se la envía al cliente.
- El navegador del cliente recibe esa respuesta  y muestra el contenido en pantalla.

![client-server.png](https://i.imgur.com/0OzgkNQ.png)

#### Servidores

Los servidores tienen este nombre porque están al servicio de otras computadoras. 

Como gestionan los recursos de una red, deben permanecer siempre encendidos. Si un servidor se apaga, o tiene errores, genera que los usuarios de la red tengan problemas, ya que no podrán disponer de sus servicios.

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">🤓<b>¿Sabías qué...?</b>
En líneas generales, los servidores operan sin ninguna intervención manual y solo deben ser configurados inicialmente.<br></p>


![Google-Centro-Datos.jpg](https://pledu-plataforma5.s3.amazonaws.com/5bc731d2-55f7-4462-b8e1-86e32484242e/Google-Centro-Datos.jpg)


#### Códigos Para HTTP _Response_

Cuando el servidor responde, además de enviar los datos pedidos, siempre genera un código numérico (de 3 dígitos) que representa el estado de la acción realizada.

El primer dígito de cada código nos da la información necesaria para entender cómo se ejecutó esa acción:

- **1:** Es una petición que devuelve información acerca del servidor.
- **2:** La operación fue satisfactoria.
- **3:** La operación se redirigió a otro sitio (otra dirección URL).
- **4:** Hay un error en el pedido del cliente. Es decir, el _Request_ generado tiene algún error.
- **5:** Hubo un error en el servidor y no se ejecutó satisfactoriamente la acción solicitada (por ejemplo, si el servidor se quedó sin espacio en el disco).

+++ ¿Qué Significa El Famoso "Error 404"?

El **Error 404** es uno de los errores más comunes que ocurren cuando navegamos en internet. Este tipo de error indica que hay un enlace roto, defectuoso o que ya no existe.

<video autoplay loop>
<source src="https://i.imgur.com/CccCxW8.mp4">
</video>

[code404](https://i.imgur.com/CccCxW8.mp4) 

_Google_ penaliza las páginas _web_ que tienen muchos enlaces con el Error 404. Los rastreadores de _Google_ interpretan que la página no está siendo revisada con frecuencia y que, por lo tanto, su mantenimiento es deficiente.

+++

---

### ¿Qué Son Las API?

Las API (del inglés  _Application Programming Interface_ o, en castellano, Interfaz de Programación de Aplicaciones) son, básicamente, un **conjunto de reglas que definen cómo se comunican dos aplicaciones entre sí**.

Mirá este video para aprender más acerca de ellas:

@youtube=uNZlk3F_N7E

Recapitulando, las API son como un puente que comunica 2 aplicaciones. Es decir, una API permite el traspaso de información y, a su vez, permite recibir retroalimentación de qué fue lo que sucedió con el requerimiento. 

Para usar una API de manera sencilla, utilizaremos la librería **jQuery**. 

#### ¿Qué Es jQuery?

*jQuery* es una de las librerías más populares de *JavaScript*. Es decir, es un archivo de JavaScript que tiene métodos y propiedades que podemos usar en nuestro _script_. 

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">📚 <em>jQuery</em> nos permite seleccionar, manipular y crear elementos; agregar <em>event listeners</em>; crear animaciones y efectos y utilizar otras funcionalidades que vamos a aprender en este módulo.<br></p>

<!--🤓 **Tip**: Podés ver las más de [9000 líneas de código de _jQuery_](https://code.jquery.com/jQuery-2.1.4.js) o tener [una documentación](https://oscarotero.com/jquery/) que te ayude a encontrar qué querés hacer.-->

#### Cómo Agregar _jQuery_

Al igual que con _Bootstrap_, hay 2 maneras de agregar _jQuery_ a una página.

1. [Descargarla](https://code.jquery.com/jquery-3.5.1.min.js) para usarla de forma local, usando el atributo `src`:

```html
<script src="jquery-3.5.1.min.js"></script>
```

2. Usarla desde un CDN (es decir, una copia online), especificando su ruta con el atributo `src`:

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
```

⚠️ **Importante:** Colocá siempre el `script` de jQuery antes de tu `script`.

📛 Para saber si agregaste correctamente jQuery en tu documento, escribí _jQuery_ en la consola. Si no te devuelve un error significa que está todo bien. 🥳

---

### AJAX

📚 **AJAX** (del inglés _Asynchronous JavaScript And XML_ o, en castellano, JavaScript Asíncrono + XML) **es un término que describe una forma de utilizar varias tecnologías existentes**: HTML o XHTML, CSS, JavaScript, DOM, XML, XSLT y el Objeto XMLHttpRequest.

En pocas palabras, **AJAX permite interactuar con otros servidores usando JS, sin tener que recargar la página.** Así, podemos crear aplicaciones _web_ más complejas. Por ejemplo, _Gmail_ nos permite leer, escribir y recibir _e-mail_ sin tener que actualizar la página cada vez.

🔍 Para leer más sobre AJAX, accedé a la documentación de [Mozilla](https://developer.mozilla.org/es/docs/Web/Guide/AJAX).

---

### Cómo Devolver Información: XML O JSON

Cuando hablamos de consumir una API, los servidores nos devuelven información en formatos muy distintos.

Estos pueden ser **XML** o **JSON**. 

Veamos las principales características de ambos.

#### 📚 XML 

**XML** (del inglés _Extensible Markup Language_) es uno de los formatos tradicionales más usados para enviar datos. 

XML es un lenguaje de etiquetas, al igual que HTML. A diferencia de este último, podemos definir nuestras propias etiquetas.

Veamos un ejemplo:

```html
<empresa>
    <id>1</id>
    <nombre>Plataforma 5</nombre>
    <sector>Educación</sector>
</empresa>

```

Podemos customizar las etiquetas para identificar un conjunto de datos en formato de texto (`<sector>`, `<empresa>`, etc.).


#### 📚 JSON

**JSON** (del inglés _JavaScript Object Notation_) es hoy por hoy el formato más utilizado para transferir información.

JSON es muy fácil de entender y manipular, ya que posee un formato muy parecido a la sintaxis de un Objeto de JavaScript.

Siguiendo el ejemplo anterior:

```js
{
    "id": 1,
    "nombre": "Plataforma 5",
    "sector": "Educación"
}
```

En síntesis, los servidores nos devuelven la misma información pero en diferentes formatos. En el caso de XML, será en formato de etiqueta; en el de JSON, en formato clave-valor.

⚠️ **Importante**: Antes de consumir una API, revisá su documentación para determinar si el código devuelto estará en formato XML o JSON.


+++
 
[Json Crack](https://jsoncrack.com/) es una herramienta que te permite visualizar tus datos JSON en forma de gráfico. Puede resultarte de mucha utilidad, ahora o en un futuro.
 
+++


#### Consumir Una API

Probá el siguiente código en tu consola:

🛎 **Recordá**: Vas a necesitar jQuery.


```js
$.getJSON("https://api.openweathermap.org/data/2.5/weather?q=San%20Francisco&appid=95176c8edea30e33338e0eaddd53a916&units=metric&lang=es", function(data) {
    console.log(data)
})
```

Los métodos `$.getJSON()` o `jQuery.getJSON()` nos permiten obtener la respuesta de cualquier API en formato JSON.

En este caso, el argumento `data` dentro de la Función _callback_ posee la respuesta en formato JSON. En este sentido, si quisiéramos imprimir en la consola (_loguear_) la temperatura, deberíamos ingresar lo siguiente:

```js

$.getJSON("https://api.openweathermap.org/data/2.5/weather?q=San%20Francisco&appid=95176c8edea30e33338e0eaddd53a916&units=metric&lang=es", function(data) {
    console.log(data.main.temp)
})

```

#### Para Pensar

Copiá la siguiente URL en tu _browser_ para ver la respuesta de la API en formato JSON:

[https://api.openweathermap.org/data/2.5/weather?q=San%20Francisco&appid=95176c8edea30e33338e0eaddd53a916&units=metric&lang=es](http://api.openweathermap.org/data/2.5/weather?q=San%20Francisco&appid=95176c8edea30e33338e0eaddd53a916&units=metric&lang=es).

¿Qué representa el `%20` en la _Query String_?

+++ 

Probá en la consola `encodeURI("San Francisco")`

+++



|||

El código `%20` reemplaza los espacios vacíos en una URL.

|||

---

### Ejercicio Aprobado Por Chuck Norris

En este ejercicio, trabajarás con [chucknorris.io](https://api.chucknorris.io/), una **API JSON** gratuita que te permitirá obtener chistes aleatorios sobre [Chuck Norris](https://en.wikipedia.org/wiki/Chuck_Norris).

![meme.jpg](https://pledu-plataforma5.s3.amazonaws.com/5bc731d2-55f7-4462-b8e1-86e32484242e/meme.jpg)

#### Cómo Usar La API

Para obtener un chiste aleatorio en formato **JSON**, debés hacer un **GET** a la API de Chuck Norris: [https://api.chucknorris.io/jokes/random](https://api.chucknorris.io/jokes/random).

Una respuesta, por ejemplo, puede ser:

```js
{
"icon_url" : "https://assets.chucknorris.host/img/avatar/chuck-norris.png",
"id" : "2XT9x9o9RDG7BCNco5Mdvg",
"url" : "https://api.chucknorris.io/jokes/2XT9x9o9RDG7BCNco5Mdvg",
"value" : "Leaving a criminal in the same room as Chuck Norris is considered cruel and unusual punishment."
}
```

⚠️ **Importante:** Como la clave `value` posee el chiste, deberás obtener su valor para usarlo en tu página.

#### ¡A Trabajar! 

##### Parte 1: HTML

1. Para empezar, creá un nuevo documento HTML y, dentro suyo, agregá un `<div>` con `class="container"`.

2. Dentro del `<div>`, agregá: 
  
  * Un _tag_ `img` con la siguiente imagen:
  [https://i.imgur.com/hLldhia.png](https://i.imgur.com/hLldhia.png).

  * Un `<h1>` con el texto: **Aprobado por Chuck Norris**.
  
  * Una etiqueta `<button>` con el texto **ACTUALIZAR** entre medio del _opening_ y el _closing tag_.
  
  * Una etiqueta `<h2>` sin contenido (acá, se agregarán los chistes tomados de la API). 
  
##### Parte 2: CSS

Ahora, deberás darle estilo a tu página:

1.  Para empezar, dale un color de fondo al `<body>`. 
2. Centrá todos los elementos del sitio. 

+++

🤓 Deberás centrar al `div class="container"` y a todos los elementos que se encuentren dentro de este `<div>`.

+++

3. Dale un estilo al botón.

4. Dale un marco punteado al chiste recibido.

+++

Si querés, usá este código:

```css

h2 {
    text-align: center;
    padding: 10px;
    border: 2px black dashed;
}

```

+++

##### Parte 3: JavaScript

Ahora, deberás llamar a la Función `getJSON`. Para eso, le pasarás la URL de la API como primer argumento y, como segundo, una Función Anónima.

+++

La Función Anónima se encargará de insertar el texto que llegue en la clave `value` dentro del `<h2>`, usando `textContent`.

+++

Luego, deberás aplicar un evento para que cada vez que se haga click en el botón "Actualizar", se presente un nuevo chiste  dentro del `<h2>`. 

Si todo funciona bien, tu página debería ser similar a esta:

![chuck.png](https://i.imgur.com/7umxbGn.png)

---

### ***Weather Channel***

¡Te damos la bienvenida al último proyecto integrador de este curso!

En este proyecto armarás un sitio para mostrar las condiciones meteorológicas de cada ciudad. Para eso, interactuarás con la API del _Weather Channel_ que viste en la sección anterior.

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

⚠️ **Importante**: En este proyecto trabajarás únicamente con el _script_ de la página. Podés inspeccionar y usar este [***template***](https://weather-channel.netlify.app) para el HTML y el CSS.

</div>




Así se verá el proyecto terminado:

<img src= "https://i.imgur.com/qXmaHyh.png" width = "350px" > 



Como viste en el ejemplo, los elementos que mostrarás en tu página son:

- Ciudad.
- Temperatura actual.
- Un ícono que ilustre la condición climática.
- Una descripción breve del clima.

Para hacerlo, seguí este **Paso a Paso**:

1. Vinculá un archivo JavaScript a tu documento HTML y dentro del `.js` creá una Función llamada `cargarCiudad`.

2. Dentro de la Función hacé un pedido AJAX que traiga la información de la ciudad de Buenos Aires y la muestre en la consola.

+++

🛎 **Recordá**: Usá `$.getJSON` para hacer un pedido AJAX.

+++

3. Obtené la referencia al botón y agregá un `eventListener` para que, cuando el usuario haga _click_, se dispare un pedido AJAX con la información de la ciudad elegida.

  🤓  **Tip:** Guardá en la Variable `ciudad` el valor de la ciudad ingresada en el `input`. Luego, concatená esta Variable a la URL de la API. Probá con alguna de las _Keys_ (**si no funciona una, probá con alguna de las otras**):
  

***KEY I***
```js

"https://api.openweathermap.org/data/2.5/weather?q=" + ciudad +"&appid=fdd533266e28101881f610f2b8f1ebe1"

```

***KEY II***
```js

"https://api.openweathermap.org/data/2.5/weather?q=" + ciudad +"&appid=1a9b3670ada3ece0551373f7325e028d"

```

***KEY III***
```js

"https://api.openweathermap.org/data/2.5/weather?q=" + ciudad +"&appid=dcec7df661b1e6b0edab51d796b7339c"

```

4. Por defecto, el CSS del proyecto no muestra el `<div class="container">`. Agregá la siguiente línea de código dentro de la Función para hacerlo visible, una vez que el usuario aprete el botón:

```js

document.querySelector(".container").style.visibility = "visible"

```

5. Para mostrar en la pantalla el nombre de la ciudad (ingresado en el `input`), asignale al `span` con el `id="ciudad"` el valor de la Propiedad `name` de la respuesta recibida. Para eso, usá la Propiedad `textContent`.
 
|||

```js
document.querySelector("#ciudad").textContent = data.name
```

|||

6. Seguí el mismo criterio para tomar la temperatura actual de la ciudad.

+++ ¿Celsius o Fahrenheit?

La temperatura llega en la escala Celsius (°C). Podés verlo en la URL del _Open Weather Map_, en la expresión `units=metric`.

+++

7. Para obtener el símbolo de Celsius (°C) al lado de la temperatura, concatená este _String_: `<sup>°C</sup>`.

  🤓  **Tip:** Usá `innerHTML`.

8. Agregá el ícono que ilustre la condición climática. Para eso, concatená la URL de la ubicación de la imagen con la del nombre de la imagen. Para acceder a la lista completa de condiciones climáticas, hacé _click_ [acá](https://openweathermap.org/weather-conditions).

9. Obtené la descripción del clima actual. Por ejemplo: "_Few Clouds_".
 
---

📛 Comprobá que todo funcione correctamente. Al ingresar una ciudad en el `input`, se deben agregar los datos en el `<div>`. Cuando se escriba una nueva ciudad, deben actualizarse los datos.

🚀  Ahora, pasá al ***Extra Credit*** para mejorar tu proyecto y desafiar tus habilidades.

---

###  🚀 ***Extra Credit***

Si querés mejorar tu proyecto agregá estas características:

- Cuando el usuario haga _click_ en el botón, se debe borrar el contenido del `input`.
- Agregá una validación en el `input` para que le muestre un `alert` al usuario si no ingresó texto al hacer _click_.
- Agregá una validación para que le muestre un `alert` al usuario si ingresa el nombre de una ciudad inexistente.

+++

Si la ciudad es inexistente, la API devolverá un Error 404.

🔍 Para aprender más, usá tus habilidades de _developer_ y _googleá_ la solución `.fail`.

+++

📛 Comprobá que todo funcione correctamente y luego pasá a la siguiente sección.

---

### Conclusión

En este módulo aprendiste qué es una API y cómo se consume mediante `jQuery`. También realizaste pedidos con AJAX y JSON. 

Por último, integraste todos estos conceptos en un proyecto útil de aplicación cotidiana.  

En el _Extra Credit_ aprendiste otro concepto importante como el "Error 404".

<img src = "https://media.giphy.com/media/1e42QlY434yCQ/giphy.gif" width = "500px">

#### ¡Felicitaciones! Terminaste todos tus proyectos 🥳.

Pasá a la siguiente sección para completar tu cursada.

<div class="editor-recuadro">

 🛎️ **Recordá**: Si algún aspecto de PLEDU no funciona como esperabas o merece revisión podés avisarle al equipo de Contenido por [acá](https://forms.gle/okCETdVFsbg9S9kX7).
 
</div>

---

