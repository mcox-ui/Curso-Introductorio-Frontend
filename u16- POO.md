### Objetivos

En este módulo, aprenderás:

* Cuáles son los distintos **paradigmas de la programación**.
* Qué es la Programación Orientada a Objetos (**POO**).
* A qué se refiere el concepto de **Clase** y de **Objeto**.
* Qué es la **Herencia** y cómo debemos usarla para crear nuevos Objetos.
* A aplicar el **Objeto nativo `Date()`** de JavaScript.

👩‍🏫👨‍🏫 Como _Contenido Bonus_, aprenderás sobre otros conceptos que son centrales para POO: **Modularidad**, **Abstracción**, **Encapsulamiento** y **Polimorfismo**. 

<div class="editor-recuadro">

🛎 **Recordá**: En la **Comunidad de P5 de Discord** podrás ver cómo otras personas tuvieron las mismas dudas y cuáles fueron las distintas formas en que las resolvieron. ¡Aprovechá los canales y las **clases gratuitas de Twitch** para revisar y consultar!

</div>

---

### ¿Qué Son Los Paradigmas De Programación?

Los paradigmas de programación son las diferentes maneras para resolver un problema.

Hay cinco paradigmas distintos:

1. Imperativo
2. Funcional
3. Lógico
4. Orientado a Objetos
5. Declarativo

