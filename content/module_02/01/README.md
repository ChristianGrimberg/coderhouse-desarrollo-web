# ¿Qué es CSS y cómo se vincula a HTML?

## Sintaxis básica de CSS

Una regla CSS está compuesta por un selector y un bloque de declaraciones:

```css
selector {
  propiedad: valor;
}
```

* __Selector__: indica a qué elemento HTML se aplicarán los estilos. Por ejemplo, `p` selecciona todos los párrafos.
* __Propiedad__: es la característica que quieres modificar, como `color` o `font-size`.
* __Valor__: es el ajuste que le das a la propiedad, como `red` o `16px`.

Ejemplo:

```css
p {
  color: blue;
  font-size: 1rem;
}
```

Este código aplica texto azul y tamaño `1rem` a todos los párrafos.
Tip para principiantes:

* ✔ Cada declaración termina en ;
* ✔ Todo el bloque va entre { }
* ✔ Cuidá la indentación: hace el código más fácil de leer.

## Formas de vincular CSS a HTML

Existen tres métodos principales para aplicar CSS a un documento HTML:

* __Estilo inline__: Se escribe directamente en la etiqueta HTML usando el atributo `style`.

  ```html
  <p style="color: red;">Texto rojo</p>
  ```

  * ✔ Rápido
  * ✘ Mezcla HTML con CSS
  * ✘ Difícil de mantener

* __Estilo interno__: Se incluye dentro de una etiqueta `<style>` en el `<head>` del documento HTML.

  ```html
  <head>
    <style>
      p { color: green; }
    </style>
  </head>
  ```

  * ✔ No requiere archivos externos
  * ✘ No escalable si tu proyecto crece
  * ✘ No reutilizable

* __Estilo externo__: Se crea un archivo .css separado y se enlaza con la etiqueta `<link>` en el `<head>`.

  ```html
  <head>
    <link rel="stylesheet" href="styles.css">
  </head>
  ```

  * ✔ Ordenado
  * ✔ Reutilizable
  * ✔ Escalable
  * ✔ Buenas prácticas de la industria

  > __Recomendación__: siempre trabajá con un archivo externo llamado `styles.css`.

El método externo es el más recomendado para proyectos reales porque permite mantener el código organizado y reutilizable.

[Video de contenido](https://vimeo.com/1137300093/d63c59bcb6?fl=pl&fe=cm)

## Incorporación de fuentes externas con Google Fonts

Google Fonts es una biblioteca gratuita que ofrece una gran variedad de tipografías para usar en tus sitios web. Para usar una fuente, debes:

1. Elegir la fuente en [Google Fonts](https://fonts.google.com/).
1. Copiar el enlace `<link>` que Google Fonts genera.
1. Pegar ese enlace en el `<head>` de tu HTML.
1. Usar la fuente en tu CSS con la propiedad `font-family`.

Ejemplo:

```html
<head>
  <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
</head>
```

```css
body {
  font-family: 'Roboto', sans-serif;
}
```

### Dato profesional

Los navegadores priorizan las fuentes seguras, por eso siempre agregamos una fuente de respaldo:

```css
font-family: 'Roboto', sans-serif;
```

### ¿Por qué usar resets?

Los navegadores aplican estilos predeterminados diferentes a los elementos HTML, lo que puede causar inconsistencias visuales. Los archivos `reset.css` o `normalize.css` son hojas de estilo que "reinician" o normalizan estos estilos para que todos los navegadores muestren los elementos de forma más uniforme.

Incluir un reset al inicio de tu CSS ayuda a evitar sorpresas y facilita el diseño consistente.

> __Nota__: En módulos posteriores profundizaremos en la cascada y especificidad, que determinan cómo se aplican las reglas CSS cuando hay conflictos.
