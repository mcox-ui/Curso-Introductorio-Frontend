### Arreglos 

Un **Arreglo** (del inglés _Array_) es una colección ordenada de elementos que identificamos mediante Índices. Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/OChnz-I3xUQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427256597-->

Recapitulando, un **Arreglo** es un conjunto de datos que se encuentran ordenados. Como vimos previamente, en _JavaScript_, los datos pueden ser de cualquier tipo (Números, _Strings_, Funciones, etc.). 

Gracias a los **Arreglos**, podemos reunir en un solo lugar los distintos tipos de datos, sin necesidad de crear una Variable para cada uno. Veamos un ejemplo:

Imaginemos que queremos agrupar los productos existentes en un _e-commerce_:

Si no usáramos **Arreglos** deberíamos crear una Variable que guarde el valor de cada elemento. 

```js
let producto1 = "iphone"
let producto2 = "smart tv"
let producto3 = "ipad"
```
<!----
<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">🛎 <b>Recordá:</b> Una buena práctica para programar es el <b>DRY</b>. Para optimizar el código y que no se repita, debemos agrupar y relacionar los elementos entre sí. De esta manera, no ocuparás espacio en la memoria creando 3 Variables distintas, sino que tendrás una sola que englobe a los elementos de la misma categoría.<br></p>

!---->

Volviendo al ejemplo, como sabemos que todos estos elementos pertenecen a la misma categoría, porque son productos del _e-commerce_, podríamos escribir un **Arreglo** que los agrupe en una lista: 

```js
let productos = ["iphone", "smart tv", "ipad"]
```

#### Sintaxis De Los Arreglos

```js
let nombreArreglo = [elemento1, elemento2, elemento3]
```

Como vimos en el ejemplo anterior, primero se define el nombre del Arreglo usando `let`. Luego del signo `=`, se deben abrir corchetes (`[]`) y, dentro suyo, enumerar los distintos elementos. 

⚠️**Importante**: Los elementos que estén dentro de los corchetes pueden ser cualquier tipo de datos. Si son _Strings_, debés escribirlos entrecomillados.

---

### ***Strings*** Como Colecciones De Caracteres

Los _Strings_ son cadenas de caracteres guardadas en direcciones de memorias continuas. Podemos acceder a cada letra usando corchetes (`[]`) y un Índice (un número que indica la posición del caracter).

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🤓 **La Propiedad Length**

La propiedad length nos permite tomar dimensión de la magnitud de un _String_. Es decir, nos ayuda a contar la cantidad de caracteres que hay en esa cadena. 

Si queremos acceder rápidamente a la propiedad length de un _String_, debemos escribir directamente la cadena de caracteres (o la Variable que la guarda) seguida por _".length"_. Por ejemplo: **variable.length**.

</div>

Teniendo en cuenta este ejemplo del _String_ `hello`, pensá qué devuelve cada sentencia sin probarlo en la consola:

