# Introducción a HTML5

# Video de la clase


[Ver clase: HTML5 - 40 min](https://bootcampqa.com/videos/introduccionhtml.mp4)

[Ver clase: Modificar HTML5 y subir cambios a github - 10 min](https://bootcampqa.com/videosauto/auto-editar-html-subir-cambios.mp4)

# Apuntes

# Introducción a HTML

## ¿Qué es HTML?
**HTML (HyperText Markup Language)** es un **lenguaje de marcado**, **NO** un lenguaje de programación.

Sirve para **etiquetar los datos de una página web**, de forma que:
- El navegador pueda interpretarlos y mostrarlos correctamente.
- Los buscadores puedan identificarlos y posicionarlos.

**HTML5** es la **última versión** de HTML.

---

## Estructura de un elemento HTML

Un elemento HTML se compone de varias partes que definen su funcionamiento y contenido.

### Partes de un elemento HTML

- **Etiqueta de apertura**  
  Establece dónde comienza el elemento HTML.

- **Etiqueta de cierre**  
  Establece dónde termina el elemento.

- **Contenido**  
  Parte visible del elemento. Generalmente es texto.

- **Atributo**  
  Contiene información adicional sobre el elemento HTML.

```
<p id = ”nombre”> Marco Soto </p>

```

## Estructura de un archivo HTML

[Ver documentación oficial: HTML Elements – W3Schools](https://www.w3schools.com/html/html_elements.asp)


Un archivo HTML básico tiene una estructura estándar que se compone de los siguientes elementos:

- `<!DOCTYPE html>`  
  Indica que el archivo es HTML5. Es obligatorio colocarlo al inicio del documento.

- `<html></html>`  
  Es el **elemento raíz** que encierra todo el contenido de la página.

- `<head></head>`  
  Contiene información sobre la página que **no es visible** para el usuario, como el título, metadatos, enlaces a hojas de estilo y scripts.

- `<body></body>`  
  Contiene todo el contenido **visible** de la página: textos, imágenes, enlaces, tablas, listas, etc.

- `<title></title>`  
  Define el título de la página que se muestra en la pestaña del navegador.

Archivo principal recomendado para la página de inicio: `index.html`.
```
<!DOCTYPE html>
<html>
  <head>
    <title>Mi primera página</title>
  </head>
  <body>
    <h1>Bienvenidos a mi página</h1>
    <p>Este es un párrafo de ejemplo.</p>
  </body>
</html>

```

### Etiquetas META
[Ver documentación oficial: Meta Tags – W3Schools](https://www.w3schools.com/tags/tag_meta.asp)

Las etiquetas **meta** sirven para dar información sobre la página web.  
Van siempre dentro de la sección `<head>` y **no son visibles** para el usuario.

**Información más común:**
- **description**: descripción de la página, útil para buscadores.
- **charset="UTF-8"**: codificación de caracteres para mostrar símbolos especiales.
- **author**: indica el autor de la página.
- **viewport**: adapta el contenido al tamaño del dispositivo  
  (`width=device-width, initial-scale=1.0`).


```
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Página de ejemplo HTML">
  <meta name="author" content="Juan Pérez">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
```

---

### Encabezados (Headings)
[Ver documentación oficial: HTML Headings – W3Schools](https://www.w3schools.com/tags/tag_hn.asp)

Los encabezados indican que el contenido es un **título o subtítulo**.

- Existen **6 niveles**: `h1`, `h2`, `h3`, `h4`, `h5`, `h6`.
- Permiten estructurar el contenido.
- Se recomienda usar **solo un `h1` por página**.

```
<h1>Título Principal</h1>
<h2>Título Secundario</h2>
<h3>Título Terciario</h3>
<h4>Título Nivel 4</h4>
<h5>Título Nivel 5</h5>
<h6>Título Nivel 6</h6>
```


---

### Párrafos (`p`)
[Ver documentación oficial: HTML Paragraphs – W3Schools](https://www.w3schools.com/html/html_paragraphs.asp)

Sirven para encerrar párrafos de contenido textual.

```
<p>Este es un párrafo de texto en HTML.</p>
<p>Este es otro párrafo con más contenido.</p>

```


---

### Comentarios
[Ver documentación oficial: HTML Comments – W3Schools](https://www.w3schools.com/html/html_comments.asp)

Los comentarios sirven al desarrollador para entender el código.  
**No se muestran al usuario**.

```
<!-- Este es un comentario en HTML -->
<p>Texto visible para el usuario</p>

```




---

### Listas (`ul` / `li`)
[Ver documentación oficial: HTML Lists – W3Schools](https://www.w3schools.com/tags/tag_ul.asp)
Las listas sirven para listar elementos.

- **ul** → indica el inicio y fin de la lista.
- **li** → indica cada uno de los elementos que componen la lista.


```
<ul>
  <li>Manzanas</li>
  <li>Lentejas</li>
  <li>Legumbres</li>
</ul>
```

---

### Enlaces (`a`)
[Ver documentación oficial: HTML Links – W3Schools](https://www.w3schools.com/tags/tag_a.asp)
Sirven para incluir enlaces a otras páginas, tanto externas como internas.

**Características:**
- El elemento `a` siempre incluye el atributo **href**.
- **Absoluto**: URL completa (web externa).
- **Relativo**: nombre del archivo HTML interno.
- El texto del enlace es el que se muestra en la página.

```
<!-- Enlace absoluto -->
<a href="https://bootcampqa.com">BootcampQA</a>

<!-- Enlace relativo -->
<a href="index.html">Página principal</a>

```

---

### Imágenes (`img`)

[Ver documentación oficial: HTML Images – W3Schools](https://www.w3schools.com/tags/tag_img.asp)

Sirven para incluir imágenes en la web.

**Atributos obligatorios:**
- **src**: ruta de la imagen (URL externa o archivo local).
- **alt**: descripción de la imagen (texto alternativo).


```
<!-- Imagen externa -->
<img src="https://bootcampqa.com/logo.png" alt="Logo BootcampQA">

<!-- Imagen local -->
<img src="images/logo.png" alt="Logo local">
```

---

### Contenedor (`div`)
[Ver documentación oficial: HTML div – W3Schools](https://www.w3schools.com/tags/tag_div.asp)
El elemento `div` sirve para **agrupar varios elementos HTML**.  
No tiene significado semántico.

Se recomienda usarlo junto con los atributos:
- **class**
- **id**

```
<div class="curso-marketing" id="curso1">
  <h1>Curso Marketing</h1>
  <p>En este curso aprenderás marketing digital.</p>
  <img src="marketing.png" alt="Imagen del curso de marketing">
</div>

```

---

### Iconos (`i`)

Sirven para agregar iconos a una página web.

**Ventajas:**
- Ocupan menos espacio que las imágenes.
- Mejoran el rendimiento de la página.

**Buscar iconos disponibles:**
- [Ver referencia de iconos – W3Schools](https://www.w3schools.com/icons/icons_reference.asp)
- [Ver documentación oficial de iconos – W3Schools](https://www.w3schools.com/icons/default.asp)

```
<i class="fa fa-file"></i>
<i class="fa fa-user"></i>

```

---
