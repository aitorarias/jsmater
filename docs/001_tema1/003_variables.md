# Variables 

La mayoría de las veces, una aplicación JavaScript necesita trabajar con información. Dos ejemplos: 

1. Una tienda online - la información incluye los bienes que se venden y un carro de la compra 
2. Un chat - la información incluye usuario, mensajes y mucho más

En definitiva, las variables las utilizamos para almacenar información: 

## Una variable

Una variable es un "named storage" para los datos. Podemos utilizar una variable para almacenar cualquier dato. 

Para crear una variable en Js, usamos ``let``. 

A continuación, creamos una variable llamada mensaje:

```javascript
let mensaje; 
```

Ahora, podemos almacenar información a esa variable usando el = 

```javascript 
let mensaje; 
mensaje = 'Hola'; // almacena el string 'Hola'
```
El string ahora está guardado dentro de la memoria asociada a la variable. Podemos acceder usando el nombre de la variable. 

```javascript 
let mensaje;
mensaje = 'Hola'; 

alert(mensaje);
```
Podemos combiar estas dos líneas y ponerlas en una única línea 

```javascript 
let mensaje = 'Hola'; 
alert(mensaje); 
```
Podemos establecer varias variables en una única línea 

```javascript 
let user = 'John', age = 25, message = 'Hello';
```

Esto podemos hacerlo, pero no lo recomendamos, por temas de legibilidad. De lo contrario, podemos hacerlo en varias líneas: 

```javascript 
let user = 'John', 
    age = 25, 
    message = 'Hello';
```

También podremos observar la presencia del ``var`` en algún repositorio o proyecto. Este hace lo mismo que let, pero de una manera ligeramente diferente. Lo veremos próximamente. 

## Una anología 

Imaginemos la variable como una caja para los datos, con un único nombre dentro. 
Por ejemplo, la variable message puede ser imaginada como una caja llamada "message" con el valor de "Hello!" dentro de ella. 

![Variable ejemplo](../../img/variable.png)

Podemos poner cualquier valor dentro de la caja . 

Podemos cambiarla tantas veces como queramos: 

```javascript
let message; 

message = 'Hello"'; 

message = 'World'; // valor cambiado

alert (message);
```

Cuando cambiamos este valor, los antiguos datos son eliminados por la variable: 

![Variable ejemplo](../../img/variable-change.png)

También podemos declarar dos variables y copiar los datos de una dentro de otra: 

```javascript 

let hello = 'Hola Mundo'; 

let message; 

// copia "Hola Mundo" de la variable hello en message; 

message = hello; 

// ahora las dos variables almacenan los mismos datos 

alert(hello); 
alert(message); 