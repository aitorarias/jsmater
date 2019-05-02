# ¿Qué es JavaScript?

JavaScript fue creado para mantener las páginas web *vivas*, siendo éste un lenguaje interpretado, no compilado. Programas como C++ o Java necesitan ser compilados antes de ser ejecutados. El código fuente es pasado a través de un programa llamado compilador, el cual traduce al bytecode lo que la máquina entiende y puede ejecutar (Fuente | University of Standford) 

Los programas en este lenguaje son llamados **scripts**. Estos scripts pueden estar escritos en una página HTML y ser ejecutados automáticamente cuando la página carga.

Los **scripts son ejecutados como un texto plano (plain text). Estos no necesitan de una preparación especial o compilación para ejecutarlos**

Según Fabio Russo, existe aún mucha discrepancia o ambigüedad en referencia a **qué es exactamente Js** (Fuente: https://dev.to/genta/is-javascript-a-compiled-language-20mf).

¿Por qué la gente sigue viendo a JS como un dinámico o interpretado lenguaje?. 

Existe una idea equivocada a cerca de la **compliación de JS**, y todavía ahora, con toda la información que disponemos en la web, la mayoría de la gente argumenta que todavía no se sabe cómo funciona exactamente JS antes de la *runtime phase*

Según la Wikipedia: 

``A compiler is computer software that transforms computer code written in one programming language (the source language) into another programming language (the target language).
Un compilador es un programa informático que transforma el código de la computadora en el lenguaje de programación que hayamos elegido, en otro lenguaje de programación (el lenguaje objetivo)
``

Contradiciendo a la Universidad de Stanford, Fabio Russo sostiene que JavaScript es un lenguaje compilado a pesar del hecho que la *compilación de JS funciona de una manera diferente a la establecida*, ya que sigue unas ciertas normas de compilación que se reflejan en dicho proceso. 

Todos sabemos que los ordenadores no **hablan** Java o Phyton y no les importa qué lenguaje estemos utilizando, nosotros siempre "traducimos" nuestro código en algo en el que la máquina lo pueda entender. 

Lo importante es que está especie de tradución es conocida como **"code generation"** y su input es el **"Abstract Syntax Tree (AST)"**, que trata sobre algunos elementos nesteados que representan la estructura del programa. La estructura de este árbol, ocurre en el "parsing" (análisis) de la fase de compilación. Más sobre esto en: https://en.wikipedia.org/wiki/Abstract_syntax_tree

JavaScript es muy diferente a Java: "Java is to JavaScript as ham is to hamster". 

*When JavaScript was created, it initially had another name: “LiveScript”. But Java was very popular at that time, so it was decided that positioning a new language as a “younger brother” of Java would help. But as it evolved, JavaScript became a fully independent language with its own specification called ECMAScript, and now it has no relation to Java at all.*

A día de hoy, JavaScript puede ser ejecutado no sólo en el navegador, sino también en el servidor, o casi cualquier dispositivo tiene un *programa especial* llamado "the JavaScript engine", el cual los diferentes motores tienen diferentes "codenames". 

- V8 en Chrome y Opera
- SpiderMonkey en Firefox 
- Otros codenames como Trident and Chakra para diferentes versiones de IE, Microsoft Edge, Nitro y SquirelFish para Safari, etc. 

## ¿Cómo funciona un motor?

A pesar de la complejidad que conlleva un motor, estos son básicamente los pasos que sigue: 

1. El motor (incrustrado si hablamos de un navegador) lee ("analiza", "parses") el script
2. Después lo convierte ("compila", "compiles") el script al lenguaje de máquina. 
3. Y después el *"machine code"* corre, muy muy rápido. 

## ¿Qué puede hacer Javascript en el navegador?

Las últimas actualizaciones de Js hacen de este un lenguaje "seguro". No proporciona acceso de bajo nivel a la memoria o la CPU, ya que fue creado inicialmente para navegadores que no lo requieren. 

Las capacidades de JavaScript dependen en gran medida del entorno en el que se ejecuta. Por ejemplo, Node.js soporta funciones que permiten a JavaScript leer/escribir archivos arbitrarios, realizar peticiones de red, etc.

En el navegador, JS puede hacer todo lo relacionado con la manipulación o edición de la web: interacción con el usuario y el webserver. 

Además, Js está capacitado para: 

1. Agregar nuevo HTML a la página, cambiar el contenido existente, modificar estilos.
2. Reacciona a las acciones del usuario, ejecuta clics del ratón, movimientos del puntero, pulsaciones de teclas.
3. Enviar peticiones a través de la red a servidores remotos, descargar y cargar archivos (las llamadas tecnologías AJAX y COMET).
4. Obtener y establecer cookies, hacer preguntas al visitante, mostrar mensajes.
5. Retiene los datos en el lado del cliente ("almacenamiento local", "local storage").

## ¿Qué NO puede hacer Javascript en el navegador?

Las capacidades de JavaScript en el navegador están limitadas por el bien de la seguridad del usuario. El objetivo es evitar que una página web malintencionada acceda a información privada o perjudique los datos del usuario.

Ejemplos de tales restricciones incluyen:

1. Es posible que JavaScript en una página web no pueda leer/escribir archivos arbitrarios en el disco duro, copiarlos o ejecutar programas. No tiene acceso directo a las funciones del sistema operativo.

2. Los navegadores modernos te permiten trabajar con archivos, pero el acceso es limitado y sólo se proporciona si el usuario realiza determinadas acciones, como "soltar" un archivo en una ventana del navegador o seleccionarlo mediante una etiqueta <input>.

3. Hay formas de interactuar con la cámara/micrófono y otros dispositivos, pero requieren el permiso explícito del usuario. Por lo tanto, es posible que una página habilitada para JavaScript no habilite sigilosamente una cámara web, observe el entorno y envíe la información a la NSA.

4. Las diferentes pestañas/ventanas generalmente no se conocen entre sí. A veces lo hacen, por ejemplo cuando una ventana utiliza JavaScript para abrir la otra. Pero incluso en este caso, es posible que JavaScript de una página no pueda acceder a la otra si provienen de sitios diferentes (de un dominio, protocolo o puerto diferente.

Esto se denomina "Política de Mismos Origen". Para evitarlo, ambas páginas deben contener un código JavaScript especial que se encargue del intercambio de datos.

Esta limitación es, una vez más, para la seguridad del usuario. Una página de http://anysite.com que un usuario haya abierto no debe poder acceder a otra pestaña del navegador con la URL http://gmail.com y robar información de allí.

5. JavaScript puede comunicarse fácilmente a través de la red con el servidor de donde proviene la página actual. Pero su capacidad para recibir datos de otros sitios/dominios está paralizada. Aunque es posible, requiere un acuerdo explícito (expresado en cabeceras HTTP) desde el lado remoto. Una vez más, es una limitación de seguridad.

## Lenguajes "sobre" Javascript

La sintaxis de Javascript no se adapta a las necesidades de todos. Así que han ido apareciendo otros lenguajes, o más bien convertidos de Js. Ejemplos como: 

1. CoffeeScript, el cual introduce sintaxis más corta, permitiendo escribir un claro y precio código. Usualmente, los desarrolladores de Ruby apruban este lenguaje. 

2. TypeScript basado en añadir "strict data typing" para simplificar el desarrollo y dar soporte a sistemas complejos. Desarrollado por Microsoft. 

3. Dart es un lenguaje independiente que tiene su propio motor que funciona en entornos que no son navegadores (como las aplicaciones móviles). Inicialmente fue ofrecido por Google como un reemplazo de JavaScript, pero a partir de ahora, los navegadores requieren que sea transpuesto a JavaScript como los otros dos.

## En resumen 

JavaScript fue creado inicialmente como un lenguaje sólo para navegadores, pero ahora también se utiliza en muchos otros entornos.
Hoy en día, JavaScript tiene una posición única como el lenguaje de navegación más ampliamente adoptado con plena integración con HTML/CSS.
Hay muchos lenguajes que se "transponen" a JavaScript y proporcionan ciertas características.