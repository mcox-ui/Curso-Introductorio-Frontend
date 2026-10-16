<!-- U13 - DOM (Document Object Model) -->
### Objetivos

En este módulo aprenderás:

- Qué es el DOM.
- Cómo se manipulan:
  - Los elementos (y sus atributos).
  - El estilo.
  - El texto.
  - El contenido.
- Cómo agregar y quitar elementos.

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">👩🏻‍💻👨‍💻 En las siguientes secciones, aprenderemos sobre el DOM a través de ejercicios en la consola. Esto sirve para hacer pruebas. Sin embargo, recordá que, como developer, manipularás el DOM a través del <em>script</em> (los archivos de JavaScript). <br></p>

🤓 Te recomendamos repasar la primera parte del curso —HTML y CSS— antes de iniciar este módulo.

![lego-ready.gif](https://media.giphy.com/media/13RH0eYA9vEAso/giphy.gif)

---

### ¿Qué Es El DOM?

Al principio del curso, aprendimos cómo se lee un documento HTML. Vimos que el _browser_ construye una representación del documento HTML que se llama **_Document Object Model_** (DOM).
![dom-html.png](https://i.imgur.com/dF8KQ4f.png)

En este sentido, el DOM lo organiza en forma de nodos y Objetos que tienen Propiedades y métodos. Tendrá la siguiente forma:

<!-- ![dom-html.png](https://simplesnippets.tech/wp-content/uploads/2018/10/document-object-model-DOM-in-JavaScript.jpg) -->
![dom-html.png](https://i.imgur.com/rONs2nD.png)

Esencialmente conecta las páginas _web_ a los _scripts_ o lenguajes de programación. Es decir, el DOM representa todo el contenido del documento HTML y permite que el _script_ de JavaScript interactúe con él.

Veamos un ejemplo. Cuando buscamos un término en el campo de búsqueda de _Google_ y se despliegan las opciones de búsqueda más frecuentes, esto sucede gracias a la interacción del código JavaScript con nuestro documento HTML (representado por Objetos) a través del DOM.

![busqueda-google.png](https://i.imgur.com/phcYuP5.png)

Para aprender más, accedé a la [documentación de Mozilla](https://developer.mozilla.org/es/docs/Referencia_DOM_de_Gecko/Introducci%C3%B3n).

+++

🤓 ¿Sabías que existe una página que registra las opciones de búsqueda más frecuentes relacionadas a un término?

Se llama [Answer The Public](https://answerthepublic.com/).

+++

---

### ¿Cómo Se Manipula El DOM?

Como vimos en la sección anterior, el DOM es la interfaz entre JavaScript y HTML+CSS.

Es decir, cuando cargamos un documento HTML+CSS en el _browser_, el DOM convierte cada _tag_ en un Objeto de JavaScript. Esto permite que el _script_ manipule los elementos HTML+CSS como si fueran Objetos.

Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/6GZDmNrwoMc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Recapitulando, las páginas _web_ previas a JavaScript eran estáticas: carecían de la interacción y el dinamismo que nos brinda JavaScript.

Por ejemplo:

![pagina-90s.png](https://i.imgur.com/9geH87G.png)

Hoy en día, la misma página _web_ se transforma: ¡Todo se basa en el DOM!

![parlantes.gif](https://i.imgur.com/GSMDVdj.gif)

#### ¿Cómo Accedemos Al Objeto De JavaScript?

Si escribimos el siguiente código en la consola:

```js
document
```

Nos va a mostrar el código HTML. Sin embargo, esto no muestra el verdadero Objeto. Para acceder, deberíamos escribir:

```js
console.dir(document)
```

Dentro de este Objeto podemos encontrar una gran cantidad de Propiedades y métodos. Por ejemplo, la Propiedad `<body>` contiene todo el cuerpo del documento HTML. A su vez, cada uno de sus elementos replica las mismas Propiedades y métodos.

🛎 **Recordá**: El DOM tiene muchísimas Propiedades. Ignorá la complejidad y buscá solo lo que necesites.

![complejo.jpg](https://i.imgur.com/VC11VMH.jpg)

---

### Manipular Los Elementos

Podemos seleccionar los elementos HTML desde la consola y, luego, acceder a sus Propiedades para modificar sus valores a través del comando `querySelector`.

Mirá este video para aprender cómo hacerlo:

<iframe width="600" height="355" src="https://www.youtube.com/embed/Aa1Q8VjV_bY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

![the-office.gif](https://i.imgur.com/Lrb6kTS.gif)

#### Paso A Paso

Para seleccionar un elemento desde la consola (o desde el _script_), debemos escribir `document.querySelector()`.

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

📚 `document.querySelector()`: Es uno de los métodos para seleccionar un elemento. Devuelve solo el primer elemento que coincida con el selector CSS dado. El término _“Query Selector”_ viene del inglés “consulta por selector”.

</div>

Veamos un ejemplo. Para seleccionar el elemento `h1`, escribimos:

```js
document.querySelector("h1") // Selecciona el primer "h1" que encuentra en el documento
```

Luego, si deseamos cambiar el color de la tipografía a lima (`lime`):

```js
document.querySelector("h1").style.color = "lime"
"lime"
```

Por último, podemos guardar esta referencia en una Variable:

```js
document.querySelector(".ejemplo_clase")
```

```js
let parrafo = document.querySelector(".ejemplo_clase")
```

Si ahora quisiéramos cambiar el color de la tipografía a rojo (`red`):

```js
parrafo.style.color = "red"
"red"
```

🛎 **Recordá**: En JavaScript no se usan guiones, se usa 🐪 _camelCase_.

#### Repaso: Selectores CSS

Abrí [esta página](https://manipulando-elementos.netlify.com/), luego abrí la consola JavaScript y prestá atención a qué selecciona cada uno de estos comandos:

```js
document.body
```
```js
document.querySelector('p')
```
```js
document.querySelector('#primary')
```
```js
document.querySelector('.important')
```
```js
document.querySelector('p.important')
```
```js
document.querySelector('#nav ol li')
```
```js
document.querySelector('h1, p')
```

---

### Manipular El Estilo

Si quisiéramos modificar las Propiedades de un documento, podríamos seleccionar un elemento con un `querySelector` y, luego, modificar su estilo. Sin embargo, esto es poco escalable.

La alternativa más práctica es definir una Clase con todas las propiedades CSS y aplicarla usando JavaScript. Para eso, usaremos un método llamado `classList`, en el que seleccionamos un elemento y le agregamos una Clase determinada pasándola como valor.

Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/Rgbaipi_-h4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

🛎 **Recordá**: En vez de cambiar todas las Propiedades del estilo desde JavaScript, la forma más escalable de hacerlo es a través de la Clase en el documento CSS.

La Propiedad `classList` nos permite acceder a las Clases presentes en un elemento. A su vez, podemos combinarlo con ciertos métodos para manipular el estilo.

Veamos un ejemplo:

```js
h2.classList.add("importante")
```

En este caso, le agregamos la Clase `importante` a un `<h2>` utilizando el método `add` (del inglés "agregar").

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

👩‍🏫👨‍🏫 `classList` es una Función que toma como valor el nombre de una Clase. Por lo tanto, no hace falta ponerle el punto adelante (`.importante`).

</div>

De la misma manera, podríamos suprimir la Clase `importante` utilizando el método `remove` (del inglés "quitar"):

```js
h2.classList.remove("importante")
```

También hay un método llamado `toggle` (del inglés "alternar") que cambia entre sacar y agregar la Clase. En otras palabras, si la Clase está presente, `toggle` la quita; si está ausente, la agrega:

```js
h2.classList.toggle("importante")
```

---

+++ `classList`: Métodos Más Usados

☑️ `add`: Agrega una Clase al elemento HTML. Si ya lo tiene, lo ignora.

☑️ `remove`: Suprime una Clase al elemento HTML. Si no lo tiene, lo ignora.

☑️ `toggle`: Agrega o suprime una Clase (si lo tiene, lo quita; si no lo tiene, lo agrega).

☑️ `item`: Obtiene una Clase por índice.

☑️ `contains`: Valida si una Clase específica está presente o no.

☑️ `replace`: Reemplaza una Clase por la otra.


+++

⚠️ **Importante:** Para nombrar una Clase, no uses términos que sean palabras reservadas (por ejemplo, usar "_purple_" cuando ya está reservada para el color). De esta manera, evitarás errores y confusión.

---

### Manipular El Texto Y Contenido

Además de manipular los estilos, podemos manipular los textos del HTML. Para eso, usaremos las Propiedades `textContent` (del inglés “contenido de texto”) y `innerHTML`.

⚠️ **Importante**: La propiedad `textContent` es para todos los elementos o _tags_ HTML que muestren texto (`h1`, `<span>`, `<p>`).

Mirá este video para aprender cómo usarlo:

<iframe width="600" height="355" src="https://www.youtube.com/embed/w2SFZfkFqTw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Veamos un ejemplo. Si quisiéramos modificar el texto presente en `h1` ("primer h1!"), primero definimos la Variable y luego utilizamos `textContent`:

```js
let h1 = document.querySelector("h1")
h1
h1.textContent = "¡Hola!"
```

|||

Contenido original:

![punto-de-partida.png](https://i.imgur.com/V6HOR4c.png)

Contenido modificado a través de la Propiedad `textContent`:

![text-content.png](https://i.imgur.com/zdYTtDf.png)

|||





Ahora, supongamos que quisiéramos agregar un _tag_ `<p>` al texto:

```js
h1.textContent = "<p>¡Hola!</p>" // Se modifica de manera literal, no interpreta si hay tags.
```

|||

![text-content-literal.png](https://i.imgur.com/LRowmSm.png)

|||

Se modifica el contenido de la etiqueta (o elemento HTML) de manera literal.

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">🛎 <strong>Recordá</strong>: En HTML, los <em>tags</em> pueden contener texto, otro <em>tag</em> o una combinación de ambos.<br></p>

Por lo tanto, si quisiéramos modificar el **contenido de HTML** de un documento, debemos usar `innerHTML`. Este devuelve el texto contenido en las etiquetas HTML. De esta manera, interpretará cada _tag_ y lo traducirá en la pantalla.

```js
h1.innerHTML = "<p>¡Hola!<p>"
```

|||

![inner-html.png](https://i.imgur.com/xFCqdkE.png)

|||

En síntesis, con la Propiedad `textContent` podemos modificar todos los elementos o _tags_ HTML que muestren texto. Con `innerHTML`,  podemos modificar el contenido del _tag_; por ejemplo, reemplazándolo por otro _tag_.

+++

Si un elemento HTML tiene contenido y no querés que lo pise, podés usar:
```js
let h1 = document.querySelector("h1")
h1.textContent += "Esto se agrega a lo que ya tiene por el +="
``` 
 
+++

---

### Manipular Los Atributos De Un Elemento

Además de manipular elementos, estilos y contenido, podemos modificar los atributos de un elemento en HTML.

+++ ¿Qué Son Los Atributos?

Según [Mozilla](https://developer.mozilla.org/es/), "los elementos en HTML tienen atributos; estos son valores adicionales que configuran los elementos o ajustan su comportamiento de diversas formas para cumplir los criterios de los usuarios". Un atributo puede ser el `src` (_source_) de una imagen, el `href` de un hipervínculo, etc.

+++

Para aprender cómo manipular los atributos desde JavaScript, mirá el siguiente video:

<iframe width="600" height="355" src="https://www.youtube.com/embed/f70aRpb_GiM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

El método `getAttribute()` nos devuelve el valor del atributo especificado. Con el método `setAttribute()` definiremos un valor para el atributo.

Veamos un ejemplo. Supongamos que tenemos el siguiente _tag_: 

```js
<a href="http://www.google.com" id="btn-google">Ir a Google</a>
```

Por ahora el _link_ nos lleva a www.google.com, pero queremos modificarlo por www.plataforma5.la. Para hacerlo, primero debemos usar el método `querySelector` desde JavaScript:

```js
let botonGoogle = document.querySelector("#btn-google");
```

Luego, usaremos `getAttribute()` y `setAttribute()`:

```js
botonGoogle.getAttribute("href") // Nos muestra cuál es el valor del atributo href.

botonGoogle.setAttribute("href", "http://www.plataforma5.la") // Cambia el valor del atributo href por el valor que se pasa como segundo Parámetro.
```

De esta manera, reemplazamos un atributo `href` por el otro.

Por último, si quisiéramos cambiar el texto "Ir a Google", debemos usar `textContent`:

```js
botonGoogle.textContent = "Ir a Plataforma 5"
```

Veamos otro ejemplo. Supongamos que queremos reemplazar una imagen por otra:

```js
<img src="logo.png">
```

```js
let logo=document.querySelector("img")
logo.getAttribute("src") // "logo.png"
logo.setAttribute("src", "http://vignette1.wikia.nocookie.net/sanicsource/images/9/97/Doge.jpg")
```

🛎 **Recordá**: `src` es una Propiedad del Objeto `img` que tiene como valor una dirección en donde está alojada la imagen.

---

### Manipular Varios Elementos 

Hasta ahora, aprendimos a usar `querySelector()` para modificar elementos específicos. Sin embargo, este método solo trae el primer elemento de un tipo.

Para seleccionar varios elementos al mismo tiempo, existe el método `querySelectorAll()`.

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

📚 `querySelectorAll()` devuelve un _Node list_ (lista de nodos) de todos los elementos que coincidan con el selector.

</div>

+++ Diferencias entre _Node list_ y Arreglo

El método `querySelectorAll()` no devuelve un Arreglo, sino un _Node list_. Para entender la diferencia entre ambos, hacé [click acá](https://www.aprenderaprogramar.com/index.php?option=com_content&view=article&id=816:nodelist-javascript-diferencias-de-nodelist-y-array-acceso-a-texto-nodos-textcontent-innertext-cu01136e&catid=78&Itemid=206).

+++

Mirá este video para aprender cómo usarlo:

<iframe width="600" height="355" src="https://www.youtube.com/embed/mdJeMy1v9jA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Recapitulando, si utilizamos `querySelector("a")`, solamente nos trae el primer _link_:

```js
document.querySelector("a") // Solamente nos trae el primer link
```

En cambio, `querySelectorAll("a")` nos devuelve una lista de nodos con todos los elementos de este tipo:

```js
document.querySelectorAll("a") // Nos devuelve una lista de nodos con todos los elementos de este tipo
```

Ahora bien, si quisiéramos modificar todos los _links_ de nuestra página, no podremos hacerlo usando `setAttribute()`, ya que solo funciona sobre Objetos (no listas). Por eso, deberás recorrerlo usando un _loop_.

Para eso, seguí estos pasos:

1. Guardá la lista de nodos en una Variable.

```js
let todosLosLinks = document.querySelectorAll("a")
```

2. Recorré la Variable con un _loop_, de modo tal que, en cada vuelta, se modifique con `setAttibute`.

```js
for (let i = 0; i < todosLosLinks.length; i++) {
todosLosLinks[i].setAttribute("href", "http://www.plataforma5.la")
}
```

🛎 **Recordá**: Es una convención usar las letras "i" o "j" para los contadores.

---

#### Ejercicio

Retomando el ejemplo anterior, supongamos que ahora queremos cambiar el texto de los párrafos.

Pensá cómo podrías hacerlo y probá el código en tu consola antes de mirar la solución.

|||

```js
let parrafos = document.querySelectorAll("p")

for (let i = 0; i < parrafos.length; i++) {
parrafos[i].textContent = "Parrafo " + (i + 1)
}
```

Debería quedar: Párrafo 1, Párrafo 2, Párrafo 3, etc.

|||

---

### Crear Elementos

Para crear diferentes elementos y luego añadirlos a un documento, debemos usar el método `createElement`.

⚠️ **Importante**: Con `createElement` se crea un Objeto que luego agregaremos al DOM.

Veamos su sintaxis:

```js
let elemento = document.createElement("elemento") // Pasamos un String como parámetro, que indica qué etiqueta queremos crear.
```

Ahora veamos un ejemplo. Si quisiéramos crear una etiqueta `h1`, primero debemos guardar su referencia en una Variable:

```js
let h1 = document.createElement("h1")
```

Luego, le podemos agregar texto usando `textContent`:

```js
h1.textContent = "Plataforma 5"
```

Por último, podemos crear un elemento `div`:

```js
let div = document.createElement("div")
```

Si querés conocer más sobre el método `createElement`, accedé a la [documentación de Mozilla](https://developer.mozilla.org/es/docs/Web/API/Document/createElement).

🛎 **Recordá**: Podés ingresar a los distintos nodos y ver cómo son las relaciones entre nodos e hijos. Hacé click [acá](https://developer.mozilla.org/es/docs/Web/API/Node) para aprender más.

En la próxima sección, aprenderás cómo agregar el `h1` creado en el `div` y cómo sumarlos a tu sitio _web_.

---

### Agregar Y Remover Elementos

#### `appendChild`

Para agregar un elemento dentro de otro usaremos el método `appendChild`. De esta forma, podemos incluir en un nodo un nuevo hijo.

Veamos su sintaxis:

```js
document.elementoPadre.appendChild(elementoHijo) // Pasamos como parámetro el Objeto que creamos en el paso anterior
```

+++

🤓 **Tip:** Si querés crear un párrafo nuevo con texto, creá el texto como un nodo de Texto que agregarás al párrafo. Luego, agregá ese párrafo al documento.

+++

⚠️ **Importante:** También podés usar este método para mover un elemento, de un elemento a otro.

Para aprender más sobre este método, accedé a la [documentación de Mozilla](https://developer.mozilla.org/es/docs/Web/API/Node/appendChild).

#### Paso A Paso

Volviendo al ejemplo anterior, si quisiéramos agregar el elemento `h1` a la Variable `div`:

1. La Variable `div` debe llamar al método `appendChild`.
2. Para ello, el argumento del método debe ser el elemento a agregar (en este caso, `h1`).

```js
div.appendChild(h1) // En este caso, h1 es el Objeto creado anteriormente. Por eso no es un String (como en el caso de document.createElement).
```

📛 En la consola, comprobá que el elemento `h1` se encuentre dentro del `div`:

![Captura-div.PNG](https://pledu-plataforma5.s3.amazonaws.com/5bc731d2-55f7-4462-b8e1-86e32484242e/Capturaz.PNG)

3. Luego, agregá el `div` al `body`, pasándolo como argumento:

```js
document.body.appendChild(div)
```

|||

Comprobá que se vea así en tu navegador:

![Capturaf.PNG](https://pledu-plataforma5.s3.amazonaws.com/5bc731d2-55f7-4462-b8e1-86e32484242e/Capturaf.PNG)

|||

---

#### `removeChild`

Para remover un elemento de nuestro sitio _web_, usamos el método `removeChild`.

Veamos su sintaxis:

```js
document.ElementoPadre.removeChild(elementoHijo)
```

Por ejemplo, el siguiente código remueve el `div` del `body`:

```js
document.body.removeChild(div)
```

---

## Ejercicios de practica

### 1)  ***¡Shuffle!***

<div class="editor-recuadro">

🛎 **Recordá**: En la **Comunidad de P5 de Discord** podrás ver cómo otras personas tuvieron las mismas dudas y cuáles fueron las distintas formas en que las resolvieron. 

</div>


1. En tu HTML creá un `<div>` con ID `source` y otro con ID `destination` (ambos con texto adentro).
2. Seleccioná ambos y guardalos en sus respectivas Variables.
3. Luego, intercambiá el contenido entre ambos `<div>` (es decir, que el texto del `<div>` de ID `source` pase al de ID `destination` y viceversa).

### 2) Ejercicio: Manipular Texto Y Contenido

1. Creá un archivo HTML que, dentro de su `<body>` solo tenga un título `<h1>`.
2. Por consola, cambiá el texto del título.

+++

Para cambiar el texto del título, usá la Propiedad `textContent`.

+++

3. Por consola, cambiá el título por un párrafo con un texto a elección.

+++

Para cambiar el título por un párrafo, usá la Propiedad `innerHTML`.

+++

4. Por consola, agregá otro párrafo al `<body>` con un texto a elección.

+++

Para agregar otro párrafo al `<body>`, usá `appendChild`.

+++

### 3) Manipular CSS

1. Creá un documento HTML con un `<div>` adentro.
2. Usando la Propiedad `style` del elemento en JavaScript, dale a ese `<div>` altura, ancho y un color de fondo.
3. Creá la clase `.square` en tu `stylesheet`, y dale las mismas Propiedades.
4. Ahora en vez de agregársela con la Propiedad `style`, hacelo con la Propiedad `classList.`

  ¿Que devuelve `div.classList`?

5. Desde tu consola, sacá la clase `.square` al `<div>`.
6. Hacé una Función que cada un segundo `(setInterval())` se fije si tiene la clase `.square`. Si la tiene, que se la quite; si no la tiene, que se la agregue.

+++

Si lo hiciste con un `if` y un `else` no está mal... pero probá usando `classList.toggle()`. Mucho más simple, ¿no?

+++

### 4) Formulario E Input

1. Creá un HTML vacío con su respectivo JavaScript.
2. A través de JavaScript, creá un formulario que contenga los siguientes elementos:

  - Un _input_ donde el usuario escriba su nombre y apellido (con su respectivo _label_).
  - Un _input_ donde el usuario escriba su e-mail, con un _placeholder_.
  - Un `radio button` donde el usuario indique si su género es "Femenino", "Masculino", "No binario", "Prefiero no decirlo".

  🛎 **Recordá**: Si tenemos cuatro opciones o menos, es mejor usar `radio button`. Si ya son más de cinco, recomendamos usar _dropdown_.

  - Un _dropdown_ para que el usuario indique su rango de edad: si es menor a 18 años; 19-30; 31-45; 46-55 o mayor a 56.
  - Un `checkbox` para señalar si el usuario es argentino o no.

3. Una vez terminado el formulario, completalo con tus datos.
4. Luego, abrí la consola y obtené:

  - El nombre y apellido ingresado.
  - El e-mail ingresado.
  - La palabra seleccionada por género identificado.
  - El rango de edad seleccionado.
  - El valor _true_ o _false_ en base a si la persona seleccionó ser argentino/a o no.
