# Estructura del código

Un punto y coma puede ser omitido siempre y cuando exista un salto de línea. Por ejemplo: 

```javascript 
alert('Hello')
alerto('World')
```
En este caso, JavaScript interpreta el salto de línea como un punto y coma implícito. Esto es conocido como un *"automatic semicolon insertion"*. 

En muchos de los casos, una nueva línea implica un punto y coma. Pero, en la mayoría de los casos, no signfica siempre. 

Hay muchos casso donde una nueva línea no implica un punto y coma, por ejemplo: 

```javascript
alert(3 + 
1
+ 20);
```

El código sale 24 porque JavaScript no inserta punto y coma aquí. Es intuitivamente obvio que si la línea termina con un más "+", entonces es una "expresión incompleta", por lo que no se requiere el punto y coma. Y en este caso eso funciona según lo previsto.

Pero hay situaciones en las que JavaScript "falla" al asumir un punto y coma en las que es realmente necesario.

## Ejemplo de error

Ejecutemos en el siguiente código: 

```javascript 
[1,2].forEach(alert)
```

todo va a funcionar perfectamente

```javascript
alert("There will be an error")

[1, 2].forEach(alert)
```
Ahora, sin embargo, el código va a romper en el último paso. 

Sin embargo, si  lo hacemos de esta manera, todo irá correcto: 

```javascript
alert("There will be an error")

[1, 2].forEach(alert)
```
Todo por el punto y coma escrito al final.

Ahora tenemos el mensaje "Todo bien ahora" seguido de 1 y 2.

El error en la variante no-semicolon ocurre porque JavaScript no asume un punto y coma antes de los corchetes [...].

Por lo tanto, dado que el punto y coma no se inserta automáticamente, el código del primer ejemplo se trata como una única sentencia. Así es como lo ve el motor:

```javascript
alert("There will be an error")[1, 2].forEach(alert)
```

## Comentarios 

A medida que pasa el tiempo, los programas se vuelven más y más complejos. Es necesario añadir comentarios que describan qué hace el código y por qué.
Los comentarios se pueden poner en cualquier lugar de un script. No afectan a su ejecución porque el motor simplemente las ignora.

Los comentarios de una línea comienzan con dos caracteres de barra oblicua //.
El resto de la línea es un comentario. Puede ocupar una línea completa propia o seguir una declaración.

Como aquí:

```javascript
// This comment occupies a line of its own
alert('Hello');

alert('World'); // This comment follows the statement
```
Los comentarios multilínea comienzan con una barra oblicua y un asterisco /* y terminan con un asterisco y una barra oblicua */.

Así:

```javascript
/* An example with two messages.
This is a multiline comment.
*/
alert('Hello');
alert('World');
```
Los comentarios nesteados no están permitidos: 


```javascript

 /*
  /* nested comment ?!? */
*/
alert( 'World' );
```

