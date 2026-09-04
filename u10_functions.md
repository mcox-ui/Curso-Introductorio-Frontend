### ¿Qué Es Una Función?

Una Función es un bloque de código que nos permite realizar una tarea en particular. Para que la Función se ejecute, "algo" debe invocarla. Es una herramienta muy útil porque estiliza el código y lo hace más escalable.  

Mirá este video para aprender por qué son útiles:

<iframe width="600" height="355" src="https://www.youtube.com/embed/KBYa-0cO1uE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<!--@vimeo=427233924-->

## ¿Por qué son útiles?

Como vimos en el video, las Funciones nos permiten guardar partes de código en paquetes que podemos volver a usar. 

Las Funciones, inicialmente, deben ser definidas y, luego, deben ser llamadas para que se puedan ejecutar.


+++ Diferencia Entre Un Procedimiento Y Una Función.

Según _Mozilla_, una Función en _JavaScript_ es similar a un Procedimiento — un conjunto de instrucciones que le indica a una computadora cómo ejecutar un programa o realizar un cálculo —.  Pero, para que un Procedimiento califique como Función, debe tomar alguna **entrada** y **devolver una salida** donde haya alguna relación obvia entre la entrada y la salida.

+++


### Declaración Y Llamado De Una Función

Para ejecutar una Función, primero hay que declararla. En este proceso, se escribe el bloque de código que se guardará para, luego, ejecutar. Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/oz_OmpofaFs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427235814-->

##### Sintaxis De La Función:


**Declaración De La Función:**

```js
function nombreEnCamelCase () { 
// Los paréntesis deben quedar vacíos y, luego, 
// se abre una llave para alojar las instrucciones.
  console.log("¡Soy una Función!") // Bloque de código que se ejecutará luego.
} // Se cierra la llave.
```

**Ejecución De La Función:**

```js
nombreEnCamelCase() // El paréntesis es el operador activador de la Función. Es decir que sirven para activarla y, por eso, siempre deben quedar vacíos. 
```

+++ Diferencia Entre Declarar Y Ejecutar Una Función.

Cuando declaramos una Función escribimos el bloque de código que engloba una funcionalidad determinada. Es decir, son las instrucciones para correr un programa. 

Ese bloque se guarda en la memoria para que lo usemos cuantas veces queramos. 

Para ejecutar el código de la Función tenemos que llamarla junto al operador de invocación `()`. Por lo tanto, al declarar una Función estamos generando las instrucciones y, al ejecutarla, la estamos usando.

+++

Mirá este ejemplo:

Imaginá que querés mostrar por consola el Feliz Cumpleaños. Podrías hacerlo de esta manera:

```js
console.log("Que los cumplas feliz.")
console.log("Que los cumplas feliz.")
console.log("Que los cumplas, Julieta.")
console.log("Que los cumplas feliz.")
```

Ahora, si quisieras volver a mostrarlo, tendrías que escribir ese código nuevamente. En cambio, con una Función, solo tendrías que escribir el código una vez y ejecutarlo cuantas veces lo necesites: 

```js
function cantarCumple (){
  console.log("Que los cumplas feliz.")
  console.log("Que los cumplas feliz.")
  console.log("Que los cumplas, Julieta.")
  console.log("Que los cumplas feliz.")
}
//Ahora, ejecuto la Función cuantas veces necesite:

cantarCumple()
cantarCumple()
cantarCumple()
```

Pensando a gran escala, en Funciones que tienen muchísimas líneas de código y que se ejecutan a lo largo de todo el programa, podemos ver cuánto se optimiza al escribirlo de esta manera.

### Más Funciones De JavaScript

Muchos comandos que venís usando son, en realidad, Funciones que engloban código nativo de JS. Mirá este video para reconocerlas:

<iframe width="600" height="355" src="https://www.youtube.com/embed/6fpRb3sYPqs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427237337-->

### `fechaYHora`

En este ejercicio deberás crear una Función que, al invocarla, devuelva un _string_ con la fecha y hora _hardcodeada_. 

+++ ¿Qué es hardcodear?

Según _Wikipedia_, _hardcodear_ es una mala práctica en el desarrollo de _software_ que consiste en incrustar datos directamente en el código fuente del programa, en lugar de obtenerlos de una fuente externa.

+++

Para eso, seguí este paso a paso:


#### En La Consola

1. En la consola de tu navegador, declará una Función que se llame `fechaYHora`.  El bloque de código que deberá ejecutar es un mensaje por consola que muestre la fecha y hora de este momento. Por ahora, escribilo manualmente.
2. Invocá tu Función varias veces desde la consola. 

|||

El mensaje deberá ser siempre el mismo.

|||


#### En El Editor De Texto

1. En tu editor de texto, creá un archivo `.html`, uno `.js` y vinculalos.
2. En el archivo `.js` declará la función `fechaYHora`. 

+++ 
Si abrís tu `.html` en el navegador se ejecutará el código y se **definirá** la función. Esta será accesible desde la consola ya que fue guardada en la memoria. 

