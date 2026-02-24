# Validación y accesibilidad básica en HTML

## ¿Qué es la validación HTML?

La __validación__ es el proceso de revisar que tu código HTML cumple con los estándares definidos por el World Wide Web Consortium (W3C). Esto ayuda a evitar errores que pueden afectar la visualización o el funcionamiento de tu sitio.

> __Dato importante__: Un HTML válido mejora la compatibilidad entre navegadores y facilita el mantenimiento.

## Herramientas para validar HTML

Existen herramientas online gratuitas como el _Validador de W3C_ que analizan tu código y te muestran errores o advertencias.

### Uso de la consola del navegador para depuración ligera

Los navegadores modernos incluyen una consola de desarrollo (accesible con `F12` o clic derecho > "Inspeccionar") que permite:

* Ver errores de carga o sintaxis
* Inspeccionar elementos y su estructura
* Probar cambios rápidos en el código

## Semántica y accesibilidad básica

La __semántica__ en HTML significa usar las etiquetas correctas para cada tipo de contenido, lo que ayuda a los navegadores y tecnologías asistivas a interpretar mejor la página.

### Buenas prácticas sencillas

* Usar atributos `alt` en imágenes para describirlas
* Utilizar etiquetas `<label>` vinculadas a campos de formulario para mejorar la navegación
* Aplicar roles ARIA básicos cuando sea necesario
* Mantener una estructura lógica con encabezados (`<h1>` a `<h6>`) y listas

Ejemplo:

```html
<label for="email">Correo electrónico:</label>
<input type="email" id="email" name="email" alt="Campo para ingresar correo electrónico">
```

Estas prácticas mejoran la experiencia para personas con discapacidades y cumplen con estándares de accesibilidad web.
