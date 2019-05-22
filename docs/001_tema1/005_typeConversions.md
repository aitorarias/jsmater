# Type Conversions 

La mayoría de las veces, operadores y funciones son convertidas automáticamente, dados los valores, al correcto type.

Por ejemplo, `alert` automáticamente convierte cualquier valor a string para mostrarlo. Operaciones matemáticas convierten los valores a números. 

## ToString 

Las conversiones a `string` aparecen cuando necesitamos un string desde un valor. 

Por ejemplo, `alert(value)` lo hace para enseñar el valor. 

Podemos, tambien, llamar a la función `String(value)` para convertirla a un String. 

```javascript
let valor = true; 
valor=String(value); 
alert(typeof(valor));
```

## ToNumber

Las conversiones a números aparecen en las funciones matemáticas de manera automática. 

Por ejemplo, cuando la division / es aplicada a no-numeros:

```javascript 
let numero = "981"
alert(typeof(numero));
//OUTPUT => string
numero=Number(numero)
alert(typeof(numero));
//OUTPUT => numero
```
Las conversiones explícitas están usualmente requeridas cuando leemos 