⚠️ **Importante:** Solo estará definida y disponible para usar. Sin embargo, no verás el resultado hasta que la invoques. Para hacerlo, **ejecutá** desde tu consola `fechaYHora()`.

+++

3. Por último, en tu `.js`, invocá `fechaYHora()` muchas veces, una debajo de la otra. 



#### Actualización Automática

Como viste en el ejercicio, al invocar la Función, el resultado siempre es el mismo. Es decir, el código ejecutado muestra el _string_ declarado manualmente. Esta solución, no sería escalable en este caso ya que la fecha y hora se debería actualizar automáticamente. Para eso, existe un **Objeto** de JS llamado `Date()` que nos la devolverá actualizada al momento de llamarlo:

```js
Date()
```


⚠️ **Importante:** _JavaScript_ es un lenguaje _case-sensitive_, osea, que las mayúsculas importan.

Para verlo en acción, modificá tu `console.log` para que, en vez de escribir la fecha y hora manualmente, concatene un mensaje con el resultado de llamar al objeto `Date()`. 

```js
console.log("Hoy es " + Date() )
```

👩‍🏫👨‍🏫 Veremos el Objeto `Date()` con más profundidad en el Módulo 16 (Programación Orientada A Objetos).

+++ Ignorá La Complejidad.

Si bien aún no aprendiste qué es un **Objeto** de _JavaScript_, usamos uno para darle sentido al ejercicio. No hace falta que te detengas a entenderlo. En un par de unidades lo veremos en detalle y todo tendrá sentido. 

