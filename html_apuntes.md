# Información y Apuntes HTML

> Se realizarán cambios mientras más se vaya agregando información en los apuntes. Mientras tanto se realizará la siguiente clasificación:

## Clasificación de comandos GIT:

- Estructura básica
- Etiquetas (Tags)
- Atributos (Attributes)
- Formularios (Forms)
- Multimedia
- Listas
- Tablas
- Enlaces (Links)
- Metadatos
- Elementos de Texto
- Elementos de Bloque
- Elementos de Semántica
- Elementos de Formato de Texto
- Elementos de HTML5
- Elementos de Accesibilidad
- Comentarios
- Otros

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

## Listas

## Tablas

## Enlaces (Links)

## Metadatos

## Elementos de Texto

## Elementos de Bloque

## Elementos de Semántica

## Elementos de Formato de Texto

## Elementos de HTML5

## Elementos de Accesibilidad

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
