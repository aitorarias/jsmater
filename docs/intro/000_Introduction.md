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

Lo importante es que está especie de tradución es conocida como **"code generation"** y su input es el **"Abstract Syntax Tree (AST)"**, que trata sobre algunos elementos nesteados que representan la estructura del programa. La estructura de este árbol, ocurre en el "parsing" (análisis) de la fase de compilación. Más sohre esto en: https://en.wikipedia.org/wiki/Abstract_syntax_tree

JavaScript es muy diferente a Java: "Java is to JavaScript as ham is to hamster". 

*When JavaScript was created, it initially had another name: “LiveScript”. But Java was very popular at that time, so it was decided that positioning a new language as a “younger brother” of Java would help. But as it evolved, JavaScript became a fully independent language with its own specification called ECMAScript, and now it has no relation to Java at all.*

A día de hoy, JavaScript puede ser ejecutado no sólo en el navegador, sino también en el servidor, o casi cualquier dispositivo tiene un *programa especial* llamado "the JavaScript engine", el cual los diferentes motores tienen diferentes "codenames". 

- V8 en Chrome y Opera
- SpiderMonkey en Firefox 
- Otros codenames como Trident and Chakra para diferentes versiones de IE, Microsoft Edge, Nitro y SquirelFish para Safari, etc. 