![string.jpg](https://i.imgur.com/Lw7htRj.png)

```js
let word = "Hello"
word[0] 
word[1] 
word[4] 
word[5] 
```

¿Qué devolverá si le pasamos una Variable?

```js
let index = 3
word[index]
```

|||

En este caso, como la Variable contiene un valor numérico, nos devolverá el caracter que ocupe esa posición.

|||


¿Qué sucedería si le pasamos un valor de mayor extensión?


```js
let largoDelString = word.length
word[largoDelString] 
```





|||

Como _`length`_ te devuelve la cantidad de elementos que tiene el _String_, el resultado será _`undefined`_ porque en esa posición no hay nada.

Por lo tanto, deberíamos escribir:

```js
word[largoDelString - 1]
```

⚠️**Importante:** Para saber la cantidad de caracteres que tiene un _String_ debemos restarle 1 a la variable `largoDelString`. Esto se debe a que la longitud de la cadena de caracteres es siempre 1 mayor que el último Índice. 

|||

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🤓 **El Índice**

El Índice (en inglés, _Index_) nos revelará cuál es la posición que ocupa cada caracter de un _String_ o de un Arreglo.

⚠️ **Importante**: El primer Índice de un _String_ es cero (0).

</div>

También funciona para _Strings_ más largas. Mirá este ejemplo y descubrí qué devuelve cada sentencia:

```js
let saludo = "¡Hola! Bienvenid@s a nuestra página"

saludo[0]// "¡"
saludo[1] // "H"
saludo[28] //" "
saludo[29] //"p"

let index = 2
saludo[index]
// "o"

let longitud = saludo.length
saludo[longitud]
// Devuelve undefined porque el último índice es, siempre, un número menor que la cantidad de elementos de una cadena de caracteres.

saludo[longitud - 1]
// "a"
```

---

### Índice De Un Arreglo En JavaScript

El **Índice** (del inglés _Index_) es la posición que ocupa un elemento dentro de un **Arreglo**. Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/Rfn8DjMZlqo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427259460-->

Como vimos en el video, los Arreglos nos permiten agrupar datos en una lista ordenada. Por lo tanto, cada elemento ocupa una posición indexada numéricamente.

Por ejemplo, en el Arreglo `amigos`...: 

```js
let amigos = ["Juan", "Pepe", "Jorge", "Francisco"]
```

... cada uno de ellos tiene un **Índice**:

| Juan | Pepe | Jorge | Francisco |
| ----------- | ----------- | ----------- | ----------- |
| 0 | 1 | 2 | 3 |

⚠️ **Importante:** Recordá que el primer Índice de un arreglo siempre es 0 (cero). Por lo tanto, el Índice más alto siempre será uno menos que la cantidad total de elementos (`length`).

```js
amigos[0] // Juan
amigos[1] // Pepe

amigos.length // 4
amigos[amigos.length]  // Es undefined porque el Índice más alto es 3 y queremos acceder al Índice 4 que responde a la propiedad .length.
amigos[amigos.length-1] // Si queremos acceder al último elemento de un Arreglo, usamos length-1, que en este caso da como resultado "Francisco".
```

+++ ¿Para Qué Se Usa La Propiedad `length`?

Podemos usar la propiedad `.length` para saber cuántos elementos tiene un Arreglo. 

```js
nombreArreglo.length
```

⚠️**Importante:** Cada vez que agregamos elementos a la lista, el valor de `.length` se modifica y, de esta manera, es facil acceder al número total.


A su vez, podemos acceder al último elemento de un Arreglo usando la fórmula `.length-1`. De esta forma podemos saber cuál es el índice máximo.

```js
nombreArreglo[nombreArreglo.length-1]
```

+++

#### Usos De Los Índices

Podemos usar los Índices para:

1. Actualizar un valor:

```js
let amigos = ["Juan", "Pepe", "Jorge", "Francisco"] // Esta es el Arreglo original.
amigos[0]="Juancito" // Cambiamos "Juan" por "Juancito"
amigos[3]="Pancho" // Cambiamos "Francisco" por "Pancho"
// El Arreglo quedará actualizado así: ["Juancito", "Pepe", "Jorge", "Pancho"]
```

2. Agregar nuevos elementos:

```js
let amigos = ["Juancito", "Pepe", "Jorge", "Pancho"]
amigos[4]="Marco" // Agregamos a "Marco" a la lista.
amigos[5] = "Mateo" // Agregamos a "Mateo" a la lista.
// El Arreglo quedará actualizado así: ["Juancito", "Pepe", "Jorge", "Pancho", "Marco", "Mateo"]
```


👩‍🏫👨‍🏫 **¿Qué pasaría si agrego un nuevo amigo en el Índice 10?**

```
amigos[10] = "Nicolas"
```

|||

```js
amigos
(11) ["Juancito", "Pepe", "Jorge", "Pancho", "Marco", "Mateo", empty × 4, "Nicolas"]
```

Los Índices del 6 al 9 quedarán vacíos (del inglés _empty_) porque nos salteamos todas esas posiciones.

|||


---

### Cómo Acceder A Los Datos De Un Arreglo

Como ya vimos, los Arreglos pueden ser una colección de cualquier tipo de dato. Mirá este video para aprender a acceder a ellos:

<iframe width="600" height="355" src="https://www.youtube.com/embed/Vk-wIISCXEM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


<!--@vimeo=427260974-->

Como vimos en el video, los Arreglos son una colección de cualquier tipo de dato. Para acceder a esta información, seguí estos pasos:

1. Localizá el elemento: Usá un Índice para acceder a su posición en el Arreglo.
2. Manipulá el dato como lo hacés regulamente: Si es una Función, por ejemplo, ejecutala; si es un sub-Arreglo usá Índices para acceder a ellos.


Mirá este ejemplo y descubrí su resultado sin probarlo en la consola:

```js
coleccionRandom=["Hola", 22, true, null, function(){console.log("hello")}, ["hola", "chau"]] // Este Arreglo tiene distintos tipos de datos.

coleccionRandom[4]
coleccionRandom[4]()
coleccionRandom[5] 
coleccionRandom[5][0] 
```

|||

```js
coleccionRandom[4] // Al acceder al quinto elemento del Arreglo, ubicamos la Función pero no la ejecutamos.
ƒ (){console.log("hello")}
```

```js
coleccionRandom[4]() // En este caso, no solo accedemos al elemento sino que ejecutamos la Función.
hello
```

```js
coleccionRandom[5] // Accedemos al elemento de la posición 5. En este caso es otro Arreglo que tiene dos datos (que son Strings).
["hola", "chau"]
```

```js
coleccionRandom[5][0] // De esta manera accedemos al valor que está en la posición cero del sub-Arreglo.
"hola"
```

|||

⚠️**Importante:** Si querés acceder a un elemento en un sub-Arreglo (un Arreglo dentro del principal):
1. Seleccioná el Arreglo dentro del principal. 
2. A continuación, accedé al elemento que querés ubicar.

---

### Ejercicio: ¿Qué Devuelven Estos Códigos? 

En este ejercicio deberás pensar qué devuelven estos códigos sin probarlo en la consola.

👉 **¿Qué devuelve este `console.log`?**

```js
let numbers =[22, 33, 54, 66, 72]

console.log(numbers[numbers.length]) 
```

👉 **¿Qué personaje se muestra en la consola?**
```js
let grupoDeAmigos =[
["Harry", "Ron", "Hermione"],
["Spiderman", "Hulk", "Ironman"],
["Penélope Glamour", "Pierre Nodoyuna","Patán"]
]
console.log(grupoDeAmigos[2][0]) 
```

|||

Si no sabés quién es este amigo, hacé *click* [acá](https://es.wikipedia.org/wiki/Pen%C3%A9lope_Glamour).

|||

---

### Ejercicio: Lista de Súper - Parte I

En este ejercicio deberás crear un Arreglo con los productos que tenés que comprar en el supermercado.

<div class="editor-recuadro">

⚠️ **Importante**: Creá un Arreglo vacío que puedas ir llenando a medida que incorpores productos a tu lista.
</div>



Para hacer este ejercicio, seguí estos pasos:

1. Instanciá un Arreglo y guardalo en la variable `listaDeSuper`.
2. Agregá los productos que tenés que comprar. 

|||

```js
listaDeSuper[0]="sal"
```

|||

3. Accedé al primer elemento de tu lista.
4. Creá una Variable llamada `ultimoElemento`. El valor de esta Variable tiene que ser un número que indique la posición del último elemento.

|||

```js
let ultimoElemento= listaDeSuper.length - 1 
```

|||

5. Accedé a ese último elemento usando la variable `ultimoElemento`.

---

### Métodos De Arreglos (Array Methods)

### `push()` Y `pop()`

![push-pop](https://i.imgur.com/0gBKL7Q.jpg)

Para manipular los Arreglos podemos usar los **Métodos de Arreglo** (del inglés, *Array Methods*).

Mirá este video para aprender acerca de dos de ellos, `push()` y `pop()`:

<iframe width="600" height="355" src="https://www.youtube.com/embed/eX_jjLi5zlE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427263627-->


#### Método `push()`

Para agregar elementos al final de nuestro Arreglo- sin necesidad de saber cuál es el último Índice-, usaremos el método `push()`. 

👩‍🏫👨‍🏫 **Sintaxis Del Método `push()`**:

```js
nombreDelArreglo.push()
```

`.push()` añade un nuevo elemento al final del Arreglo. Para agregar el valor, debés pasarlo como argumento del método.

⚠️ **Importante:** Para agregar varios elementos dentro del mismo método, debés separar los valores con comas (`,`):

```js
.push(valor1, valor2) 
```

Veamos un ejemplo:

```js
let colores=["rojo", "verde", "azul"]

colores.push("amarillo")

// el Arreglo colores quedará confomado por "rojo", "verde", "azul" y "amarillo".
```

Como vemos, `push` agregará el elemento `amarillo` al final del Arreglo. En caso de que quisiéramos sumar más de un elemento, los incluiremos dentro del mismo método, sin necesidad de volver a usar `push`.

```js
colores.push("marron","violeta")

// ["rojo", "verde", "azul", "amarillo", "marron", "violeta"]
```

👩‍🏫👨‍🏫 El método `push`, además de agregar valores a un Arreglo, retorna la cantidad de elementos que hay guardados en él.


```js
let colores=["rojo", "verde", "azul"]

colores.push("amarillo")
4
colores.push("marron","violeta")
6
```


#### Método `pop()`

El método `.pop()` saca el último elemento del Arreglo y lo retorna. Ese valor, a su vez, lo podemos guardar para volverlo a usar. 

⚠️**Importante:** El método `pop` no lleva Argumentos y solamente saca el último elemento, uno por vez.

👩‍🏫👨‍🏫 **Sintaxis Del Método `pop()`**:

```js
nombreDelArreglo.pop()
```

Veamos un ejemplo:

```js
let color = colores.pop() // "amarillo"

// ["rojo", "verde", "azul"]
```

Como vemos, `.pop()` no solo quitó el último elemento del Arreglo, sino que también lo devolvió. Ese valor podemos guardarlo en una Variable para, luego, utilizarla.

Veamos en este ejemplo un poco más acerca de `.pop()`:



```js
let numbers = [] // Inicializamos un Arreglo vacío para que tenga los métodos de un Arreglo, aunque no tenga elementos.

numbers.push(2) // Agrega 2 al Arreglo.
numbers.push(4, 5, 7) // Agrega 4, 5 y 7 después del 2.

numbers.pop() // Quita el último elemento.

7 // En este caso es el 7, y lo retorna.
```


Qué sucedería si hacemos: `console.log(numbers)`

|||
```js
console.log(numbers) 

(3) [2, 4, 5]
```

|||

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

👩‍🏫👨‍🏫 **¿Qué Sucedió Con El Número 7?**

Como no hicimos nada cuando sacamos el número 7, ahora no lo podemos re-utilizar. 

Si hubiéramos querido conservarlo, deberíamos haberlo guardado en una Variable al ejecutar el `.pop()`: `let guardarValor= nombreArreglo.pop()`.

</div>

|||
```js
let numbers = [] 
numbers.push(2)
numbers.push(4, 5, 7)
let ultimoNumero = numbers.pop()
console.log("Guardé el último número: "+ ultimoNumero)
alert("Si corremos otra vez .pop(), sacaremos otro número: "+ numbers.pop())
```
|||

---

### `unshift()` y `shift()`

Los métodos `unshift` y `shift`, agregan y quitan elementos al comienzo del Arreglo. Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/-XnEOziITmA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427264647-->

Como vimos en el video, para agregar elementos al comienzo de nuestro Arreglo, usaremos el método `unshift` siguiendo esta sintaxis:

```js
nombreArreglo.unshift(elemento/s)
```

El método `shift`, en cambio, quita los elementos que estén al comienzo de la posición y los retorna:

```js
nombreArreglo.shift() // Retorna el o los valores eliminados
```

🛎 **Recordá**: Si querés reutilizar el valor que retorna `shift`, guardalo en una Variable.

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

⚠️ **Importante**: Para agregar varios elementos separalos con una coma (`,`). 

</div>

Veamos este ejemplo para entender mejor cómo funcionan estos métodos:

```js
let numerosPrimos = [7, 11, 13, 17]
numerosPrimos.unshift(5)
// [5, 7, 11, 13, 17]
numerosPrimos.unshift(1, 2, 3)
// [1, 2, 3, 5, 7, 11, 13, 17]

let noEsUnNP=numerosPrimos.shift() // 1
// [2, 3, 5, 7, 11, 13, 17]
```

---

### `indexOf()`

El método `indexOf()` verifica la posición de un elemento dentro de un Arreglo y nos devuelve su Índice. 

Mirá el siguiente video al respecto:

<iframe width="600" height="355" src="https://www.youtube.com/embed/Cbuzd_Tdmv8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

⚠️ **Importante:** Si ese elemento no existiera en el Arreglo, nos retornará `-1`.


#### Sintaxis De `indexOf()`

```js
nombreArreglo.indexOf(elemento)
```

Veamos un ejemplo para entender cómo funciona:

```js
let amigos = ["Juan", "Pepe", "Jorge", "Francisco", "Juan"]
amigos.indexOf("Pepe") // nos devuelve el índice 1.
amigos.indexOf("Juan") // devuelve la primera coincidencia, es decir, 0.
amigos.indexOf("Guille") // Devuelve -1 porque no hay un Guille en este arreglo.
amigos.indexOf("juan") // Devuelve -1 porque es "case sensitive"
```

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🛎 **Recordá**: JavaScript es ***case sensitive***, es decir, las mayúsculas y las minúsculas tienen codificaciones distintas. Por eso, el elemento que pasemos como Argumento tiene que ser exactamente el mismo que contenga el Arreglo. 

</div>

#### Ejercicio:

1. En este ejercicio deberás crear un Arreglo con 5 amigos. Dos de ellos, deben repetirse.

|||
```js
let amigos = ["Juan", "Pepe", "Jorge", "Francisco", "Juan"] 
```
|||

2. Luego:
  + Escribí un código que chequee si tenés algun amigo llamado Félix. 
  + Si es así, deberá mostrar un mensaje que diga: *"Tengo un amigo que se llama Félix"*, sino: *"Sería bueno tener un amigo que se llame Félix"*.
  
3. Transformá tu código en una Función que reciba como Argumento cualquier nombre y verifique si tenés ese amigo o no (repitiendo las mismas frases que en el punto anterior).

---

### `slice()`

El método `slice()` se usa para generar una copia de un Arreglo. Esto sirve para trabajar sobre el clon del Arreglo sin afectar su original. Mirá este video para aprender cómo funciona y cuál es su utilidad: 

<iframe width="600" height="355" src="https://www.youtube.com/embed/It33mttgfyI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427591815-->


Recapitulando, como los Arreglos se pasan por referencia y no por valor, necesitamos un método para poder alterar un Arreglo sin afectar el original. 

+++ ¿Qué Sucede Si No Usamos El Método Slice?

Si queremos hacer una copia de un Arreglo pero sin usar el método `slice()`, podemos obtener resultados no deseados.

Como los Arreglos se pasan por referencia, si tenés dos Variables que apuntan a la misma, cualquier cambio que hagas en una va a modificar a ambas. Esto se debe a que apuntan al mismo espacio en memoria, por ende, tienen relación entre sí.

Veamos un ejemplo:  

```js
let frutas =["banana", "naranja", "limón", "manzana", "sandia", "mango"] // Un Arreglo con varias frutas.
let frutas2 = frutas // La variable "frutas2" referencia al Arreglo guardado en "frutas".
frutas2.pop() // Quitamos el último elemento de "frutas2".
"mango" // Ese elemento es "mango".
frutas // Si llamamos al Arreglo "frutas", nos devolverá sus elementos:
(5) ["banana", "naranja", "limon", "manzana", "sandia"]// El elemento "mango" del Arreglo "frutas" fue quitado usando el método pop sobre "frutas2".
```

⚠️ **Importante:** Como ambas Variables apuntaban al mismo espacio en memoria, al hacer un cambio en una, la otra también fue afectada. 

+++

En síntesis, el método `slice` nos permite clonar nuestro Arreglo de tal forma que, si cambiamos nuestro clon, el original no se vea afectado.

#### Sintaxis Del Método `slice()`

```js
let arregloCopia = arreglo.slice()
```

#### Los Argumentos Del Método `slice()`

- `.slice()`: Si el Argumento queda vacío, `slice` copia el Arreglo entero. Debemos guardar ese valor en una Variable.

- `.slice(argumento1)`: Clona el Arreglo desde el Índice pasado como Argumento (en este caso, `argumento 1`) y lo clona desde ese elemento inclusive hasta el último. 

- `.slice(argumento1, argumento2)`: Clona el Arreglo desde el Índice pasado como primer Argumento (`argumento 1`), lo selecciona, y clona desde ese Índice hasta el segundo Argumento (`argumento2`), sin incluirlo. 

Veamos un ejemplo para ver la diferencia de cada caso:

```js
let todasFrutas = frutas.slice(); // Clona el Arreglo entero.
```

|||

```js
frutas
["banana", "naranja", "limon", "manzana", "sandia"]
let todasFrutas = frutas.slice();
todasFrutas
["banana", "naranja", "limon", "manzana", "sandia"]
```

|||

```js
let todosMenosBanana = frutas.slice(1) // Clona desde el Índice 1 inclusive hasta el final.
```

|||

```js
frutas
["banana", "naranja", "limon", "manzana", "sandia"]
let todosMenosBanana = frutas.slice(1) 
todosMenosBanana
["naranja", "limon", "manzana", "sandia"] // Clona el Arreglo "frutas" desde el Índice 1 inclusive hasta el final.
```

|||

```js
let citricos = frutas.slice(1, 3) // Clona desde el Índice 1 hasta el 2, sin incluir el 3.
```

|||

```js
frutas
["banana", "naranja", "limon", "manzana", "sandia"]
let citricos = frutas.slice(1, 3)
citricos
["naranja", "limon"] ) // Clona desde el Índice 1 hasta el 2, sin incluir el 3.
```

|||


---

### `splice()`

El método `.splice()` elimina de un Arreglo una cantidad de elementos a partir de una posición dada. Mirá este ejemplo para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/JVMFbSp3MXM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427593858-->

Como vimos en el video, con `.splice()` podemos elegir desde dónde sacar uno o más elementos de un Arreglo. La diferencia con los métodos `shift` y `pop` es que, con ellos, solo podíamos quitar los del comienzo o el final de un arreglo.

Veamos la sintaxis del método `.splice()`:

```js
nombreArreglo.splice(argumento1,argumento2)
```

En este método, el `argumento1` determinará el Índice a partir del cual quiero remover los elementos (incluyendo esa posición). Por su parte, el `argumento2` establecerá la cantidad de elementos que quiero remover.

⚠️**Importante:** El método `.splice()` devuelve los elementos eliminados en un nuevo Arreglo. 

Veamos un ejemplo:

```js
let puntajes = [1,7,0,8,4,9] // Definimos el Arreglo.
let comenzandoEnIndice = 2 // Posición a partir de la que vamos a remover elementos.
let numeroAremover = 3 // Cantidad de elementos que vamos a quitar.
puntajes.splice(comenzandoEnIndice,numeroAremover) // Método aplicado.
[0, 8, 4] // Retorna en un Arreglo los elementos que quitó.
```

👩‍🏫👨‍🏫 Para optimizar el código, hacelo de esta manera:

```js
let puntajes = [1,7,0,8,4,9]
puntajes.splice(2,3) // Método aplicado.
```
+++ ¿Cómo Guardar Los Elementos Eliminados En Una Variable?

Para guardar los elementos eliminados en una Variable, definila antes de aplicar el método:

```js
let puntajes = [1,7,0,8,4,9] // Definimos el Arreglo.
let guardarValor = puntajes.splice(2,3) // Guardamos el Arreglo en una Variable para reutilizarlo.
```
+++

---


#### Contenido Bonus

Con `.splice()` podés:

- Eliminar elementos desde la posición elegida y, al mismo tiempo, añadir otros en ese lugar. 
- Añadir elementos desde una posición determinada sin necesidad de eliminar nada.

Veamos cuál es la sintaxis para el primer caso:

```js
nombreArreglo.splice(argumento1,argumento2,argumento3)
```

En este caso, el `argumento3` indica el elemento nuevo a incorporar. 

⚠️**Importante:** Para incorporar más elementos, deberás agregarlos separándolos por comas (`,`).


Mirá este ejemplo:

```js
let puntajes = [1,7,0,8,4,9]
puntajes.splice(5,1,6) // Elimina el valor de la posición 5 y agrega, en su lugar, el número 6.
puntajes
[1, 7, 0, 8, 4, 6] // Reemplazó el número 9 por el 6.
```

En cambio, si queremos añadir elementos desde una posicion en particular, sin eliminar ningun otro, debemos seguir esta sintaxis:

```js
nombreArreglo.splice(argumento1,0,argumento3)
```

En este caso, el `0` indica que no estoy eliminando ningún elemento y, `argumento3` indica los elementos nuevos a incorporar desde la posición dada por `argumento1`. 

```js
let puntajes = [1,7,0,8,4,9]
puntajes.splice(1,0,4)
[]// Esto indica que no sacamos nada, por eso el Arreglo queda vacío.
puntajes // Si llamamos a puntajes, nos devolverá el nuevo Arreglo con el número 4 en posición 1.
[1, 4, 7, 0, 8, 4, 9]
```

---

### `join()` Y `split()`

El **método `join()`** convierte un Arreglo en una cadena de caracteres. Mientras que **`split()`** convierte una cadena de caracteres en un Arreglo. Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/yY0qWSsJed8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427596013-->

Como vimos en el video, estos métodos son muy simples.

Analicemos el **método `join()`** pasándole distintos datos como Argumento:

1. Sin pasarle datos como Argumento:

```js
let arr = ["Hola", "Mery"]
arr.join()// No le pasamos nada como Argumento. 
"Hola,Mery"// Separa los elementos del Arreglo por una coma.
```

2. Pasando como Argumento unas comillas (`""`):

```js
let arr = ["Hola", "Mery"]
arr.join("")
"HolaMery"
```

En este caso, une los elementos del Arreglo en una sola cadena de caracteres.

3. Pasando como Argumento un caracter:

Si pasamos como Argumento un caracter, `join()` nos devolverá los elementos del Arreglo sepadados por ese caracter. Por ejemplo, si le pasamos como Argumento un espacio: 

```js

let arr = ["Hola", "Mery", "¿cómo", "estas?"]
arr.join(" ") // Le pasamos como Argumento un espacio.
"Hola Mery ¿cómo estas?" // Nos devuelve un String con los datos separados por espacios.
```

Si le pasáramos una _string_ como "(sic)", retornará: 

```js
let arr = ["Hola", "Mery", "¿cómo", "estas?"]
arr.join("(sic)")
"Hola(sic)Mery(sic)¿cómo(sic)estas?"
```

⚠️ **Importante:** Cuando hacemos `join()` no modificamos el Arreglo original sino que tomamos sus elementos y los manipulamos.

En cambio, el **método `split()`**, separa un _String_ y lo convierte en un Arreglo con sus distintas posiciones. 

⚠️ **Importante:** Aquello que le pasemos como Argumento le indicará al método dónde debe hacer el corte. 

Veamos cómo funciona pasando como Argumento un espacio:

```js
let cadena = "Hola Mery"
let arr = cadena.split(" ")// Le indicamos dónde hacer el corte. En este caso, en donde haya un espacio.
console.log(arr)
["Hola", "Mery"] // Retorna un Arreglo con los Strings separados en cada posición.
```

Veamos cómo funciona cuando le pasamos como Argumento la letra "e":

```js
let cadena = "Hola Mery"
let arr = cadena.split("e")// Le indicamos dónde hacer el corte. En este caso, la letra "e".
console.log(arr)
["Hola M", "ry"] // JS buscará, primero, si existe ese caracter en la cadena. Luego, lo eliminara y, por último, me devolverá el Arreglo separando sus elementos por dónde estaba ese caracter.
```

---

### ***Filter***

`.filter()` es un método que retorna un nuevo Arreglo, con los datos filtrados según una Función que le pasamos por Parámetro. 

Veamos un ejemplo: supongamos que queremos saber cuántos alumnos aprobaron un examen. Si quisiéramos filtrar solo las notas de aquellos alumnos que sacaron más de un 6, podríamos hacerlo de esta manera:

```js
let notas = [1, 2, 3, 4, 10, 7, 6, 4, 8];
let aprobadas = [];

for (let i = 0; i < notas.length; i++) {
 if (notas[i] >= 6) {
   aprobadas.push(notas[i])
 }
}
console.log(aprobadas); // [10, 7, 6, 8] - hay 4 notas aprobadas
console.log(notas); // [1, 2, 3, 4, 10, 7, 6, 4, 8] - es el arreglo original
```

Sin embargo, con el método `.filter()` podríamos resolverlo de una forma mucho más sencilla:

**Con ***Arrow Functions***:** 

```js
let notas = [1, 2, 3, 4, 10, 7, 6, 4, 8];
let aprobadas = notas.filter(nota => nota >= 6)
```

**Sin ***Arrow Functions***:**

```js
let notas = [1, 2, 3, 4, 10, 7, 6, 4, 8];


let aprobadas = notas.filter(function(nota) {
return nota >= 6; });
console.log(aprobadas); // [10, 7, 6, 8] - hay 4 notas aprobadas
console.log(notas); // [1, 2, 3, 4, 10, 7, 6, 4, 8] - es el arreglo original
```

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

⚠️ **Importante**: Con el método `.filter()` podemos filtrar Arreglos que contengan cualquier tipo de datos.

</div>

Si quisiéramos crear un filtro manipulando datos booleanos (_true_ y _false_), podríamos hacerlo de la siguiente forma.

En este ejemplo, filtramos solo la comida vegetariana:

```js
let comidas = [
 { nombre: '1', vegetariana: false }, { nombre: '2', vegetariana: true },
 { nombre: '3', vegetariana: true }, { nombre: '4', vegetariana: false }
];

let vegetarianas = comidas.filter(comida => comida.vegetariana === true)
//  const vegetarianas = comidas.filter(function (comida) {
//   return comida.vegetariana;
//  });

console.log(vegetarianas);
// [{ nombre: '2', vegetariana: true }, { nombre: '3', vegetariana: true }]

---

### Ejercicio: Lista De Súper - Parte II

En este ejercicio, deberás poner en práctica lo aprendido usando como base el ejercicio de la Lista de Súper - Parte I. 

1. Agregá dos nuevos productos al final de la lista.

|||

Usá `.push()`.

|||

2. Agregá dos productos al principio de tu lista.

|||

Usá `.unshift()`.

|||

3. Determiná cuán largo es el Arreglo en este momento.

|||

Usá la propiedad `length`.

|||

4. Sacá un producto y guardalo en una Variable que se llame `noHabia`.

|||

Usá `.pop()`.

|||

5. Sacá un producto y guardalo en otra Variable que se llame `comprado`.

|||

Usá `.shift()`.

|||

6. ¿Cuán largo es el Arreglo ahora?

---

### Iteración De Arreglos

### Iterar Un Arreglo

Iterar un Arreglo en JavaScript es recorrerlo para acceder a sus elementos. 

Pero, ¿por qué tendríamos que hacerlo?

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

👩‍🏫👨‍🏫 Deberíamos **iterar** un Arreglo para acceder a sus elementos. Es decir, determinar mediante **Índices** las diferentes posiciones. Para hacerlo, usamos una **Estructura de Control Repetitiva** (un bucle o, en inglés, _loop_) para recorrer el Arreglo y acceder a cada valor.

</div>

Esta es una de las tareas más comunes para manipular Arreglos. En las próximas secciones veremos dos formas de _loopear_ sobre un Arreglo: ***For Loop*** y ***For Each***.

---

### ***For Loop***

Como vimos en la sección anterior, los _For Loops_ son una de las maneras para iterar un Arreglo. Mirá este video para aprender más acerca de ellos:

<iframe width="600" height="355" src="https://www.youtube.com/embed/Pa3VvIuhfcQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427598673-->

Recapitulando, los _For Loops_ son muy útiles para recorrer un Arreglo y mostrar todos sus elementos. Sin embargo, no es la única manera de hacerlo. Veamos algunos ejemplos usando el bucle que ya conocemos: el _While Loop_.

#### ***For Loop*** Vs. ***While Loop***

Imaginemos que tenemos un Arreglo con colores y queremos mostrar cada uno en la consola. Veamos cómo podríamos escribir este código:

```js
let colores=["Rojo", "Azul", "Verde", "Amarillo"] // Este es el Arreglo que vamos a iterar

console.log(colores[0])
console.log(colores[1])
console.log(colores[2])
console.log(colores[3])
```

Como podemos ver, este código es muy repetitivo: estamos haciendo la misma acción sobre cada uno de los elementos. 

Si quisiéramos optimizarlo, podríamos usar un _While Loop_. Para eso, deberíamos seguir estos pasos:

1. Inicializar una Variable que empiece en cero y que funcione como **Contador** del _Loop_ hasta el último índice. 
2. Establecer la **condición**. 
3. Escribir el **bloque de código** que indique lo que haremos dentro del _While_.

```js
while(condicion){
bloque de codigo
}
```

4. Asegurar que el _While_ tenga una **condición de corte**. 

|||

En este caso será un incremento de los valores hasta igualar la cantidad de elementos del Arreglo.

Para acceder a cada uno por separado, deberíamos iterarlo tantas veces como elementos tenga. Para esto, usaremos la propiedad  `.length`, que nos dirá el total de elementos que tiene el Arreglo. 
Cuando el **Contador** sea igual al `.length`, la Variable habrá tomado el valor de cada uno de sus Índices y habrá accedido a todos sus elementos.

|||

Siguiendo estos pasos, nuestro código se verá así:

```js
let colores=["Rojo", "Azul", "Verde", "Amarillo"] // Inicializo la Variable colores.
let i = 0 // Inicializo la Variable Contador.

while(i < colores.length){ // Se establece la condición.
console.log(colores[i]) // Bloque de código que indica la acción que se ejecutará.
i++ // Incremento del Contador que asegura la condición de corte.
}
```
|||
```js
Rojo
Azul
Verde
Amarillo
```
|||

Sin embargo, hay una manera todavía más útil para iterar un Arreglo: el _For Loop_. Veamos su sintaxis:

```js
for (inicializacion; condicion; incremenento/decremento) {
    // Bloque de código que indica lo que querés hacer dentro del for.
}
```

Veamos cada elemento por separado:
- **Inicialización:** Es la Variable que permite iterar el Arreglo. Esta expresión se ejecuta una sola vez. Solemos llamar a esta variable **Contador**.

⚠️ **Importante:** Podemos inicializar todas las Variables que queramos, separándolas con una coma (`,`).

- **Condición:** Es una expresión que se evalúa en cada iteración.  
- **Incremento/Decremento**: Es una expresión que actualiza el valor de la Variable **Contador** después de cada iteración y asegura la condición de corte. Podemos especificar de qué manera queremos que se incremente o decremente el valor (si de uno en uno, de dos en dos, etc.)

Si bien el `For Loop` no es muy distinto al _While Loop_, su sintaxis es más simple para manipular arreglos. Veamos cómo quedaría el ejemplo anterior optimizado con un _For Loop_:

```js
let colores=["Rojo", "Azul", "Verde", "Amarillo"]
for(let i = 0; i < colores.length; i++ ){
  console.log(colores[i]) 
}
```

Como podemos ver, usamos menos líneas de código y es más ordenado. 

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 
👩‍🏫👨‍🏫Creamos una Variable <em>i</em> dentro del <i>For</i> que solo existe momentáneamente mientras corre ese <i>Loop</i> (a diferencia del <i>While</i> cuya variable es global).
<p>

+++ ¿Cuándo Te Conviene Usar Un _For_ Y Cuándo Un _While_?

Si bien podrías usar de forma indistinta un _While Loop_ o un _For Loop_, las buenas prácticas sugieren que uses el _While Loop_ cuando no sepas cuántas iteraciones sucederán hasta que la condición sea _false_. En cambio, se utiliza el _For Loop_, sobre todo, con Arreglos en los que se sabe de antemano cuántos elementos contiene. De esta manera, la propiedad `.length` asegurará la **condición de corte**. 

Veamos este ejemplo para entender mejor cuándo usar un _While Loop_:


```js

let input

while( !(input = prompt('Escriba su nombre, por favor.')) ){
  alert("No recibimos la información.")
}

alert("¡Gracias! Su nombre es: " + input + ".")

```

En este caso, como no sabemos cuántos intentos (o iteraciones) va a llevar que el usuario cumpla con lo pedido, es mejor usar un _While Loop_. 


+++

---

+++ ¿Por Qué En Un _For Loop_ Conocemos La Cantidad De Iteraciones?

Como existen expresiones que se reemplazan por números, podemos saber de ante mano la cantidad de iteraciones que tendrá un _For Loop_. Por ejemplo:

```js
i < array.length
```

Es decir, `array.length` será igual a la cantidad de elementos que tenga ese Arreglo y, por lo tanto, será un número.

+++

Para ver más ejemplos, mirá este video:

<iframe width="600" height="355" src="https://www.youtube.com/embed/c6b9b_la5-g" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427600256-->


---

### `forEach()`

`forEach()` es una manera relativamente nueva, y aún más simple, de iterar sobre un Arreglo. Mirá este video para aprender más acerca de este método:

<iframe width="600" height="355" src="https://www.youtube.com/embed/uyvgpKSBgRA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427602209-->


Recapitulando, la ventaja de usar `forEach()` es su potencia para simplificar un mismo código. Analicemos su sintaxis:

```js
nombreArreglo.forEach(function(elemento){
// Accion sobre cada elemento
})
```

- `nombreArreglo`: Es el Arreglo que queremos recorrer.
- `.forEach()`: Es el iterador que usaremos.
- `function()`: Es la Función que se ejecutará sobre cada elemento. Para hacerlo, deberás pasarle un Parámetro (dentro del paréntesis).
- `elemento`: Es el Parámetro que hace referencia a cada elemento del Arreglo (irá cambiando en cada iteración hasta haberlos recorrido completamente). 
- `acción`: Es la Función que queremos que se ejecute sobre cada elemento del Arreglo.

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

👩‍🏫👨‍🏫 El Iterador `forEach()` permite ejecutar una Función sobre cada elemento del Arreglo.

El beneficio de este Iterador sobre el resto es que no hace falta ni inicializar una Variable, ni plantear una condición, ni asegurar una acción de corte.

`forEach()`, por lo tanto, debería usarse solamente cuando queremos recorrer el Arreglo entero y ejecutar la misma Función para todos los elementos

</div>

Veamos un ejemplo para entender la ventaja de usar `forEach()`:

Si quisiéramos mostrar por consola todos los elementos, podríamos usar un _For Loop_:

```js
let colores=["Rojo", "Azul", "Verde", "Amarillo"]

for(let i = 0; i < colores.length; i++ ){
  console.log(colores[i]) 

}
```

Sin embargo, hacer la misma acción repetidamente sobre los mismos elementos, deriva en un código redundante. Para simplificarlo, es más potente el método `forEach()`:

```js
let colores=["Rojo", "Azul", "Verde", "Amarillo"]

colores.forEach(function(color){
  console.log(color)
})
  
```

De esta manera, el programa ejecutará la Función sobre cada uno de elementos del Arreglo y, en cada ejecución, tomará un elemento distinto como Argumento. Esto se cumplirá hasta que recorra todos los elementos del Arreglo.

También podríamos escribir:

```js
var loggeaColores = function(color){
  console.log(color)
}
colores.forEach(loggeaColores)
```

En conclusión, `forEach()` hace más simple el acceso y manipulación de cada uno de los elementos de un Arreglo. 

<div class="editor-recuadro">

 🛎️ **Recordá**: Si algún aspecto de PLEDU no funciona como esperabas o merece revisión podés avisarle al equipo de Contenido por [acá](https://forms.gle/okCETdVFsbg9S9kX7).
 
</div>

---

# Otros metodos

### Introducción: Métodos De ES6

<div class="editor-recuadro">

⚠️ **Importante:**  Las siguientes secciones son un **Contenido Bonus** de la clase. Puede presentar un nivel de dificultad mayor y es necesario estar al día para poder realizarlos. Si querés desafiarte como _developer_, no dejes de realizarlos.

</div>


A continuación, veremos los siguientes métodos para iterar Arreglos:
- `.map()`
- `.reduce()`


Estos métodos surgen con la última actualización de ES6 y son **alternativas** que simplifican el código.

Para leer más sobre ECMAScript, podés revisar la [documentación oficial (en inglés)](https://tc39.es/ecma262/).

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 
 
 ⚠️**Importante:** como estos métodos sirven para Arreglos ubicamos este contenido en la presente unidad. Sin embargo, algunos ejercicios pueden requerir conocimientos de Objetos (que se trabajarán en la próxima clase). 
 
  
</div>

---

### ***Map***

El método `.map()` es una forma de iterar sobre cada elemento del arreglo. Recibe una función que tiene dos argumentos (el elemento y el índice) y retorna el nuevo valor del elemento.

Por ejemplo:

```
let playlist = ['Creep', 'House of cards', 'Step'];
// return no hace falta porque está implícito
const newPlaylist = playlist.map((cancion, i) => '${i} - ${cancion}')

console.log(newPlaylist);
//  '0 - Creep',
//  '1 - House of cards',
//  '2 - Step' ]
```

Si querés conocer más sobre este método, entrá a la [documentación de Mozilla](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/map).

Veamos otro ejemplo. Si quisiéramos pasar todos los nombres a mayúsculas, podríamos hacerlo de esta manera:

```js
let nombres = ["Ana", "Pedro", "Pablo"];
let mayusculas = [];

for (let i = 0; i < nombres.length; i++) {
 mayusculas.push( nombres[i].toUpperCase() );
}
console.log(mayusculas) // ['ANA', 'PEDRO', 'PABLO']
console.log(nombres) // ['Ana', 'Pedro', 'Pablo']
```

Sin embargo, podríamos utilizar el método `.map()` de esta forma:

```js
let nombres = ["Ana", "Pedro", "Pablo"];

let mayusculas = nombres.map(function (nombre) {
 return nombre.toUpperCase();
});

console.log(mayusculas) // ['ANA', 'PEDRO', 'PABLO']
console.log(nombres) // ['Ana', 'Pedro', 'Pablo']
```

Además, podés combinarlo con `arrow functions`:

```js
let nombres = ["Ada Lovelace", "Hedy Lamarr", "Grace Hopper"];

let mayusculas = nombres.map(nombre => nombre.toUpperCase());

console.log(mayusculas) // ["ADA LOVELACE", "HEDY LAMARR", "GRACE HOPPER"]
console.log(nombres) // ["Ada Lovelace", "Hedy Lamarr", "Grace Hopper"]
```

## Diferencia entre Map y ForEach

Consideremos el siguiente arreglo:

```js
let arr = [1, 2, 3, 4, 5]
```
Queremos obtener el doble de cada valor: para eso vamos a utilizar `map` y `forEach`.

##### forEach:

```js
arr.forEach((num, index) => {
    return arr[index] = num * 2;
})

console.log(arr)
// [2, 4, 6, 8, 10]
```

##### Map:

```js
let doubled = arr.map(num => {
    return num * 2;
})

console.log(doubled)
// [2, 4, 6, 8, 10]
```


**jsPerf** es un sitio _web_ para probar la velocidad de diferentes métodos y funciones de JavaScript.

Al comparar `map` con `forEach`, vemos que  `forEach` es un 18% más lento que `map`:

![jsPerf.png](https://pledu-plataforma5.s3.amazonaws.com/5bc731d2-55f7-4462-b8e1-86e32484242e/pasted%20image%200.png)

Sin embargo, estos valores pueden variar ya que dependen del navegador utilizado. Hacé la [misma prueba](https://web.archive.org/web/20191115093328/https://jsperf.com/map-vs-foreach-speed-test) desde tu navegador.


---

### ***Map*** : Ejercicios

## Ejercicio 1
Tenemos un arreglo de números en la variable `numbers` y deberás crear uno nuevo que contenga el doble de cada número, usando `.map()`.

```js
let numbers = [3, 7, 13, 99];
// CODEA LA SOLUCIÓN 
console.log(numbers); // [3, 7, 13, 99]
console.log(dobles); // [6, 14, 26, 198]
```

## Ejercicio 2
Tenemos un arreglo en la variable `frases` con varias sentencias al azar. Usá la función `map()` para que cada frase empiece y termine con signos de exclamación.

```js
let frases = ['Labore sea dolor.', 'Justo rebum dolor.', 'Stet lorem amet.'];
// CODEA LA SOLUCIÓN
console.log(frases); // ['Labore sea dolor.', 'Justo rebum dolor.', 'Stet lorem amet.']
console.log(frasesExclamadas); // [ '¡Labore sea dolor.!', '¡Justo rebum dolor.!', '¡Stet lorem amet.!' ]
```

<!--## Ejercicio 3
Tenemos un Arreglo de Objetos que representa una lista de _Spotify_. Cada Objeto es una canción que tiene nombre y duración (**en segundos**). Deberás obtener un Arreglo con las duraciones de las canciones **en minutos**.

```js
const playlist = [
 { nombre: 'Everlong', duracion: '120' },
 { nombre: 'The Pretender', duracion: '168' },
 { nombre: 'Learn to Fly', duracion: '204' }
];
// CODEA LA SOLUCIÓN
console.log(duracionesEnMinutos); // [ 2, 2.8, 3.4 ]
```

## Ejercicio 3

Usando el método `.map()`, completá la Función `fizzBuzz`, para que reciba un Arreglo de números y retorne un Arreglo teniendo en cuenta estas condiciones: 

1. Si el número es múltiplo de 3, lo reemplace por la palabra `fizz`.
2. Si el número es múltiplo de 5, lo reemplace por la palabra `buzz`; 
3. Si el número es múltiplo de 3 y de 5, lo reemplace por la palabra `fizzBuzz`. 

⚠️ **Importante:** en cualquier otro caso dejar el número. 

```js
let numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]; 

// CODEA LA SOLUCIÓN

console.log( fizzBuzz(numeros) ); 

// [ 1, 2, 'fizz', 4, 'buzz', 'fizz', 7, 8, 'fizz', 'buzz', 11, 'fizz', 13, 14, 'fizzbuzz', 16, 17, 'fizz', 19, 'buzz' ]
```

-->

---

### ***Reduce***

El método `.reduce()` nos permite recorrer el arreglo y obtener un resultado reducido en base a cada elemento del arreglo.

Para aprender más sobre este método, mirá la [documentación de Mozilla](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/reduce).

Veamos un ejemplo:

```js
let notas = [1, 2, 3, 4, 10, 5];
let sumaDeNotas = notas.reduce((total, nota) => total + nota, 0);
// const sumaDeNotas = notas.reduce(function(total, nota) {
//  return total + nota;
// }, 0);
console.log(sumaDeNotas); // 25
```
Si no hubiéramos usado el método `.reduce()`, el código se vería de esta manera:

```js
let notas = [1, 2, 3, 4, 10, 5];
let sumaDeNotas = 0;
for (let i = 0; i < notas.length; i++) {
 sumaDeNotas += notas[i];
}
console.log(sumaDeNotas); // 25
```
Recapitulando, el método `.reduce()` tiene un segundo parámetro que es el valor inicial del acumulador.

```js
let numeros = [1, 2, 3];
let sumaConInicialCero = numeros.reduce(function(acc, num) { return acc + num; }, 0);
let sumaSinInicial = numeros.reduce(function(acc, num) { return acc + num; });
let sumaConInicialQuince = numeros.reduce(function(acc, num) { return acc + num; }, 15);
console.log(sumaConInicialCero); // 6
console.log(sumaSinInicial); // 6
console.log(sumaConInicialQuince); // 21
```

El método `.reduce()` es muy versátil: se ejecuta sobre un arreglo y puede retornar cualquier otro tipo de dato (ya sea un Arreglo, Objeto, Número, _String_, etc.) 

Veamos un ejemplo:

```js
let numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9];
let pares = numeros.reduce((acc, numero) => {
 if (numero % 2 == 0) {
    acc.push(numero);
 }
 return acc;
}, []);
console.log(pares); // [ 2, 4, 6, 8 ]
```
Por último, también podemos usarlo para concatenar _Strings_.

```js
let palabras = ['¡', 'Hola,', 'mundo', '!'];
// en este ejemplo estamos haciendo una reducción del array a un string
let frase = palabras.reduce((acc, item) => acc + "" + item);
// const frase = palabras.reduce(function(acc, item) {
//   return acc + ' ' + item;
// }, 'Frase:');
console.log(frase); // Frase: ¡ Hola, mundo !
```

---


### ***Reduce*** : Ejercicios

## Ejercicio 1
Teniendo un Arreglo de números al azar (llamado `numbers`), usá `.reduce()` para obtener la multiplicación total de todos los números.

⚠️ **Importante**: Prestá atención al valor inicial del acumulador.

```js
let numbers = [6, 1, 34, 94, 3, 17];
const mul = // CODEA LA SOLUCIÓN
console.log(mul);
// debería mostrar 977976
```

## Ejercicio 2

Teniendo un Arreglo de números en la variable `numeros`, usá `.reduce()` para crear un nuevo Arreglo que contenga solo los números impares.


```js
let numeros = [3, 7, 6, 13, 2, 24, 99];
let impares = // CODEA LA SOLUCIÓN
console.log(impares) // [3, 7, 13, 99]
```

## Ejercicio 3

Teniendo un Arreglo de números (llamado `numbers`), usá `.reduce()` para obtener el máximo valor que posea el Arreglo.

```js
let numbers = [5, 4, 1, 9, 2]
let max = // CODEA LA SOLUCIÓN
console.log(max)
// debería mostrar 9
```

## Ejercicio 4

Completá la Función `join` que reciba un Arreglo de números y retorne un _String_ con todos los números concatenados.

```js
let join = arr => {
 // CODEA LA SOLUCIÓN
}
console.log( join( [1,2,3] ) ) // "123"
```
## Ejercicio 5

Teniendo un Arreglo de números en la variable `numeros`, usá `.reduce()` para crear un Arreglo con los mismos números pero eliminando los repetidos.

+++

👩🏻‍💻👨‍💻 El método `indexOf()` puede ayudarte. Para más información, accedé a la [documentación de Mozilla](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/String/indexOf).

+++

```js
let numeros = [5, 1, 7, 12, 5, 2, 9, 0, 11, 9, 11]
let sinRepetidos = // CODEA LA SOLUCIÓN
console.log(sinRepetidos)
// debería mostrar [ 5, 1, 7, 12, 2, 9, 0, 11 ]
```
## Ejercicio 6

Teniendo un Arreglo llamado `notasDeTPs`(con números del 1 al 10), usá `.reduce()` para calcular la nota promedio final de todos los trabajos prácticos de este curso.

+++

🤓 Recordá que el promedio se calcula sumando todas las notas y dividiéndolo por la cantidad total.

+++

```js
let notasDeTPs = [4, 7, 8, 5, 10]
let notaFinal = // CODEA LA SOLUCIÓN
console.log(notaFinal)
// debería mostrar 6.8
```

---

### ***Reduce*** : Ejercicios

## Ejercicio 1
Teniendo un Arreglo de números al azar (llamado `numbers`), usá `.reduce()` para obtener la multiplicación total de todos los números.

⚠️ **Importante**: Prestá atención al valor inicial del acumulador.

```js
let numbers = [6, 1, 34, 94, 3, 17];
const mul = // CODEA LA SOLUCIÓN
console.log(mul);
// debería mostrar 977976
```

## Ejercicio 2

Teniendo un Arreglo de números en la variable `numeros`, usá `.reduce()` para crear un nuevo Arreglo que contenga solo los números impares.


```js
let numeros = [3, 7, 6, 13, 2, 24, 99];
let impares = // CODEA LA SOLUCIÓN
console.log(impares) // [3, 7, 13, 99]
```

## Ejercicio 3

Teniendo un Arreglo de números (llamado `numbers`), usá `.reduce()` para obtener el máximo valor que posea el Arreglo.

```js
let numbers = [5, 4, 1, 9, 2]
let max = // CODEA LA SOLUCIÓN
console.log(max)
// debería mostrar 9
```

## Ejercicio 4

Completá la Función `join` que reciba un Arreglo de números y retorne un _String_ con todos los números concatenados.

```js
let join = arr => {
 // CODEA LA SOLUCIÓN
}
console.log( join( [1,2,3] ) ) // "123"
```
## Ejercicio 5

Teniendo un Arreglo de números en la variable `numeros`, usá `.reduce()` para crear un Arreglo con los mismos números pero eliminando los repetidos.

+++

👩🏻‍💻👨‍💻 El método `indexOf()` puede ayudarte. Para más información, accedé a la [documentación de Mozilla](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/String/indexOf).

+++

```js
let numeros = [5, 1, 7, 12, 5, 2, 9, 0, 11, 9, 11]
let sinRepetidos = // CODEA LA SOLUCIÓN
console.log(sinRepetidos)
// debería mostrar [ 5, 1, 7, 12, 2, 9, 0, 11 ]
```
## Ejercicio 6

Teniendo un Arreglo llamado `notasDeTPs`(con números del 1 al 10), usá `.reduce()` para calcular la nota promedio final de todos los trabajos prácticos de este curso.

+++

🤓 Recordá que el promedio se calcula sumando todas las notas y dividiéndolo por la cantidad total.

+++

```js
let notasDeTPs = [4, 7, 8, 5, 10]
let notaFinal = // CODEA LA SOLUCIÓN
console.log(notaFinal)
// debería mostrar 6.8
```

---

### ***Filter***

`.filter()` es un método que retorna un nuevo Arreglo, con los datos filtrados según una Función que le pasamos por Parámetro. 

Veamos un ejemplo: supongamos que queremos saber cuántos alumnos aprobaron un examen. Si quisiéramos filtrar solo las notas de aquellos alumnos que sacaron más de un 6, podríamos hacerlo de esta manera:

```js
let notas = [1, 2, 3, 4, 10, 7, 6, 4, 8];
let aprobadas = [];
for (let i = 0; i < notas.length; i++) {
 if (notas[i] >= 6) {
   aprobadas.push(notas[i])
 }
}
console.log(aprobadas); // [10, 7, 6, 8] - hay 4 notas aprobadas
console.log(notas); // [1, 2, 3, 4, 10, 7, 6, 4, 8] - es el arreglo original
```

Sin embargo, con el método `.filter()` podríamos resolverlo de una forma mucho más sencilla:

**Con ***Arrow Functions***:** 

```js
let notas = [1, 2, 3, 4, 10, 7, 6, 4, 8];
let aprobadas = notas.filter(nota => nota >= 6)
```

**Sin ***Arrow Functions***:**

```js
let notas = [1, 2, 3, 4, 10, 7, 6, 4, 8];
let aprobadas = notas.filter(function(nota) {
return nota >= 6; });
console.log(aprobadas); // [10, 7, 6, 8] - hay 4 notas aprobadas
console.log(notas); // [1, 2, 3, 4, 10, 7, 6, 4, 8] - es el arreglo original
```

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

⚠️ **Importante**: Con el método `.filter()` podemos filtrar Arreglos que contengan cualquier tipo de datos.

</div>

Si quisiéramos crear un filtro manipulando datos booleanos (_true_ y _false_), podríamos hacerlo de la siguiente forma.

En este ejemplo, filtramos solo la comida vegetariana:

```js
let comidas = [
 { nombre: '1', vegetariana: false }, { nombre: '2', vegetariana: true },
 { nombre: '3', vegetariana: true }, { nombre: '4', vegetariana: false }
];

let vegetarianas = comidas.filter(comida => comida.vegetariana === true)
//  const vegetarianas = comidas.filter(function (comida) {
//   return comida.vegetariana;
//  });
console.log(vegetarianas);
// [{ nombre: '2', vegetariana: true }, { nombre: '3', vegetariana: true }]
```

---

### ***Filter***: Ejercicios

## Ejercicio 1
Usando `.filter()`, completá la Función `mayoresOIgualesA5` para que reciba números y retorne un nuevo Arreglo solo con números que sean mayores o iguales a 5.

```js
let mayoresOIgualesA5 = arr => {
 // Codeá la solución
}
console.log(mayoresOIgualesA5([3, 6, 8, 21])); // [6, 8, 21]
```

## Ejercicio 2
Tenemos un Arreglo de números en la Variable `numbers`. Usando `.filter()`, creá un nuevo Arreglo que contenga solo los números pares.

```js
let numeros = [3, 7, 6, 13, 2, 24, 99];
// Codeá la solución
console.log(pares); // [6, 2, 24]
```
## Ejercicio 3
Tenemos un Arreglo de palabras al azar en la Variable `palabras`. Usando `.filter()`, deberás separar en un nuevo Arreglo aquellas palabras que no tengan más de 3 letras.

```js
let palabras = ['Et', 'Voluptua', 'Sed', 'At', 'Diam', 'Lorem']
const palabrasCortas = // Codeá la solución
console.log(palabrasCortas);
// [ 'Et', 'Sed', 'At' ]
```

## Ejercicio 4
Tenemos un Arreglo de Objetos, donde cada uno representa a una persona. Usando `.filter()`, creá un nuevo Arreglo con las personas que tengan más de 27 años.

```js
let personas = [ { nombre: 'Ana', edad: '28'},
{ nombre: 'María', edad: '24' }, { nombre: 'José', edad: '31' }
];
let personasConMasDe27 = // Codeá la solución
console.log(personasConMasDe27);
// [{ nombre: 'Ana', edad: '28' }, { nombre: 'José', edad: '31' }]
```
## Ejercicio 5
Tenemos un Arreglo en una Variable `mix` con varios elementos, de distintos tipos de datos. Usando `.filter()`, creá un nuevo Arreglo con todos los elementos que sean _Strings_ y guardalo en la Variable `soloStrings`. 

+++

🤓 Para saber si algo es un _String_ en JavaScript, usá `typeof`.

+++

```js
const mix = [
 'Ut vero.',
 2,
 function () { console.log('hola mundo!') },
 56,
 'Diam rebum nonumy et.',
 true,
 false,
 'Kasd stet.',
 'Sit et dolor.',
 null,
 null,
 [ 1, 2, 3],
 'Dolore.'
];
// Codeá la solución
console.log(soloStrings);
// Debería mostrar
// [ 'Ut vero.', 'Diam rebum nonumy et.', 'Kasd stet.', 'Sit et dolor.', 'Dolore.' ]
```
## Ejercicio 6
Tenemos un Arreglo `playlist` con canciones seleccionadas al azar por _Spotify_ para reproducir. 
Tenemos otro Arreglo `playlistEscuchada` que tiene canciones que ya escuchamos. 
Usando `.filter()`, creá una nueva lista con las canciones guardadas en `playlist` que no estén en `playlistEscuchada`. 
Guardá el resultado en la Variable `playlistSinEscuchar`.

```js
let playlist = ['Smells Like Teen Spirit', 'Everlong', 'Come As You Are', 'The Pretender', 'Heart-Shaped Box', 'Learn to Fly', 'Lithium']
let playlistEscuchada = ['The Pretender', 'Lithium', 'Come As You Are']
let playlistSinEscuchar = /// Codeá la solución
console.log(playlistSinEscuchar);
// Debería mostrar
// [ 'Smells Like Teen Spirit', 'Everlong', 'Heart-Shaped Box', 'Learn to Fly' ]
```

---

# Ejercicios de practica

### ¿Qué Devuelve Este Código? 

<div class="editor-recuadro">

🛎 **Recordá**: En la **Comunidad de P5 de Discord** podrás ver cómo otras personas tuvieron las mismas dudas y cuáles fueron las distintas formas en que las resolvieron. ¡Aprovechá los canales para revisar y consultar!

</div>


1. En este ejercicio deberás descubrir qué devuelve este código sin probarlo en la consola: 

```js
let numbers = [0,1,2,3,4,5,6,7,8,9,10]
let colores=["Rojo", "Azul", "Verde", "Amarillo"]
numbers.forEach(function(color){
  if(color % 3 === 0){
    console.log(color)
  }
})
```

---

### Lista de Súper - Parte III

Volvé al ejercicio anterior y seguí estos pasos:

1. Usá un `for Loop` y mostrá cada ítem de `listaDeSuper` en la consola.
2. Refactoreá tu código de manera tal que el `for loop` viva dentro de una Función que se llame `logItems`. La Función deberá tomar un Arreglo como Parámetro e imprimir sus elementos en la consola.


+++ **Cómo Se Usa El Método `forEach()`**
 
 Este método es muy útil para esta consigna. Para saber cómo funciona podés hacer _click_ [acá](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach.).
 
+++


3. Invocá `logItems` 2 veces, pasando `listaDeSuper` la primera vez y otro Arreglo la segunda vez (deberás crear uno nuevo).
4. Refactoreá el código de `logItems` para que use `.forEach()` en vez de un `for loop`.

---

### ***Reverse***

En este ejercicio deberás crear una Función que imprima por consola un Arreglo con sus elementos invertidos, sin modificarlo. Luego, deberás hacer una Función que lo modifique e invierta el orden de sus elementos.

+++ 🤓 ¿Cómo Abordar Este Ejercicio?

Te damos algunas pistas para que pienses este ejercicio.

1. Creá la Función `printReverse` que tome un Arreglo como Argumento y que imprima en la consola cada elemento en orden inverso (no tenés que invertir el Arreglo).
2. Creá la Función `reverser` que tome un Arreglo como Argumento y devuelva uno nuevo invertido.

Usá este código para testear tus Funciones:

```js
printReverse(["a", "b", "c"])
// c
// b
// a
printReverse([1, 2, 3, 4])
// 4
// 3
// 2
// 1
reverser(["a", "b", "c"]) // ["c","b", "a"]
reverser([1, 2, 3, 4]) // [4, 3, 2, 1]
```
3. Cuando lo resuelvas, podés volver a realizarlo sin el método `reverse`. Esto te ayudará a mejorar tu lógica de programación.

+++

---

### Poema Desordenado

En este ejercicio deberás **ordenar el poema del Martín Fierro**. 
En una parte dice: 

_"Los hermanos sean unidos porque ésa es la ley primera, tengan unión verdadera, en cualquier tiempo que sea, porque si entre ellos se pelean los devoran los de ajuera"_

⚠️ **Importante:** Si no conocés a este personaje de la literatura argentina, entrá en este [_link_](https://es.wikipedia.org/wiki/El_Gaucho_Mart%C3%ADn_Fierro).



👩🏻‍💻👨‍💻Usá todo lo visto hasta este momento para ordenar correctamente este fragmento:

```js
let poemaDesordenado = "los sean porque es ley tengan verdadera cualquier que porque entre pelean devoran de ajuera los los ellos si sea tiempo en unión primera la ésa unidos hermanos"
```

+++

1. Usá `.split(' ')` en `poemaDesordenado` y guardalo en un Arreglo llamado `arregloDesordenado`.
2. Instanciá un nuevo Arreglo llamado `arregloOrdenado`.
3. Mientras que el largo de `arregloDesordenado` sea mayor que 0, sacá el primer y el último elemento y guardalo en `arregloOrdenado`. 

👩‍🏫 ¿Cómo sería la condición si usaras un `for loop` o un `while loop`?
  
4. Creá la Variable `poemaOrdenado` y dale el valor de un _String_ usando `arregloOrdenado` y el método `.join(' ')`.

+++

|||**Video**

@youtube=Y9zkFT01iWY
  
|||

---

### Desafío `isUniform()`


<div class="editor-recuadro">

🏆 Se trata del **DESAFÍO** de la clase 11 que te proponemos que lo compartas en Discord cuando termines.
</div>

En este ejercicio deberás crear la Función `isUniform` que tome un Arreglo como Parámetro y devuelva `true` si todos los elementos del Arreglo son idénticos. De lo contrario, deberá devolver `false`. 

⚠️ **Importante:** Salvo que sea necesario, tu Función no debe recorrer todo el Arreglo si no es idéntico. Es decir, al momento que encuentre una diferencia deberá cortar.

Usá este código para testear tu solución:

```js
isUniform([1, 1, 1, 1]) // true
isUniform([1, 2, 1, 1]) // false
isUniform(["a", "b", "p"]) // false
isUniform (["b", "b", "b"]) // true

---

### ***Biggest Smallest***

En este ejercicio deberás:

1- Escribir una Función llamada `biggest_smallest` que tenga un Argumento (que haga referencia a un Arreglo de números). 

2- Utilizar el método `forEach()` para encontar el número más grande y el número más chico. 

3- La función debe devolver por consola un Arreglo que contenga los números mínimo y máximo.


💡 **Ejemplo**:
 
```js
[111, 27, 31, 44, 101, 213, 33, 58]
// Salida: 27, 213
```
 
---

### Ejercicios: ***Filter***

## Ejercicio 1
Usando `.filter()`, completá la Función `mayoresOIgualesA5` para que reciba un Arreglo de números y retorne un nuevo Arreglo (solo con números que sean mayores o iguales a 5).

```js
let mayoresOIgualesA5 = arr => {
 // Codeá la solución
}
console.log(mayoresOIgualesA5([3, 6, 8, 21])); // [6, 8, 21]
```

## Ejercicio 2
Tenemos un Arreglo de números en la Variable `numbers`. Usando `.filter()`, creá un nuevo Arreglo que contenga solo los números pares.

```js
let numeros = [3, 7, 6, 13, 2, 24, 99];
// Codeá la solución
console.log(pares); // [6, 2, 24]
```
## Ejercicio 3
Tenemos un Arreglo de palabras al azar en la Variable `palabras`. Usando `.filter()`, deberás separar en un nuevo Arreglo aquellas palabras que no tengan más de 3 letras.

```js
let palabras = ['Et', 'Voluptua', 'Sed', 'At', 'Diam', 'Lorem']
const palabrasCortas = // Codeá la solución
console.log(palabrasCortas);
// [ 'Et', 'Sed', 'At' ]
```

## Ejercicio 4
Tenemos un Arreglo en una Variable `mix` con varios elementos, de distintos tipos de datos. Usando `.filter()`, creá un nuevo Arreglo con todos los elementos que sean _Strings_ y guardalo en la Variable `soloStrings`. 

+++

🤓 Para saber si algo es un _String_ en JavaScript, usá `typeof`.

+++

```js
const mix = [
 'Ut vero.',
 2,
 function () { console.log('hola mundo!') },
 56,
 'Diam rebum nonumy et.',
 true,
 false,
 'Kasd stet.',
 'Sit et dolor.',
 null,
 null,
 [ 1, 2, 3],
 'Dolore.'
];
// Codeá la solución
console.log(soloStrings);
// Debería mostrar
// [ 'Ut vero.', 'Diam rebum nonumy et.', 'Kasd stet.', 'Sit et dolor.', 'Dolore.' ]
```

---

### ***Playlist***
Tenemos un Arreglo `playlist` con canciones seleccionadas al azar por _Spotify_ para reproducir. 
Tenemos otro Arreglo `playlistEscuchada` que tiene canciones que ya escuchamos. 

Usando `.filter()`, creá una nueva lista con las canciones guardadas en `playlist` que no estén en `playlistEscuchada`. 
Guardá el resultado en la Variable `playlistSinEscuchar`.

```js
let playlist = ['Smells Like Teen Spirit', 'Everlong', 'Come As You Are', 'The Pretender', 'Heart-Shaped Box', 'Learn to Fly', 'Lithium']
let playlistEscuchada = ['The Pretender', 'Lithium', 'Come As You Are']
let playlistSinEscuchar = /// Codeá la solución
console.log(playlistSinEscuchar);
// Debería mostrar
// [ 'Smells Like Teen Spirit', 'Everlong', 'Heart-Shaped Box', 'Learn to Fly' ]
```

|||
 
No te preocupes, la numeración cambió pero el ejercicio es el mismo.

@youtube=/knyIz4VSb_w

|||

---

### Fibonacci

## 🤓 ¿Qué Es La Serie Fibonacci?

La sucesión de Fibonacci comienza con los números 0 y 1. A partir de estos, «cada término es la suma de los dos anteriores». Por ejemplo, los primeros diez números de la serie son:

```js
0,1,1,2,3,5,8,13,21,34
0 + 1 = 1
1 + 2 = 3
3 + 5 = 8
// ¡Y así, sucesivamente, la serie seguirá realizando 
// la suma de los últimos dos números! 
```



⚠️ **Importante:** La relación de recurrencia define a la serie de Fibonacci.


## 👉 Ejercicio
 En este ejercicio deberás escribir una Función que acepte un número X (que indica la posición) y que devuelva otro número (el que se encuentra en esa posición) en la serie de Fibonacci. En otras palabras, imprimirá el número que está en la posición contando X cantidad de lugares. 

Serie: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55…

- Fibonacci (2): 1
- Fibonacci (5): 3
- Fibonacci (8): 13


|||Con Funciones
 
```js
function fibonacci(N) {
    let i = N
    let resultado = 0
    let siguiente = 1
    while (i > 1) {
        siguiente = siguiente + resultado;
        resultado = siguiente - resultado;
        i--
    }
    return resultado
}
```
|||


|||Con Arreglos

Si hubiera que imprimir toda la lista:
  

![alt](https://i.imgur.com/PurJU5F.png)

|||


---

### ***To Do List***

En este ejercicio harás un programa que organice en un Arreglo las tareas del usuario. 

Para eso, deberás crear un `prompt` que le pregunte al usuario qué quiere hacer. Si el usuario pone:
- "nuevo": Le permitirá agregar una tarea nueva.
- "listar": Mostrará sus tareas en la consola. 
- "borrar": Eliminará la tarea que quiera.
- "salir": Cerrará el programa.

#### Paso A Paso

1. En un nuevo documento, en el _tag_ `<script>` iniciá un nuevo Arreglo `tareas`.
2. Preguntale al usuario qué quiere hacer y guardalo en la Variable `input`. Según lo que el usuario responda, deberás generar las distintas acciones.
3. Si el usuario ingresa "listar", mostrale el Arreglo de tareas en la consola.
4. Si responde "nuevo", generá otro `prompt`, que le pregunte qué tarea quiere agregar a la lista. Su respuesta se agregará al Arreglo `tareas`.
5. Si pone "salir", deberá aparecer un mensaje en la consola que avise que el programa se cerró.

⚠️ **Importante:** Creá un _While Loop_ en el que, mientras `input` sea diferente a "salir", siga preguntando al usuario qué quiere hacer.

6. Usá un `forEach` o un _For Loop_ para refactorizar tu comando "listar". De esta manera, no deberá mostrar el Arreglo entero en pantalla, sino que iterará sobre cada tarea y lo imprimirá con el número de índice por delante. 

🤓 **Tip:** Podés poner unos asteriscos (`*`) arriba y abajo de la lista para darle más estilo. 

  Cómo se verá en la consola:

```js
**********
0: Ir al super
1: Hacer la cama
2: Darle de comer al perro
**********
```


---

+++ ¿Cómo Agrego Un Índice?

Para tomar el Índice, podés utilizar el método `indexOf()` o agregar un segundo Argumento al `forEach` que tenga el valor del Índice.

+++

7. Agregá un comando "borrar". De esta manera, si le pasás un número, eliminará el elemento del Arreglo que esté en esa posición. Para hacerlo, usá el método `.splice()`. Una vez removido el elemento, lo mostrará en la consola con un mensaje apropiado (por ejemplo, "El elemento ha sido eliminado.").

#### Extra Credit

Si tenés tiempo, refactorizá tu código para que sea más elegante y DRY. Si bien no cambiará la funcionalidad de tu programa, el código estará más ordenado y será más fácil de leer. 

🤓 **Tip:** Escribí la acción de cada comando en una Función aparte y solo ejecutá esa Función. Por ejemplo:

```js
if(input === "list"){
  listTareas()
}
```

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

👩‍🏫👨‍🏫 Incorporá la refactorización como una buena práctica a la hora de _codear_. No solo hará que tu código sea más prolijo sino que se verá más profesional.

</div>

---


### `sumArray()`

En este ejercicio, deberás crear una Función `sumArray` que acepte un Arreglo de números y devuelva la suma de todos ellos. Usá este código para testear tu Función:

```js
sumArray([1,2,3]) // 6
sumArray([10, 3, 10, 4]) // 27
sumArray([-5,100]) // 95
```



|||
 
Este ejercicio tiene la [solución](https://github.com/aylu2910/pledu_ejercicios/blob/main/arreglos/sumArray.js) en el Repo Intro de GitHub.

🛎️ **Recordá**: GitHub es un sitio _social coding_. Permite subir repositorios de código para almacenarlo en el sistema de control de versiones Git.

En el _Bootcamp Prep_ te explicaremos más cuestiones sobre esta herramienta 🚀.
  
|||

---

### 🚀 Simulación del `Array.join()`

En este ejercicio deberás crear una Función llamada `join` que reciba un Arreglo y simule el comportamiento del método `Array.join()`.

⚠️**Importante**: No podés usar el método `Array.join()` original.

Por ejemplo:

`join(["h","o","l","a"])` debe retornar el _string_ **"hola"**.

`join(["c","h","a","u"])` debe retornar el _string_ **"chau"**.



|||
 
Este ejercicio tiene la [solución](https://github.com/aylu2910/pledu_ejercicios/blob/main/arreglos/join.js) en el Repo Intro de GitHub.

🛎️ **Recordá**: GitHub es un sitio _social coding_. Permite subir repositorios de código para almacenarlo en el sistema de control de versiones Git.

  
|||





 
