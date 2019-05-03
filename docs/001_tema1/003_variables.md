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
