# Introduccion a los objetos en JavaScript

### Objetivos

En este módulo aprenderás:
- Qué son los Objetos y para qué se usan.
- Cómo acceder a los valores de un Objeto a través de:
	- _Dot notation_.
	- _Bracket notation_.
- Cómo modificar Objetos y agregar Propiedades nuevas.
- Cómo anidar Objetos dentro de Arreglos.
- Cómo iterar sobre un Objeto.
- _Loop_ `for...in`.
### Objetos

En JavaScript, un **Objeto** es una entidad independiente con Propiedades. A su vez, esas Propiedades tienen valores.

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">🤓 Los Objetos son tan importantes en programación que surgió una rama entera dedicada a ellos: la <strong>Programación Orientada a Objetos</strong> (POO; en inglés <em>Object-Oriented Programming</em>). Volveremos a este tema en el próximo módulo.<br></p>

El concepto de Objetos puede compararse con entidades de la vida real. Por ejemplo, una persona representaría un Objeto con ciertas Propiedades: su color de pelo, cierta edad, la ciudad en la que vive, etc. Del mismo modo, los Objetos en JavaScript pueden tener Propiedades que definan sus características.

Imaginemos entonces que queremos crear el modelo de una persona en JavaScript. 

🎥 Mirá este video para aprender cómo hacerlo a través de un Objeto:

<iframe width="600" height="355" src="https://www.youtube.com/embed/9E_CtsccKzs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427603491-->


#### Sintaxis De Los Objetos

```js
let objeto = {
  clave1: "Valor1", // Las propiedades se escriben en formato key-value pair (en castellano, par clave-valor) y se separan con comas. El valor de cada clave puede ser cualquier tipo de dato, inclusive otros Objetos, Arreglos o Funciones.
  clave2: "Valor2"
}
```

Veamos la sintaxis con mayor profundidad:

- Para declarar un Objeto, utilizamos llaves: `{ }`.

🛎 **Recordá**: En los Arreglos usamos corchetes `[ ]`.

- Los Objetos tienen Propiedades que se escriben en formato _key-value pairs_. Es decir, cada ítem viene de a pares. Por ejemplo, dentro de la clave (en inglés, _key_) `nombre` está el valor "Guillermo"; dentro de la clave `edad` está el valor "22", etc.

Si querés profundizar tu conocimiento de Objetos, hacé _click_ en este [_link_](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Trabajando_con_objectos).

⚠️ **Importante**: Cada _key-value pair_ va separada por comas.

Por ejemplo, si quisiéramos modelar en JavaScript el nombre, el apellido y la ocupación de Mario, podríamos expresarlo así:

```js
let persona = {
nombre: "Mario",
apellido: "Mario",
trabajo: "Plomero",
}
```

🤓 ¿Sabías que…

