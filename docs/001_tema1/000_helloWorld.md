# Hello World

El <script> tag contiene código JavaScript que se ejecuta automáticamente cuando el navegador procesa la etiqueta.

Marcado moderno
La etiqueta <script> tiene algunos atributos que son raramente usados hoy en día pero que todavía se pueden encontrar en el código antiguo:

El atributo type: <script type=...>
El antiguo estándar HTML, HTML4, requería que un script tuviera un tipo. Normalmente era type="texto/javascript". Ya no es necesario. Además, el moderno estándar HTML, HTML5, cambió totalmente el significado de este atributo. Ahora, se puede utilizar para módulos JavaScript. Pero ese es un tema avanzado; hablaremos de los módulos en otra parte del tutorial.

El atributo de idioma: <Lenguaje de script=...>
Este atributo estaba destinado a mostrar el lenguaje del script. Este atributo ya no tiene sentido porque JavaScript es el lenguaje por defecto. No hay necesidad de usarla.

Comentarios antes y después de los scripts.
En libros y guías realmente antiguos, puedes encontrar comentarios dentro de <script> tags, como este:

<script type="text/javascript"><!-- --
    ...
//----></script>
Este truco no se usa en JavaScript moderno. Estos comentarios ocultaban el código JavaScript de navegadores antiguos que no sabían cómo procesar la etiqueta <script>. Dado que los navegadores lanzados en los últimos 15 años no tienen este problema, este tipo de comentario puede ayudarle a identificar código realmente antiguo.