![paradigmas-programación.png](https://i.imgur.com/GeGEmYD.png)

Hasta el momento, trabajamos con JavaScript bajo el paradigma Imperativo, resolviendo los problemas de manera secuencial. Es decir,  escribimos instrucciones, paso a paso, y utilizamos ciclos y condiciones para llegar a una solución.

La mayoría de las personas que aprenden a programar se inician bajo este paradigma. Sin embargo, JavaScript se conoce como un lenguaje **multiparadigma**.

En este módulo abordaremos JavaScript desde un nuevo paradigma: el **Paradigma Orientado a Objetos**.

---

### ¿Qué Es La POO?

La **_Programación Orientada a Objetos_ (POO)** es una manera de programar que facilita el desarrollo de sistemas complejos y de gran tamaño.

Esta técnica nació a fines de los años 80 y se volvió popular rápidamente porque es más cercana a cómo expresaríamos las cosas en la vida real: dividiendo los componentes de un programa en Objetos que poseen datos (**Propiedades**) y comportamientos (**Métodos**) que se comunican entre sí.

Dentro de sus ventajas, podemos destacar:

* Fácil de modificar.
* Escalabilidad.
* Reusabilidad.
* Mantenibilidad.

+++ 📚 ¿Qué Es Mantenibilidad?

Según [AEC](https://www.aec.es/web/guest/centro-conocimiento/), mantenibilidad es "la capacidad de un elemento, bajo determinadas condiciones de uso, para conservar, o ser restaurado a, un estado en el que pueda realizar la función requerida, cuando el mantenimiento se realiza bajo determinadas condiciones y usando procedimientos y recursos establecidos."

+++

---

### Clases

Hasta ahora, si queríamos crear 2 Objetos de tipo `auto` teníamos que replicar la misma estructura. Es decir, generábamos 2 Objetos literales con una marca, modelo, año, color y precio. Por ejemplo:

```js
let auto = { 
    marca: "Peugeot",
    modelo: "208",
    año: 2018,
    color: "negro",
    precio: 400000
}
```

```js
let autoIdeal = { 
    marca: "Dodge",
    modelo: "1500",
    año: 1973,
    color: "verde",
    precio: 25000
}
```

Gracias a POO, podemos optimizar nuestro código, reutilizando componentes. Para eso, existen las **Clases**.

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">📚 Las Clases son un molde para crear Objetos. Podemos instanciarlos si cumplen con las características de esa Clase. <br></p>

+++ 📚 ¿Qué Significa Instanciar?

Según [Wikipedia](https://es.wikipedia.org/wiki/Instancia_(inform%C3%A1tica)), una **instancia** (en inglés, _instance_) es la particularización, realización específica u ocurrencia de una determinada Clase, entidad (modelo entidad-relación) o prototipo.

En los lenguajes de Programación Orientada a Objetos, un Objeto es una instancia de una Clase.

+++

![molde-objeto.png](https://i.imgur.com/1VYGvs9.png)

Recapitulando, a la hora de armar una Clase debemos tener en cuenta cuáles son las características que se repiten entre los distintos Objetos.

Veamos un ejemplo:

![ejemplo-auto.jpg](https://i.imgur.com/BdpmvDS.png)

Ambos Objetos comparten las mismas características. Se instancian a partir del mismo "molde": la Clase `Auto`.

⚠️ **Importante**: Por convención, el nombre de una Clase va siempre en mayúscula.

+++ **JavaScript Y Clases**

🤓 JavaScript incorpora la sintaxis de Clases en 2015, de la mano de ECMAScript 6. Esta sintaxis es muy similar a lo que se puede ver en otros lenguajes de programación, como C#, C++ o Java.

+++

---

### Sintaxis De Una Clase

Para generar una Clase desde la cual podamos construir Objetos, debemos respetar una sintaxis. Veamos un ejemplo:

![CLASE-01-01.jpg](https://pledu-plataforma5.s3.amazonaws.com/08fdb581-9674-460a-af27-883c3ccfdf90/CLASE-01-01.jpg)

Como podemos observar en el ejemplo, para construir una Clase tenemos que usar algunas palabras que tienen un significado especial:

📚 `constructor()`: Se trata de un método especial para la creación e inicialización de un Objeto. Puede haber solo un `constructor` por Clase.

📚 **Propiedades**: Las Propiedades son similares a las Variables, porque nos permiten definir las características que tendrán los Objetos (posteriormente instanciados). 
En nuestro ejemplo, las Propiedades son: _marca_, _modelo_, _año_, _color_ y _precio_.

📚 `this`: Hace referencia al atributo propio de la Clase. Esto nos permite diferenciar el valor que llega como Parámetro del Método `constructor`, de la Propiedad en sí. Por ejemplo:

```js
this.marca = marca
```

La palabra `marca` después del = toma el valor que recibe por parámetro en el `constructor`. Ese valor se asigna a la Propiedad `marca`, que es propia del Objeto. La _keyword_ `this` sirve para diferenciar una de la otra.

⚠️ **Importante**: Esta relación entre los parámetros que se reciben en el `constructor` con las Propiedades del Objeto no tiene que ser una relación una a una. Esto significa que podemos construir una Propiedad en base a los parámetros recibidos en el `constructor`.

Por ejemplo:

```js
class Persona{
    constructor(nombre, apellido){
        this.nombreYApellido = nombre + " " + apellido
    }
}
```

En este caso, los Objetos de Clase `persona` tendrán una sola Propiedad (`nombreYApellido`) pero su `constructor` recibe dos parámetros: `nombre, apellido`.

---

### Objetos

Recapitulando, los Objetos son instancias de una Clase. Es decir, podemos crear diferentes Objetos a partir del mismo "molde".

Estos Objetos se refieren a algo que puede ser concreto y tangible como, por ejemplo, una persona o un vehículo, hasta algo abstracto (o conceptual) como una canción.

Veamos a continuación cómo podemos instanciar Objetos de tipo _Auto_ en base a la Clase desarrollada.

---

### Objetos Tipo Auto

Supongamos que quisiéramos crear 2 Objetos: uno que represente mi auto actual (`miAuto`) y mi auto ideal (`autoIdeal`). Estos Objetos forman parte de la misma Clase `Auto`.

Podríamos emplear la siguiente sintaxis:

```js
let miAuto = new Auto("Peugeot", "208", 2018, "negro", 400000) 
let autoIdeal = new Auto("Dodge", "1500", 1973, "verde", 25000)
```

🛎 **Recordá**: Para utilizar este código, primero debemos definir la Clase `Auto`, como vimos en la sección anterior:

```js
class Auto {
  constructor(marca, modelo, año, color, precio) {
    this.marca = marca
    this.modelo = modelo
    this.año = año
    this.color = color
    this.precio = precio
  }
}
```

Como podemos ver, estos Objetos comparten las mismas características de la Clase (_marca_, _modelo_, _año_, etc.) pero tienen distintos valores (_Peugeot_ y _Dodge_, _208_ y _1500_, etc.).

Avanzá a la siguiente sección para aprender cómo acceder a los datos de nuestros Objetos.

![expectativa-realidad.png](https://i.imgur.com/bBjPDPN.jpg?1)

---

### Cómo Acceder A Los Datos De Nuestros Objetos

Para acceder a los valores de nuestros Objetos podemos usar tanto _Dot_ como _Bracket notation_.

Por ejemplo, para acceder al valor de la Propiedad `color` de cada auto, deberíamos respetar la siguiente sintaxis:

```js
autoIdeal.color
autoIdeal["color"]
```

En ambos casos, obtenemos el valor `verde`.

---

### Cómo Agregar Propiedades A Nuestros Objetos

Para agregar Propiedades a nuestros Objetos también podemos usar _Dot_ o _Bracket notation_.

Por ejemplo, si quisiéramos agregar una Propiedad que tenga un valor booleano (`tieneVTV`) podríamos escribir:

```js
autoIdeal.tieneVTV = false
```

De esta manera, modificamos el Objeto `autoIdeal`:

![auto-ideal.png](https://i.imgur.com/bjEw5Ix.png)

Sin embargo, el Objeto `miAuto` permanece igual:

![mi-auto.png](https://i.imgur.com/sK5FmRV.png)

🛎 **Recordá**: Si bien estos Objetos comparten la misma Clase, son independientes uno del otro.

---

### Cómo Eliminar Propiedades De Nuestros Objetos

Para eliminar una Propiedad debemos usar el operador `delete`.

Veamos un ejemplo. Si quisiéramos eliminar la Propiedad "color" del Objeto `miAuto`, podríamos escribir:

```js
delete miAuto.color
```

Ahora, probalo en tu consola y mirá el código: a través del operador `delete`, eliminamos la Propiedad "color".

---

### Métodos

Como ya vimos, los Objetos poseen datos (Propiedades) y comportamientos (Métodos).

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">📚 Podemos pensar a los Métodos como Funciones que pueden o no recibir un parámetro y que sirven para la correcta realización de distintas tareas. Pueden ser especificados al definir la Clase. <br></p>

#### Cómo Crear Un Método

Siguiendo el ejemplo anterior, veamos cómo crear un método modificando la Clase `Auto`.

```js
class Auto {
  constructor(marca, modelo, año, color, precio, sucio) {
    this.marca = marca
    this.modelo = modelo
    this.año = año
    this.color = color
    this.precio = precio
    this.sucio = sucio
  }
  mostrarAuto() {
      console.log("Un hermoso " + this.marca + " " + this.modelo + " color " + this.color)
  }
  lavarAuto() {
      this.sucio = false  
  }
}
```

Ahora instanciamos 2 Objetos con los nuevos valores para la Propiedad `sucio`.

```js
let miAuto = new Auto("Peugeot", "208", 2018, "negro", 400000, true) 
let autoIdeal = new Auto("Dodge", "1500", 1973, "verde", 25000, true)
```

Los Objetos instanciados de tipo `Auto` ahora pueden invocar el Método `mostrarAuto` usando _Dot_ o _Bracket notation_, seguido del nombre del método y los paréntesis.

```js
miAuto.mostrarAuto(); 
autoIdeal.mostrarAuto();  
```

Nos mostrará el siguiente mensaje:

```js
miAuto.mostrarAuto(); // "Un hermoso Peugeot 208 color negro"
autoIdeal.mostrarAuto(); // "Un hermoso Dodge 1500 color verde"
```

Ahora supongamos que quisiéramos modificar el valor de la Propiedad `sucio` del Objeto `autoIdeal`, sin modificarlo en el Objeto `miAuto`.

Deberíamos escribir la siguiente sentencia:

```js
autoIdeal.lavarAuto()
```

Esto modifica el valor de la Propiedad `sucio` del Objeto `autoIdeal`, asignándole el valor `false`.

Ahora, usando _Dot notation_ podemos ver que este valor es distinto en cada Objeto:

```js
autoIdeal.sucio
false
```

```js
miAuto.sucio
true
```

🛎 **Recordá**: En una Clase podemos crear infinitos métodos, pero solo podemos definir un constructor.

---

### Ejercicio: Mis Libros

En este ejercicio, deberás poner en práctica lo aprendido en esta unidad, creando Objetos, Clases y Métodos.

#### Crear El Molde

1. Definí una Clase llamada `Libro` que posea las siguientes Propiedades: nombre del libro, autor, editorial y género.
2. Luego, creá un Método en la definición de la Clase llamado `mostrarLibro`, que devuelva un mensaje con todas las Propiedades que posee un libro.

#### Instanciar Los Objetos

Instanciá 3 Objetos de tipo `Libro` con diferentes valores e invocá al Método `mostrarLibro` desde cada Objeto.

#### Poblar Un Arreglo

Creá un Arreglo llamado `libros` y cargalo con los Objetos definidos previamente.

#### Filtrar Libros

Por último, creá una Función llamada `filtrarPorAutor` que reciba el Arreglo de libros y el autor y devuelva los libros pertenecientes a dicho autor.

---

### Herencia

La **herencia** es uno de los conceptos más importantes de la Programación Orientada a Objetos.

Una Clase puede heredar las características (Propiedades y Métodos) de otra, que estén definidos en una ***superclase*** también llamada "Clase Padre".

![luke-clasepadre.png](https://i.imgur.com/Mc3ccri.jpg)

Es decir, gracias a la herencia podemos definir nuevas Clases basadas en otras preexistentes, generando una jerarquía. De esta manera, reutilizamos el código. Esto es muy útil, ya que la subclase tiene todos los atributos y métodos definidos en la superclase y, a la vez, está abierta a redefinirlos.

Por ejemplo, supongamos que tenemos una superclase `mamifero` cuyo método `reproduccion` está definido por defecto como "gestación". La subclase `ornitorrinco` podría redefinir ese método, implementando la reproducción por "huevos".

⚠️ **Importante**: Si bien una Clase puede heredar las características de otra, también podemos añadir nuevas Propiedades y Métodos para distinguirlas entre sí.

Veamos otro ejemplo.

![herencia.png](https://i.imgur.com/tlN7CSz.png)

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">👩‍🏫👨‍🏫 <strong>Generalización Y Especificidad</strong><br>Si pensamos en la relación de herencia como un árbol o pirámide, cuanto más alto será más genérico y cuanto más bajo será más específico. Es decir, los conceptos más importantes estarán en la copa del árbol.<br></p>

---

### Herencia En Práctica

Veamos otro ejemplo. Supongamos que quisiéramos modelar tres Objetos distintos: `Persona`, `Profesor` y `Estudiante`. Si bien estos no son exactamente iguales, poseen Propiedades y Métodos en común: `nombre`, `edad`, `institucion` y el método `saludar`.

![herencia.png](https://happy-cori-b31a79.netlify.app/herencia.png)

🛎 **Recordá**: Los Objetos son instancias de una Clase. Es decir, podemos crear diferentes Objetos a partir del mismo "molde".

#### Paso A Paso

1. Definir la Clase `Persona`:

```js
class Persona {
    constructor(nombre, edad, institucion) {
        this.nombre = nombre
        this.edad = edad
        this.institucion = institucion
    }

    saludar() {
        console.log("¡Hola! Mi nombre es " + this.nombre)
    }
}
```

2. Definir las Clases `Profesor` y `Estudiante`.

Para hacerlo, usaremos la _keyword_ `extends` (del inglés "extiende"). De este modo, la Clase `Profesor` heredará los atributos y métodos que posee la Clase `Persona` (en este caso, la "Clase Padre").

```js
class Profesor extends Persona {

} // La Clase Profesor ahora posee los atributos nombre, edad, institución y el método saludar.
```

**Repetí este paso para definir la Clase `Estudiante`.**

+++ Cómo Verificar Que Un Objeto Posee Las Propiedades Y Métodos Heredados

Podemos verificar que el Objeto `Profesor` posee las Propiedades y Métodos heredados del Objeto `Persona` de esta manera:

```js
let profesor = new Persona("Román", 42, "Plataforma 5")
profesor.saludar()
```

Se verá así en la consola:

```js
profesor {nombre: "Román", edad: 42} 
edad: 42
nombre: "Román"
¡Hola! Mi nombre es Román
```

👩‍🏫👨‍🏫 Si solo quisiéramos replicar el Objeto `Persona` de manera exacta, sería más fácil definir un Objeto de forma independiente. La utilidad de la herencia está en reutilizar una parte del código para, luego, definir nuevos atributos y métodos.

⚠️ **Importante**: Una Clase puede tener muchas subclases, pero en general solo hay una superclase. Si bien existen algunos lenguajes que admiten herencia múltiple, no los veremos en este curso.

+++

3. Definir **nuevos** atributos y métodos.

Vamos a definir un **nuevo** atributo para la Clase `Profesor`: `cursosACargo`. Además, **modificaremos** el método `saludar`.

Para hacerlo, incorporaremos la _keyword_ `super` en nuestro constructor.

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

📚 Al usar la _keyword_ `super`, llamamos al constructor de la "Clase Padre" y le pasamos los parámetros que ésta posee.

</div>

⚠️ **Importante**: Al llamar al constructor de la "Clase Padre", debemos pasar los parámetros en el orden en el que fue definido.

```js
class Profesor extends Persona {
    constructor(nombre, edad, institucion, cursosACargo) {
        super(nombre, edad, institucion)
        this.cursosACargo = cursosACargo
    }
    
    saludar() {
        console.log("¡Hola! Mi nombre es " + this.nombre + " y soy profesor en " + this.institucion)
    } 

   informarCantidadDeCursos(){
       console.log("Me encuentro dando " + this.cursosACargo + " cursos en la institución " + this.institucion)
   }
}
```

Si instanciamos nuevamente al Objeto `Profesor` con nuevos valores, veremos lo siguiente en la consola:

```js
let profesor = new Profesor("Román", 42, "Plataforma 5", 2)
profesor.saludar()
```

```js
Profesor {nombre: "Román", edad: 42, institucion: "Plataforma 5", cursosACargo: 2}
cursosACargo: 2
edad: 42
institucion: "Plataforma 5"
nombre: "Román"

¡Hola! Mi nombre es Román y soy profesor de Plataforma 5 // Este método reemplazó el método de la "Clase Padre"
```

Ahora, probá en tu consola: `profesor.informarCantidadDeCursos()`. ¿Qué te devuelve el código?

|||


```js

Me encuentro dando 2 cursos en la institución Plataforma 5

```

|||



Luego, vamos a definir un **nuevo** atributo para la Clase `Estudiante`: `cursoActual`. Además, **crearemos** un nuevo método `saludar` para reemplazar al anterior.

```js
class Estudiante extends Persona {
    constructor(nombre, edad, institucion, cursoActual) {
        super(nombre, edad, institucion)
        this.cursoActual = cursoActual
    }
    
    saludar() {
        console.log("¡Hola! Mi nombre es " + this.nombre + " y estoy haciendo el " + this.cursoActual + " en " + this.institucion)
    } 
}
```

Esta vez, si instanciamos al Objeto `Estudiante` con estos nuevos valores, veremos lo siguiente en la consola:

```js
let estudiante = new Estudiante("Gabriela", 24, "Plataforma 5", "Coding Bootcamp")
estudiante.saludar()
¡Hola! Mi nombre es Gabriela y estoy haciendo el Coding Bootcamp en Plataforma 5
```

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">👩‍🏫👨‍🏫 En síntesis, la POO nos permite optimizar nuestro código y hacerlo más conciso. Al definir nuestra "Clase Padre" (el molde), podemos facilitar la creación de nuevas Clases con características en común.<br></p>

#### Para Pensar

En la teoría, existe una relación de herencia entre una subclase y una superclase. Por ejemplo, la subclase `Profesor` hereda los atributos y métodos de la superclase `Persona`, pues un profesor es una persona.

Ahora, supongamos que nuestro profesor en realidad es un robot.

![robot-bender.gif](https://media.giphy.com/media/rSCVJasn8uZP2/giphy.gif)

¿Tiene sentido crear una subclase `profesorRobot` que herede los atributos y métodos de la superclase `Persona`?

Pensá tu respuesta antes de mirar la solución.

|||

Si la superclase `Persona` incluyera un método como "respirar", la subclase `profesorRobot` lo heredaría. Sin embargo, esto es incorrecto. Si bien nuestro robot es un profesor, no es una persona: no respira.

No tiene sentido crear una relación de herencia entre una subclase `profesorRobot` y la superclase `Persona`.

|||

---

### Ejercicio: Herencia

En este ejercicio, deberás diseñar un programa para darle funcionalidad a un auto. Para eso, poné en práctica lo aprendido hasta ahora.

Diseñá una clase `Auto` con las siguientes Propiedades:
- Marca.
- Modelo.
- Año de fabricación.
- Cantidad de puertas.

Luego, creá dos métodos:
1. `Acelerar`: debe loguear "Acelerando..."
2. `subirVidrios`: debe loguear "Subiendo vidrios..."

Por último, creá nuevas Clases para autos a gas, a nafta y eléctricos. Cuando cada uno acelere, debe loguear qué mecanismo utiliza (por ejemplo: "Acelerando a gas...").

---

### El Objeto `Date()`

![troy-objetodate.png](https://i.imgur.com/ET5AtEA.jpg?1)

Como mencionamos en el Módulo 10 (Funciones), el Objeto `Date()` nos permite trabajar con fechas y horas proporcionadas por nuestro navegador.

#### Creación de Objetos `Date()`

Podemos instanciar distintos Objetos `Date()` dependiendo de la cantidad de argumentos que le proporcionemos al constructor.

Por ejemplo:

```js
let ahora = new Date(); // Devuelve día y hora actual
let navidad = new Date(2022, 11, 25): // Navidad del año 2021
let casiNavidad = new Date(2022, 11, 24, 23, 59, 59); // Un segundo antes de navidad
```


En el caso de que no hubiera uno, el constructor instanciará un Objeto con la hora local y fecha de hoy.

Por ejemplo:

```js
let date = new Date();
console.log(date)
```

`> Tue Nov 02 2021 00:51:52 GTM-0300`

⚠️ **Importante**: el Objeto `Date()` es estático. Si volvemos a llamar a la Variable asignada `date`, su valor será el mismo (por más que haya transcurrido tiempo).

---

### Métodos Del Objeto `Date()`

El Objeto `Date()` puede invocar diferentes métodos. Veamos algunos de ellos:

##### `getFullYear()`

El método `getFullYear()` nos devuelve el año actual.

```js
console.log(date.getFullYear())
```
`> 2021`

#### `getMonth()`

El método `getMonth()` nos devuelve el valor numérico que corresponde al mes actual. 

⚠️ **Importante**: Tené en cuenta que el primer mes (enero) posee el número 0 (cero), por lo que el mes de diciembre tiene como valor el número 11 (once).

```js
console.log(date.getMonth())
```
`> 9`

#### `getDate()`

El método `getDate()` nos devuelve el valor numérico que corresponde al día del mes en curso.

```js
console.log(date.getDate())
```
`> 12`

#### `getDay()`

El método `getDay()` nos devuelve un valor numérico que corresponde al día de la semana.

⚠️ **Importante**: Tené en cuenta que se toma como el primer día de la semana al domingo y se le asigna el valor 0 (cero).

```js
console.log(date.getDay)()
```

---

### Ejercicio: ¿Qué Día Es?

En este ejercicio, deberás crear un programa que use el Objeto `Date()` para devolver un `alert` que exprese qué día de la semana es.

⚠️ **Importante**: Debe existir una respuesta por cada valor numérico que pueda llegar.

+++ ¿Qué Tipo De Dato Tiene `alert`?

El `alert` debe devolver un _String_.

+++

---

+++ ¿Qué Estructura Condicional Debés Usar?

Si bien podés usar `if...else`, te recomendamos que uses `switch`.
 
+++

#### 🚀 ***Extra Credit*** 

¿Cómo lo harías sin utilizar la estructura condicional `if...else` o `switch`?

---

### Ejercicio: ¿Cuánto Falta Para El Sábado?

En este ejercicio, crearás un sitio que le informe al usuario cuántos días faltan para el sábado.

![sabaduki.png](https://i.imgur.com/fYvY8uw.jpg)

Aplicá todo lo que aprendiste hasta ahora en HTML, CSS y el Objeto `Date()`.

Cuando termines, no te olvides de subir tu sitio a Netlify y compartir tu aporte en el canal de _Discord_.

+++

Podés crear el sitio que quieras, pero si no se te ocurre nada, podés imitar la famosa "Placa Roja":

![pista.png](https://pledu-plataforma5.s3.amazonaws.com/08fdb581-9674-460a-af27-883c3ccfdf90/pista.png)

+++

#### 🚀 ***Extra Credit***

Hacé que tu sitio muestre distintos recursos para mostrar cuántos días faltan para el sábado. Por ejemplo, sumá imágenes, gifs o fondos de distintos colores.

---

### Otros Conceptos De POO

Además del concepto de **Herencia**, existen otros que son centrales para POO: **Modularidad**, **Abstracción**, **Encapsulamiento** y **Polimorfismo**. En esta sección desarrollaremos brevemente cada una.

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🚀 Si querés aprender más, podés seguir estudiando estos conceptos en el Coding Bootcamp. Escribí a [Admisiones](mailto:admisiones@plataforma5.la?Subject=Consulta%20-%20Coding%20Bootcamp) para conocer nuestras próximas fechas.

</div>


Supongamos que tuviéramos un concesionario de autos. Podemos ingresar nuevos autos, venderlos y obtener una lista de autos disponibles por marca. Además, cada unidad tiene en común ciertas características (marca, año de fabricación, etc.) y acciones (acelerar). Sin embargo, también pueden tener diferencias: por ejemplo, un auto puede ser manual mientras otro es automático.

#### 📚 Modularidad

La POO permite dividir nuestra aplicación en partes más pequeñas e independientes (módulos).

Volviendo al ejemplo, esto nos permitiría crear una Clase `Concesionario` y una Clase `Auto`. De esta forma, podríamos crear Subclases como `AutoNaftero` y `AutoElectrico`.

#### 📚 Abstracción

La abstracción implica captar las características esenciales de un Objeto (por ejemplo: su comportamiento). Es decir, aisla un elemento de su contexto o del resto de los elementos.

En nuestro ejemplo, el concesionario conoce las características de los autos, pero puede abstraerse de los detalles de su funcionamiento interno.

#### 📚 Encapsulamiento

El encapsulamiento permite restringir y controlar el uso de una Clase, ya que consiste en el ocultamiento de las Propiedades y acciones de un Objeto. De esta manera, se pueden cambiar mediante las operaciones definidas para ese Objeto.

+++ ¿Qué Significa Restringir Y Controlar?

Al **restringir** un comportamiento o atributo privado de una Clase, indicamos que no podrá ser accedido por otras.

Al **controlar**, damos ciertos mecanismos para modificar el estado de una Clase.

+++

En nuestro ejemplo, el concesionario tiene atributos públicos (por ejemplo: su dirección y horario de atención) y privados (como el balance del último mes).

🔍 Para aprender más sobre privacidad en JavaScript, accedé a la [documentación de Mozilla](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Classes/Private_class_fields).

#### 📚 Polimorfismo

El polimorfismo nos permite asociar diferentes estrategias de resolución para un mismo comportamiento.

En nuestro ejemplo, todos los autos aceleran. Sin embargo, algunos lo hacen a combustión y otros de manera eléctrica.

<div class="editor-recuadro">

 🛎️ **Recordá**: Si algún aspecto de PLEDU no funciona como esperabas o merece revisión podés avisarle al equipo de Contenido por [acá](https://forms.gle/okCETdVFsbg9S9kX7).
 
</div>

---

### Introducción: Cargar Pedidos

En este proyecto, deberás crear un sistema de carga de pedidos para una librería.


Tu programa deberá recibir los datos de las compras y notificar al servicio de delivery para que entregue los libros a los distintos clientes. Por lo tanto, deberá permitirle al usuario ingresar el **nombre del libro, autor y dirección del comprador**.

Una vez cargados los datos, aparecerá un recuadro con todos los detalles de la compra.

Comenzarás generando la estructura con el HTML, luego definirás el comportamiento de tu sitio _web_ con _JavaScript_ y por último agregarás estilos con CSS.

🚀 Este proyecto te preparará para el siguiente desafío: el **To Do List**. Te tomará un poco más de tiempo que los ejercicios anteriores, ¡pero la práctica hace la diferencia!

---

### Generar La Estructura

Para generar la estructura de tu sistema de carga de pedidos, seguí el siguiente paso a paso.

Al finalizar esta sección, tu proyecto debería verse así:

<img src="https://i.ibb.co/8bZ4K2J/pedidos-Inicial.png" style="display:block;margin:0 auto;width:60%;border:1px solid black;border-radius:24px">

#### Paso A Paso

1. Creá un documento HTML con su estructura básica y vinculalo a una hoja de estilos y un archivo _JavaScript_.

2. Ingresá un valor para la etiqueta `<title>`. Por ejemplo: "Cargar Pedidos".

3. Armá la siguiente estructura básica para el `<body>` de tu documento HTML:

- Un `<div>` con `class="container"` que tenga:
  - Un título con el valor "Delivery De Compras De Libros".
  - Un `<hr>` para separar la sección del título.
  - Un subtítulo con el valor "Datos del pedido".
  - Un `<div>` con `class="datos-pedido"` que incluya tres `input`:
      - Nombre del libro.
      - Nombre del autor del libro.
      - Dirección del comprador (donde se entrega el pedido).

🛎 **Recordá**: La convención en HTML es utilizar el 🥙 **kebab-case**. Escribimos las palabras en minúsculas y las separamos con guiones medios.

<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

🤓 **Tip**: En cada uno de tus `input`, incluí atributos `id` y `placeholder` con sus respectivos valores para, luego, identificarlos fácilmente.

</div>

  - Un `<div>` con `class="btn-container"` para poner dos botones:
     - Un `button` con `id="cargar"` y el texto "CARGAR".
     - Un `button` con `id="refrescar"` y el texto "REFRESCAR". Dentro de este botón insertarás un ícono "🔄". Para ello, usarás _font-awesome_.

+++ Cómo Incorporar Íconos Con _Font Awesome_

Para incorporar íconos dentro de tu proyecto, ingresá la siguiente etiqueta antes del cierre del `<body>`:

```html

<script src="https://kit.fontawesome.com/be6f6f9a32.js" crossorigin="anonymous"></script>

```

Luego, para asociar tu `button` con `id="refrescar"` al ícono "🔄", agregá el siguiente _tag_ antes del texto "REFRESCAR":

```html

<i class="fas fa-redo-alt fa"></i>
    
```

+++

  - Un `<div>` con `class="confirmaciones"` para que los datos de los pedidos estén visibles en un recuadro. Incluí dentro del `<div>` una lista desordenada vacía. De este modo, los datos se agregarán como ítems.

---

### Definir El Comportamiento

En esta sección del proyecto, le darás funcionalidad a tu servicio de carga de pedidos. Para eso, deberás vincular tu archivo JavaScript con tu proyecto y seguir este paso a paso.

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">👩‍🏫👨‍🏫 Esta sección es más larga que las anteriores. Recordá ignorar la complejidad y avanzar paso a paso. <strong>¡No te desanimes!</strong><br></p>

![keep-swimming.png](https://i.imgur.com/gGfnBoI.gif)

#### 1. Referenciar Elementos HTML

- Referenciá los siguientes elementos HTML en Variables JavaScript:
  - `<div>` con `class="confirmaciones"` (`div.confirmaciones`).
  - Los botones con `id="cargar"` y con `id="refrescar"`.
  - La lista desordenada (`<ul>`).

👩🏻‍💻👨‍💻 Guardá los diferentes elementos en Variables para no tener que seleccionarlos mediante el DOM cada vez que debas referenciarlos.

- Usá los `id` asignados a cada `input` en el HTML y guardá la referencia en tres Variables. Los necesitarás al llegar al recuadro de confirmaciones.

🤓 **Tip**: Usá los comentarios de JavaScript para ordenar las Variables en dos categorías de elementos: `input` y `<div>`.

#### 2. Trabajar con Clases

Para darle funcionalidad al proyecto, aplicá lo aprendido hasta ahora en POO y el DOM.

- Creá la Clase `Pedido`. Ésta posee en su `constructor` el llamado a un método propio: `cargarItems`.

Esta Función añadirá los valores de los tres `input` a `div.confirmaciones`. Luego, le asignarás un Evento _click_ a los botones, que agregarán nuevos ítems a la lista desordenada (o los borrarán).

⚠️ **Importante**: El llamado de la Función necesitará tres Argumentos para que incluya todos los detalles del pedido (y figuren como ítems de `<ul>`). Podés llamarlos `titulo`, `autor` y `direccion`. Por su parte, el `constructor`, deberá tomar estos valores como Parámetros para que `cargarItems` los reciba como Argumentos.

|||

El código debería quedarte así:

```js
class Pedido {
  constructor(titulo, autor, direccion) {
    this.cargarItems(titulo, autor, direccion);
  }
```

|||

- Luego, creando la Función `cargarItems`, definí el método `crearDiv` y pasá los mismos Parámetros.
- Dentro del método, creá el `<li>` (que irá dentro de la `<ul>`). Para eso, usá `createElement` y guardalo en una Variable.

+++ Cómo Utilizar `createElement`

Veamos la sintaxis del método `createElement`:

```js

document.createElement("elementoNuevo")

```

+++

- Una vez creado el `<li>`, agregale contenido. Cada `<li>` deberá tener el siguiente formato:

`✓ El libro titulado ... , del autor ... será llevado a la dirección ...`

Primero, definí tu Variable y usá la Propiedad `textContent` para modificar el contenido. Luego, concatená los _Strings_ ("✓ El libro titulado") con los Parámetros del método (es decir, `titulo`, `autor` y `direccion`). Al instanciar la Clase, tomarán los valores de sus respectivos `input`.

|||

Deberías definir el contenido del `<li>` de la siguiente manera:

```js

li.textContent = "✓ El libro titulado " + titulo + ", del autor  " + autor + " será llevado a  la dirección " + direccion

```

⚠️ **Importante**: La Variable `li` fue previamente definida y hace referencia al `<li>` creado antes.

|||

- Por último, agregá el nuevo ítem de la lista a la `<ul>`.

+++

🔍 Si no sabés qué método usar, investigá el uso de `appendChild()`.

+++

#### 3. Agregar Eventos A Los Botones

Ahora, agregarás un Evento para que se instancie un nuevo Objeto que añada o remueva ítems cada vez que el usuario presione los botones.

##### Botón "CARGAR"

El botón "CARGAR" añadirá nuevos ítems a la lista.

- Agregá un `eventListener` al botón, con un tipo de Evento _click_.
- Dentro de la Función _callback_, instanciá el nuevo Objeto a partir de la Clase `Pedido`.

   
+++ Cómo Instanciar El Objeto

Para instanciar un Objeto a partir de una Clase, usá la palabra reservada `new`, seguida del nombre de la Clase y los paréntesis (con los Argumentos correspondientes).

Incluí el valor de los `input` como Argumentos del método `constructor`. Para eso, usá la Propiedad `.value`, que devolverá los caracteres ingresados en un `input` determinado.

+++

---

|||

El código de la Función _callback_ debería verse así:

```js

new Pedido(input1.value, input2.value, input3.value)

```

En donde `input1`, `input2` e `input3` son los nombres de las Variables de cada `input`.

🛎 **Recordá**: Antes de cerrar la Función _callback_, deberás indicar que los valores de los `input` queden vacíos. Sino, el contenido nuevo se sumará a lo cargado previamente.

|||

- Especificá un límite de 5 ítems por pedido. Además, creá un `alert` que le indique al usuario cuando haya superado la capacidad máxima del sistema. En ese caso, el usuario deberá hacer _click_ en el botón "REFRESCAR" para borrar todos los ítems.

+++ Cómo Poner Un Máximo De Ítems En La Lista

El método `document.querySelectorAll("elemento")` devuelve un _Node list_ con la cantidad de elementos coincidentes con el selector CSS.

+++

##### Botón "REFRESCAR"

El botón "REFRESCAR" eliminará los ítems de la `<ul>`.

- Agregá un `eventListener` al botón, con un tipo de Evento _click_.
- Dentro de la Función _callback_, indicá que se eliminen los `li`.

+++ Cómo Remover Elementos De La Lista

Recorré los ítems de la lista y usá el método `.remove()`.

🛎 **Recordá**: Este método remueve el elemento sobre el cual se aplica. Su sintaxis es: `elemento.remove()`

+++

#### ¡Felicidades!

Llegaste al final de esta sección. Si todo funciona bien, continuá a la siguiente sección para agregarle estilos a tu proyecto.

![everest.gif](https://i.imgur.com/LJ7zLth.gif)

#### 🚀 _Extra Credit_

Para que tu proyecto se vea más profesional, completá estos _Extra Credit_:

1. Hacé que el sistema solo cargue el libro si el usuario completó todos los campos.

2. Incluí un número de gestión para cada pedido. Debe ser único y aleatorio.

🤓 **Tip**: Podés generar el número de gestión a través de un botón en la sección de **Datos del Pedido**.

---

### Agregar Estilos

En esta última sección, definirás los estilos de tu proyecto. Para eso, deberás usar la hoja de estilos que vinculaste a tu archivo HTML al comienzo de la unidad.

Al finalizar esta sección, tu proyecto debería verse así:


![librería](https://i.imgur.com/PT2Wr4m.png)

#### 1. Dar Estilos Al `<body>`

En tu archivo `.css`, dale al `<body>` el siguiente formato:
  -  Una altura de `100vh`.

+++ ¿Qué Significa `vh`?

🛎 **Recordá**: `vh` significa _viewport height_. Es decir, el valor `100vh` representa el alto de la pantalla. Para aprender más hacé _click_ [acá](https://stackoverflow.com/questions/41793228/min-height-in-vh-vs-for-body/41793897).

+++

  -  Márgenes de `20px` en todos sus lados.
  -  Alineación centrada.
  -  Una tipografía distinta a la que está por _default_ y en color blanco.
  -  Un color de fondo azul marino.

|||

```css

body {
  min-height: 100vh;
  margin: 20px;
  text-align: center;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  background: #0a1f44;
  color: white;
}

```

|||

#### 2. Estilizar El `input`

Dale al `input` el siguiente formato:
  - Un tamaño tipográfico de `1.5rem`.
  - Alineación centrada.
  - Una altura de `25px`.
  - Un `padding` de `5px`, `5px` y `10px`.
  - Un borde inferior sólido de `1px`.

+++ ¿Qué Es La Unidad Rem?

Rem es una unidad de CSS relativa. Es decir, tiene como referencia de medida el tamaño tipográfico del elemento raíz: la etiqueta <html>. A diferencia de em, que tiene como referencia el tamaño tipográfico del elemento donde se usa esa unidad.

+++

---

|||

```css

input {
  font-size: 1.5rem;
  text-align: center;
  height: 25px;
  padding: 5px 5px 10px;
  border-bottom: 1px solid;
}

```

|||

#### 3. Dar Estilos Al `button`

Dale al `button` el siguiente formato:
  - Un tamaño tipográfico de `1rem` y en negrita.
  - Un espacio entre caracteres de `0.1em`.
  - Un `padding` de `15px` y `20px`.
  - Un margen izquierdo de `15px`.
  - Un fondo con el siguiente color: `#ff1e42`.
  - Un `border-radius` de `5px` y sin borde.

Hacé que, cuando el cursor pase sobre el botón, cambie el color de fondo a `#c3112d`.

|||

```css

  button {
      font-size: 1rem;
      font-weight: bold;
      letter-spacing: 0.1em;
    
      padding: 15px 20px;
      margin-left: 15px;
    
      background: #ff1e42;
      border-radius: 5px;
      border: none;
}

```

Para cambiar el color de fondo del botón, utilizá el pseudo-selector:

```css
  button:hover {
     background: #c3112d;
  }

```

|||

#### 4. Estilizar Los `input` Y `button` En Conjunto

Modificá el formato del `input` y `button` en conjunto:
  - Sacá el borde, color de fondo y contorno.
  - Dale un color blanco al texto.

|||

```css

  button,input {
      border: none;
      background: none;
      outline: none;
      color: white;
}
```

|||

#### 5. Modificar Los `div`

Modificarás cada `div` de forma individual.

##### `div.container`

- Modificá el ancho predeterminado al `80%`.
- Usá la propiedad `margin: 0 auto` para centrar el contenido.

|||

```css
 
 .container {
  width: 80%;
  margin: 0 auto;
}

```

|||

##### `div.datos-pedido`

- 🔍 Investigá cómo usar **Flexbox** para posicionar el recuadro con los `input`.

|||

```css
   .datos-pedido {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

```

|||

##### `div.confirmaciones`

Dale el siguiente formato:
  - Color de fondo blanco.
  - Color de texto `#1e2432`.
  - Un ancho de `50%`.
  - Un `border-radius` de `20px`.
  - Un `padding` de `12px`.
  - Una altura mínima de `180px`.
  - Usá la propiedad `margin: 0 auto` para centrar el contenido.
 
|||

```css
.confirmaciones {
      background-color: white;
      color: #1e2432;
      width: 50%;
      border-radius: 20px;
      padding: 12px;
      margin: 0 auto;
      min-height: 180px;
}

```

|||

##### `div.btn-container`

- 🔍 Investigá nuevamente cómo usar **Flexbox** para posicionar los botones.

|||
 
```css
.btn-container {
  display: flex;
  justify-content: center;
  text-align: center;
}
 
``` 

|||

¡Ya falta poco para terminar!

![homer-mountain.gif](https://media.giphy.com/media/l2Je9zHYveK012EVi/giphy.gif)

#### 6. Modificar La Lista De Confirmaciones De Pedidos

Primero, dale al `ul` el siguiente formato:
  - Un `margin` y `padding` `0`.
  - Alineación a la izquierda.
  - Un `text-decoration` y `list-style` `none`.

|||

```css
ul {
  margin: 0;
  padding: 0;
  text-align: left;
  text-decoration: none;
  list-style: none;
}

```

|||

Luego, dale al `li` el siguiente formato:
  - Un margen de `12px`.
  - Un tamaño tipográfico de `16px`.
  - Alineación centrada.

||| 

```css

li {
  margin: 12px;
  font-size: 16px;
  text-align: center;
}

```

|||

Por último, agregá un tamaño `2em` a la tipografía del `h3`.

|||

```css

h3 {
  font-size: 2em;
}

```

|||

#### ¡Felicidades!

¡Terminaste tu proyecto!

![the-office-champagne.gif](https://media.giphy.com/media/mp1JYId8n0t3y/giphy.gif)

🚀 Ya estás list@ para tu siguiente desafío: La ***To Do List***.

---

### El Juego Del Buscaminas

Esta sección es para aquellas personas que quieran desafiarse más y buscan mejorar sus _skills_ como _developers_. Se trata de un Contenido Bonus.

👩🏻‍💻👨‍💻 La idea es que puedas profundizar en la **Programación Orientada a Objetos** a partir de la codificación de un juego: el famoso "Buscaminas".

Acá lo podés ver y recordar. Pero, atención: no quedará exactamente igual si te animás a programarlo.

![alt](https://www.freecodecamp.org/news/content/images/2022/04/minesweeper-mine.gif)

Además del mismo juego y de sus funcionalidad también podrás conocer un poco más sobre otro lenguaje de programación: Phyton. De esta forma, además de JavaScript, podés ampliar tus recursos para POO utilizando otros lenguajes.

¿Empezamos? Mirá el siguiente tutorial y seguí el paso a paso:

@youtube=OqbGRZx4xUc

Si te animaste a hacer el proyecto (y encima te salió) no dudes en subirlo a Discord. Será un gran aporte para toda la Comunidad de P5.

