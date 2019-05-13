# Data types 

Una variable en Javascript puede contener datos. Una variable puede ser en un momento un string, y en otro momento, un number. 

```javascript 
let message = "hello"; 
message = 123456; 
```

Los lenguajes de programación que nos permiten esto son conocidos como **dynamically typed**, lo que significa que hay data types, pero las variables no están vinculadas a ninguno de ellos. 

Hay siete data types básicos en JS. 

## Number 

El number type representa los numeros enteros y decimales. 

Existen múltiples operaciones para los números, por ejemplo, multiplicación, división, suma, resta y demás.

Además de los números regulares, tenemos los llamados "special numeric values" el cual pertenece a este data type: `Infinity`, `-Infinity` y `NaN`. 

- Infinity representa el número infinito. 
- NaN representa un error de computación. Es el resultado de un incorrecto o indefinida operación matemática, por ejemplo: 

```javascript
alert( "not a number" / 2 ); // NaN, such division is erroneous

or 

alert( "not a number" / 2 + 5 ); // NaN
```

Si NaN está en algún lado, se propagará en todo el resultado. 

```
Mathematical operations are safe
Doing maths is “safe” in JavaScript. We can do anything: divide by zero, treat non-numeric strings as numbers, etc.
The script will never stop with a fatal error (“die”). At worst, we’ll get NaN as the result.
```

## String

Un string en Javascript siempre ha de contener quotes: 

```javascript
let str = "Hello";
let str2 = 'Single quotes are ok too';
let phrase = `can embed ${str}`; 
```
En Js tenemos tres tipos de citas: 

1. Double quotes: "Hello"
2. Single quotes: 'Hello'
3. Backticks: `Hello`

Doubles y single quotes son quotes sencillas. No existe diferencia entre ellas. 

Backtickts tienen una **funcionalidad extendida**. Nos permiten inscrutar variables y expresiones dentro de un string agrupandolo con ${...}, por ejemplo: 

```javascript
let name = 'Aitor'; 
const yearOfBirth = 1993; 

console.log (`El nombre de esta persona es ${name} y su año de nacimiento fue en ${yearOfBirth}`); 

// OUTPUT
El nombre de esta persona es Aitor y su año de nacimiento fue en 1993
```
La expresion dentro de ${...} es evaluada y el resultado se convierte en parte del string. Podemos poner cualquier cosa que queramos: un variable llamada `name` o una expresión aritmética `1+2` o algo más complejo. 

Por favor, tengamos en cuenta que esto es sólo posible con los backticks. Con las double o singles quoutes el resultado sería el siguietne: 

```javascript 
alert( "the result is ${1 + 2}" ); // the result is ${1 + 2} (double quotes do nothing)
```

```
There is no character type.
In some languages, there is a special “character” type for a single character. For example, in the C language and in Java it is char.

In JavaScript, there is no such type. There’s only one type: string. A string may consist of only one character or many of them.
```

## Boolean (logic type)

El boolean puede tener dos valores: `true` o `false`. 

Este type es comunmenete utilizado para almacenar si/no valores. `true` siginifica "sí, es correcto" y `false` significa "no, no es correcto". 

```javascript 
let nameFieldChecked = true; // yes, name field is checked
let ageFieldChecked = false; // no, age field is not checked
```

Los valores booleanos también vienen como un resultado de comparaciones: 

```javascript
let isGreater = 4 > 1;

alert( isGreater ); // true (the comparison result is "yes")
```

## El valor "null"

El valor especial `null` no pertenece a ningún tipo descrito anteriormente. 

```javascript
let age = null;
```

En JavaScript, null no es una "referencia a un objeto inexistente" o un "puntero nulo" como en otros lenguajes.

Es sólo un valor especial que representa "nada", "vacío" o "valor desconocido".

El código anterior indica que la edad es desconocida o está vacía por alguna razón.

## Undefined

El valor especial `undefined` también se mantiene aparte, como null. Es un type propio. 

El significado de undefined es "valor no asignado"

Si una variable es declarada, pero no asignada, entonces su valor es indefenido. 

```javascript
let x;

alert(x); // shows "undefined"
```

Técnicamente, podemos asignar un `undefined` a una variable.

```javascript
let number = 123; 

number = undefined; 

console.log(number);
```

**No es en absoluto recomendable que hagamos esto. Normalmente, usamos null para asignar un "empty" o "unknown" valor a una variable, y usamos undefined para checkear si una varible ha sido asignada**

## Objects y Symbols

El `object` type es especial. 

Todos los demás types son llamados **primitivos** porque sus valores pueden contener un único valor (string, número o lo que sea). En contraste, los objetos son utilizados para **almacenar una colección de datos y entidades más complejas**. 

El `symbol` type es usado para crear únicos identificadores para los objectos. 

## El operador typeof

El operador `typeof` devuelve el tipo del argumento. Es útil cuando queremos procesar valores para los diferentes tipos o queremos hacer un rápido check. 

Soporta dos formas de sintaxis: 

1. Como un operador: typeof 
2. Como una función: typeof(x)

La llamada a typeof x nos devuelve un string explicandonos el tipo: 

```javascript 

typeof undefined // "undefined"

typeof 0 // "number"

typeof true // "boolean"

typeof "foo" // "string"

typeof Symbol("id") // "symbol"

typeof Math // "object"  (1)

typeof null // "object"  (2)

typeof alert // "function"  (3)
```

Los últimos tres valores necesitan una explicación adicional: 

1. `Math` es un objecto que provee operaciones matemáticas. 
2. El resultado de `typeof null` nos da "object". Obviamente no lo es, esto es un error reconocido en JavaScript. 
3. El resultado de `typeof alert` es `function` porque `alert` es una función del lenguaje. Funciones permanecen al object type, pero typeof los trata de forma diferente. Formalmenete es incorrecto, pero conveniente en la práctica. 

## En resumen 

Hay siete tipos de datos básicos: 

1. `number` para los números de todo tipo: integer o floating-point
2. `string` para strings. Un string puede tener un o más caracteres, y tampoco hay single-character (char) type.
3. `boolean` para `true/false`
4. `null` para valores desconocidos, un tipo autónomo que tiene un valor null. 
5. `object` para estructuras de datos más complejas
6. symbol para identificadores unicos
7. `undefined` para valores no asignados, un valor autonomo que devuelve undefined.

El operador typeof nos permite ver que tipo está almacenado en una variable:

- Dos formas: typeof o typeof(x)
- Nos devuelve un string con el nombre del type, como "string"
- Para null nos devuelve "object". esto es un error del lenguaje. 


