# Conceptos de display y flujo de documento

## Propiedad CSS display y su impacto en el flujo del documento

La propiedad display define cómo se presenta un elemento en la página y cómo interactúa con otros elementos. Los valores más comunes que veremos son:

* __block__
* __inline__
* __inline-block__

### 1. Display: block

Un elemento con `display: block` se comporta como un bloque que ocupa todo el ancho disponible de su contenedor, iniciando en una nueva línea. Ejemplos típicos son `<div>`, `<p>`, `<h1>`.

#### Características

* Ocupa toda la línea horizontal disponible.
* Permite definir `width` y `height`.
* Se respetan las propiedades del modelo de caja: `margin`, `padding`, `border`.

### Ejemplo

```css
div {
  display: block;
  width: 300px;
  margin: 10px auto;
  padding: 20px;
  border: 2px solid #333;
}
```

### 2. Display: inline

Los elementos con `display: inline` solo ocupan el espacio necesario para su contenido y no inician una nueva línea. Ejemplos comunes son `<span>`, `<a>`, `<strong>`.

#### Características

* No se puede modificar `width` ni `height`.
* `margin` y `padding` afectan solo horizontalmente, verticalmente pueden no tener efecto visible.
* Se alinean en línea con otros elementos.

#### Ejemplo

```css
span {
  display: inline;
  padding: 5px; /* vertical padding puede no afectar el flujo */
  margin: 0 10px;
}
```

### 3. Display: inline-block

Combina características de `inline` y `block`. El elemento se comporta como un bloque en línea, permitiendo definir `width`, `height`, y respetando el modelo de caja, pero sin iniciar una nueva línea.

#### Características

* Permite definir dimensiones.
* Se alinea en línea con otros elementos.
* Útil para maquetar elementos que deben estar en línea pero con control de tamaño.

#### Ejemplo

```css
button {
  display: inline-block;
  width: 150px;
  height: 40px;
  margin: 5px;
  padding: 10px;
  border: 1px solid #000;
}
```

### 4. Interacción con el Modelo de Caja (Box Model)

Recordemos que el modelo de caja define cómo se calculan las dimensiones de un elemento:

* __Content__: área del contenido
* __Padding__: espacio interno alrededor del contenido
* __Border__: borde que rodea el padding
* __Margin__: espacio externo que separa el elemento de otros

Para elementos `block` e `inline-block`, podemos controlar `width`, `height`, `margin` y `padding` para ajustar su tamaño y separación. En cambio, para `inline`, estas propiedades tienen limitaciones, especialmente en dimensiones verticales.

> __Nota__: El conocimiento del modelo de caja es fundamental para prever cómo se comportarán los elementos según su display.

__Con esta base, estarás listo para entender cómo estos valores afectan la maquetación y el flujo de los elementos en una página web.__
