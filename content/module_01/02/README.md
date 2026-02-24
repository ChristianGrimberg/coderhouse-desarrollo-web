# Elementos estructurales y jerarquía en HTML

## Elementos de bloque vs elementos en línea

En HTML, los elementos se clasifican principalmente en dos tipos según cómo afectan la estructura y el flujo del contenido:

* __Elementos de bloque__: ocupan todo el ancho disponible y comienzan en una nueva línea. Ejemplos comunes son `<div>`, `<p>`, y los encabezados `<h1>` a `<h6>`.
* __Elementos en línea__: solo ocupan el espacio necesario y no interrumpen el flujo del texto. Ejemplos son `<span>`, `<a>`, y `<img>`.

> __Nota__: Entender esta diferencia es clave para organizar correctamente el contenido y aplicar estilos posteriormente.

## Etiquetas semánticas básicas

Las etiquetas semánticas aportan significado al contenido, ayudando a navegadores, motores de búsqueda y tecnologías de asistencia a interpretar la página.

* `<header>`: representa la cabecera de una sección o página, suele contener títulos, logotipos o menús principales.
* `<nav>`: define una sección de navegación con enlaces a otras partes del sitio.
* `<main>`: contiene el contenido principal único de la página.
* `<article>`: representa contenido independiente y autocontenido, como un artículo o entrada de blog.
* `<section>`: agrupa contenido temáticamente relacionado dentro de una página.
* `<footer>`: define el pie de página de una sección o documento, con información como derechos de autor o enlaces secundarios.

## Atributos importantes (refuerzo)

Recordemos que las etiquetas pueden tener atributos que añaden información o comportamiento, por ejemplo:

* `href` en `<a>` para definir el destino del enlace.
* `src` en `<img>` para indicar la fuente de la imagen.
* `alt` en `<img>` para describir la imagen, fundamental para accesibilidad.

Estos atributos son esenciales para que los elementos funcionen correctamente y sean accesibles.
