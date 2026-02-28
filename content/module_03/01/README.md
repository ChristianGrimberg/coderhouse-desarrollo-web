# Introducción al Box Model

## ¿Qué es el Box Model en CSS?

El __Box Model__ es un modelo que describe cómo se calculan las dimensiones y el espacio que ocupa cada elemento en una página web. Cada elemento se representa como una caja rectangular compuesta por cuatro áreas:

* __Content (Contenido)__: Es el área donde se muestra el texto, imágenes u otros elementos.
* __Padding (Relleno)__: Espacio entre el contenido y el borde. Aumenta el área interna sin afectar el tamaño del contenido.
* __Border (Borde)__: Línea que rodea el padding y el contenido. Puede tener grosor, color y estilo.
* __Margin (Margen)__: Espacio externo que separa la caja de otros elementos.

### Visualización del Box Model

```plaintext
+-----------------------------+
|          Margin             |
|  +-----------------------+  |
|  |        Border         |  |
|  |  +-----------------+  |  |
|  |  |     Padding     |  |  |
|  |  |  +-----------+  |  |  |
|  |  |  | Content   |  |  |  |
|  |  |  +-----------+  |  |  |
|  |  +-----------------+  |  |
|  +-----------------------+  |
+-----------------------------+
```

Cada una de estas áreas afecta cómo se ve y se posiciona el elemento en la página.

[Video del contenido](https://vimeo.com/1140409611/6f8ea95004?fl=pl&fe=cm)

## ¿Qué es box-sizing y por qué se usa?

Hasta ahora vimos cómo funciona el Box Model tradicional, donde el ancho (`width`) y alto (`height`) __solo consideran el contenido__, el padding y el borde se suman por fuera.

Este comportamiento puede volver más difícil controlar el tamaño real de los elementos.

Para evitar confusiones, en la mayoría de los proyectos modernos se utiliza la propiedad:

```css
box-sizing: border-box;

```

### ¿Qué hace?

* Hace que el width y height incluyan el contenido + padding + borde.
* Simplifica la maquetación y evita que los elementos “crezcan” inesperadamente.

## Estructura HTML básica para maquetación

Para aplicar estilos CSS y entender el Box Model, es importante conocer la estructura HTML que usaremos. Aquí un ejemplo simple:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Ejemplo Box Model</title>
</head>
<body>
  <header>Encabezado</header>
  <main>
    <section>
      <div class="caja">Contenido de la caja</div>
    </section>
  </main>
  <footer>Pie de página</footer>
</body>
</html>
```

* Las etiquetas como `<header>`,`<main>`, `<section>`, `<footer>` son contenedores semánticos comunes.
* El `<div>` con clase `caja` será el elemento al que aplicaremos estilos para observar el Box Model.

> __Nota__: En la siguiente unidad aprenderemos a usar las herramientas DevTools del navegador para inspeccionar visualmente estas áreas y entender mejor cómo se aplican los estilos.
