# Introducción a CSS3

# Video de la clase


[Ver clase: CSS3 - 15 min](https://bootcampqa.com/videos/introduccioncss.mp4)
[Ver clase: Modificar CSS3 y subir cambios a github - 10 min](https://bootcampqa.com/videosauto/auto-editar-css-github.mp4)

# Apuntes
# CSS

## ¿Qué es CSS?
**Cascading Style Sheets (CSS)**  
Se utiliza para definir el diseño de una página web: colores, tamaños, márgenes.  
Permite separar el diseño del contenido.

[Documentación oficial: Introducción a CSS](https://www.w3schools.com/css/css_intro.asp)

---

## Sintaxis de CSS
Un estilo CSS se compone de:  
- **Selector CSS:** indica a qué elemento se aplicará el estilo  
- **Propiedad CSS:** define qué característica se quiere cambiar (color, alineación, tamaño, etc.)  
- **Valor:** indica el valor que se asignará a la propiedad

[Documentación oficial: Sintaxis CSS](https://www.w3schools.com/css/css_intro.asp)


```
h1 {
  color: red;
}
```

---

## Cómo añadir CSS
Se recomienda siempre usar un archivo CSS externo:  
1. Crear un archivo `.css`  
2. Incluirlo en el `<head>` de tu HTML mediante `<link>`  

[Documentación oficial: Cómo añadir CSS](https://www.w3schools.com/css/css_intro.asp)

---

## Propiedades básicas de CSS

### Fondo (background)
Define el color o imagen de fondo de un elemento.

[Documentación oficial: Propiedad Background](https://www.w3schools.com/css/css_background.asp)


```
body {
  background-color: lightblue;
}
```


---

### Texto
- **Color (`color`)**: define el color del texto  
  [Documentación oficial: Color de texto](https://www.w3schools.com/css/css_text.asp)  
- **Alineación (`text-align`)**: define la alineación del texto (center, left, right)  
  [Documentación oficial: Alineación de texto](https://www.w3schools.com/css/css_text_align.asp)

```
h1 {
  color: red;
}

p {
  text-align: center;
}

```
---

### Fuentes
- **Font-family**: indica el tipo de letra  
- **Font-size**: indica el tamaño del texto

[Documentación oficial: Fuentes](https://www.w3schools.com/css/css_font.asp)  
[Documentación oficial: Tamaño de fuente](https://www.w3schools.com/css/css_font_size.asp)

```
h1 {
  font-family: Arial, sans-serif;
  font-size: 36px;
}

```
---

### Tamaño (Height y Width)
Define la altura y anchura de un elemento.

[Documentación oficial: Dimensiones (Height/Width)](https://www.w3schools.com/css/css_dimension.asp)


```
img {
  width: 200px;
  height: 150px;
}


```

---

### Márgenes (Margin)
Define los márgenes de un elemento: superior, inferior, izquierdo y derecho.

[Documentación oficial: Márgenes](https://www.w3schools.com/css/css_margin.asp)
```
body {
  margin-top: 20px;
  margin-bottom: 20px;
  margin-left: 10px;
  margin-right: 10px;
}


```