![imagen](https://i.imgur.com/p88M47d.png)

+++


### Funciones Con Parámetros

Podemos ejecutar Funciones pasándoles un Parámetro. Mirá este video para aprender más:

<iframe width="560" height="315" src="https://www.youtube.com/embed/xLSpJoZIv1w" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427239373-->

## ¿Qué Es Un Parámetro?*

Un Parámetro es una Variable que creamos al momento de definir una Función y, cada vez que la ejecutamos, le pasamos un argumento(su valor) como _input_.

Generalmente los terrminos "Parametros y "Argumentos" se utilizan de manera indistinta para referirse a los datos que le pasamos a la función, sin embargo, su connotación es diferente. S querés indagar más sobre las diferencias entre estos términos, hace _click_ [acá](https://docs.microsoft.com/es-es/dotnet/visual-basic/programming-guide/language-features/procedures/differences-between-parameters-and-arguments).

Cuando le pasamos un Parámetro a una Función estamos haciendo un código mucho más escalable. 

---

Volviendo al ejemplo del Feliz Cumpleaños, podríamos variar el nombre del cumpleañero usando un Parámetro. Si bien es factible declarar varias Funciones, una por cada persona (como cantarCumpleClaudia, o cantarCumpleElon, etc.), optimizaríamos el código de esta manera: 

```js
function cantarCumpleA(nombre)  { // Cuando declaramos la Función, entre los paréntesis, definimos el nombre del Parámetro. En este caso: nombre.
  console.log("¡Que los cumplas feliz!")
  console.log("¡Que los cumplas feliz!")
  console.log("¡Que los cumplas " + nombre + "!")
  console.log("¡Que los cumplas feliz!")
}

// Usaremos los Parámetros en el código, aunque aún no sepamos exactamente cuál será su valor. 

cantarCumpleA("Claudia")
cantarCumpleA("Elon")
cantarCumpleA("Jeff")

// El valor del Parámetro lo obtendrán una vez que se ejecute.
```

Veamos otro ejemplo de una Función que utiliza Parámetros:

```js
function areaCuadrado(lado) {
  console.log(lado * lado)
}

// Ahora, cuando ejecutamos areaCuadrado le pasaremos por Parámetro un valor que reemplace a lado.

areaCuadrado(3)
areaCuadrado(10)
areaCuadrado(4)
```


+++ ¿Cómo Manejar Los Errores En Programación?

Los que trabajamos en desarrollo de _software_ estamos acostumbrados a enfrentarnos con errores en el sistema, llamados frecuentemente _bug_. Los problemas en la lógica de nuestra aplicación, o en casos de uso que no se contemplaron originalmente, ocurren todo el tiempo sin importar la experiencia que tengas. Por eso, es muy importante no perder la calma ni caer en la frustración, ya que te alejarán de su resolución.

Hay muchas técnicas para depurar programas. Todas se basan en identificar el error y corregirlo. Uno de los más comunes es:

`Uncaught TypeError : cannot read property “x” of undefined`
Para solucionarlo, te recomendamos:

1. Identificar el problema: En este caso, no se puede leer una propiedad `x` de un Objeto indefinido.

2. Saber por qué está ocurriendo: Para esto debemos controlar cuál es nuestra Variable en cada momento para saber cuándo quedó indefinida.

3. Corregir el problema en la línea de código donde encontramos el error.

Estos pasos los podés implementar para todos los errores que se muestren en tu consola. 

+++

### Ejercicio: `decirHola`

En este ejercicio deberás crear una Función que muestre en la consola un saludo.

Luego, deberás modificar la Función para que tome por parámetro un nombre y salude a esa persona cuando la ejecutes.


Por último, ejecutá tu Función con varios nombres.

---

### Funciones Con Múltiples Parámetros


Podemos ejecutar las Funciones pasándoles todos los Parámetros que necesitemos. Mirá este video para aprender cómo incorporarlos:

<iframe width="600" height="355" src="https://www.youtube.com/embed/eUUjJvl_cCk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427242088-->

##### Sintaxis De Las Funciones Con Múltiples Parámetros

Debemos separar los Parámetros con una coma. Mirá este ejemplo:

```js
function areaTriangulo(base, altura) { 
  console.log(base * altura / 2)
}
```

Al invocar la Función, también debemos separar los valores de cada Parámetro con una coma.

```js
areaTriangulo(2, 5) 
```

⚠️**Importante:** El orden de los Parámetros puede afectar el resultado. Mirá este ejemplo: 

```js
function saludarTres(nombre1, nombre2, nombre3) {
  console.log("Hola "+ nombre1)
  console.log("Hola "+ nombre2)
  console.log("Hola "+ nombre3)
}
saludarTres("Ron", "Harry", "Hermione") 
saludarTres("Hermione", "Harry", "Ron") 
```

👩‍🏫 ¿Qué sucede si dejamos un Parámetro sin definir? Probá este ejemplo en tu consola:

```js
saludarTres("Ron", "Harry") 
```

|||

Como el Parámetro no tiene un valor, la consola mostrará que está sin definir (`undefined`).

```js
Hola Ron 
Hola Harry
Hola undefined
```

|||


¿Y si le pasamos Argumentos de más? Comprobá qué sucede en tu consola:

```js
saludarTres("Ron", "Harry", "Hermione", "Hagrid", "Dumbledore", "Snape", "Severus")
```

|||

La consola ignorará todos los valores para los que no encuentra un Parámetro.

```js
Hola Ron 
Hola Harry
Hola Hermione
```

|||

---


### Funciones Con Variables Por Parámetro

El Parámetro que le pasemos a una Función también puede ser un valor guardado en una Variable. Mirá este video para aprender cómo hacerlo:

<iframe width="600" height="355" src="https://www.youtube.com/embed/tAYQhGb45gc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427244265-->

Como vimos en el video, al ejecutar una Función que lleve un _input_, podemos pasarle una Variable como Parámetro. Por ejemplo:

```js
function cantarCumple(persona) {
  console.log("¡Que los cumplas feliz, " + persona + "!")
}

let nombre = prompt ("¿Quién cumple años hoy?")
cantarCumple(nombre)
```

Ejecutá este código en tu consola para ver cuál es el resultado.

|||

![imagen](https://i.imgur.com/gVliQyV.jpg)

```js
¡Que los cumplas feliz, Mery!
```

|||
---

### Parámetros Por ***Default*** 

Los ***Parámetros Por Default*** permiten que los Parámetros de una Función sean definidos con un valor inicial.

Veamos un ejemplo:
```js
function multiply(a, b = 1) {
  console.log (a * b);
}
multiply(5, 2);
multiply(5);
```

|||

Al ejecutar la Función **suma** sin pasarle Parámetros, **a** y **b** son `undefined` y, por lo tanto, **no son un número**.

|||

#### Sintaxis 

Para asignarle un valor por defecto a cualquiera de los Parámetros, tenemos que agregar **`= valor`** después del Parámetro.

```js
let suma = (a = 0, b = 0) => {
 return a + b;
}
console.log( suma() );
// retorna 0
```
|||

Al ejecutar la Función **suma** sin Parámetros, **a** y **b** ahora toman el valor por defecto y, por lo tanto, la Función puede retornar un número.

Más adelante verás [**Arrow Functions**](https://pledu.plataforma5.la/curso-introductorio---front-end/10--funciones/arrow-functions-9fa2cb55) y entenderás bien esta lógica.

|||

<div class="editor-recuadro">

⚠️**Importante:** Podemos asignar un valor por _default_ a uno o varios Parámetros. También podrías no asignárselo, tal como venías haciendo hasta ahora. 

</div>


Mirá en este ejemplo qué sucede cuando le asignamos un valor por defecto solo a **b**:

```js
let suma = (a, b = 0) => {
 return a + b;
}
console.log( suma() );
// retorna NaN (not a number)
console.log( suma(3) ); // 3 es el valor de a.
// retorna 3
```




---


### La ***Keyword*** `return`

La _keyword_ `return` se usa al declarar una Función para devolver un valor específico de ella. Esto sucede para guardar ese valor en una Variable o usarlo por fuera del bloque de definición de la Función.

⚠️**Importante:** Al usar esta palabra reservada se da por finalizada la ejecución de la Función, independientemente de la extensión del bloque de código.

Mirá este video para aprender más acerca de la _keyword_ `return`:

<iframe width="600" height="355" src="https://www.youtube.com/embed/UTZW4ZXrwk4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427253788-->



Veamos un ejemplo: 

```js
function cuadrado(numero) {
  console.log(numero * numero)
}
cuadrado(4)
> 16

console.log("El resultado de 4 al cuadrado es: " + cuadrado(4))
> 16
> El resultado de 4 al cuadrado es: undefined
undefined
```

En este código, el resultado de la operación se muestra por consola. Sin embargo, al no usar `return` ese valor no puede reutilizarse y, por lo tanto, se imprime `undefined`.

Observemos la ventaja de usar `return`:

```js
function cuadrado(numero) {
  return (numero * numero)
}
console.log("El resultado de 4 al cuadrado es: " + cuadrado(4))
> El resultado de 4 al cuadrado es: 16
```

Con el keyword `return` tomamos el resultado de la operación para, luego, reutilizarlo y lograr que la Función nos devuelva el valor del cuadrado de un número.


```js
function cuadrado(numero) {
  return (numero * numero)
}
console.log("El resultado de 4 al cuadrado es: " + cuadrado(4))
> El resultado de 4 al cuadrado es: 16
let resultado = cuadrado(5)
```

```js

function cuadrado(numero) {
  console.log(numero * numero)
} 
let resultado = cuadrado(5)

> 25 // Al no usar return, la consola muestra el resultado de la operación pero no la guarda en memoria. 
console.log(resultado)
> undefined // Si le pedimos que nos muestre el valor de la Variable resultado, nos dirá que no ha sido definido y, por eso, nos muestra undefined.

```

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🤓 Al usar la _keyword_ `return` guardamos el valor de una Función para, luego, reutilizarlo.

</div>

Mirá este ejemplo usando `return` para guardar el valor de la función `cuadrado` y reutilizarla en la variable `resultado`:

```js
function cuadrado(numero) {
  return(numero * numero)
} 
let resultado = cuadrado(5)
console.log(resultado)
> 25 // Como usamos return, el valor quedó guardado en la Variable resultado. Por eso, pudimos reutilizarlo.
```

Por último, mirá en este ejemplo otro uso de `return`:

```js
function cuadrado(numero) {
  return(numero * numero)
} 
cuadrado(cuadrado(2)) // En esta Función estamos reutilizando el valor que retorna la Función cuadrado. 
> 16 
```
⚠️**Importante:** Si hubiéramos usado `console.log` en vez de `return`, no hubiéramos podido hacer esta operación. 

|||

```js
function cuadrado(numero) {
  console.log(numero * numero)
} 
cuadrado(cuadrado(2))
> 4
> NaN // Como no retornamos el valor de cuadrado, la operación sería entre dos undefined. Por eso, la consola nos dice que no es un número. 
```

|||

---

+++ ¿Cuál Es El Beneficio De Usar `return`?

Si bien a veces solo queremos que la Función realice una acción, como mostrar algo en la consola, otras veces queremos que nos devuelva un valor que podamos utilizar. Para eso, usamos la _keyword_ `return`. 

+++ 

---


### El Alcance De Las Variables En JavaScript

El alcance (en inglés _scope_) de una Variable indica cuán disponible estará cuando se la invoque. Las **Variables Globales** son aquellas que están accesibles en todo el bloque de código de un programa. 

En cambio, las **Variables Locales** son accesibles solo en el ámbito de la Función donde fueron declaradas. 

Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/QT7vip5HkkI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427254039-->

Veamos algunos ejemplos para entender el alcance de las distintas Variables:

```js
let nombre = "Juan" // nombre es una Variable Global

function saludar() {
    let apellido = "Lopez" // apellido es una Variable Local
    console.log("Hola, " + nombre + " " + apellido)
}
saludar()
```

Cuando ejecutemos la Función `saludar`, la consola nos devolverá como resultado los valores guardados tanto en la Variable `nombre` como `apellido`. Esto sucede porque la Variable `nombre` es Global y `apellido` es Local dentro de la Función que estamos ejecutando.

Sin embargo, en caso de que quisiéramos seguir avanzando en nuestro código para crear una Función `despedir`, que reutilice ambos valores, la consola nos devolverá un error porque la Variable `apellido` no está definida dentro de la Función `despedir`:

```js
function despedir() {
    console.log("Chau, " + nombre + " " + apellido)
}

despedir()
```

|||

Como `apellido` es una Variable de alcance Local, solo puede utilizarse dentro de la Función en la que fue creada: `saludar`.

|||

⚠️**Importante:** Para poder reutilizar la Variable `apellido` deberíamos crearla por fuera de la Función `saludar`.



```js
let nombre = "Juan" // nombre es una Variable Global.
let apellido = "Lopez" // apellido ahora es una Variable Global.

function saludar() {
    
    console.log("Hola, " + nombre + " " + apellido)
}
saludar()
function despedir() {
    console.log("Chau, " + nombre + " " + apellido)
}

despedir()
```

Veamos otro ejemplo. En este caso, hay dos Variables `edad`, una definida localmente y otra globalmente. 

```js
let edad = 32

function mostrarEdad() {
    let edad = 44
    console.log("La edad es " + edad)
}

mostrarEdad()
```

¿Qué valor se mostrará por consola cuando llamemos a la Función `mostrarEdad`? 

|||

La consola imprimirá el valor de la Variable Local, priorizándola por sobre la Global.

```js
44
```

|||

¿Qué pasará si queremos mostrar por consola el valor de `edad` por fuera de la Función `mostrarEdad`?

|||

La consola imprimirá el valor que tiene `edad` cuando fue definida de manera Global.

```js
32
```

|||



<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">🤓<strong>¿Sabías qué...? </strong>

<br>
Una buena práctica en programación es definir todas las Variables Globales al principio de tu código.<br></p>

---

### ***Hoisting*** En JavaScript

El _Hoisting_ es, en pocas palabras, un escaneo previo que hace JS para guardar en memoria las Funciones que deberá ejecutar. Eso permite invocar la Función tanto antes como después de que sea definida. Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/ePHl7gRAM_E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=427255161-->


Veamos un ejemplo en el que declaramos una Función, usando la _keyword function_ y asignándole un nombre: 

```js
saludar1()
function saludar1 (){
  console.log("Hola")
} // En este caso, primero llamamos a la Función, y luego, la definimos usando la keyword function.
```
|||

```js
Hola
```
|||

⚠️**Importante:** Siempre que declares la Función usando la _keyword function_ y le asignes un nombre, podrás invocarla tanto antes como después de definirla. 

Otra manera de declarar Funciones es usar Variables. Veamos un ejemplo:


```js
let saludar2 = function(){
  console.log("Aloha")
} // En este caso, guardamos la Función dentro de la Variable y, luego, la ejecutamos.
```

Veamos qué pasa cuando invocamos la Función `saludar2` antes y después de ser declarada:

**Antes De Ser Declarada:** 
```js
saludar2()
let saludar2 = function(){
  console.log("Aloha")
}
```
|||
```js
saludar2 is not defined 
```

Cuando se invoca la Variable, _JavaScript_ no encuentra en memoria cuál es su definición. Por eso, devuelve que `saludar2` no ha sido definida. 

|||


**Después De Ser Declarada:**

```js
let saludar2 = function(){
  console.log("Aloha")
}
saludar2()
```
|||
```js
Aloha
```

Cuando se invoca la Variable, JavaScript encuentra en memoria cuál es su definición y ejecuta todo lo que se encuentra en el cuerpo de la Función. 
|||

⚠️**Importante:** Cuando declaramos Funciones usando Variables, solo tendremos éxito invocándola si el llamado es posterior a su creación. Esto sucede porque no se aplica el _Hoisting_ cuando asignamos una Función a una Variable.

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🤓 **¿Sabías qué...?**
 
... Con la actualización de JavaScript en ECMAScript 6 (ES6), se redefinió el concepto de *Hoisting*. 
</div>

---

### ***Arrow Functions***

Las _Arrow Functions_ son una nueva forma de crear Funciones incorporadas a partir de ES6. Una de sus ventajas es que son más concisas que las Funciones clásicas creadas con `function`.


```js
// forma clásica
function sumar(a, b) {
 return a + b;
}
console.log( sumar(1, 3) );
// 4
```
```js
// ES6 arrow function
let sumar = (a, b) => a + b;

console.log( sumar(1, 3) );
// 4
```

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🥳 Lo que en la forma clásica llevaba tres líneas de código, con las _Arrow Functions_ lo podés resolver en una sola.

</div>

#### Sintaxis

Las _Arrow Functions_ se crean usando el _Token_ (**=>**). Además:
- Son anónimas ya que no se declaran. 
- Del lado izquierdo del _Token_, se escriben los Parámetros. 
- Del lado derecho, las acciones que se deben ejecutar.

Veamos este ejemplo y cómo se simplifica gracias a la plasticidad de las _Arrow Functions_:

```js
let sumar = (a, b) => {
  return a + b
}
console.log( sumar(2, 3) ) // 5
console.log( sumar(7, 14) ) // 21
console.log( sumar(4, 2) ) // 6
```

##### Plasticidad De Las ***Arrow Functions***

Las _Arrow Functions_ son muy flexibles a la hora de codear; su sintaxis se puede adaptar a cada caso. Veamos algunos ejemplos:

1. Si las _Arrow Functions_ tienen una sola expresión, se escriben sin las llaves `{}`. En ese caso, tienen el `return` implícito y, por lo tanto, podemos evitar usar la _keyword_ `return`.

```js
let sumar = (a, b) => a + b

console.log( sumar(2, 3) ) // 5
console.log( sumar(7, 14) ) // 21
console.log( sumar(4, 2) ) // 6
```

2. Cuando una _Arrow Function_ tiene un solo Parámetro, los paréntesis son opcionales.

```js
function saludar0 (nombre) {
 return `¡Hola, ${nombre}!`
}
let saludar1 = (nombre) => {
 return `¡Hola, ${nombre}!`
}
let saludar2 = nombre => {
 return `¡Hola, ${nombre}!`
}
let saludar3 = nombre => `¡Hola, ${nombre}!`;

console.log(saludar0('María'))
// ¡Hola, María!
console.log(saludar1('Ana'))
// ¡Hola, Ana!
console.log(saludar2('Claudia'))
// ¡Hola, Claudia!
console.log(saludar3('Lucía'))
// ¡Hola, Lucía!
```

3. Cuando una _Arrow Function_ no tiene parámetros, debemos escribir los paréntesis.

```js
let mostrarSaludo = () => {
 console.log('¡Hola!')
}

let mostrarSaludoMinima = () => console.log('¡Hola!')

mostrarSaludo() // Muestra por consola ¡Hola!
mostrarSaludoMinima() // Muestra por consola ¡Hola!
```
4. Siempre que una _Arrow Function_ tenga más de una expresión entre sus acciones, es obligatorio poner las llaves. En caso de que querramos retornar algo, debemos usar la _keyword_ `return`.

```js
let saludar = nombre => {
 if (nombre) {
   return `¡Hola, ${nombre}!`
 } else {
   return `¡Hola, anónimo!` 
 }
}
console.log( saludar() ) // ¡Hola, anónimo!
console.log( saludar('Luis') ) // ¡Hola, Luis!
```


---

### ***Arrow Functions*** 🏹

Las _Arrow Functions_ son una alternativa a la función clásica. Estas son incorporadas a partir de ES6 y se ven a menudo en dferentes ejemplos de internet. 

Una de sus ventajas es que su sintaxis es más compacta y flexible que las Funciones clásicas creadas con `function`.

🎥 Mirá el siguiente video para saber de qué se tratan las _Arrow Functions_:

@youtube=QNk8ycQ-aE0

Recapitulemos, a través de distintos ejemplos, cómo se escribe cada una:


```js
// Función Clásica
function sumar (a, b) {
 return a + b;
}
console.log( sumar(1, 3) );
// 4
```
```js
// Arrow Function
let sumar = (a, b)  => {
  return a + b;
}
console.log( sumar(1, 3) );
// 4
```


#### Sintaxis

Las _Arrow Functions_ se componen de 3 partes:
- Los parámetros entre paréntesis, en este caso (a,b). 
- Del lado derecho de los parámetros, un _Token_ (=>).
- Por último, las llaves donde dentro estarán las acciones que se deban ejecutar.


<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

📚 Resulta imporante entender que se tratan de funciones anónimas. En el ejemplo la igualamos a una variable "sumar" para luego ejecutarla.

</div>



##### Compactas y Flexibles

Las _Arrow Functions_ son muy flexibles a la hora de codear. Su sintaxis se puede adaptar a cada caso. 

Sigamos con el primer ejemplo:

 ```js
let sumar = (a, b)  => {
  return a + b;
}
```
1. Podemos ver que la función posee una sola expresión, es decir, dentro de sus llaves contiene directamente el _return_. Gracias a la flexibilidad de las _Arrow functions_ podemos simplificar el primer ejemplo a esto:

```js
let sumar = (a, b)  => a + b
```

2. Se eliminan las llaves `{}` y el `return` pasa a ser implícito.


3. Además, cuando una _Arrow Function_ tiene un solo Parámetro, los paréntesis son opcionales. 

Veamos este caso:

 ```js
let multiplicar = a  => a * 5 
console.log( multiplicar(4) );
// 20
```
Veamos la descomposición desde una función clásica a una _Arrow function_ :

```js
// Funcion Clásica
function saludar(nombre) {
  return "¡Hola, " + nombre + "!";
}
// Pasamos a Arrow Function
let saludar = (nombre) => "¡Hola, " + nombre + "!";
// Sacamos los paréntesis del parámetro (ya que es uno solo)
let saludar = (nombre) => "¡Hola, " + nombre + "!";
// Compactamos, eliminamos llaves y el return pasa a ser implícito luego del Token
let saludar = (nombre) => "¡Hola, " + nombre + "!";
```


Cuando una _Arrow Function_ no tiene parámetros, debemos escribir los paréntesis. 

Por ejemplo:


```js
let mostrarSaludo = ( )  => console.log('¡Hola!')
mostrarSaludo() // Muestra por consola ¡Hola!
```
4. Siempre que una _Arrow Function_ tenga más de una expresión entre sus acciones, es obligatorio poner las llaves. En caso de que querramos retornar algo, debemos usar la _keyword_ `return`.

```js
let saludar = (nombre) => {
  if (nombre) {
    return "¡Hola, " + nombre + "!";
  } else {
    return "¡Hola, anónimo!";
  }
};

console.log(saludar()); // ¡Hola, anónimo!
console.log(saludar("Luis")); // ¡Hola, Luis!
```

## Ejercicio Práctico

En este ejercicio deberás convertir las siguientes Funciones a _Arrow Functions_:

```js
function sumarLosTres(num1, num2, num3) {
 return num1 + num2 + num3
}

function cuadrado(num) {
 return num * num
}

function decirHola() {
 console.log('¡Hola!');
}
```




---

### ***Arrow Functions*** : Ejercicios

## Ejercicio 1

En este ejercicio deberás convertir las siguientes Funciones a _Arrow Functions_:

```js
function sumarLosTres(num1, num2, num3) {
 return num1 + num2 + num3
}

function cuadrado(num) {
 return num * num
}

function decirHola() {
 console.log('¡Hola!');
}
```

## Ejercicio 2

En este ejercicio deberás convertir la siguiente Función a una _Arrow Function_.

```js
function saludar (nombre) {
 if (nombre === undefined) {
   return "hola anónimo";
 } else {
   return "hola " + nombre;
 }
}
```

## Ejercicio 3

En este ejercicio deberás arreglar las siguientes _Arrow Functions_.

```js
let nombreCompleto = (nombre, apellido) =>
  "¡Hola, " + nombre + " " + apellido + "!";
```
```js
let exclamar = str => {
 `str`
}
```
```js
let mayusculas = (str) => return str.toUpperCase()
```
```js
let minusculas = (str) => str.toLowerCase()
```

Salida por consola esperada:

```js
console.log( nombreCompleto('Ada', 'Lovelace') ); // Ada Lovelace
console.log( exclamar('Hedy') ); // ¡Hedy!
console.log( mayusculas('grace') ); // GRACE
console.log( minusculas('SHERYL') ); // sheryl
```


---

### 📞 ***Callback Functions*** 


<div class="editor-recuadro">

📚 Llamamos _Callback Function_ a una función que es argumento de otra y, luego, es ejecutada por esta.

Callback le permite una función poder llamar a otra función.
</div>


⚠️ **Importante:** entender qué es una _Callback_ resulta clave ya que se usa mucho en programación (y cobrará mayor sentido cuando lleguemos a la clase de Eventos). 

A modo de resumen:

![alt](https://i.imgur.com/lMLjshh.jpg[/img])




## 👩🏻‍💻👨‍💻Ejemplo Práctico
Para entender mejor este nuevo concepto realicemos el siguiente ejercicio:

Creá una función `fn` que reciba como Parámetros un número y una función `fnCallback`. `fn` deberá retornar el resultado de `fnCallback` pasándole como argumento el número que llega por parámetro a `fn`.

🎥 Mirá el siguiente video:


@youtube=A3wiKk41ebw

```js
function fn ( num, fnCallback ){
  return fnCallback(num)
}

fn(5, (a)=>{return a * 10}) // 50
fn(25, (a)=>{return a / 5}) // 5
```


<div class="editor-recuadro">

 🛎️ **Recordá**: Si algún aspecto de PLEDU no funciona como esperabas o merece revisión podés avisarle al equipo de Contenido por [acá](https://forms.gle/okCETdVFsbg9S9kX7).
 
</div>



---

### Ejercicios de practica

### ¿Qué Devuelve Cada Función?

<div class="editor-recuadro">

🛎 **Recordá**: En la **Comunidad de P5 de Discord** podrás ver cómo otras personas tuvieron las mismas dudas y cuáles fueron las distintas formas en que las resolvieron. ¡Aprovechá los canales y las **clases gratuitas de Twitch** para revisar y consultar!

</div>


1. En este ejercicio deberás pensar qué devuelve cada Función sin ejecutarla en la consola:

```js
function test1(x, y) {
  return y - x
}

test1(10, 40)
```

+++

No importa el orden en que pasamos los **Argumentos** sino el de los **Parámetros** en el `return`. 

+++


```js
function test2(x, y) {
  return x * 2
  console.log(x)
  return x / 2
}

test2(10)
```


+++

Cuando JS encuentra la _keyword_ `return`, devuelve el valor pedido y termina la ejecución del bloque. Es decir, el resto del código que queda debajo no se ejecuta.

+++


---

### Matemática Simple

En este ejercicio deberás crear:

1. Una función que se llame `triplicador` que tome un número como _input_ (osea, como Parámetro) y retorne el triple de ese valor.
2. Una función `multiplicador` que tome dos números como Parámetros y devuelva el producto de los dos.
3. Una función `division` que tome dos números como Parámetros y devuelva el resultado de dividir el primero por el segundo.
4. Una función `resto` que tome dos números como Parámetros y devuelva el resultado del módulo del primero sobre el segundo.

Por último, calculá el valor de triplicar 5, luego multiplicar eso por 12, dividir por 12 y encontrar el resto de dividir eso en 3.

⚠️**Importante:** Usá solamente las funciones que escribiste antes, sin otros operadores.



---

### `contarDeA_n`

En este ejercicio deberás escribir una Función llamada `contarDeA_n` que tenga los Parámetros `contar_de_a` y `contar_hasta`. Además, deberá escribir en la consola los números desde el 1 hasta `contar_hasta` en intervalos de `contar_de_a`.

+++

Si ponemos 2 y 10 como Argumentos en el llamado, la Función deberá contar de a dos hasta llegar a diez.

+++

|||**Video**

@youtube=axiU4nM-dVw
  
|||

---

### Desafío ***FizzBuzz II*** 

<div class="editor-recuadro">

🏆 Se trata del **DESAFÍO** de la clase 10 que te proponemos que lo compartas en Discord cuando termines.
</div>

En este ejercicio, deberás escribir una nueva versión de FizzBuzz (`fizzBuzz2`) que tome dos _Strings_ como Argumento y reimplemente el `FizzBuzz` original. Elegí una palabra para cada _String_ (`palabra1` y `palabra2`) que reemplace a `Fizz` y a `Buzz`. 

+++ ¿Cuáles Eran las Instrucciones de Fizzbuzz?

En ese ejercicio escribiste un programa que imprimía en la consola los números del 1 al 100, teniendo en cuenta estos criterios:

- Si el número era múltiplo de 3, imprimía "Fizz" en vez del número.
- Si era múltiplo de 5, imprimía "Buzz".
- Si era, a la vez, múltiplo de 3 y de 5, imprimía "FizzBuzz".

+++

Para completar este ejercicio, deberás: 

1. Lograr que `fizzBuzz2` devuelva un _String_ con los números separados por comas. 
2. Mejorar la Función para que el usuario pueda decidir hasta qué número tiene que contar `fizzBuzz2`.
3. Mejorar la Función para que el usuario pueda ingresar `fizz_num` y `buzz_num` para que la sustitución de palabras ocurra en los números múltiplos de los nuevos argumentos de entrada (en vez de solo 3 y 5).

⚠️**Importante:** Intentá no ayudarte con tu código anterior de `Fizzbuzz`.

<!----
|||
 
Este ejercicio tiene la [solución](https://github.com/aylu2910/pledu_ejercicios/blob/main/funciones/fizzBuzz2.js) en el Repo Intro de GitHub.


🛎️ **Recordá**: GitHub es un sitio _social coding_. Permite subir repositorios de código para almacenarlo en el sistema de control de versiones Git.

En el _Bootcamp Prep_ te explicaremos más cuestiones sobre esta herramienta 🚀.


|||

<!---->


---

### `Factorial()`

En este ejercicio, deberás crear una Función `factorial` que reciba un número y devuelva el factorial de este número. 

Por ejemplo, si hacemos `factorial(5)` la Función deberá hacer la operación 5x4x3x2x1 y devolver el resultado: 120. 



+++ 🤓 **¿Qué Es El Factorial De Un Número?**

La función factorial es una fórmula matemática representada por el signo de exclamación “!”. En la fórmula Factorial se deben multiplicar todos los **números enteros** y **positivos** que hay entre el número que aparece en la fórmula y el número 1.
Si querés ver ejemplos, hacé click [aquí](https://factorialhr.ar/numero-funcion-factorial).

⚠️**Importante:** Por convención, **el factorial de 0 es igual a 1**. Es decir, si el usuario ingresa factorial(0) el resultado deberá ser 1.

+++



Para hacer el ejercicio, tené en cuenta estas indicaciones:

+ Deberás hacer una Variable para almacenar el resultado.
+ Deberás usar un _Loop_ hasta alcanzar el número que recibís como _input_.
+ En cada vuelta del _Loop_ deberás actualizar el resultado para no caer en un _Loop_ infinito.
+ En caso de que el usuario ingrese 0 o un número negativo, deberás generar acciones compatibles con la definición del Factorial de un Número. 

+++

Usá estos ejemplos para ver si tu código funciona:

```js
factorial(5) //120
factorial(2) //2
factorial(10) //3628800
factorial(0) //1
```  

+++

|||

Este ejercicio tiene la [solución](https://github.com/aylu2910/pledu_ejercicios/blob/main/funciones/factorial.js) en el Repo Intro de GitHub.

🛎️ **Recordá**: GitHub es un sitio _social coding_. Permite subir repositorios de código para almacenarlo en el sistema de control de versiones Git.

En el _Bootcamp Prep_ te explicaremos más cuestiones sobre esta herramienta 🚀.

|||

---

### Fibonacci


👉 En este ejercicio deberás escribir una Función que acepte un número X (que indica la posición) y que devuelva otro número (el que se encuentra en esa posición) en la serie de Fibonacci. En otras palabras, imprimirá el número que está en la posición contando X cantidad de lugares. 

Serie: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55…

- Fibonacci (2): 1
- Fibonacci (5): 3
- Fibonacci (8): 13

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


|||Caminos Posibles
 

![alt](https://i.imgur.com/PurJU5F.png)
  
[Otra alternativa](https://www.programiz.com/javascript/examples/fibonacci-series#:~:text=A%20fibonacci%20sequence%20is%20written,of%20the%20previous%20two%20terms)

|||

---

### Parámetros Por ***Default*** : Ejercicios

## Ejercicio 1

En este ejercicio deberás agregar Parámetros por _default_ a la Función, para que al ejecutarla no devuelva ningún error.

```js
const longitudDelNombre = (nombre) => nombre.length

console.log( longitudDelNombre() ); // 0
console.log( longitudDelNombre('Ana') ); // 3
```

## Ejercicio 2

En este ejercicio deberás refactorizar la Función para obtener el mismo resultado usando un código más reducido.

```js
const saludarVisitanteWeb = (nombreUsuario) => {
 if (nombreUsuario === undefined) {
   return '¡Hola, anónimo!';
 } else {
   return `¡Hola, ${nombreUsuario}!`;
 }
}
console.log( saludarVisitanteWeb() ); // ¡Hola, anónimo!
console.log( saludarVisitanteWeb('José') ); // ¡Hola, José!
```
