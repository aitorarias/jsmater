# Use strict 

El modo estricto de ECMAScript 5 es una forma de elegir una variante restringida de JavaScript, así implícitamente se deja de lado el "sloppy mode" (modo poco riguroso). El modo estricto no es sólo un subconjunto: intencionalmente tiene diferencia semántica del código normal. Los navegadores que no soportan el modo estricto ejecutarán el código con un comportamiento diferente a los que sí lo soportan, por lo tanto no confíes en el modo estricto sin antes hacer pruebas de sus características más relevantes. Modo estricto y no estricto pueden coexistir, por lo tanto el código puede transformarse a modo estricto incrementalmente.

El modo estricto tiene varios cambios en la semántica normal de JavaScript:

Elimina algunos errores silenciosos de JavaScript cambiándolos a que lancen errores.
Corrige errores que hacen difícil para los motores de JavaScript realizar optimizaciones: a veces, el código en modo estricto puede correr más rápido que un código idéntico pero no estricto.
Prohibe cierta sintaxis que probablemente sean definidas en futuras versiones de ECMAScript.

## ¿Por qué strict mode?

Se implementa para hacer tus programas o funciones seguir un operando estricto. Esto significa, los errores que han sido ignorados por el compilador, este nos lanzará mensajes de excepción. 

Así pues, cómo cambiamos nuestro modo de non-strict mode a strict? Simplemente añadimos el string "use strict" al pirncipio de nuestro programa o función, y listo, ya estamos en "strict mode". 

```javascript 
"use strict"; 
// Ahora estamos en modo estricto
```

Si tenemos en cuenta el ***scope**, cuando usamos "use strict" es también muy importante. No siempre es una buena opción usar el "use strict" siempre, por lo que pedirá de lo que nos pidan y los requirimientos del código. 

A propósito del scope, aquí un par de ejemplos: 

```javascript
"use strict"; 
// Ahora nuestro código está en modo strict mode
// TODO el programa sigue el modo estricto
function foo (){
    // definicion
    // sigue el modo estricto 
}
foo (); 
```

Pero, sin embargo: 

```javascript 
function foo (){
    "use strict"
    // definicion
    // sigue el modo estricto
    // pero solo afecta a la funcion (function scope)
}

foo(); 
```

Miremos diferentes escenarios, donde este simple cambio lo dice todo. 

``Una variable no será añadida al global/window object si no está declarada``


```javascript
// variables no declaradas no se añaden al window/global object 
testVariables = 'este variable no está declarada'
console.log(testVariable); 
console.log(window.testVariable); 

OUTPUT
esta variable no está declarada
esta variable no está declarada
```

Para evitar estos escenarios, vamos a probar con el modo estricto. Strict mode no permite el uso de variables las cuales no han sido declaradas. 

```javascript 

"use strict"; 

var myVal; // variable declarada
myVal=10; // variable no declarada
// un error en la escriutra puede causar un output no deseado, y además, 
// más dificil de localizar 
if(myVal!==10)console.log("desired output"); 

OUTPUT
ReferenceError: myVar is not defined at strict:4
```

También nos sirve para palabras reservadas: 

```javascript
"use strict"

var let = 10 

if(let===10)console.log("desired error"); 

OUTPUT

SyntaxError: Unexpected strict mode reserved word
```

Sin embargo, sin modo estricto: 

```javascript 

var let = 10 

if(let===10)console.log("desired error"); 

OUTPUT
desired error
```

Sin modo estricto, estamos autorizados a declarar una variable de nombre let la cual es una palabra reservada del ES6. Técnicamente esto nos debe lanzar un error de sintaxis, pero está ignorado por el compilador. Con el modo estricto, esto no pasa. 

El operador **delete** también nos da una clara versión del modo estricto. 

```javascript 
"use strict"; 

var myObj = {
    propertyOne:10, 
    propertyTwo: 20
    }; 
//sintaxis valida 
delete myObj.propertyTwo; 
console.log(myObj); 
```

Esto nos borra la propiedad dos del objecto, perfectamente válido. 

El operador **delete** no sirve para borrar una funcion, variable o argumento. Sin modo estricto: 

```javascript 
function foo(){
    console.log('ejecutando la funcion foo')
    // definicion
}
//sintaxis invalida
delete foo; 
foo(); 

OUTPUT
ejecutando la funcion foo
```

```javascript 
"use strict"
function foo(){
    console.log('ejecutando la funcion foo')
    // definicion
}
//sintaxis invalida
delete foo; 
foo(); 

OUTPUT
Uncaught SyntaxError 
```

En definitiva, **el modo estricto elimina errores silenciosos, lo que obligó a escribir un código mejor y no cometer errores.**
