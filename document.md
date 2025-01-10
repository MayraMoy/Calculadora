<h1>Anotaciones de conceptos que no recuerdo</h1>

<h1>HTML</h1>

<h2>DOCTYPE html </h2>

<p>Es una declaración que se coloca al principio de un documento HTML para indicar al navegador que el documento está escrito en HTML5. Esto ayuda al navegador a interpretar y renderizar correctamente el contenido del documento.</p>

<h2>head</h2>

<p>

La etiqueta `<head>` en HTML es una sección del documento que contiene metadatos y enlaces a recursos externos que son necesarios para la página web. Esta sección se encuentra al principio del documento HTML, justo después de la etiqueta `<html>` y antes de la etiqueta `<body>`.

Dentro de la etiqueta `<head>`, puedes incluir varios elementos importantes como `<title>`, que define el título de la página que aparece en la pestaña del navegador; `<meta>`, que proporciona metadatos como la descripción de la página, palabras clave y la codificación de caracteres; `<link>`, que se utiliza para enlazar hojas de estilo CSS externas; y `<script>`, que se usa para incluir o enlazar archivos JavaScript.

</p>

<h2>div</h2>

<p>

La etiqueta `<div>` en HTML es un contenedor genérico utilizado para agrupar elementos de la página web y aplicarles estilos o scripts de manera conjunta. La etiqueta `<div>` no tiene un significado semántico específico, lo que significa que no aporta información sobre el contenido que contiene. En cambio, se utiliza principalmente para estructurar y organizar el contenido de la página.

</p>

<h1>CSS</h1>

<h2>*</h2>

<p>Aplica un conjunto de estilos a todos los elementos de la página web. Esto se logra utilizando el selector universal *, que selecciona todos los elementos del documento.</p>

El bloque de código CSS proporcionado aplica un conjunto de estilos a todos los elementos de la página web. Esto se logra utilizando el selector universal `*`, que selecciona todos los elementos del documento.

1. **`padding: 0;`**: Establece el relleno interno de todos los elementos a cero. El relleno es el espacio entre el contenido de un elemento y su borde.

2. **`margin: 0;`**: Establece el margen externo de todos los elementos a cero. El margen es el espacio fuera del borde de un elemento que separa ese elemento de otros elementos.

3. **`box-sizing: border-box;`**: Cambia el modelo de caja de todos los elementos para incluir el relleno y el borde en el ancho y alto total del elemento. Esto facilita el diseño de elementos, ya que el tamaño total del elemento no cambia al agregar relleno o borde.

4. **`outline: 0;`**: Elimina cualquier contorno que pueda aparecer alrededor de los elementos cuando son enfocados o seleccionados. Los contornos son líneas que rodean un elemento para indicar que está activo o enfocado.

5. **`transition: all 0.5s ease;`**: Aplica una transición suave a todos los cambios de estilo en los elementos, con una duración de 0.5 segundos y una función de tiempo "ease". Esto hace que los cambios de estilo, como el color o el tamaño, se animen suavemente en lugar de ocurrir instantáneamente.

<h2>a</h2>

<p>

Aplica estilos específicos a todos los elementos `<a>` (enlaces) de la página web.

</p>

1. **`text-decoration: none;`**: Esta propiedad elimina cualquier decoración de texto predeterminada de los enlaces, como el subrayado. Por defecto, los navegadores suelen subrayar los enlaces para indicar que son interactivos. Al establecer `text-decoration` en `none`, se elimina este subrayado, lo que puede ser útil para aplicar estilos personalizados a los enlaces.

<h1>JavaScript</h1>

<p>Primera Parte</p>

1. **`const display = document.querySelector('#display');`**: Esta línea utiliza el método `querySelector` del objeto `document` para seleccionar el primer elemento en el DOM que coincide con el selector CSS `#display`. El selector `#display` se refiere a un elemento con el atributo `id` igual a "display". El elemento seleccionado se asigna a la constante `display`, lo que permite manipularlo más adelante en el código. 

2. **`const buttons = document.querySelectorAll('button');`**: Esta línea utiliza el método `querySelectorAll` del objeto `document` para seleccionar todos los elementos en el DOM que coinciden con el selector CSS `button`. El selector `button` se refiere a todos los elementos `<button>` en la página. El método `querySelectorAll` devuelve una NodeList (una colección de nodos) que contiene todos los elementos `<button>` encontrados. Esta colección se asigna a la constante `buttons`, permitiendo iterar y manipular cada botón individualmente.

<p>Segunda Parte</p>

1. **buttons.forEach((item) => { ... })**: Itera sobre cada botón en la colección buttons.

2. **item.onclick = () => { ... }**: Asigna una función de flecha como controlador de eventos onclick para cada botón. Esta función se ejecutará cuando el botón sea clicado.

3. **`if (item.id == 'clear') { ... }`**: Si el id del botón es "clear", se limpia el contenido del elemento display estableciendo su innerText a una cadena vacía.

4. **`else if (item.id == 'backspace') { ... }`**: Si el id del botón es "backspace", se elimina el último carácter del texto en el elemento display. Convierte el texto a una cadena, luego utiliza substr para obtener una subcadena que excluye el último carácter y actualiza el innerText del display.

5. **`else if (display.innerText != '' && item.id == 'equal') { ... }`**: Si el id del botón es "equal" y el display no está vacío, se evalúa la expresión matemática contenida en el display utilizando la función eval y se actualiza el innerText del display con el resultado.

6. **`else if (display.innerText == '' && item.id == 'equal') { ... }`**: Si el id del botón es "equal" y el display está vacío, se muestra el texto "Empty" en el display y luego se borra después de 2 segundos utilizando setTimeout.

7. **`else { ... }`**: Para cualquier otro botón, se agrega el id del botón al texto actual del display. Esto permite construir expresiones matemáticas a medida que se presionan los botones.

<p>Tercera Parte</p>

1. **`const themeToggleBtn = document.querySelector('.theme-toggler');`**: Selecciona el botón que se utiliza para alternar el tema, utilizando el selector de clase `.theme-toggler`. Este elemento se asigna a la constante `themeToggleBtn`.

2. **`const calculator = document.querySelector('.calculator');`**: Selecciona el contenedor principal de la calculadora, utilizando el selector de clase `.calculator`. Este elemento se asigna a la constante `calculator`.

3. **`const toggleIcon = document.querySelector('.toggler-icon');`**: Selecciona el icono dentro del botón de alternancia de tema, utilizando el selector de clase `.toggler-icon`. Este elemento se asigna a la constante `toggleIcon`.

4. **`let isDark = true;`**: Declara una variable booleana `isDark` que se utiliza para rastrear el estado actual del tema. Inicialmente, se establece en `true`, asumiendo que el tema oscuro está activado por defecto.

5. **`themeToggleBtn.onclick = () => { ... }`**: Asigna una función de flecha como controlador de eventos `onclick` para el botón de alternancia de tema. Esta función se ejecutará cuando el botón sea clicado.

6. **`calculator.classList.toggle('dark');`**: Alterna la clase `dark` en el elemento `calculator`. Si la clase `dark` está presente, se elimina; si no está presente, se agrega. Esto cambia el tema de la calculadora entre claro y oscuro.

7. **`themeToggleBtn.classList.toggle('active');`**: Alterna la clase `active` en el botón de alternancia de tema. Esto puede ser utilizado para cambiar la apariencia del botón cuando se activa o desactiva.

8. **`isDark = !isDark;`**: Invierte el valor de la variable `isDark`. Si `isDark` es `true`, se establece en `false`, y viceversa. Esto actualiza el estado actual del tema.