… Aunque Nintendo inicialmente no le dio un apellido, Shigeru Miyamoto, el creador de Mario, reveló en una [entrevista](https://as.com/meristation/2012/09/25/noticias/1348566720_108304.html) que el apellido de Mario y Luigi sería “Mario”.

![mario.gif](https://media.giphy.com/media/l1KtXmfi3EnjM5zpK/giphy.gif)

#### Propiedades De Los Objetos

Las Propiedades de los Objetos suelen ser flexibles; por ejemplo, los valores incluyen números, palabras, otros Objetos, cadenas de caracteres e, incluso, Funciones.

⚠️ **Importante**: En caso de querer agregar números o dos (o más) palabras, deberás agregar un _String_.

Mirá este video para aprender más sobre las propiedades de los Objetos:

<iframe width="600" height="355" src="https://www.youtube.com/embed/xL7qCSzSpU4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427605048-->

---

### Comparación Entre Arreglos Y Objetos

Siguiendo el ejemplo anterior, imaginemos que queremos crear el modelo de una persona en JavaScript. Podríamos hacerlo de dos maneras distintas:
1. Con Arreglos (como vimos en el módulo anterior).
2. Con Objetos.

Modelar con Objetos resulta más fácil y eficiente. Mirá este video para aprender por qué:

<iframe width="600" height="355" src="https://www.youtube.com/embed/psLKLDBDRgQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!----
<iframe src="https://player.vimeo.com/video/427606402" width="640" height="364" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
!---->

Recapitulando, si quiero modelar ciertas Propiedades de una entidad (como nombre, edad, ciudad, etc.) con un Arreglo, podría expresarlo de la siguiente forma:

```js
let persona1 =["Violeta", 21, "Buenos Aires", function() { console.log("Hola")}]
```

Sin embargo, esto resultaría confuso porque el Arreglo solo contiene **valores**. Es decir, el valor `"Violeta"` podría referirse tanto a un nombre propio como a un color o a una flor.

En cambio, modelar con Objetos permite crear campos fácilmente identificables y evitar este problema:
  
```js
let persona ={
  nombre: "Violeta",
  edad: 21,
  ciudadNatal: "Buenos Aires",
  saludar: function(){
    console.log("Hola")
  }
}
```

⚠️ **Importante**: Si el nombre de la propiedad tiene espacios, deberás escribirlo entre comillas.

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">🛎 <strong>Recordá</strong>: El <em>key-value pair</em> admite cualquier tipo de datos, siempre que respetes la sintaxis de cada uno. Por ejemplo, si es un <em>String</em> acordate de escribirlo entre comillas.<br></p>

---

# Acceso A Los Valores De Un Objeto

### ***Bracket Notation***

Hay dos maneras de acceder a los valores de un Objeto en JavaScript:
- _Bracket notation_ (del inglés Notación por corchetes)
- _Dot notation_ (del inglés Notación por punto)

Mirá este video para aprender cómo acceder a través de la _Bracket notation_.

<iframe width="600" height="355" src="https://www.youtube.com/embed/z0fYiniwXRo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427609737-->

Recapitulando, los valores guardados en los Objetos no tienen un orden (a diferencia de los Arreglos). Por lo tanto, no podemos acceder a ellos a través de un índice númerico.

Veamos un ejemplo. Supongamos que tenemos un Objeto que representa un auto (marca Tesla, nuevo, modelo "Model Y", etc.).

```js
let auto = {
marca: "Tesla",
modelo: "Model Y",
kilometros: 0,
nuevo: true,
arrancar: function() {
        alert("el auto se enciende!")
  }
}
```

#### Cómo Acceder A Los Valores De Un Objeto

1. Escribí el nombre de la Variable.

2. Escribí – en formato _String_ – el nombre de la propiedad a la cual queremos acceder entre corchetes.

Por ejemplo, si quisiéramos conocer el valor de la propiedad "marca":

```js
auto[“marca”]
“Tesla”
```

A su vez, si quisiéramos acceder al valor de "arrancar" (una Función):
```js
auto["arrancar"]
ƒ () { // Esto nos indica que el valor de "arrancar" es una Función.
        alert("el auto se enciende!") // Esto nos indica que el contenido de la Función es una alerta.
    }
``` 

⚠️ **Importante**: Si la propiedad es una Función y querés activarla, agregá paréntesis después de cerrar los corchetes.

```js
auto["arrancar"]()
```

Probalo en tu consola y fijate qué sucede.

|||

![solucion-funcion-activada.png](https://i.imgur.com/WsKuYrf.png)

|||


### ***Dot Notation***

Otra manera de acceder a los valores de un Objeto es usando _Dot notation_ (Notación por punto).

Mirá este video para aprender cómo acceder utilizando _Dot notation_.

<iframe width="600" height="355" src="https://www.youtube.com/embed/S5NaJ2IgPv4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427960503-->

Recapitulando, _Dot notation_ es una manera más fluida para acceder a los Objetos y da como resultado un código más simple de leer.

#### Cómo Acceder A Los Valores De Un Objeto

Siguiendo con el ejemplo anterior (del Objeto `auto`), seguí estos pasos:

1. Escribí el nombre del Objeto.
2. Poné un punto.
3. Escribí el nombre de la propiedad a la cual querés acceder.

+++ Código Del Objeto `auto`
```js
let auto = {
marca: "Tesla",
modelo: "Model Y",
kilometros: 0,
nuevo: true,
arrancar: function() {
        alert("el auto se enciende!")
    }
}
```
+++

Si quisiéramos conocer el valor de la propiedad `nuevo`:
```js
auto.nuevo
true
```

---

### Ventajas Y Limitaciones

Si bien _Dot notation_ es más cómodo y rápido de escribir, es un poco más limitado porque:

**1. No acepta Variables.**

Por ejemplo, si escribiéramos `auto.propiedad`, va a buscar el texto `propiedad` de forma literal.

Cuando utilicemos _loops_ con Variables que cambien de valor, se va a notar más este problema.

**2. No nos permite acceder a Propiedades que tengan números al principio o espacios.**

Veamos dos ejemplos:

```js
let auto = {
marca: "Tesla",
"1er service": "10000 km",
"pais de origen": "Estados Unidos"
}
```

⚠️ **Importante**: En estos casos, JavaScript no reconocerá `1er service` y `pais de origen`, ya que en el primer caso la Propiedad tiene un número al principio y en el segundo caso contiene espacios.

Por convención en JavaScript debemos escribir los nombres de Variables y las Propiedades de Objetos con notación 🐪 _camelCase_.

+++ ¿Por Qué Usar _camelCase_?

Aunque podemos escribir la clave entre comillas dobles (o simples), en JavaScript recomendamos utilizar la notación 🐪 _camelCase_. Es una manera de evitar errores innecesarios y además alinear a toda la comunidad de programadores.

+++

```js
let auto = {
marca: "Tesla",
primerService: "10000 km", // Recordá que la clave no puede empezar con un número. 
// Te sugerimos escribirlo con letras.
paisDeOrigen: "Estados Unidos"
}
```

En cambio, si utilizáramos _Bracket notation_, podríamos acceder al valor de las Propiedades de la siguiente forma:

```js
auto["primerService"]
"10000 km"
```
```js
auto["paisDeOrigen"]
"Estados Unidos"
```

Por último, además de acceder a las Propiedades con _Strings_ explícitos, con _Bracket notation_ podemos acceder si el _String_ está dentro de otra Variable.

Por ejemplo:

```js
let propiedades = ["marca", "primerService"];

propiedades.forEach(propiedad => {
    console.log(auto[propiedad]);
})
```

```js
let propiedad = "marca"
auto[propiedad]
```

Sería lo mismo escribir:
```js
auto[propiedad]
```
O:

```js
auto["marca"]
```

---

### Ejercicio: Mi Primer Objeto

En este ejercicio deberás crear un Objeto y acceder a los valores utilizando los métodos aprendidos hasta ahora.

#### Parte 1: Crear Mi Objeto

👩🏻‍💻👨‍💻 Esta parte del ejercicio la podés escribir tanto desde tu consola como tu editor de texto.

Creá un Objeto `nave` con las siguientes Propiedades y Valores:

+ Tipo de nave: Un _String_ que diga "Espacial".
+ País: Un _String_ que indique de qué país es la nave.
+ Cantidad de tripulantes: Un número que indique la cantidad de tripulantes de la nave.
+ Tripulantes: Un Arreglo con los nombres de los tripulantes.
+ Estado: Un _String_ que diga "Usada".
+ Despegar:
  
  a) Una Función que imprima en la consola el siguiente mensaje:

"🚀 ¡Todo listo para el despegue! 👍

Oh no ... 😱 ¡algo se rompió!"

<blockquote>b) Y tire un <em>Alert</em> que diga:</blockquote>
🔥 ¡BOOOOOOM! 🔥

---

_Nota: El desperfecto fue rápidamente reparado y la tripulación está sana y salva._ 🌈 💫

---

+++

🛎 **Recordá**: JavaScript es _case sensitive_. Para evitar errores innecesarios, si el nombre de la propiedad tiene espacios, deberás escribirlo con notación 🐪 _camelCase_. Por ejemplo, "cantidadDeTripulantes" en vez de "Cantidad de tripulantes".

+++

#### Parte 2: Acceso A Los Valores

Ahora desde la consola seguí este paso a paso para extraer los valores del Objeto `nave`:

1. Extraé el país de la nave usando _Dot notation_.
2. Extraé el tipo de nave usando _Bracket notation_.
3. Extraé la cantidad de tripulantes usando _Dot notation_... ¿se puede?

+++

👩🏻‍💻👨‍💻 Repasá las diferencias entre _Bracket_ y _Dot notation_ en la sección anterior.

+++
4. Extraé la cantidad de tripulantes usando _Bracket notation_ y guardá ese valor en una Variable que se llame `cantTrip`.
5. Creá una Variable que se llame `test` y guardá adentro un _String_ que diga "Estado".
6. Usá la Variable `test` para extraer el valor dentro de la Propiedad "Estado". Probá usando _Dot notation_ y _Bracket notation_. ¿Cuál funciona?
7. Ejecutá la Función dentro de la Propiedad "Despegar".

+++

🛎 **Recordá**: Si la Propiedad es una Función y querés activarla, deberás agregar paréntesis () después de cerrar los corchetes.

+++

---

### Ejercicio: Acceso A Los Valores De Un Objeto

En el siguiente video te planteamos dos ejercicios para poner a prueba lo aprendido en esta unidad.

👩‍🏫👨‍🏫 _Te recomendamos pausar el video para pensar una posible solución antes de avanzar con el siguiente ejercicio._

<iframe width="600" height="355" src="https://www.youtube.com/embed/uaCKt-RBl90" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--<iframe src="https://player.vimeo.com/video/427975208" width="640" height="564" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>-->

#### Ejercicio 1

Tenemos un Objeto `demo` con tres Propiedades (`uno`, `dos` y `tres`) y luego una Variable que se llama `uno` y contiene el Valor `tres`:

```js
let objeto_demo = {
    uno: 1,
    dos: 2,
    tres: 3
}
let uno = "tres"
```

¿Qué debería devolver el siguiente código?

```js
objeto_demo['dos']
```

|||

Usando _Bracket notation_ podemos acceder a la Propiedad `dos`, y por lo tanto nos devuelve el número "2".

|||

¿Y este código?

```js
objeto_demo[uno]
```

|||

`uno` es una Variable que contiene un _String_ ("tres"). Entonces va a la Propiedad `tres` dentro del Objeto `demo` y devuelve el Valor correspondiente: el número 3.

🛎 **Recordá**: Las Variables se escriben sin comillas. Mirá la diferencia entre buscar un Valor usando comillas:

```js
let objeto_demo = {
    uno: 1,
    dos: 2,
    tres: 3
}
let uno = "tres"

objeto_demo[uno] // Busca la Variable uno
3
objeto_demo["uno"] // Busca la Propiedad uno dentro del Objeto
1
```
|||

#### Ejercicio 2

Tenemos un Objeto `capitales` con dos Propiedades (`Argentina` y `Uruguay`) y luego una Variable que se llama `lugar` y contiene el Valor `Uruguay`:

```js
let capitales = {
    Argentina: 'Buenos Aires',
    Uruguay: 'Montevideo'
}

let lugar = 'Uruguay'
```

¿Qué debería devolver cada una de estas sentencias?

```js
capitales['lugar']
```

|||

`undefined` porque estamos usando _Bracket notation_. El Objeto `capitales` no tiene ninguna Propiedad que se llame `lugar`.

🛎 **Recordá**: Para escribir un _String_, podés usar tanto la comilla simple ('') como la doble ("").

|||

```js
capitales.lugar
```

|||

`undefined` porque _Dot notation_ busca una Propiedad que se llame `lugar`, pero no hay ninguna en ese Objeto.

|||

```js
capitales[lugar]
```

|||

El Valor es "Montevideo" porque _Bracket notation_ busca la Variable `lugar`, que a su vez tiene guardado el _String_ `Uruguay`.

|||

```js
capitales['Argentina']
```

|||

Es "Buenos Aires" porque es el Valor de la Propiedad `Argentina`, guardada dentro del Objeto `capitales`.

|||

```js
capitales.Argentina
```

|||

Al igual que en el caso anterior, es "Buenos Aires" porque es el Valor de la Propiedad `Argentina`, guardada dentro del Objeto `capitales`.

|||

```js
capitales[Argentina]
```

|||

Tira error porque pusimos Argentina sin comillas. Puesto así es una Variable, no un _String_. Como no lo encuentra, nos indica que no existe ninguna Variable llamada así.

|||

![gif-girl.png](https://media.giphy.com/media/bQEVifmPjIBkA/giphy.gif)

---

# Modificar Y Agregar Valores

### Modificar Objetos

Podemos modificar las Propiedades de un Objeto. Mirá este video para aprender cómo:

<iframe width="600" height="355" src="https://www.youtube.com/embed/bFGXVKUxLGA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427963570-->

Recapitulando, las Propiedades de un Objeto se pueden modificar fácilmente. Para hacerlo, debemos acceder a esa Propiedad y asignarle un nuevo valor. Podemos utilizar tanto _Bracket_ como _Dot notation_.

Por ejemplo, supongamos que tenemos el siguiente Objeto:

```js
let heroe = {
  nombre: "Mario",
  trabajo: "Plomero",
}
```

Si quisiéramos modificar el nombre (y reemplazar "Mario" por "Luigi"), podríamos hacer lo siguiente:

***Dot notation***

```js
heroe.nombre = "Luigi"
```

***Bracket notation***

```js
heroe['nombre'] = 'Luigi'
```

![mario-luigi.png](https://i.imgur.com/hIkAFwh.gif)

---

### Agregando Propiedades A Un Objeto

Además de modificar Propiedades existentes, podemos agregar Propiedades nuevas a un Objeto. Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/h7o_2hCNie8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427965089-->

Por ejemplo, si quisiéramos agregar la nacionalidad del Objeto `heroe`, podríamos hacerlo utilizando _Bracket_ o _Dot notation_.

Hasta ahora, la Propiedad `nacionalidad` no existe (y devolvería `undefined`). Entonces, podríamos declararla de las siguientes formas:

***Dot notation***

```js
heroe.nacionalidad = "italiano"
```

***Bracket notation***

```js
heroe['nacionalidad'] = 'italiano'
```

+++ Una Propiedad, ¿Puede Tener Más De Un Valor Al Mismo Tiempo?

👩🏻‍💻👨‍💻 No. En todo caso, deberíamos poner un Objeto dentro de la Propiedad y agregarle a ese Objeto las Propiedades con los valores que se quieran.

+++


#### Modificar Objetos Vacíos

Hasta ahora vimos que podemos crear Objetos escribiéndolos directamente. También podemos inicializar un Objeto vacío y agregar nuevas Propiedades. Para eso, hay que:
1. Crear una Variable (por ejemplo, `let perro`).
2. Crear el Objeto vacío (a través de las llaves "{}") y asignarlo a la Variable recién creada.
3. Agregar nuevas Propiedades.

Por ejemplo:

```js
let perro = {}
perro.nombre = "Firulais"
perro["edad"] = 3
perro["ladrar"] = function() {alert("GUAU!")}
perro.ladrar() // GUAU!
perro["juguetes"] = ["hueso", "pelota", "peluche"]
```

---

# Objetos Dentro De Arreglos

### Objetos Dentro De Arreglos

Dentro de un Objeto, podemos anidar un Arreglo que a su vez contenga otros Objetos. Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/LmQ7fPyvHqw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427962521-->

Podemos acceder a los Objetos dentro de Arreglos a través de _Bracket_ o _Dot notation_.

Retomando el ejemplo del Tesla, supongamos que el Objeto `auto` tuviera un Arreglo llamado `partes`:

```js
let auto = {
marca: "Tesla",
modelo: "Model Y",
kilometros: 0,
nuevo: true,
arrancar: function() {
        alert("el auto se enciende!")
    },
partes: [{ nombre: "bateria", estado: "nuevo"}, {nombre: "motor", estado: "nuevo"}]
}
```

Usando _Dot notation_ nos devuelve el Arreglo `partes` (que contiene los dos Objetos):

```js
auto.partes
0: {nombre: "bateria", estado: "nuevo"}
1: {nombre: "motor", estado: "nuevo"}
```

Si a su vez quisiéramos entrar al primer Objeto, debemos poner dentro de los corchetes la posición que ocupa:

```js
auto.partes[0]
{nombre: “bateria”, estado: “nuevo”}
```

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">🛎 <strong>Recordá</strong>: La primera posición en un Arreglo u Objeto siempre es 0.<br></p>

Por último, si quisiéramos acceder al Valor de la clave `estado`, podríamos hacerlo de la siguiente forma:

```js
auto.partes[0].estado
"nuevo"
```

Usando _Bracket notation_ se vería así:

```js
auto[”partes”][0][“estado”]
"nuevo"
```

<div class="editor-recuadro">

 🛎️ **Recordá**: Si algún aspecto de PLEDU no funciona como esperabas o merece revisión podés avisarle al equipo de Contenido por [acá](https://forms.gle/okCETdVFsbg9S9kX7).
 
</div>

### Ejercicio: Objetos Dentro de Arreglos

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">🚀 <strong>Ejercicio Nivelatorio:</strong> Este ejercicio es similar a los de preparación para el Coding Challenge. No te preocupes si necesitás dedicarle más tiempo.<br></p>

Supongamos que tenemos un Arreglo llamado `autos` que tiene dos Objetos (un auto marca "Citroen" y otro marca "Honda").

```js
let autos = [
    {
        marca: "Citroen",
        modelo: "C3",
        año: 2013,
        dueño: "Juan",
        color:{
            capot: "gris",
            puertas: "negro"
        },
        dueñosAnteriores: [] // Lo compro 0KM
    },
    {
        marca: "Honda",
        modelo: "Fit",
        año: 2016,
        dueño: "Santiago",
        color:{
            capot: "rojo",
            puertas: "rojo"
        },
        dueñosAnteriores: ["Jorge", "Iván"]
    }
]
```

Santiago le compra el auto a Juan y le pinta el capot a negro.

¿Cómo harías para modificar esas Propiedades?

|||

```js
autos[0].dueño = "Santiago";
autos[0].dueñosAnteriores.push("Juan");
autos[0].color.capot = "negro";
```

|||



---

# Recorrer / iterar Un Objeto

### Recorrer Un Objeto

Podemos recorrer un Objeto con un nuevo tipo de _loop_ que se llama `for...in`. Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/wtbHL08kDhk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=429482884-->

Los Objetos, a diferencia de los Arreglos, tienen Propiedades sin un orden numérico. Por eso, para recorrer un Arreglo podíamos usar `forLoop` mientras que, con los Objetos, usaremos `for...in`.

Este _loop_ sirve para recorrer un Objeto y saber cuáles son sus Propiedades y Valores.

Veamos su sintaxis:

```js
for(let propiedad in nombreDelObjeto) {
// Acción que queremos que realice
}
```

El iterador `for...in` tomará alguna de las claves de las Propiedades del Objeto en cada vuelta.

Veamos un ejemplo: supongamos que queremos recorrer el Objeto `nuevaHeroina`, que a su vez tiene tres Propiedades (`nombreAvenger`, `nombreHumano`, `poder`).

```js
let nuevaHeroina = {
    nombreAvenger: 'capitana marvel',
    nombreHumano: 'carol danvers',
    poder: 'ser archi fuerte y volar por el espacio',
}
```

En cada iteración, el _loop_ `for...in` tomará el nombre de cada Propiedad de este Objeto:

```js
for (let propiedad in nuevaHeroina) {
    console.log(propiedad)
}
```

Como resultado, veremos las siguientes claves en la consola:

```js
nombreAvenger
nombreHumano
poder
```

Si utilizamos _Bracket notation_, cada iteración mostrará el Valor de cada una de las Propiedades del Objeto:

```js
for (let propiedad in nuevaHeroina) {
    console.log(nuevaHeroina[propiedad])
}
```

```js
capitana marvel
carol danvers
ser archi fuerte y volar por el espacio
```

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🛎 **Recordá**: En este caso utilizamos _Bracket notation_, ya que _Dot notation_ no acepta Variables. Intentará buscar el texto `propiedad` de forma literal y no lo encontrará (porque no existe). 

</div>

---



