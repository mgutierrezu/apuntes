# Información y Apuntes HTML

> Se realizarán cambios mientras más se vaya agregando información en los apuntes. Mientras tanto se realizará la siguiente clasificación:

## Clasificación de contenidos HTML:

- [Estructura básica](#estructura-basica)
- [Etiquetas (Tags)](#etiquetas-tags)
- [Atributos (Attributes)](#atributos-attributes)
- [Formularios (Forms)](#formularios-forms)
- [Multimedia](#multimedia)
- [Listas](#listas)
- [Tablas](#tablas)
- [Enlaces (Links)](#enlaces-links)
- [Metadatos](#metadatos)
- [Elementos de Texto](#elementos-de-texto)
- [Elementos de Bloque](#elementos-de-bloque)
- [Elementos de Formato de Texto](#elementos-de-formato-de-texto)
- [Comentarios](#comentarios)
- [Otros](#otros)

## Estructura básica

Esta declaración define el tipo de documento y la versión de HTML utilizada en el documento. Especifica a los navegadores qué tipo de documento esperar y cómo interpretarlo.

```html
<!DOCTYPE html>
```

Esta etiqueta delimita el comienzo y el final del documento HTML y contiene todo el contenido HTML.

```html
<html></html>
```

La sección head contiene metadatos y enlaces a recursos externos, como hojas de estilo CSS y scripts JavaScript. También incluye el título de la página, que se muestra en la barra de título del navegador.

```html
<head></head>
```

Esta etiqueta define el conjunto de caracteres utilizado en el documento HTML. El valor utf-8 se utiliza comúnmente para admitir una amplia gama de caracteres Unicode.

```html
<meta charset="utf-8" />
```

Esta etiqueta define el conjunto de caracteres utilizado en el documento HTML. El valor utf-8 se utiliza comúnmente para admitir una amplia gama de caracteres Unicode.

```html
<title>
```

Contiene todo el contenido visible de la página web, como texto, imágenes, enlaces, etc. Todo lo que se muestra en la página se coloca dentro de esta etiqueta.

```html
<body></body>
```

Esta sección define el encabezado de la página, que generalmente contiene elementos como el logotipo, el menú de navegación y cualquier otro contenido que se desee mostrar en la parte superior de la página.

```html
<header></header>
```

Define el pie de página de la página web. Contiene información adicional como derechos de autor, información de contacto o enlaces a páginas relacionadas.

```html
<footer></footer>
```

Define la sección de navegación de la página. Contiene enlaces a diferentes partes del sitio web, lo que facilita a los usuarios la navegación por el contenido.

```html
<nav></nav>
```

La etiqueta script se utiliza para incluir scripts JavaScript en la página. Puede estar ubicada en la sección head o al final del cuerpo body. Se utiliza para agregar interactividad y funcionalidad dinámica a la página web.

```html
<script>
```

Esta etiqueta <meta> se utiliza para controlar cómo se ajusta y escala la página en dispositivos móviles. Es esencial para garantizar una experiencia de usuario adecuada en dispositivos móviles.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

## Etiquetas (Tags)

Definen encabezados o títulos de diferentes niveles de importancia. h1 es el encabezado más importante y h6 es el menos importante.

```html
<h1></h1>
```

Define un párrafo de texto. Se utiliza para separar y organizar el contenido de la página en secciones legibles.

```html
<p></p>
```

Define un enlace a otra página web o recurso. El atributo href dentro de esta etiqueta especifica la URL o ruta a la que se enlaza.

```html
<a href="URL/ruta"></a>
```

Inserta una imagen en la página web. El atributo src dentro de esta etiqueta especifica la URL de la imagen que se mostrará.

```html
<img src="" alt="" />
```

> alt: es un atributo y se utiliza para realizar una descripción del recurso.

Define una división o contenedor genérico para organizar y estructurar el contenido de la página web. Se utiliza comúnmente junto con hojas de estilo CSS para aplicar estilos y diseños.

```html
<div></div>
```

Define una sección en línea genérica o contenedor para aplicar estilos o manipular contenido específico dentro de un párrafo u otro elemento en línea.

```html
<span></span>
```

## Atributos (Attributes)

Identifica de manera única un elemento en un documento HTML, permitiendo su posterior manipulación con CSS o JavaScript.

```html
id=""
```

Asigna una o más clases a un elemento, permitiendo su estilo mediante CSS o su selección y manipulación con JavaScript.

```html
class=""
```

Especifica la ruta de origen para recursos incrustados, como imágenes, audio, video, etc.

```html
src=""
```

Especifica la URL de destino para enlaces, permitiendo la navegación a otras páginas web o recursos.

```html
href=""
```

Proporciona un texto alternativo para imágenes que se muestra en caso de que la imagen no se pueda cargar o para usuarios con discapacidad visual.

```html
alt=""
```

Proporciona un título descriptivo para elementos, que generalmente se muestra como un tooltip cuando el usuario pasa el cursor sobre el elemento.

```html
title=""
```

Permite especificar estilos en línea para un elemento, como color de fondo, tamaño de fuente, etc.

```html
style=""
```

Muestra un texto de marcador de posición en campos de entrada (input, textarea) que desaparece cuando el usuario comienza a escribir.

```html
placeholder=""
```

Desactiva la funcionalidad de un elemento, como un botón (button) o un campo de entrada (input), impidiendo su interacción.

```html
disabled
```

Indica que un campo de entrada (input, textarea) es obligatorio y debe completarse antes de enviar un formulario.

```html
required
```

El atributo name se utiliza para asignar un nombre a un elemento HTML, como un campo de entrada o un elemento de formulario.

```html
name=""
```

> Este nombre se utiliza para identificar el elemento cuando se envía el formulario y se procesa en el servidor. Es importante para la estructura y el manejo de datos enviados a través de formularios HTML.

## Formularios (Forms)

- ### Etiquetas Formulario.

Define un formulario HTML para recopilar datos de usuario. Especifica la URL a la que se enviarán los datos (action) y el método de envío (method).

```html
<form></form>
```

Crea un campo de entrada en el formulario. Puede ser de varios tipos como texto, contraseña, botón de radio, casilla de verificación, etc. El atributo name identifica el campo y type define el tipo de entrada.

```html
<input />
```

Proporciona una etiqueta descriptiva para un elemento de formulario. Se asocia al campo de entrada mediante el atributo **for**.

```html
<label></label>
```

Crea un menú desplegable que permite al usuario seleccionar una opción de una lista. Las opciones se definen dentro de select mediante option.

```html
<select></select>
```

Define una opción dentro de un menú desplegable. Puede tener un valor asociado (value) y un texto que se muestra al usuario.

```html
<option></option>
```

Crea un área de texto de múltiples líneas para que el usuario ingrese texto.

```html
<textarea>
```

Define un botón en el formulario, que puede ser de tipo "submit" (enviar), "reset" (restablecer) o "button" (personalizado).

```html
<button></button>
```

- ### Atributos Formulario.

Action: Especifica la URL a la que se enviarán los datos del formulario.

```html
<form action="/procesar_datos.php"></form>
```

Method: Define el método HTTP utilizado para enviar los datos del formulario (GET o POST).

```html
<form method="post"></form>
```

Name: Identifica el campo de entrada en el formulario.

```html
<input type="text" name="username" />
```

For: Asocia una etiqueta (label) con un campo de entrada mediante su id.

```html
<label for="username">Nombre de usuario:</label>
```

Value: Define el valor predeterminado para un campo de entrada.

```html
<input type="text" value="John Doe" />
```

Placeholder: Muestra un texto de marcador de posición en un campo de entrada.

```html
<input type="text" placeholder="Introduce tu nombre" />
```

Required: Indica que un campo de entrada es obligatorio.

```html
<input type="text" required />
```

Readonly: Indica que un campo de entrada es obligatorio.Define un campo de entrada como de solo lectura.

```html
<input type="text" value="Solo lectura" readonly />
```

disabled: Desactiva la funcionalidad de un elemento de formulario.

```html
<input type="text" disabled />
```

autocomplete: Especifica si el navegador debe habilitar el autocompletado para campos de entrada en el formulario.

```html
<input type="text" autocomplete="off" />
```

novalidate: Indica al navegador que no valide los campos del formulario antes de enviarlos al servidor.

```html
<form novalidate></form>
```

maxlength: Limita el número máximo de caracteres que se pueden ingresar en un campo de entrada.

```html
<input type="text" maxlength="10" />
```

min y max: Establece los valores mínimo y máximo permitidos para un campo de entrada numérico.

```html
<input type="number" min="0" max="100" />
```

pattern: Define un patrón de expresión regular que el valor de un campo de entrada debe seguir.

```html
<input type="text" pattern="[A-Za-z]{3}" />
```

## Multimedia

- ### Etiquetas Multimedia.

Inserta imágenes en una página web. No tiene etiqueta de cierre y utiliza el atributo **src** para especificar la URL de la imagen.

```html
<img />
```

Incrusta contenido de audio en una página web. Puede incluir múltiples fuentes de audio para compatibilidad con diferentes formatos.

```html
<audio></audio>
```

Incrusta contenido de video en una página web. Similar a <audio>, permite la inclusión de varias fuentes de video para compatibilidad.

```html
<video></video>
```

Define fuentes de medios para elementos de audio y video. Permite especificar diferentes formatos de medios para compatibilidad con varios navegadores.

```html
<source />
```

Permite incrustar contenido externo, como mapas de Google Maps o contenido de redes sociales, en una página web.

```html
<iframe></iframe>
```

Proporciona un lienzo gráfico para dibujar gráficos, gráficos y animaciones utilizando JavaScript.

```html
<canvas></canvas>
```

Incrusta contenido externo, como archivos multimedia, en una página web. Se usa comúnmente para incrustar contenido Flash.

```html
<embed />
```

Incrusta objetos multimedia, como animaciones Flash o contenido de Silverlight, en una página web.

```html
<object></object>
```

Define pistas de texto o subtítulos para elementos de video y audio. Se utiliza para proporcionar subtítulos o descripciones de audio para personas con discapacidad auditiva.

```html
<track />
```

Proporciona una forma de definir varias fuentes de imágenes con condiciones de visualización basadas en la resolución y el tamaño de la pantalla. Es útil para la optimización de imágenes responsivas.

```html
<picture></picture>
```

- ### Atributos Multimedia.

src: Especifica la URL de la fuente de medios, como una imagen, audio, o video.

```html
<img src="imagen.jpg" alt="Texto alternativo" />
```

> alt: Proporciona un texto alternativo que se muestra si el contenido multimedia no se puede cargar. Es especialmente útil para personas con discapacidad visual o cuando la imagen no se puede cargar.

autoplay: Indica si el contenido multimedia debe comenzar a reproducirse automáticamente después de que se cargue la página.

```html
<video src="video.mp4" autoplay></video>
```

controls: Muestra controles de reproducción para el elemento multimedia, como botones de reproducción/pausa, barra de progreso y controles de volumen.

```html
<video src="video.mp4" controls></video>
```

loop: Especifica si el contenido multimedia debe reproducirse en un bucle continuo después de finalizar.

```html
<video src="video.mp4" loop></video>
```

preload: Indica cómo y cuándo se deben cargar los datos multimedia cuando se carga la página. Puede ser none, metadata o auto.

```html
<video src="video.mp4" preload="auto"></video>
```

width y height: Especifican el ancho y la altura del contenido multimedia, respectivamente. Ayudan a definir el tamaño y la disposición del elemento en la página.

```html
<img src="imagen.jpg" width="300" height="200" />
```

poster: Especifica una imagen de vista previa para elementos de video. Esta imagen se muestra antes de que se inicie la reproducción del video.

```html
<video src="video.mp4" poster="imagen.jpg"></video>
```

type: Define el tipo de medio especificado por la URL en el atributo src. Por ejemplo, type="audio/mp3" o type="video/mp4".previa para elementos de video.

```html
<source src="audio.mp3" type="audio/mp3" />
```

muted: Indica si el contenido de audio del elemento multimedia debe estar silenciado inicialmente cuando se carga la página.

```html
<video src="video.mp4" muted></video>
```

## Listas

- ### Etiquetas para Listas.

Define una lista desordenada donde los elementos se presentan con viñetas.

```html
<ul></ul>
```

Define una lista ordenada donde los elementos se presentan con números o letras.

```html
<ol></ol>
```

Define un ítem de lista, ya sea para listas desordenadas o ordenadas.

```html
<li></li>
```

Define una lista de definición que consta de pares de términos y sus definiciones.

```html
<dl></dl>
```

Define un término en una lista de definición (<dl>).

```html
<dt></dt>
```

Define la definición de un término en una lista de definición (<dl>).

```html
<dd></dd>
```

Define una lista de comandos o enlaces de navegación.

```html
<menu></menu>
```

Define una lista de directorios.

```html
<dir></dir>
```

Define una lista de directorios.

```html
<dir></dir>
```

Define un elemento de menú dentro de un menú contextual.

```html
<menuitem></menuitem>
```

- ### Atributos para Listas.

type: Especifica el tipo de marcador o numeración para una lista ordenada (ol).

```html
<ol type="1"></ol>
```

start: Especifica el valor inicial de una lista ordenada (ol).

```html
<ol start="5"></ol>
```

reversed: Revierte el orden de una lista ordenada (ol).

```html
<ol reversed></ol>
```

compact: Reduce el espaciado entre los elementos de la lista.

```html
<ul compact></ul>
```

value: Define el valor del elemento de la lista (li) en una lista ordenada.

```html
<li value="3"></li>
```

label: Define la etiqueta para un grupo de comandos (menu).

```html
<menu label="Opciones"></menu>
```

menu: Especifica el id de un menú contextual asociado a un elemento (menuitem).

```html
<menuitem menu="menu-contextual"></menuitem>
```

## Tablas

- ### Etiquetas para Tablas.

Define una tabla en HTML. Es el contenedor principal para todas las filas, columnas y celdas de la tabla.

```html
<table></table>
```

(Table Row): Define una fila en una tabla. Contiene una o más celdas de datos (td) o celdas de encabezado (th).

```html
<tr></tr>
```

(Table Header Cell): Define una celda de encabezado en una fila de la tabla. Se utiliza para etiquetar las filas o columnas de la tabla.

```html
<th></th>
```

(Table Data Cell): Define una celda de datos en una fila de la tabla. Contiene el contenido real de la tabla.

```html
<td></td>
```

(Table Head): Define la sección de encabezado de una tabla. Contiene una o más filas de celdas de encabezado (th).

```html
<thead></thead>
```

(Table Body): Define la sección del cuerpo de una tabla. Contiene una o más filas de celdas de datos (td).

```html
<tbody></tbody>
```

(Table Foot): Define la sección de pie de una tabla. Contiene una o más filas de celdas de datos (td).

```html
<tfoot></tfoot>
```

Define el título o descripción de una tabla. Se coloca dentro del elemento (table) y se muestra encima de la tabla.

```html
<caption></caption>
```

(Column): Define las propiedades de una o más columnas en una tabla.

```html
<col />
```

(Column Group): Define un grupo de una o más columnas en una tabla. Se utiliza junto con (col) para aplicar propiedades a varias columnas a la vez.

```html
<colgroup></colgroup>
```

- ### Atributos para Tablas.

border: Especifica el ancho del borde de la tabla.

```html
<table border="1"></table>
```

cellspacing: Especifica el espacio entre las celdas de la tabla.

```html
<table cellspacing="5"></table>
```

cellpadding: Especifica el espacio entre el contenido de la celda y su borde.

```html
<table cellpadding="10"></table>
```

width: Especifica el ancho de la tabla.

```html
<table width="500"></table>
```

height: Especifica la altura de la tabla.

```html
<table height="300"></table>
```

align: Alinea el contenido de la tabla horizontalmente.

```html
<table align="center"></table>
```

valign: Alinea el contenido de la tabla verticalmente.

```html
<table valign="middle"></table>
```

colspan: Especifica el número de columnas que una celda debe abarcar.

```html
<td colspan="2"></td>
```

rowspan: Especifica el número de filas que una celda debe abarcar.

```html
<td rowspan="3"></td>
```

scope: Especifica el ámbito de una celda de encabezado.

```html
<th scope="col"></th>
```

summary: Proporciona una descripción concisa de la estructura y contenido de la tabla para ayudar a las personas con discapacidad visual o cognitiva.

```html
<table summary="Resumen de la tabla"></table>
```

frame: Especifica qué partes de la tabla deben tener bordes visibles.

```html
<table frame="above"></table>
```

bgcolor: Define el color de fondo de la tabla.

```html
<table bgcolor="#f0f0f0"></table>
```

bordercolor: Define el color del borde de la tabla.

```html
<table bordercolor="#333333"></table>
```

## Enlaces (Links)

- ### Etiquetas para Enlaces.

(Anchor): Define un enlace (hipervínculo) a otro recurso.

```html
<a href="https://www.ejemplo.com">Enlace a Ejemplo</a>
```

Define la relación entre el documento actual y un recurso externo, como una hoja de estilos CSS.

```html
<link rel="stylesheet" href="estilos.css" />
```

(Navigation): Define una sección de navegación en un documento, típicamente contiene enlaces a otras páginas.

```html
<nav>
  <a href="pagina1.html">Página 1</a>
  <a href="pagina2.html">Página 2</a>
</nav>
```

Define un botón que puede actuar como un enlace a otra página o ejecutar una acción en el mismo documento.

```html
<button onclick="window.location.href='pagina.html'">Ir a Página</button>
```

Define un formulario que puede contener elementos de entrada y enviar datos a otro recurso, como una página web.

```html
<form action="procesar.php" method="post">
  <input type="text" name="nombre" />
  <input type="submit" value="Enviar" />
</form>
```

Define una opción dentro de un elemento (select) o (datalist).

```html
<select>
  <option value="1">Opción 1</option>
  <option value="2">Opción 2</option>
</select>
```

- ### Atributos para Enlaces.

(Hypertext Reference): Especifica la URL del recurso al que enlaza el elemento (a).

```html
<a href="https://www.ejemplo.com">Enlace a Ejemplo</a>
```

target: Especifica dónde abrir el recurso vinculado (\_self, \_blank, \_parent, \_top).

```html
<a href="pagina.html" target="_blank">Abrir en nueva ventana</a>
```

rel (Relationship): Define la relación entre el documento actual y el recurso vinculado (stylesheet, icon, alternate, etc.).

```html
<link rel="stylesheet" href="estilos.css" />
```

download: Indica al navegador que el recurso vinculado debe descargarse en lugar de abrirse en una nueva ventana o pestaña

```html
<a href="documento.pdf" download>Descargar PDF</a>
```

title: Proporciona un título o información adicional sobre el enlace.

```html
<a href="pagina.html" title="Enlace a Página">Ir a Página</a>
```

media: Especifica qué tipo de dispositivo o medio de salida es adecuado para el recurso vinculado

```html
<link rel="stylesheet" href="estilos.css" media="screen" />
```

hreflang: Especifica el idioma del recurso vinculado.

```html
<link rel="alternate" hreflang="es" href="pagina-es.html" />
```

charset: Especifica la codificación de caracteres del recurso vinculado.

```html
<link rel="stylesheet" href="estilos.css" charset="UTF-8" />
```

name: Especifica un nombre para el enlace, que se puede utilizar como destino para enlaces internos dentro del mismo documento.

```html
<a href="#seccion2" name="seccion2">Ir a Sección 2</a>
```

## Metadatos

Define la codificación de caracteres del documento HTML.

```html
<meta charset="UTF-8" />
```

Proporciona una descripción breve del contenido del documento.

```html
<meta name="description" content="Descripción breve del documento" />
```

Especifica palabras clave relacionadas con el contenido del documento.

```html
<meta name="keywords" content="palabra1, palabra2, palabra3" />
```

Indica el autor del documento.

```html
<meta name="author" content="Nombre del autor" />
```

Especifica cómo se debe controlar la escala y el ancho de la ventana gráfica en dispositivos móviles.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

Refresca automáticamente la página después de un tiempo especificado.

```html
<meta http-equiv="refresh" content="5;url=https://www.ejemplo.com" />
```

Define el nombre de la aplicación web.

```html
<meta name="application-name" content="Nombre de la Aplicación" />
```

## Elementos de Texto

- ### Etiquetas para Texto.

(Paragraph): Define un párrafo de texto.

```html
<p>Este es un párrafo de texto.</p>
```

(Heading): Define encabezados de diferentes niveles.

```html
<h1>Encabezado de nivel 1</h1>
```

> Va desde h1 hasta h6 (el mas pequeño).

Define un contenedor de texto en línea.

```html
<span>Texto en línea</span>
```

Define texto importante resaltado visualmente.

```html
<strong>Texto importante</strong>
```

(Emphasis): Define texto enfatizado.

```html
<em>Texto enfatizado</em>
```

(Italic): Define texto en cursiva.

```html
<i>Texto en cursiva</i>
```

(Underline): Define texto subrayado.

```html
<u>Texto subrayado</u>
```

(Bold): Define texto en negrita.

```html
<b>Texto en negrita</b>
```

(Block Quote): Define una cita destacada.

```html
<blockquote>Cita destacada</blockquote>
```

(Code): Define una sección de código.

```html
<code>console.log("Hola Mundo")</code>
```

- ### Atributos para Texto.

id: Define un identificador único para el elemento.

```html
<p id="parrafo1">Texto del párrafo</p>
```

class: Define una o más clases para el elemento.

```html
<span class="destacado">Texto destacado</span>
```

style: Define estilos CSS para el elemento.

```html
<h1 style="color: blue;">Encabezado azul</h1>
```

title: Define información adicional sobre el elemento que se muestra como un tooltip.

```html
<span title="Información adicional">Texto con tooltip</span>
```

lang: Define el idioma del contenido del elemento.

```html
<p lang="es">Texto en español</p>
```

dir: Define la dirección del texto dentro del elemento (ltr: de izquierda a derecha, rtl: de derecha a izquierda).

```html
<p dir="rtl">Texto de derecha a izquierda</p>
```

accesskey: Define una tecla de acceso rápido para enfocar o activar el elemento.

```html
<button accesskey="s">Guardar</button>
```

contenteditable: Indica si el contenido del elemento es editable.

```html
<div contenteditable="true">Texto editable</div>
```

hidden: Oculta el elemento en la página.

```html
<p hidden>Texto oculto</p>
```

spellcheck: Indica si se debe verificar la ortografía del texto del elemento.

```html
<input type="text" spellcheck="true" />
```

## Elementos de Bloque

- ### Etiquetas de bloque.

DIV: Define una sección genérica o un contenedor.

```html
<div>Contenido aquí</div>
```

SECTION: Se utiliza para dividir el contenido en secciones temáticas o áreas distintas.

```html
<section>Contenido de la sección</section>
```

ARTICLE: Se utiliza para representar una composición autónoma, como un artículo, una entrada de blog o un comentario.

```html
<article>Contenido del artículo</article>
```

ASIDE: Se utiliza para representar contenido secundario que está relacionado con el contenido principal, pero que puede ser considerado independiente de él.

```html
<aside>Contenido relacionado</aside>
```

BLOCKQUOTE: Se utiliza para representar una sección de texto que ha sido citada de otro origen.

```html
<blockquote>Cita larga aquí</blockquote>
```

- ### Atributos de bloque.

id: Se utiliza para identificar de manera única un elemento en un documento HTML.

```html
<div id="seccion1">Contenido de la sección</div>
```

class: Se utiliza para aplicar estilos o comportamientos específicos a uno o más elementos.

```html
<article class="contenido">Contenido del artículo</article>
```

style: Se utiliza para aplicar estilos específicos directamente al elemento.

```html
<header style="background-color: #f0f0f0;">Encabezado de la página</header>
```

title: Define información adicional sobre el elemento que se muestra como un tooltip.

```html
<footer title="Pie de página">Información adicional</footer>
```

role: Se utiliza para especificar el papel del elemento para tecnologías de asistencia como lectores de pantalla.

```html
<nav role="navigation">Enlaces de navegación</nav>
```

hidden: Se utiliza para ocultar un elemento del diseño de la página.

```html
<aside hidden>Contenido relacionado</aside>
```

## Elementos de Formato de Texto

- ### Etiquetas de Formato de Texto.

STRONG: Define texto importante visualmente resaltado.

```html
<strong>Texto importante</strong>
```

EM: Define texto enfatizado.

```html
<em>Texto enfatizado</em>
```

U: Define texto subrayado.

```html
<u>Texto subrayado</u>
```

B: Define texto en negrita.

```html
<b>Texto en negrita</b>
```

I: Define texto en cursiva.

```html
<i>Texto en cursiva</i>
```

SMALL: Define texto más pequeño.

```html
<small>Texto pequeño</small>
```

MARK: Define texto resaltado o marcado.

```html
<mark>Texto marcado</mark>
```

DEL: Define texto eliminado o tachado.

```html
<del>Texto eliminado</del>
```

INS: Define texto insertado.

```html
<ins>Texto insertado</ins>
```

SUB: Define texto subíndice.

```html
<sub>Texto subíndice</sub>
```

- ### Atributos de Formato de Texto.

lang: Define el idioma del contenido del elemento.

```html
<i lang="en">Texto en cursiva</i>
```

dir: Define la dirección del texto dentro del elemento (ltr: de izquierda a derecha, rtl: de derecha a izquierda).

```html
<small dir="rtl">Texto pequeño</small>
```

aria-label: Define una etiqueta accesible para el elemento.

```html
<mark aria-label="Texto marcado">Texto marcado</mark>
```

aria-describedby: Define el identificador de otro elemento que proporciona una descripción del elemento actual.

```html
<del aria-describedby="descripcion">Texto eliminado</del>
```

## Comentarios

Este es el tipo de comentario más básico en HTML y se utiliza para incluir comentarios que no se muestran en la página web. Todo el texto dentro de el es ignorado por el navegador.

```html
<!-- ... -->
```

Este tipo de comentario condicional se utiliza para dirigir estilos y scripts específicamente a versiones antiguas de Internet Explorer.

```html
<!--- [if IE]> ... <![endif]-->
```

## Otros
