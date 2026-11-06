### Qué Son Los ***Loops*** En Programación Y Para Qué Nos Sirven

Los _Loops_ (en castellano, Bucles) son muy útiles. Sirven para repetir una tarea, una determinada cantidad de veces, hasta que se cumpla una condición dada de antemano. 

Mirá este video para aprender más:

<iframe width="600" height="355" src="https://www.youtube.com/embed/xHG_fHmA4Os" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=426866526-->

---

### ***While***

Como vimos en el video anterior, el `while` _Loop_ se parece a la declaración del `if...else` ya que ambos evalúan una condición y ejecutan un bloque de código. 

Sin embargo, el `while` _Loop_ lo re-evalúa **repetidas veces** y ejecuta su bloque de código hasta que la condición deja de ser verdadera. 

Para saber cómo usar el `while` _Loop_, mirá este video: 

<iframe width="600" height="355" src="https://www.youtube.com/embed/mzIdcwFOidU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=426869968-->

#### Sintaxis Del `while` Loop

```js
while(unaCondicion){
  //Ejecuta este código
  // Hace algo para que la condición eventualmente se deje de cumplir
}
```

⚠️ **Importante:** Este código se va a ejecutar siempre que el resultado sea `true`. Cuando la condición sea `false`, saldremos del bucle, evitando entrar en lo que se conoce como un **_Loop Infinito_**. 

Veamos un ejemplo: 

```js
let pasajero = 1
while(pasajero <= 20){
  console.log("Puede pasar, su asiento es el: " + pasajero)
  pasajero++
}
```

Con este código, podríamos cobrar el boleto a cada una de las 20 personas que estén en la fila, dejando pasar a quienes paguen, desde el primero hasta el último pasajero.


Probá en la consola el código y mirá el resultado. Analicemos qué sucede:

1. **Declaramos una Variable:** En este caso, la llamamos `pasajero` y le asignamos el valor _1_.

2. **Definimos el `while` y la condición que tiene que evaluar el programa:** "Mientras(`while`) la variable `pasajero` sea menor o igual a 20 (pasajero <= 20)...

3. **Dentro de las llaves(`{}`), ponemos el código que queremos que se ejecute siempre que la condición sea verdadera**. En este caso, que se muestre por consola si el pasajero puede pasar y cuál es su lugar.

4. **Antes de cerrar la llave, ponemos un código que modifica la Variable para que, eventualmente, la condición sea `false`**. En este caso, `pasajero++` incrementa en _1_ el valor de la Variable cada vez que se ejecuta. Esto hará que, eventualmente, `pasajero` sea mayor a 20 y que la condición sea falsa (saliendo del bucle). 

+++ ¿Qué Hace `++` Y `--`?

El **++** incrementa en una unidad el valor de la variable. En cambio, **--** la decrece. 

⚠️ **Importante:** En caso de querer incrementar de 2 en 2, por ejemplo, podés usar los operadores de esta forma:

```js

let count = 5
while(count <= 20){
  console.log("count es: "+count)
  count+=2
}
```


Aprendé más acerca de estos operadores en este [link](https://codeburst.io/javascript-increment-and-decrement-8c223858d5ed).

+++

## Otro Ejemplo Con El Bucle `while` Y El Diagrama De Flujo

Si todavía no te quedó del todo claro cómo opera un `while` _Loop_ y cuál es su diferencia respecto al `if...else`, mirá este video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/tyYiZSj95M0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--@vimeo=426877272-->


