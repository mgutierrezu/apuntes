# Información y Apuntes CSS.

> Se realizarán cambios mientras más se vayan agregando comandos en los apuntes. Mientras tanto se realizará la siguiente clasificación:

## Clasificación de información CSS:

- [Introducción y Fundamentos](#introducción-y-fundamentos)
- [Selectores y Propiedades](#selectores-y-propiedades)
- [Modelo de Caja y Layout](#modelo-de-caja-y-layout)
- [Diseño Responsivo](#diseño-responsivo)
- [Flexbox y Grid](#flexbox-y-grid)
- [Animaciones y Transiciones](#animaciones-y-transiciones)
- [Pseudoclases y Pseudoelementos](#pseudoclases-y-pseudoelementos)
- [Importancia de la Performance](#importancia-de-la-performance)
- [Prácticas de Organización](#prácticas-de-organización)
- [Herramientas y Frameworks](#herramientas-y-frameworks)

## Introducción y Fundamentos:

- ### Conceptos básicos de CSS.

CSS, que significa "Cascading Style Sheets" (Hojas de Estilo en Cascada), es un lenguaje de estilo utilizado para describir el aspecto y el formato de un documento escrito en un lenguaje de marcado, como HTML. Aquí tienes algunos conceptos básicos de CSS:

**Selector:** Un selector en CSS es una expresión que identifica los elementos HTML a los que se aplicará un estilo. Puede ser el nombre de un elemento HTML (como p para párrafos), una clase (precedida por un punto, como .clase), un id (precedido por un hashtag, como #id), o incluso pseudoclases (como :hover para cuando el cursor está sobre un elemento).

```html
<p>Este es un párrafo.</p>
```

```css
/* Selector de elemento */
p {
  color: blue;
}
```

**Propiedad:** Una propiedad es un aspecto específico del estilo que se quiere aplicar a un elemento HTML. Por ejemplo, color, font-size, background-color, etc.

```css
/* Propiedad */
p {
  color: red; /* Propiedad color */
}
```

**Valor:** Cada propiedad en CSS tiene un valor asociado que define cómo se aplicará la propiedad al elemento seleccionado. Por ejemplo, red para el color, 16px para el tamaño de fuente, etc.

```css
/* Valor */
p {
  font-size: 20px; /* Valor 20px para el tamaño de fuente */
}
```

**Declaración:** Una declaración en CSS consiste en una propiedad y su valor separados por dos puntos y terminados con un punto y coma. Por ejemplo, color: blue;.

```css
/* Declaración */
p {
  color: blue; /* Declaración de color */
  font-size: 16px; /* Declaración de tamaño de fuente */
}
```

**Cascada:** En CSS, cuando hay conflictos entre diferentes reglas, la cascada decide cuál prevalece. Por ejemplo, si tienes dos reglas para el mismo elemento pero con propiedades contradictorias, la regla más específica o la que está más abajo en el código prevalecerá.

**Box Model:** El Modelo de Caja describe cómo se representa visualmente un elemento HTML. Por ejemplo, si aplicas un padding de 10px a un div, eso agregará un espacio de 10px entre el borde del div y su contenido.

**Clases y ID:** Son atributos que se pueden añadir a los elementos HTML para luego ser seleccionados y estilizados con CSS. Una clase se define con un punto (.) y puede ser aplicada a múltiples elementos, mientras que un ID se define con un hashtag (#) y debe ser único en todo el documento HTML.

```html
<p class="destacado">Este es un párrafo destacado.</p>
<p id="unico">Este es un párrafo único.</p>
```

```css
/* Clase */
.destacado {
  color: green;
}

/* ID */
#unico {
  font-weight: bold;
}
```

- ### Integración de CSS en HTML.

Hay tres formas principales de integrar CSS en un documento HTML:

1. **Estilo en línea (Inline Styles):** Se utiliza el atributo style en una etiqueta HTML para aplicar estilos directamente a un elemento específico. Por ejemplo:

```html
<p style="color: blue; font-size: 16px;">
  Este es un párrafo con estilo en línea.
</p>
```

2. **Estilo interno (Internal Styles):** Se utiliza la etiqueta (style) en la sección (head) del documento HTML para definir estilos que se aplicarán a múltiples elementos dentro del mismo documento. Por ejemplo:

```html
<head>
  <style>
    p {
      color: blue;
      font-size: 16px;
    }
  </style>
</head>
<body>
  <p>Este es un párrafo con estilo interno.</p>
</body>
```

3. **Estilo externo (External Styles):** Se utiliza un archivo CSS externo que se enlaza al documento HTML utilizando la etiqueta (link) en la sección (head). Esto permite aplicar estilos a múltiples documentos HTML desde un solo archivo CSS. Por ejemplo:

```html
<head>
  <link rel="stylesheet" type="text/css" href="styles.css" />
</head>
```

## Selectores y Propiedades

- ### Selectores de tipo, clase, y ID.

En CSS (Cascading Style Sheets), los selectores son patrones que se utilizan para seleccionar y aplicar estilos a elementos HTML específicos. Los selectores pueden ser de varios tipos, incluyendo selectores de tipo, clase y ID.

1. **Selector de tipo:** Este selector selecciona todos los elementos de un tipo específico en un documento HTML. Por ejemplo, si quieres aplicar un estilo a todos los párrafos (p) en tu página, usarías un selector de tipo de la siguiente manera:

```css
p {
  /* Estilos aquí */
}
```

En este caso, todos los elementos (p) en tu documento HTML tendrán los estilos definidos dentro de las llaves {}.

2. **Selector de clase:** Los selectores de clase se utilizan para seleccionar elementos que tienen un atributo class específico en HTML. Puedes aplicar la misma clase a múltiples elementos y luego aplicar estilos a todos esos elementos de una vez. <br>
   Para seleccionar una clase en CSS, antepones un punto (.) seguido del nombre de la clase. Por ejemplo, si tienes una clase llamada destacado, usarías un selector de clase de la siguiente manera:

```css
.destacado {
  /* Estilos aquí */
}
```

Luego, en tu HTML, aplicarías la clase así:

```html
<p class="destacado">Este párrafo está destacado.</p>
```

Todos los elementos con la clase destacado tendrán los estilos definidos dentro del selector.

3. **Selector de ID:** Los selectores de ID son similares a los selectores de clase, pero en lugar de aplicar a múltiples elementos, se aplican a un único elemento. Cada ID debe ser único en todo el documento HTML. <br>
   Para seleccionar un ID en CSS, antepones un signo de almohadilla (#) seguido del nombre del ID. Por ejemplo, si tienes un elemento con el ID encabezado, usarías un selector de ID de la siguiente manera:

```css
#encabezado {
  /* Estilos aquí */
}
```

```html
<div id="encabezado">Contenido del encabezado</div>
```

- ### Propiedades de estilo (color, tamaño, posición, etc.).

Color (color): Define el color del texto.

```css
p {
  color: blue;
}
```

Fondo (background): Define el color de fondo de un elemento.

```css
body {
  background-color: #f0f0f0;
}
```

Tamaño de fuente (font-size): Define el tamaño del texto.

```css
h1 {
  font-size: 24px;
}
```

Familia de fuente (font-family): Define la fuente utilizada para el texto.

```css
h1 {
  font-size: 24px;
}
```

Ancho (width): Define el ancho de un elemento.

```css
.container {
  width: 80%;
}
```

Alto (height): Define la altura de un elemento.

```css
.box {
  height: 100px;
}
```

Margen (margin): Define el espacio alrededor de un elemento.

```css
.box {
  margin: 10px;
}
```

Relleno (padding): Define el espacio dentro de un elemento.

```css
.box {
  padding: 10px;
}
```

Borde (border): Define el borde de un elemento.

```css
.box {
  border: 1px solid black;
}
```

> Solid le da la propiedad a una linea continua. Black define el color del borde.

Posición (position): Define el método de posicionamiento de un elemento.

```css
.box {
  position: relative;
}
```

Alineación de texto (text-align): Define la alineación horizontal del texto dentro de un elemento.

```css
p {
  text-align: center;
}
```

Opacidad (opacity): Define la transparencia de un elemento.

```css
.element {
  opacity: 0.5;
}
```

Display (display): Define el tipo de visualización de un elemento.

```css
.element {
  display: inline-block;
}
```

Flotado (float): Define si un elemento debe estar a la izquierda o a la derecha de su contenedor.

```css
.image {
  float: left;
}
```

background-color: Define el color de fondo de un elemento.

```css
.container {
  background-color: #f0f0f0;
}
```

background-image: Define una imagen de fondo para un elemento.

```css
.header {
  background-image: url("imagen.jpg");
}
```

background-size: Define el tamaño de la imagen de fondo.

```css
.header {
  background-size: cover;
}
```

## Modelo de Caja y Layout

- ### Concepto del modelo de caja.

El modelo de caja es un concepto fundamental en diseño web que describe cómo se representan y se estructuran los elementos en una página web. Cada elemento HTML se considera una "caja" rectangular que consta de contenido, relleno (padding), borde y margen.

- ### Propiedades de margin, padding, border.

**Contenido (Content):** Es el área donde se muestra el contenido del elemento, como texto, imágenes, etc.

**Relleno (Padding):** Espacio transparente alrededor del contenido dentro del borde.

**Borde (Border):** Línea que rodea el relleno y el contenido del elemento.

**Margen (Margin):** Espacio transparente fuera del borde del elemento, que separa este elemento de otros elementos cercanos.

Ejemplo de código HTML con propiedades CSS:

```html
<div
  style="width: 200px; height: 100px; border: 1px solid black; padding: 20px; margin: 10px;"
>
  Contenido de la caja
</div>
```

- ### Box-sizing y Margin collapsing.

**box-sizing:** Es una propiedad de CSS que determina cómo se calcula el ancho y el alto total de un elemento, considerando o no el relleno y el borde. Los valores típicos son content-box (valor predeterminado) y border-box.

**Margin collapsing:** Ocurre cuando los márgenes verticales de dos elementos adyacentes se superponen, en cuyo caso el margen resultante es el máximo de los márgenes individuales.

Ejemplo de código CSS:

```css
.caja {
  width: 200px;
  height: 100px;
  padding: 10px;
  border: 1px solid black;
  box-sizing: border-box; /* El ancho total incluye el relleno y el borde */
}

.otra-caja {
  margin-top: 20px;
}
```

- ### Diseño de cajas flexibles y bloque.

**Cajas flexibles (flexbox):** Permite diseñar diseños flexibles y eficientes en términos de espacio, alineando y distribuyendo elementos de manera dinámica dentro de un contenedor flexible.

**Cajas de bloque (block):** Los elementos de bloque ocupan todo el ancho disponible y comienzan en una nueva línea.

Ejemplo de código CSS con flexbox:

```css
.contenedor-flex {
  display: flex;
  justify-content: space-between; /* Distribuye el espacio entre los elementos */
}

.caja-flex {
  flex: 1; /* Hace que las cajas flexibles se expandan para ocupar todo el espacio disponible */
}
```

Ejemplo de código CSS con caja de bloque:

```css
.caja-bloque {
  display: block;
  width: 300px;
  height: 150px;
  background-color: lightblue;
}
```

> Estos conceptos son esenciales para comprender y controlar el diseño y la disposición de los elementos en una página web.

## Diseño Responsivo

El diseño responsivo es una técnica de diseño web que garantiza que los sitios web se vean bien en una variedad de dispositivos y tamaños de pantalla, desde computadoras de escritorio hasta dispositivos móviles. Aquí hay algunos conceptos clave relacionados con el diseño responsivo,

- ### Uso de media queries.

Las media queries son una característica de CSS que permite aplicar estilos basados en ciertas características del dispositivo, como el ancho de la pantalla, la orientación, la resolución, etc. Esto permite crear diseños específicos para diferentes dispositivos.

Ejemplo de una media query en CSS:

```css
@media screen and (max-width: 768px) {
  /* Estilos aplicados cuando el ancho de la pantalla es igual o menor a 768px */
  body {
    font-size: 14px;
  }
}
```

- ### Unidades de medida relativas (em, rem).

Las unidades de medida relativas son unidades que se basan en el tamaño de otro elemento en lugar del tamaño de la ventana del navegador. Esto hace que el diseño sea más flexible y adaptable a diferentes tamaños de pantalla. em se basa en el tamaño de fuente del elemento padre, mientras que rem se basa en el tamaño de fuente del elemento raíz (html).

Ejemplo de uso de unidades em y rem en CSS:

```css
body {
  font-size: 16px; /* Tamaño de fuente base */
}

.caja {
  width: 20em; /* Ancho de 20 veces el tamaño de fuente del elemento padre */
  padding: 1rem; /* Relleno de 1 vez el tamaño de fuente del elemento raíz */
}
```

- ### Viewport y diseño adaptativo.

El viewport es el área visible de una página web en el navegador. En el diseño adaptativo, se utiliza el metaetiqueta (meta name="viewport") en HTML para controlar cómo se ajusta la página al viewport del dispositivo. Esto es crucial para garantizar que los sitios web se vean correctamente en dispositivos móviles y tablets.

Ejemplo de uso de la etiqueta de viewport en HTML:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Diseño Responsivo</title>
  </head>
  <body>
    <!-- Contenido de la página -->
  </body>
</html>
```

> Estos conceptos son fundamentales para crear sitios web que se adapten y se vean bien en una amplia gama de dispositivos y tamaños de pantalla. Al utilizar media queries, unidades de medida relativas y ajustar el viewport, los desarrolladores pueden crear experiencias de usuario consistentes y optimizadas para diferentes contextos de visualización.

## Flexbox y Grid

- ### Flexbox: Conceptos básicos y uso.

Flexbox es un modelo de diseño unidimensional que permite distribuir el espacio entre elementos de manera eficiente incluso cuando tienen tamaños desconocidos o dinámicos. Algunos conceptos clave de Flexbox incluyen:

- **Contenedor flex (Flex container):** El elemento que contiene los elementos flexibles se convierte en un contenedor flex estableciendo la propiedad display: flex o display: inline-flex.

- **Elementos flexibles (Flex items):** Los elementos hijos directos del contenedor flex son los elementos flexibles. Se pueden controlar utilizando propiedades como flex-grow, flex-shrink, flex-basis, etc.

- **Ejes principales y secundarios:** Flexbox tiene un eje principal y un eje secundario, que pueden ser horizontal o vertical dependiendo de la dirección del flujo principal (flex-direction).

Ejemplo de uso de Flexbox en CSS:

```css
.contenedor-flex {
  display: flex;
  justify-content: center; /* Centra los elementos a lo largo del eje principal */
  align-items: center; /* Centra los elementos a lo largo del eje secundario */
  height: 300px; /* Altura del contenedor */
}

.elemento-flex {
  flex: 1; /* El elemento flexible ocupará todo el espacio disponible */
  margin: 10px; /* Margen entre elementos */
}
```

Ejemplo de HTML:

```html
<div class="contenedor-flex">
  <div class="elemento-flex">Elemento 1</div>
  <div class="elemento-flex">Elemento 2</div>
  <div class="elemento-flex">Elemento 3</div>
</div>
```

- ### Grid: Conceptos básicos y uso.

CSS Grid Layout es un sistema de diseño bidimensional que permite crear diseños complejos y flexibles mediante la definición de filas y columnas. Algunos conceptos clave de Grid incluyen:

- C**ontenedor de cuadrícula (Grid container):** El elemento que contiene los elementos de la cuadrícula se convierte en un contenedor de cuadrícula estableciendo la propiedad display: grid.

- **Filas y columnas:** Se pueden definir filas y columnas utilizando las propiedades grid-template-rows y grid-template-columns, respectivamente.

- **Celdas de la cuadrícula:** Los elementos secundarios del contenedor de cuadrícula se colocan en celdas de la cuadrícula, utilizando las propiedades grid-row y grid-column.

Ejemplo de uso de Grid en CSS:

```css
.contenedor-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr; /* Tres columnas de igual ancho */
    grid-gap: 10px; /* Espacio entre celdas */
}

.elemento-grid {
    background-color: lightblue;
    padding: 20px;
    text-align: center;
}
```

Ejemplo de HTML:
```html
<div class="contenedor-grid">
    <div class="elemento-grid">Elemento 1</div>
    <div class="elemento-grid">Elemento 2</div>
    <div class="elemento-grid">Elemento 3</div>
</div>
```
> En este ejemplo, se crea un contenedor de cuadrícula con tres columnas de igual ancho y un espacio de 10px entre ellas. Cada elemento secundario se coloca en una celda de la cuadrícula y se le aplica un estilo de fondo y relleno.

## Animaciones y Transiciones

- ### Transiciones CSS.
- ### Animaciones CSS.
- ### Efectos de transformación y keyframes.

## Pseudoclases y Pseudoelementos

- ### Uso de pseudoclases para interactividad.
- ### Pseudoelementos para estilización adicional.

## Importancia de la Performance

- ### Optimización del rendimiento CSS.
- ### Minificación y concatenación de archivos CSS.

## Prácticas de Organización

- ### Metodologías CSS (BEM, SMACSS, etc.).
- ### Arquitectura de estilos (CSS escalable, OOCSS).

## Herramientas y Frameworks

- ### Preprocesadores CSS (Sass, Less).
- ### Frameworks CSS (Bootstrap, Foundation).
- ### Herramientas de construcción (Webpack, Gulp).
