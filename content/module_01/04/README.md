# Listas, tablas y formularios

## Listas en HTML

Las listas son una forma sencilla y efectiva de organizar elementos relacionados. En HTML existen dos tipos principales:

* Listas desordenadas (`<ul>`): muestran elementos sin un orden específico, usando viñetas.
* Listas ordenadas (`<ol>`): muestran elementos numerados o con un orden definido.

Cada elemento de la lista se define con la etiqueta `<li>`.

__Ejemplo de lista desordenada__:

```html
<ul>
  <li>Manzana</li>
  <li>Banana</li>
  <li>Cereza</li>
</ul>
```

__Ejemplo de lista ordenada__:

```html
<ol>
  <li>Preparar ingredientes</li>
  <li>Mezclar</li>
  <li>Hornear</li>
</ol>
```

## Tablas en HTML

Las tablas permiten organizar datos en filas y columnas, facilitando su lectura y comparación. Las etiquetas principales son:

* `<table>`: contenedor de la tabla.
* `<tr>`: define una fila.
* `<td>`: define una celda dentro de una fila.

__Ejemplo de tabla simple__:

```html
<table>
  <tr>
    <td>Producto</td>
    <td>Precio</td>
  </tr>
  <tr>
    <td>Camisa</td>
    <td>$20</td>
  </tr>
  <tr>
    <td>Pantalón</td>
    <td>$30</td>
  </tr>
</table>
```

### Cuándo usar tablas

Para mostrar datos tabulares, como horarios, precios o comparaciones.
No se recomienda para diseño o maquetación visual.

[Creando Listas, Tablas y Formularios en HTML 📊](https://www.loom.com/share/dba69c8e919f4e83b3d7e449bedee0cd)

## Formularios básicos en HTML

Los formularios permiten capturar información del usuario. La estructura básica incluye:

* `<form>`: contenedor del formulario.
* `<input>`: campos para ingresar datos (texto, correo, contraseña, etc.).
* `<label>`: etiqueta descriptiva para cada campo, mejora la accesibilidad.

__Ejemplo de formulario básico__:

```html
<form>
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre">
  <label for="email">Correo electrónico:</label>
  <input type="email" id="email" name="email">
  <input type="submit" value="Enviar">
</form>
```

### Buenas prácticas con `<label>`

* Usa el atributo for en `<label>` que coincida con el id del `<input>` correspondiente.
* Esto mejora la experiencia para usuarios con lectores de pantalla y facilita la interacción.

> Con estos conceptos, estarás listo para organizar información y crear formularios funcionales en tus páginas web.
