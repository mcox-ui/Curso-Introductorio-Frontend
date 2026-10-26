### Introducción

En este proyecto, crearás un juego en el que el usuario deberá adivinar un color a partir de su código RGB. 

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

⚠️ **Importante:** La clave del éxito de tu proyecto es que hagas todo paso a paso. Es decir, no pienses en el paso 6 antes de que funcionen los 5 anteriores.
 
</div>

Avanzá a las siguientes secciones para leer sobre nuestra metodología y las reglas del juego.

![back-to-the-future.gif](https://media.giphy.com/media/0DYipdNqJ5n4GYATKL/giphy.gif?cid=ecf05e47mtjbei0ki94g51lx1sz0udbcvp0mqki3wf5csjo5&rid=giphy.gif&ct=g)

---

### Metodología

👩‍🏫👨‍🏫 Sugerimos que realices este proyecto usando el 🍅  **Método Pomodoro**.

#### ¿Qué Es El 🍅 Método Pomodoro?

El Método Pomodoro (del italiano "tomate") es una técnica de administración del tiempo creada por Francesco Cirillo.

Para conocer este Método mirá este video:

@youtube=ykMzzZolhdk

Recapitulando, el método consiste en dividir el tiempo de trabajo en **bloques de 25 minutos** ("pomodoros"), separados por **cinco minutos de descanso**.

Durante esos 25 minutos, deberás concentrarte solo en una actividad hasta que suene la alarma. Luego, sugerimos que te levantes, estires y desconectes antes de retomar tu trabajo.

Al completar cuatro "pomodoros", podrás tomarte un descanso más largo de 20 o 30 minutos.

Mirá el siguiente gráfico:

![tecnica-pomodoro.png](https://imgur.com/x1OtM6w.png)

#### ¿Para Qué Sirve?

El Método Pomodoro:
- Sirve para fijar un límite de tiempo.
- Facilita la realización de tareas al dividirlas en bloques manejables.
- Fomenta la concentración.
- Aumenta la productividad.
- Evita el _multitasking_: la realización de más de una tarea al mismo tiempo.

#### Herramientas Digitales

Existen muchas herramientas _online_ para medir el tiempo. Algunas de ellas son:
- [_Pomodoro Tracker_](https://pomodoro-tracker.com/?lang=es)
- [_Pomofocus_](https://pomofocus.io/)
- [_Pomodor_](https://pomodor.app/timer)
- [_Marinara Timer_](https://www.marinaratimer.com/cKjpu)

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

👩‍🏫👨‍🏫 ¡Elegí la herramienta que mejor se adapte a tus necesidades!

</div>

---

### Las Reglas Del Juego

Las reglas del juego son simples. El programa mostrará un código RGB y opciones posibles para que el usuario adivine cuál es la correcta. 
El usuario podrá jugar en dos niveles: el fácil (con 3 colores) o el difícil (con 6). En cualquier caso, el juego le permitirá hacer _click_ en todas las opciones hasta que dé con la correcta. 

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

⚠️ **Importante**: para entender mejor mirá este [Proyecto](https://luciacolorgame.netlify.app/).

</div>

#### Sintaxis De Las Funciones

Asegurate de escribir tus funciones usando esta sintaxis:

```
function saludar() {
  console.log("¡Hola!");
}
```

Al hacerlo, JavaScript primero guardará la Función en la memoria y, luego, cuando la queramos llamar ejecutará el código. 

Esto nos servirá para organizar mejor el código, poniendo la definición de las Funciones en una sección y su uso en otra.

Si ejecutarámos la Función antes de declararla, funcionaría igual porque JS ya la leyó antes de empezar a correr el programa.

Veamos un ejemplo de esto último: 

```js
llamarBatman();
function llamarBatman() {
  alert("Soy Batman.");
}
```

---

### Paso A Paso (Parte 1)


#### Paso 1: Archivos HTML y CSS

Para que practiques JavaScript a fondo te ayudaremos con los pasos de HTML y CSS:

- Creá los archivos `index.html` y `style.css`. 
- Luego ingresá a este [link](https://github.com/Plataforma5/colorGame).
- Copiá el código que se encuentra dentro de cada uno de los archivos y pegalos en los que creaste en el VSC, según corresponda.

<div class="editor-recuadro">

⚠️ **Importante** :  más allá de que te demos resuelta esta parte, tenés la libertad de hacer las modificaciones que quieras en tus archivos.

</div>


##### Paso 2 : Dar Color A Las Tarjetas

 - Creá un archivo JavaScript para darle a cada cuadrado un color distinto: 
    - Creá un Arreglo llamado `colors` y escribí 6 colores en formato RGB. 
  
⚠️ **Importante**: Escribí los colores respetando esta sintaxis (con los espacios) `"rgb(240, 14, 128)"`. 

+++

Escribí los _Strings_ con una misma sintaxis. Un espacio de más (o de menos) puede hacer que el juego no funcione.

+++

2. Asignale a cada cuadrado un color: 
  + Seleccioná todos los cuadrados usando `querySelectorAll()`.
  + Recorrelos usando un `for` _Loop_. En cada vuelta del _Loop_, asignale un color del Arreglo `colors`. 
  
+++

Aprovechá la Variable `i`, no solo para acceder al cuadrado específico, sino también al color.

+++

📛 Asegurate de que los 6 cuadrados tengan los colores del Arreglo `colors`.


<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

👩🏻‍💻👨‍💻**Acerca De Los Selectores**
 
Cada vez que selecciones un elemento utilizá una Variable para guardarlo. Por ejemplo, escribir la Variable `square`, es más rápido que `document.querySelectorAll(".square")`

</div>


Avanzá a la siguiente sección para continuar con tu proyecto.


![todavíafalta](https://media.giphy.com/media/l2Je9zHYveK012EVi/giphy.gif)




---


### Paso A Paso (Parte 2)

#### Paso 3: El Contenido De La Página

En esta parte del proyecto, crearás el título del juego: ***"The Great Guessing Game"***. Deberás lograr que se muestre el código RGB del color ganador.

Para hacerlo, seguí estos pasos:

1. Dentro del span `#colorDisplay` irá el código RGB del color ganador.

2. Creá la Variable `pickedColor`. Dale un color específico (por ejemplo `colors[3]`) y su valor al texto de `#colorDisplay`.

👩‍🏫👨‍🏫 Más adelante, la Variable tendrá un color aleatorio (seleccionado del Arreglo).

3. Comprobá que el código RGB aparezca correctamente en el `<h1>`.

#### Paso 4: Un Poco Del Juego

Ahora empecemos con la lógica del juego.

Cuando el usuario haga _click_ en un cuadrado incorrecto, éste desaparecerá (cambiando su color de fondo al mismo que el del `<body>`) y, al mismo tiempo, aparecerá el mensaje "Intentalo nuevamente".

Si el usuario adivina, en cambio, todos los cuadrados y el `<h1>` deberán tener el color del cuadrado ganador y aparecerá el mensaje "¡Correcto!". 

Para lograr esta dinámica, seguí estos pasos:
  
1. Dentro del `span#message` mostraremos el mensaje
2. Agregá un evento de _click_ a cada uno de los cuadrados.

+++

Podés aprovechar el _Loop_ que hiciste antes.

+++

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🤓 **Tip:** Cuando el usuario haga _click_ en un cuadrado necesitarás guardar su código RGB en una variable `clickedColor`. Luego, lo compararás con `pickedColor` y comprobarás si el color _clickeado_ es el mismo que el color ganador previamente seleccionado. 

</div>

#### Qué Sucede Si Los Colores Son Distintos

Si son distintos, le darás a ese cuadrado el color de fondo del `<body>` y le mostrarás el mensaje "Intentalo Nuevamente" en el `<span>`.


📛 Fijate si funciona correctamente cuando hacés _click_ en los colores equivocados.

#### Qué Sucede Si Los Colores Son Iguales

Si son el mismo color, seguí estos pasos:

1. Mostrá el mensaje "¡Correcto!" en el `<span>`. 
2. Asignale al `<h1>` el color de fondo del ganador.

+++

🤓 **Tip:** Para cambiar el color de los cuadrados, hacé una Función por fuera. De esta manera, mantendrás el código ordenado.

+++

3. Dentro de una nueva Función `changeColors`, que tomará como Argumento un color, iterá sobre todos los cuadrados y dale el color de fondo del Argumento. 
4. Ejecutá la Función en el momento que el usuario hace _click_ en el color correcto y pasale como Argumento ese color. 

📛 Fijate si funciona cuando hacés _click_ en el color correcto.

5. Creá una Función para asignarle a `pickedColor` un color aleatorio del Arreglo de colores. Para eso, creá la Función `pickColor` que devuelva un color _random_:
    1. Dentro de la Función `pickColor` creá un número aleatorio entre los Índices del Arreglo `colors`.
    2. Usá ese número para devolver un color del Arreglo.
    3. Asigná lo que devuelve la Función a la Variable `pickedColor`. 

📛 Fijate si cada vez que actualizás la página el color del `<h1>` es distinto y si el juego sigue funcionando.

6. Creá la Función `randomColor` para generar y devolver un color aleatorio. 

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🛎 **Recordá:** RGB son siempre 3 números entre 0 y 255.
</div>

7. Creá la Función `generateRandomColors` que generará de forma aleatoria el Arreglo de colores usando la `randomColor`. 
  + La Función tomará como Argumento un número que indique la longitud del Arreglo (6 o 3 cuadrados, dependiendo si se está jugando en _Easy_ o _Hard Mode_). 
  + El Arreglo que devuelva esta Función se lo asignarás a la Variable `colors`. 

📛 Por último, fijate si cada vez que cargás la página aparecen colores _random_ en los cuadrados y funciona el juego.

---

### Botones

En esta parte del ejercicio crearás el botón de "_Play Again?_".

Este botón tiene 2 funcionalidades:
1. Cuando se está jugando el juego, ofrece pedir nuevos colores.
2. Si se ganó el juego, ofrece jugar otra vez.


+++
 
Te recomendamos guardar todo en una función `reset` ya que luego la vas a necesitar.
 
+++

En ambos casos el efecto es el mismo: **reinicia el juego con nuevos colores**.

Para crear el botón "Play Again?", seguí estos pasos:
  
 1. Seleccioná el `button#reset` y dale un `event listener` para que, cuando se haga _click_:
  + Genere nuevos colores en el Arreglo.
  + Vuelva a elegir un color de ese Arreglo (para que sea el ganador) y aparezca en `#colorDisplay`. 
  + Cambie los colores de los cuadrados con los nuevos colores. 

📛 Fijate si todo sigue funcionando correctamente.

  2. Agregá un evento para que, cuando el usuario gane, #reset cambie su texto a "Play Again?". 
  3. Agregá en el _listener_ de #reset un evento para que, cuando el usuario haga _click_, vuelva a decir "Nuevos Colores" y desaparezca el mensaje "Intentalo Nuevamente" y "¡Correcto!".
  

+++
 
Podés modificar tu primera función para agregar estos eventos.
 
+++


📛 Antes de seguir avanzando, volvé a _resetear_ el color de fondo del `<h1>` y fijate si todo esta funcionando como debería.

#### Los Botones ***Easy Y Hard***

En esta parte del ejercicio crearás los_ niveles. Al final del `div#stripe` tenés dos botones _Easy_ y _Hard_ que modificarán la dificultad del juego. Para hacerlo, seguí los pasos indicados para cada botón.

#### El Botón ***Hard***

1.El botón _Hard_ tiene asignado la clase `selected` para que, al cargar la página, indique que está seleccionado. También cada botón tiene un ID para poder identificarlo.

2. Creá un `event listener` a cada uno para que, cuando le hagas _click_, le agregue la clase `selected` y se la quite al otro. 

📛 Fijate si funciona correctamente cuando hacés _click_ en ambos botones.

#### El Botón ***Easy***

Cuando hagamos _click_ en el botón _Easy_ queremos que se generen solo 3 colores con un color ganador y que se muestre en el título cuál es.

Para lograrlo, le asignaremos a los primeros 3 cuadrados los 3 colores del Arreglo y ocultaremos los otros 3 a través de la Propiedad `display:none;`.

+++

Debe ser un _String_ con el color.
🤓 Si el _String_ es verdadero, le asignará el color al cuadrado, sino (si no hay ningún elemento en ese Índice y nos devuelve `undefined`) le cambiará al cuadrado la propiedad CSS `display` a `none`. De esta manera, el cuadrado se esconderá.

+++

📛 Fijate que cuando hagas _click_ en _Easy_ los 3 primeros cuadrados cambien de color y los otros tres se escondan.

#### La Última Milla

En esta parte del ejercicio, te enfocarás nuevamente en el botón _Hard_. 

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;">

👩‍🏫👨‍🏫 No te preocupes si el código se empieza a repetir. Antes de terminar el proyecto lo podrás refactorizar.
  
</div>

Ahora deberás:
1. Generar nuevos colores (que vuelvan a ser 6).
2. Elegir un color ganador.
3. Mostrar en el título cuál es ese color. 

Para hacerlo, seguí estos pasos:

1. Hacé _Loop_ a todos los cuadrados y asignale a todos un color del Arreglo. 
2. Para poder volver a mostrar los cuadrados escondidos, dale a los cuadrados el Valor `block` a la propiedad CSS `display`.

📛 Fijate si después de ir a _Easy_ y volver a _Hard_ se muestran los cuadrados escondidos y si aparecen nuevos colores. También corroborá si el juego funciona correctamente en ambos modos.

+++ Un 🐞 _Bug_ En El Juego

💣 En este momento, tenés un _bug_ en el juego: cuando estás en el modo _Easy_ y hacés _click_ en `#reset` se generan 6 nuevos colores en el Arreglo que no se muestran en la pantalla. 

Para solucionar este problema, crearás la Variable `numberOfSquares` que registre con cuántos cuadrados se está jugando en ese momento: 
- La Variable iniciará siendo 6. 
- Cuando se haga _click_ en _Easy_ cambiará a 3.
- Cuando se haga _click_ en _Hard_ volverá a 6. 
- Luego, cada vez que se ejecute `generateNumberColors` ya no se pasará el número _Hard_ codeado como Argumento sino que se pasará la Variable `numberOfSquares`. 

📛 Fijate si se solucionó el _bug_ mostrando por consola cuántos elementos hay en el Arreglo `colors`.

![my-code.png](https://i.imgur.com/hKJXveu.png)

+++

---

### Estilo

Ahora que el juego funciona, nos enfocaremos en el estilo. En este punto, existen 2 caminos:
1. Seguir el maqueteado del ejemplo.
2. Crear tu propia versión. 


👩‍🏫👨‍🏫 Si elegís la segunda opción, tenés que respetar los lineamientos generales:

1. Los botones de "Nuevos Colores", _"Easy"_ y _"Hard"_, no deben parecer botones clásicos ni tener una línea azul alrededor (en inglés, _outline_) cuando le hacemos _click_.
2. El mensaje de "¡Correcto!" y de "Intentalo Nuevamente" no tienen que mover a los otros elementos cuando aparecen.
3. Los cuadrados deben desaparecer con un efecto de transición de CSS. 🔍 Investigá cómo hacerlo.
  
<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🤓 **Tip**: Cualquier duda acerca de los colores, tamaños y tipografías los podés averiguar usando el Inspector De Elementos.

</div>

🚀 Avanzá a la siguiente sección para potenciar tu proyecto.


---


### ***DRY***

Si tu juego funciona correctamente y tiene el estilo que te gusta, **¡refactorizá tu código!**

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🤓 **Tip**: El Principio No Te Repitas (_Don’t Repeat Yourself_, DRY) es uno de los principios en el desarrollo de _software_ cuyo principal objetivo es evitar la duplicación de código. Cuando refactorizamos el código no solo lo volvemos más elegante y prolijo sino que lo optimizamos.

</div>

🚀 Para potenciar tu proyecto refactorizá el código siguiendo estos pasos:

1. Los botones de _Easy_ y _Hard_ tienen un `event listener` similar. La diferencia entre ellos es que uno muestra 3 y, el otro, 6 colores. Para optimizarlo:
  + Sacale el ID y hacé que ambos compartan la misma clase. 
  + Comentá las 2 funciones de los botones. 
2. Seleccioná los botones y agregá un `event listener` que le dé la clase `selected` al botón cliqueado. 
3. Para actualizar `numSquare`, creá una condicional en la que, dependiendo del `textContent` del botón cliqueado, el Valor de `numSquare` sea 3 o 6. 🤓 Podés hacerlo con un operador ternario para ahorrar líneas de código.
4. Generá una Función `reset` para simplificar las líneas de código de estos procesos:
  + Generar nuevos colores en el Arreglo.
  + Elegir un color ganador.
  + Actualizar el _display_ de la página correctamente. 

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

👩‍🏫 **La Función `reset`**

La Función `reset` deberá considerar el mismo `if statement` en el que, dependiendo de si hay un color lo mostremos y, si no lo hay, lo ocultemos. Esto funcionará tanto en modo _Easy_ como en _Hard_.

</div>

⚠️ **Importante:** Ahora que existe la Función `reset`, borrá un poco del código. Por ejemplo, cuando hacés _click_ el botón `#reset` llama directamente a esa Función.

+++ Otros Usos De La Función `reset`

🤓 También podés usar la Función `reset` cuando recién carga la página: Podría estar en una nueva Función `init` donde esté todo lo que necesita hacer cuando se carga la página (por ejemplo, el evento para los botones de modo y el `event listener` de los cuadrados).

+++

#### Últimos Detalles

- Como las Variables `colors` y `pickedColor` son definidas por `reset`, deberás definirlas sin un Valor.
- Ejecutá `init`.
- Emprolijá `init`: Hacé 2 Funciones para los _listeners_ agregados. De esta manera, `init` solo será una Función que ejecuta 3 Funciones.

📛 Revisá y comprobá que tu proyecto funcione correctamente. Luego, pasá a la última sección de este proyecto.

---


### ***DRY***

Si tu juego funciona correctamente y tiene el estilo que te gusta, **¡refactorizá tu código!**

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🤓 **Tip**: El Principio No Te Repitas (_Don’t Repeat Yourself_, DRY) es uno de los principios en el desarrollo de _software_ cuyo principal objetivo es evitar la duplicación de código. Cuando refactorizamos el código no solo lo volvemos más elegante y prolijo sino que lo optimizamos.

</div>

🚀 Para potenciar tu proyecto refactorizá el código siguiendo estos pasos:

1. Los botones de _Easy_ y _Hard_ tienen un `event listener` similar. La diferencia entre ellos es que uno muestra 3 y, el otro, 6 colores. Para optimizarlo:
  + Sacale el ID y hacé que ambos compartan la misma clase. 
  + Comentá las 2 funciones de los botones. 
2. Seleccioná los botones y agregá un `event listener` que le dé la clase `selected` al botón cliqueado. 
3. Para actualizar `numSquare`, creá una condicional en la que, dependiendo del `textContent` del botón cliqueado, el Valor de `numSquare` sea 3 o 6. 🤓 Podés hacerlo con un operador ternario para ahorrar líneas de código.
4. Generá una Función `reset` para simplificar las líneas de código de estos procesos:
  + Generar nuevos colores en el Arreglo.
  + Elegir un color ganador.
  + Actualizar el _display_ de la página correctamente. 

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

👩‍🏫 **La Función `reset`**

La Función `reset` deberá considerar el mismo `if statement` en el que, dependiendo de si hay un color lo mostremos y, si no lo hay, lo ocultemos. Esto funcionará tanto en modo _Easy_ como en _Hard_.

</div>

⚠️ **Importante:** Ahora que existe la Función `reset`, borrá un poco del código. Por ejemplo, cuando hacés _click_ el botón `#reset` llama directamente a esa Función.

+++ Otros Usos De La Función `reset`

🤓 También podés usar la Función `reset` cuando recién carga la página: Podría estar en una nueva Función `init` donde esté todo lo que necesita hacer cuando se carga la página (por ejemplo, el evento para los botones de modo y el `event listener` de los cuadrados).

+++

#### Últimos Detalles

- Como las Variables `colors` y `pickedColor` son definidas por `reset`, deberás definirlas sin un Valor.
- Ejecutá `init`.
- Emprolijá `init`: Hacé 2 Funciones para los _listeners_ agregados. De esta manera, `init` solo será una Función que ejecuta 3 Funciones.

📛 Revisá y comprobá que tu proyecto funcione correctamente. Luego, pasá a la última sección de este proyecto.

---

### Conclusión

En este proyecto creaste un juego interactivo aplicando diferentes herramientas:

+ Usaste el DOM para manipular los elementos de HTML.
+ Utilizaste los eventos para darle interactividad al juego.
+ Aprendiste la utilidad de las Funciones en un proyecto real.
+ Optimizaste tu código.

**¡Felicitaciones por todo lo logrado!** Compartí tu proyecto en Discord y recordá incluirlo en tu Portfolio para la entrega final.

![starwars](https://i.imgur.com/YpRkw5P.jpg)

<div class="editor-recuadro">

 🛎️ **Recordá**: Si algún aspecto de PLEDU no funciona como esperabas o merece revisión podés avisarle al equipo de Contenido por [acá](https://forms.gle/okCETdVFsbg9S9kX7).
 
</div>

---

# Entrega: Color Game Project 🎨

En esta actividad pondrás en práctica tus conocimientos de JavaScript, DOM y eventos para desarrollar un juego interactivo de colores. ¡Es momento de demostrar lo aprendido y poner a prueba tus habilidades!


<div style="display:flex; align-items:center; justify-content:space-between; gap:16px; padding:24px; background:#2e7cd1; border-radius:12px; color:white; font-family:Arial,sans-serif; flex-wrap:wrap;">

  <div>
    <h2 style="margin:0 0 8px; font-size:22px;">
      U14 - Color Game Project 🎨
    </h2>
    <p style="margin:0; font-size:14px;">
      Poné en práctica lo aprendido y entregá tu proyecto.
    </p>
  </div>

  <a href="https://forms.gle/JhgGJpkh6F23hjA48" target="_blank" style="padding:12px 18px; background:white; color:#2e7cd1; border-radius:8px; text-decoration:none; font-weight:bold; white-space:nowrap;">
    Entregar trabajo  →
  </a>

</div>
