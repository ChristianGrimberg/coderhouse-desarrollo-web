# Unidades, color y tipografía

## Color, tipografía y fondos

### Color

CSS permite definir colores con varios formatos:

* __Hexadecimal__: `#RRGGBB` (ejemplo: `#3498db`)
* __RGB__: `rgb(52, 152, 219)`
* __HSL__: `hsl(204, 70%, 53%)`

> __Consejo__: Usa colores con buen contraste para mejorar la accesibilidad.

### Tipografía

Las propiedades básicas para controlar la tipografía son:

* `font-family`: define la fuente tipográfica, por ejemplo, `'Arial', sans-serif`.
* `font-size`: tamaño de la fuente, preferiblemente en `rem` para escalabilidad.
* `line-height`: altura de línea para mejorar la legibilidad.

Puedes incorporar fuentes externas usando [Google Fonts](https://fonts.google.com/), lo que amplía las opciones de diseño.

### Fondos

La propiedad `background` permite definir color de fondo, imágenes, posición y repetición.

```css
body {
  background-color: #f0f0f0;
  background-image: url('fondo.png');
  background-repeat: no-repeat;
  background-position: center;
}
```

> __Recuerda__: Un buen uso del color y la tipografía mejora la experiencia del usuario y la coherencia visual de tu sitio.

## Unidades de medida en CSS

Para definir tamaños y espacios, CSS ofrece diferentes unidades:

| Unidad | Descripción | Uso común |
| ------ | ----------- | --------- |
| `px` | Píxeles, unidad absoluta | Tamaños fijos, precisión en pantallas estándar |
| `em` | Relativa al tamaño de fuente del elemento padre | Escalabilidad en tipografía y espacios relacionados |
| `rem` | Relativa al tamaño de fuente raíz (`<html>`) | Consistencia en tamaños relativos en toda la página |
| `%` | Porcentaje relativo al elemento contenedor | Layouts fluidos y adaptativos |
| `vw` | 1% del ancho de la ventana gráfica | Diseño responsivo basado en ancho de pantalla |
| `vh` | 1% de la altura de la ventana gráfica | Altura adaptable según pantalla |

### ¿Cuándo usar unidades relativas o absolutas?

* Usa `px` para elementos que requieren precisión y no deben escalar.
* Prefiere `rem` para tipografía para mantener consistencia y accesibilidad.
* Usa `%`, `vw`, `vh` para layouts flexibles y responsivos.
