# Selectores, especificidad y herencia

## Selectores CSS: la puerta de entrada para aplicar estilos

Los __selectores__ son patrones que nos permiten elegir elementos HTML para aplicarles estilos. Los tipos básicos que veremos son:

* __Selector por etiqueta (tipo)__: selecciona todos los elementos de una etiqueta específica.
  * Ejemplo: `p` selecciona todos los párrafos.
* __Selector por clase__: selecciona elementos que tienen una clase específica.
  * Ejemplo: `.destacado` selecciona todos los elementos con clase "destacado".
* __Selector por ID__: selecciona un elemento único con un identificador específico.
  * Ejemplo: `#menu` selecciona el elemento con id "menu".
* __Selector por atributo__: selecciona elementos que tienen un atributo o valor específico.
  * Ejemplo: `[type="text"]` selecciona todos los inputs de tipo texto.

### Nueva aclaración útil para principiantes

Los IDs deben usarse solo cuando realmente se necesite algo único. En el desarrollo moderno, la mayoría de los estilos se aplican usando clases, no IDs.

## Combinadores

* __Combinadores__: permiten seleccionar elementos en relación con otros.
  * Descendiente: `div p` selecciona todos los `p` dentro de un `div`.
  * Hijo directo: `ul > li` selecciona los `li` hijos directos de un `ul`.
  * Adyacente: `h1 + p` selecciona el `p` que sigue inmediatamente a un `h1`.

## Cascada, herencia y especificidad: ¿qué regla gana?

Cuando múltiples reglas CSS apuntan al mismo elemento, el navegador sigue estas reglas para decidir cuál aplicar:

* __Importancia__: reglas con `!important` tienen prioridad máxima (pero su uso debe evitarse).
* __Especificidad__: se calcula según el tipo de selector:

  | Selector                                | Puntos de especificidad |
  | --------------------------------------- | ----------------------- |
  | Inline styles                           | 1000                    |
  | ID selectors (#id)                      | 100                     |
  | Class, atributo, pseudo-clase selectors | 10                      |
  | Elemento, pseudo-elemento selectors     | 1                       |

  > __Regla práctica__: suma los puntos de cada selector; gana el que tenga mayor puntaje.

* __Orden de aparición__: si la especificidad es igual, gana la regla que aparece después en el CSS.

## Herencia

Algunas propiedades CSS se heredan automáticamente de los elementos padre a los hijos, como `color` y `font-family`. Otras, como `margin` o `border`, no se heredan.

> __Ejemplo__: si defines `color: blue` en el `body`, los textos dentro heredarán ese color a menos que se sobrescriba.

## Buenas prácticas para organizar y mantener tu CSS

* Usa nombres de clases significativos y consistentes para facilitar la lectura.
* Evita abusar de selectores ID para no complicar la especificidad, se prioriza siempre el uso de clases.
* __No uses__ `!important` salvo casos muy justificados.
* Separa responsabilidades: estilos generales, componentes y utilidades en bloques claros.
* Comenta tu código para explicar decisiones complejas.

> Mantener un CSS limpio y organizado facilita la colaboración y el mantenimiento a largo plazo.
