### Introducción: ***To Do List***

En este proyecto aplicarás nuevamente todos los conceptos aprendidos hasta el momento a través de la creación de una **lista de tareas** (_To Do List_ ).

Comenzarás generando la estructura con el HTML, luego agregarás estilos con CSS y, por último, escribirás la lógica de tu aplicación _web_ con JavaScript.

![todolist.png](https://media.giphy.com/media/26tPpStnC0XthM19u/giphy.gif)

---

### Generar La Estructura

En esta sección armarás la estructura de tu lista de tareas. Para que te des una idea, tu proyecto debería verse así:

![todolist](https://happy-lalande-5c655b.netlify.app/todoSinEstilos.png ) 

#### Paso A Paso

1. Creá un documento HTML con su estructura básica y vinculalo con una hoja de estilos y un archivo _JavaScript_.

2. Dentro del `<body>` agregá los siguientes elementos:

- Un título con el texto: "COSAS PARA HACER".
- Un primer `<div>` con `class="input-div"` que contenga:
  - Un `input` de tipo "text" con `class="input"`.
  - Un atributo `placeholder` con el valor "Tarea a agregar".
  - Un `button` con `class="boton-agregar"` y el ícono "➕".
- Un segundo `<div>` con `class="container"` que contenga:
  - Un `<div>` con `class="item"`.
     - Un `input` de tipo "text" con `class="item-input"`y atributo `disabled`.
  - Un `button` con `class="boton-editar"` y el ícono "🔒" (candado).
  - Un `button` con `class="boton-remover"` y el ícono "🗑️" (tacho de basura).
  
<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

⚠️ **Importante**: Dentro de cada botón insertarás un ícono. Hay distintas formas de hacerlo. A continuación, te presentaremos una.
</div>





#### Cómo Incorporar Íconos desde Font-Awesome
  
Para incorporar íconos dentro de tu proyecto usando [_Font-Awesome_](https://fontawesome.com/v6.0/icons?s=thin), ingresá la siguiente etiqueta en el `<body>` de tu sitio:

```html
<script src="https://kit.fontawesome.com/ba0ece2d64.js"></script>
```

Por ejemplo, para asociar tu `button` con `class="boton-agregar"` al ícono "➕", agregá el siguiente _tag_:

```html
<i class="fas fa-plus"></i>
```

🏋🏻‍♀️🏋️ Ahora, asociá el resto de los botones con sus íconos.


Por último, asigná un valor al `input` de tipo "text" con `class="item-input"` (por ejemplo, "Regar las plantas"). Servirá de prueba para ver cómo queda tu lista de tareas.

<div style="border:3px; border-style:solid; border-color: grey; padding: 1em;"> 

👩‍🏫👨‍🏫 Antes de pasar a la siguiente sección, te recomendamos dos cosas más:
1. Asigná un valor al `input` de tipo "text" con `class="item-input"` (por ejemplo, "Regar las plantas"). Servirá de prueba para ver cómo queda tu lista de tareas.
2. Luego de esto, comentá todo el código que se encuentra dentro del `<div>` con `class="container"`. Para generar ese _input_ y los dos botones, vas a interactuar con el DOM. 

</div>

---




### Agregar Estilos

¡Es hora de darle estilo a tu lista de tareas! Para eso, seguí este nuevo paso a paso.

Al finalizar esta sección, el estilo de tu proyecto debería verse así:

![estilo](https://i.imgur.com/nQmDO9r.png)

#### Paso A Paso
1\. Creá un nuevo archivo `.css` y vinculalo al documento HTML anterior.

2\. Dale estilo a tu `<body>`:

  - Modificá la tipografía, el color de fondo y centrá el contenido.
  - Cambiá el color de `<h1>` a blanco.

3\. Estilizá el `input` principal. En tu CSS incluí estas propiedades:

- Dale un `width` de `450px` y un `height` de `50px`. 
- Dale un margen general de `5px`, un `padding` _top_ y _bottom_ de `0px` y un `padding` _left_ y _right_ de `20px`.
- Eliminá el borde que trae el `input` por _default_.

- Agregá un `border-radius` de `10px`, un `background-color: white` y un `font-size` de `18px`.

4\. Dale estilo a tu `button`. En tu CSS, hacé la declaración apuntando a la Clase `.boton-agregar`:

- Dale un `width` y un `height` de `50px`.
- Dale un margen general de `5px`.
- Eliminá el borde que trae por defecto.
- Agregá un `border-radius` de `10px`, cambiá el color de fondo a `rgb(255, 6, 46);` y el color del texto a blanco.
- Usá el pseudo-selector `hover` para que la opacidad del botón sea de 0.9 al posar el cursor encima.

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 
 
 📛  Revisá y probá que funcione correctamente. Luego, pasá a la siguiente sección.

</div>

---

### Clase `Item` 

¡Llegó la hora de darle funcionalidad a tu lista de tareas! 

Para empezar, seleccionarás los elementos del `"input"` principal. Luego, continuarás con el `"boton-agregar"` y el  `"container"`. Para eso, usarás `querySelector()` y guardarás estas referencias en tres Variables distintas.  

Al finalizar, el proyecto debería funcionar así:

<img src="https://ecstatic-hermann-e2c29e.netlify.app/sinEstilosFinales.gif" style="box-shadow: 3px 4px 15px -2px rgba(0,0,0,0.75);border-radius:24px">

#### Trabajar Con Clases:

Para empezar, creá la Clase `Item`.  Ésta posee en su `constructor` el llamado a un método propio: `crearDiv`.

+++ ¿Cómo Debe Ser El `div`?

Deberás crear un `div` que contenga un `input`. Este formará parte de la lista de tareas a realizar.

El `constructor` de la Clase `Item` recibirá como parámetro el valor del `input` de la tarea a agregar; por ejemplo, "Lavar los platos". El método `crearDiv` recibirá este mismo valor.

+++

Luego, definí el método `crearDiv` (dentro de la Clase `Item`) y pasá como parámetro la nueva tarea.

|||

El código del `constructor` debería quedarte así:

```js
constructor(nuevaTarea) {
        this.crearDiv(nuevaTarea)
}
```

|||

📛 Revisá este proceso. Luego, pasá a la siguiente sección para aprender el método que te permitirá crear tareas.

---

### Método `crearDiv` (Parte 1)

Este método te permitirá agregar tareas a tu lista. Para eso, seguí estas recomendaciones:

+ Dentro del método `crearDiv`, usá `createElement` para crear un `input` de tipo "text".

⚠️ **Importante**: Guardá la referencia a este elemento en la Variable `inputItem`.

+ Establecé la Propiedad `disabled` de la Variable `inputItem` con el valor _true_.

+ Usá el método `classList.add` para agregar la clase css `item-input` a la Variable `inputItem`.

+ Tomá el parámetro del constructor para asignarle un valor a la variable `inputItem`.

+ Por último, usá `createElement` para crear un nuevo `div`. Guardá la referencia a este elemento en una Variable y agregale la clase css `item`.

##### Trabajar Con Botones

Ahora, crearás los botones para editar y remover los `input` de la lista.

**Botón "EDITAR" ("🔒 ")**

+ Creá el botón para editar el `input` de la tarea agregada. Guardá la referencia en una Variable llamada `botonEditar`.

+ Usá `innerHTML` para insertar su ícono dentro del `botonEditar`.

|||

`innerHTML`= `"<i class='fas fa-lock'></i>"`

|||

+ Por último, usá `classList.add` para agregar la Clase `boton-editar` a tu botón.

**Botón "REMOVER" ("🗑 ")️**

+ Repetí los mismos pasos para crear el botón "Remover". Guardá su referencia en una Variable llamada `botonRemover`.

+++

Usá `innerHTML` para insertar su ícono dentro del `botonRemover`.

`innerHTML`= `"<i class='fas fa-trash'></i>"`

+++

🛎️ **Recordá**: agregá la Clase `boton-remover` a tu botón.


##### Agregar Elementos A La Lista

Ahora, agregarás el `div`, `input` y botones a la lista.

+ Primero, para agregar el `input` y los botones al `div`, deberás usar `appendChild`.

+ Luego, con la misma Función, deberás agregar el `div` (que ya contiene los otros elementos) a la Variable `container`.

📛 Si todo funciona bien, pasá a la siguiente sección.



---

### Método `crearDiv` (Parte 2)

En esta sección definirás el comportamiento de los botones dentro del método `crearDiv`.

Para eso, definí el comportamiento del `botonEditar` para que el usuario pueda hacer _click_ y modificar el `input` de la tarea agregada. 

Además, al presionar el botón, el ícono debe cambiar a un candado abierto ("🔓"): `"<i class='fas fa-lock-open'></i>"`. Al volver a presionar, debe cerrarse otra vez y deshabilitar la edición.

+++ Cómo Generar Este Comportamiento

Podemos generar este comportamiento negando (`!`) el valor _boolean_ de `input.disabled`. De esta manera, cada vez que el usuario haga _click_ en el candado, se usará ese valor para generar un comportamiento o el otro (🔒 = `!`🔒). 

+++

Luego, definí el comportamiento del `botonRemover`para que el usuario pueda hacer _click_ y se remueva el `div` creado inicialmente.

---
#### ¡Ya escribiste la Clase `Item` y el método `crearDiv`! 

Pasá a la siguiente sección para verificar el `input`.

![youcandoit](https://media.giphy.com/media/nYYtQdLqwwlTe3ccKh/giphy.gif)

---

### Verificar El ***Input***

Ahora, deberás definir una Función llamada `chequearInput` para comprobar si el `input` de la nueva tarea tiene un valor. Si es así, debe instanciar un Objeto de tipo `Item` y pasarle al `constructor` ese valor.

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 
 
⚠️ **Importante**: la Función `chequearInput` debe ir por fuera de la Clase `Item`.

</div>


Además, una vez que el usuario agregue una tarea a la lista, el `input` debe volver a quedar vacío.

Por último, el `botonAgregar` debe llamar a la Función `chequearInput` cada vez que el usuario haga _click_.

📛 Si todo funciona bien, pasá a la siguiente sección para definir los detalles finales a tu proyecto.

<div class="editor-recuadro">

 🛎️ **Recordá**: Si algún aspecto de PLEDU no funciona como esperabas o merece revisión podés avisarle al equipo de Contenido por [acá](https://forms.gle/okCETdVFsbg9S9kX7).
 
</div>  

---

### Retoques Finales

¡Ya estás cerca de terminar tu proyecto!

En esta sección, agregarás los detalles finales: mejorarás la estética de los botones y de los `input`.

Al finalizar, tu proyecto debería verse así:

![final](https://pledu-plataforma5.s3.amazonaws.com/08fdb581-9674-460a-af27-883c3ccfdf90/todo.gif)

#### Paso A Paso

 **Modificar Los `input`**

En tu hoja de estilos, hacé referencia a la Clase `.item-input` y dale el siguiente formato:
- Una altura y un ancho de `50px`.
- Un `padding` de `0px` hacia arriba y abajo y de `20px` hacia los costados.
- Un borde sólido y blanco de `1px`.
- Un `border-radius` de `10px`.
- Un tamaño tipográfico de `18px`.
- Un color de texto blanco.
- Remové el fondo con la Propiedad `background: none`.
- Eliminá el contorno de los `input` nuevos.



**Modificar El Espaciado**

+ Para generar más espacio entre los ítems, agregale un margen inferior de `10px` a la Clase `.item`.


**Modificar El Botón "Editar"**

Hacé referencia a la Clase `.boton-editar` y dale el siguiente formato:
- Un margen de `0px` arriba y abajo y de `5px` hacia los costados.
- Remové el borde que viene por _default_ con la Propiedad `border: none`.
- Remové el fondo con la Propiedad `background: none`.
- Asigná al texto el color `#62d0ff`, un tamaño `1.4rem` y una tipografía `Montserrat, sans-serif`.

**Modificar El Botón "Remover"**

Hacé referencia a la Clase `.boton-remover` y dale el siguiente formato:
- Una altura y un ancho de `50px`.
- Un margen de `0px` arriba y abajo y de `5px` hacia los costados.
- Remové el borde.
- Un `border-radius` de `10px`.
- Asigná el color `rgb(255, 6, 46)` al fondo y un tamaño tipográfico de `20px`.

---

### Conclusión

##### ¡Felicitaciones!

¡Terminaste tu primera lista de tareas! A disfrutarlo así:

![chandler.gif](https://media.giphy.com/media/S9iMXx6Lqrr5mJoMxC/giphy.gif)

Este ejercicio te permitió integrar todos los conceptos trabajados hasta el momento y crear una herramienta útil para vos y para las personas que quieras. 

🔍 Podés leer más sobre experiencia de usuario (para esta herramienta u otras que vayas haciendo) en el siguiente [link](https://97cosas.com/programador/averigua-que-haria-usuario.html).

🛎️ **No te olvides de compartirlo en Discord ni de agregarlo a tu Portfolio**.

---

  