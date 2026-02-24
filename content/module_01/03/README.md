# Etiquetas y atributos comunes

## Uso de enlaces con la etiqueta `<a>`

La etiqueta `<a>` (de "anchor" o ancla) se utiliza para crear __enlaces__ que permiten navegar de una página a otra o a una sección específica dentro de una misma página.

El atributo principal es `href`, que indica la __dirección del enlace__.

Ejemplo básico:

```html
<a href="https://www.ejemplo.com">Visita Ejemplo</a>
````

Este código crea un enlace que, al hacer clic, lleva al usuario a "[https://www.ejemplo.com](https://www.ejemplo.com)".

> __Nota__: Si `href` está vacío o no existe, el enlace no funcionará correctamente.

## Insertar imágenes con la etiqueta `<img>`

La etiqueta `<img>` se usa para mostrar imágenes en la página. Es una etiqueta vacía, es decir, no tiene etiqueta de cierre.

* Atributos importantes:
  * `src`: ruta o URL de la imagen.
  * `alt`: texto alternativo que describe la imagen, fundamental para accesibilidad y SEO.

Ejemplo:

```html
<img src="imagenes/logo.png" alt="Logo de la empresa">
````

> __Importante__: Siempre incluye el atributo `alt` para que personas con discapacidad visual o navegadores que no cargan imágenes puedan entender el contenido.

## Introducción a multimedia simple con `<video>`

La etiqueta `<video>` permite insertar videos en la página web.

* Atributos clave:
  * `src`: ruta del archivo de video.
  * `controls`: muestra controles de reproducción (play, pausa, volumen).

Ejemplo básico:

```html
<video src="videos/presentacion.mp4" controls></video>
```

> __Nota__: Para mayor compatibilidad, se pueden usar etiquetas `<source>` dentro de `<video>`, pero para esta introducción, el atributo src es suficiente.

## Rutas de archivos: relativas y absolutas

Para que los enlaces y recursos funcionen, es crucial entender las rutas:

* __Ruta relativa__: indica la ubicación del archivo en relación con el archivo HTML actual.
  * Ejemplo: `imagenes/foto.jpg` busca la imagen dentro de la carpeta "imagenes" en el mismo nivel que el archivo HTML.
* __Ruta absoluta__: es la dirección completa, puede ser una URL completa.
  * Ejemplo: `https://www.ejemplo.com/imagenes/foto.jpg`

> Usar rutas relativas es común en proyectos locales o cuando se controla la estructura de carpetas.

### Buenas prácticas para enlaces e imágenes

* Siempre usa `alt` descriptivo en imágenes.
* Verifica que las rutas sean correctas para evitar enlaces rotos o imágenes que no cargan.
* Usa enlaces claros y descriptivos para mejorar la experiencia del usuario.
* Para enlaces externos, considera usar el atributo `target="_blank"` para abrir en una nueva pestaña (esto se verá en unidades futuras).
