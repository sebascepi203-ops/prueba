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

Compatibilidad con JavaScript: se pueden modificar en tiempo real,
favoreciendo la construcción de interfaces interactivas.
