**UNIVERSIDAD NACIONAL DEL CENTRO DEL PERÚ**

<img width="400" height="350" src="https://upload.wikimedia.org/wikipedia/commons/9/92/Escudo_UNCP.png" />

**FACULTAD DE INGENIERÍA DE SISTEMAS**

**DESARROLLO DE APLICACIONES WEB**

**Conocimientos avanzados del lenguaje de diseño CSS**

**PRESENTADO POR:**

Cerrón Pizarro Sebastián José

Huaire Maravi Edison Orlando

Huaman Huaynatez Jean Franco

Janampa Choccelahua Gian Alessandro

Mateo Cabello Raúl Julián

Ramirez Buitrón Kenyo Wilder

**HUANCAYO -- PERÚ**

**2025**

# ÍNDICE

#  {#section .TOC-Heading}

[ÍNDICE [2](#índice)](#índice)

[INTRODUCCIÓN [3](#introducción)](#introducción)

[CAPITULO 1 [4](#capitulo-1)](#capitulo-1)

[CAPITULO 2 [5](#_Toc207475039)](#_Toc207475039)

[CAPITULO 3 [6](#_Toc207475040)](#_Toc207475040)

[CAPITULO 4 [7](#_Toc207475041)](#_Toc207475041)

[CAPITULO 5 [8](#_Toc207475042)](#_Toc207475042)

[CAPITULO 6 [9](#_Toc207475043)](#_Toc207475043)

[CAPITULO 7 [10](#_Toc207475044)](#_Toc207475044)

[CAPITULO 8 [11](#_Toc207475045)](#_Toc207475045)

[CAPITULO 9 [12](#_Toc207475046)](#_Toc207475046)

[CAPITULO 10 [13](#_Toc207475047)](#_Toc207475047)

[CONCLUSIÓN [14](#_Toc207475048)](#_Toc207475048)

[REFERENCIA BIBLIOGRÁFICA [15](#_Toc207475049)](#_Toc207475049)

# INTRODUCCIÓN

La siguiente monografía profundiza el tema del lenguaje de diseño CSS,
conocido como Cascading Style Sheets, la cual aplicar estilos a
documentos, en su mayoría documentos HTML. Este lenguaje permite que la
información de los documentos HTML tenga un aspecto que sea organizado,
llamativo e interesante para los usuarios añadiendo el diseño de los
bloques, los colores de las letras o fondos de los bloques, las formas
que pueden tomar algunos bloques, entre otras funciones (Manz, s. f.).
Por la funcionalidad que tiene este lenguaje, es muy importante para un
desarrollador de páginas web el tener conocimientos sobre CSS al ser un
tema fundamental para las páginas web.

Por lo tanto, se tiene como objetivo el conocer temas más avanzados
relacionados con CSS. Para ello se buscará información de fuentes
fiables para los temas seleccionados que se mostrarán en los capítulos
para luego mostrar ejemplos aplicables de los temas utilizando códigos y
sus resultados.

Esta investigación resulta pertinente debido al aumento de la
importancia de las páginas web en la actualidad, ya que para las
organizaciones al intentar captar la atención de los usuarios buscan que
su página web, aparte que tenga la información relevante sobre ellos,
también buscan que sea llamativo, atractivo y tenga una buena
optimización de rendimiento, por lo cual beneficia a las organizaciones
utilizar CSS. También es importante para el aspecto académico, ya que,
al ser importante para las organizaciones, es muy demandado por el
mercado laboral, la cual servirá para los front-end, diseñadores
gráficos y especialistas en experiencia de usuario.

El tipo de esta investigación será de Investigación documental y
descriptiva, ya que se buscará información revisando documentos,
artículos, cursos y recursos web especializados. también es exploratoria
ya que busca profundizar en temas avanzas relacionados con CSS.

# CAPITULO 1

Variables CSS y Custom Properties

Ambos términos representan lo mismo, el Custom Properties es la forma
oficial de decirle a las variables, el término fue dado por W3C, la cual
es una organización internacional que desarrolla los estándares y
directrices para la web (World Wide Web Consortium, s. f.). Las
variables se consideran como un mecanismo que sirve personalizar las
propiedades CSS, se usa para evitar escribir un valor en varias
ocasiones. Permitiendo que sea fácil de entender y de configurar (Manz,
s. f.).

Para declarar una propiedad personalizada, primero se crea la clase,
luego se escribe dos guiones ( - ), después el nombre de la variable y
al final un valor admitido en CSS. Para admitir una variable de manera
global al documento html se utiliza el pseudo-clase ":root". Para el uso
de la variable, se escoge la clase que tendra esta variable, luego de
poner el nombre de la propiedad, se coloca "var()" y dentro del
paréntesis se pone el nombre de la variable.

+-----------------------------------------------------------------------+
| :root {                                                               |
|                                                                       |
| \--background-color: yellow;                                          |
|                                                                       |
| }                                                                     |
|                                                                       |
| body {                                                                |
|                                                                       |
| background: var(\--background-color);                                 |
|                                                                       |
| }                                                                     |
+=======================================================================+
+-----------------------------------------------------------------------+

Una característica que tiene la función var() es que se puede escoger
una opción de respaldo si en el caso de la variable que ingresaste
dentro del paréntesis aun no ha sido definida. A esta alternativa se le
conoce como Fallback, Si se desea que la opción de respaldo también sea
una variable, se ingresa otra función var() y luego su variable.

+-----------------------------------------------------------------------+
| **Primer Código**                                                     |
|                                                                       |
| body {                                                                |
|                                                                       |
| background: var(\--background-color, green);                          |
|                                                                       |
| }                                                                     |
+=======================================================================+
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| **Segundo Código**                                                    |
|                                                                       |
| body{                                                                 |
|                                                                       |
| background-color: var( \--my-var, var(\--my-background, pink) );      |
|                                                                       |
| }                                                                     |
+=======================================================================+
+-----------------------------------------------------------------------+

Se puede utilizar :root para hacer de manera global, pero también se
puede hacer de manera local, utilizando una clase padre.

+-----------------------------------------------------------------------+
| **Código CSS**                                                        |
|                                                                       |
| .parent {                                                             |
|                                                                       |
|   \--background-color: black;                                         |
|                                                                       |
|   background: indigo;                                                 |
|                                                                       |
|   padding: 1rem;                                                      |
|                                                                       |
|   display: flex;                                                      |
|                                                                       |
|   gap: 1rem;                                                          |
|                                                                       |
| }                                                                     |
|                                                                       |
| .child {                                                              |
|                                                                       |
|   width: 100px;                                                       |
|                                                                       |
|   height: 100px;                                                      |
|                                                                       |
|   background: var(\--background-color);                               |
|                                                                       |
| }                                                                     |
|                                                                       |
| .first {                                                              |
|                                                                       |
|   \--background-color: gold;                                          |
|                                                                       |
| }                                                                     |
+=======================================================================+
+-----------------------------------------------------------------------+

Como se muestra, en la clase parent se tiene una variable, para
utilizarlas en las demás clases, estas tienen que estar dentro de la
clase en el codigo HTML.

+-----------------------------------------------------------------------+
| **Código HTML**                                                       |
|                                                                       |
| \<div class=\"parent\"\>                                              |
|                                                                       |
| \<div class=\"first child\"\>First child\</div\>                      |
|                                                                       |
| \<div class=\"second child\"\>Second child\</div\>                    |
|                                                                       |
| \<div class=\"third child\"\>Third child\</div\>                      |
|                                                                       |
| \</div\>                                                              |
+=======================================================================+
+-----------------------------------------------------------------------+

Como se muestra en el código, al estar dentro de la clase "parent",
puede utilizar la variable que tiene su clase padre. En el caso de la
clase "firts" se priorizará su variable, cambiando de blanco a negro.

**Ventajas**

-   Reutilización de código: permite aplicar el mismo valor en múltiples
    lugares sin repetirlo.

-   Facilidad de mantenimiento: un cambio en la variable se refleja
    automáticamente en todos los elementos donde fue utilizada.

-   Diseños dinámicos: posibilitan cambiar estilos de forma más sencilla
    en proyectos grandes.

-   Compatibilidad con JavaScript: se pueden modificar en tiempo real,
    favoreciendo la construcción de interfaces interactivas.
