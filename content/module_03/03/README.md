# Fundamentos de Flexbox y propiedades clave

## Reforzando conceptos: display y flujo de elementos

Antes de sumergirnos en Flexbox, recordemos cómo funcionan los tipos de display más comunes:

* __block__: Elementos que ocupan todo el ancho disponible y comienzan en una nueva línea.
* __inline__: Elementos que ocupan solo el espacio necesario y se colocan en línea con otros elementos.
* __inline-block__: Combina características de `inline` y `block`, permitiendo definir dimensiones pero manteniendo el flujo en línea.

Estos tipos determinan cómo los elementos se posicionan y afectan el flujo del documento.

## Introducción a Flexbox

Flexbox es un modelo de layout unidimensional que facilita la distribución de espacio y alineación de elementos dentro de un contenedor flexible.

> __Definición clave__: Un __contenedor flex__ es un elemento cuyo `display` está configurado como `flex` o `inline-flex`. Los elementos hijos de este contenedor se llaman __ítems flex__.

### Propiedades principales del contenedor flex

| Propiedad | Descripción |
| --------- | ----------- |
| `display: flex` | Activa el modo flex para el contenedor, haciendo que sus hijos sean ítems flex. |
| `flex-direction` | Define la dirección principal del layout: `row` (horizontal), `column` (vertical), etc. |
| `justify-content` | Alinea los ítems `flex` a lo largo del eje principal (por ejemplo, izquierda, centro, espacio). |
| `align-items` | Alinea los ítems `flex` a lo largo del eje transversal (por ejemplo, arriba, centro, abajo). |
| `gap` | Define el espacio entre los ítems `flex`, facilitando separación sin márgenes manuales. |

### `flex-wrap`

Permite definir si los ítems deben ajustarse automáticamente a una nueva línea cuando el contenedor no tiene suficiente espacio.

Valores: `nowrap` (por defecto), `wrap`, `wrap-reverse`.

#### Ejemplo básico de contenedor flex

```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 10px;
}
```

Este código crea un contenedor donde los ítems se distribuyen horizontalmente, centrados tanto en el eje principal como en el transversal, con un espacio de `10px` entre ellos.

### Relación entre contenedor e ítems flex

Los ítems `flex` responden a las propiedades del contenedor para adaptarse y distribuirse eficientemente. Por ejemplo, si el contenedor tiene `justify-content: space-between`, los ítems se separarán uniformemente a lo largo del eje principal.

Los ítems también pueden tener propiedades propias como:

* `flex-grow`: cuánto espacio extra pueden ocupar
* `flex-shrink`: cómo se reducen cuando falta espacio
* `flex-basis`: tamaño inicial del ítem

Esto forma la abreviatura:

```css
flex: grow shrink basis;
```

> __Nota__: Flexbox es un modelo unidimensional, lo que significa que controla la distribución en una sola dirección a la vez, a diferencia de modelos bidimensionales como Grid.

[Video del contenido](https://vimeo.com/1140411118/48c613b85b?fl=pl&fe=cm)
