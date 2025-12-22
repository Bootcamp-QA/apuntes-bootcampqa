# Tema 2.5 Validación de formularios en html5

# Video de la clase


[Ver clase: Formularios y validaciones html5 - 20 min](https://bootcampqa.com/videos/herramientasdegestiondepruebas.mp4)

# Apuntes

## ¿Qué es un formulario en HTML5?
Un **formulario en HTML5** es un conjunto de campos dentro de una página web que permite a los usuarios introducir y enviar datos a un servidor.  
Está contenido dentro de la etiqueta `<form>` y puede incluir distintos tipos de elementos de entrada como campos de texto, botones de radio, casillas de verificación (checkbox), menús desplegables, campos de carga de archivos, entre otros.

El formulario generalmente se utiliza para recopilar información como datos personales, comentarios o realizar búsquedas. Los datos introducidos son enviados al servidor para ser procesados o almacenados.

[Ver clase: Formularios HTML5 - 10 min](https://www.w3schools.com/html/html_forms.asp)

---

## Estructura Básica de un formulario
Para crear un formulario en HTML5 se utiliza la etiqueta `<form>` y dentro se colocan los diferentes campos de entrada como texto, contraseñas, correos, etc.

[Ver documentación oficial: Estructura básica de formularios - 10 min](https://www.w3schools.com/html/html_forms.asp)
```
<form action="/submit" method="post">
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" required>

  <label for="email">Correo Electrónico:</label>
  <input type="email" id="email" name="email" required>

  <input type="submit" value="Enviar">
</form>
```

---

## Tipos de Inputs en HTML5

### Input de Texto (`text`)
Este es el tipo de campo más básico, para cualquier entrada textual.  
**Validaciones:** `maxlength`, `required`.

[Ver documentación oficial: Input Texto - 10 min](https://www.w3schools.com/html/html_form_input_types.asp)

```
<label for="usuario">Usuario:</label>
<input type="text" id="usuario" name="usuario" required maxlength="20">
```

---

### Input de Correo Electrónico (`email`)
Valida automáticamente que el formato ingresado corresponda a un correo electrónico.  
**Validaciones:** `required`, `multiple`.

[Ver documentación oficial: Input Email - 10 min](https://www.w3schools.com/html/html_form_input_types.asp)

```
<label for="email">Correo electrónico:</label>
<input type="email" id="email" name="email" required multiple>

```

---

### Input de Contraseña (`password`)
Oculta el texto introducido, ideal para contraseñas.  
**Validaciones:** `required`, `minlength`.

[Ver documentación oficial: Input Contraseña - 10 min](https://www.w3schools.com/html/html_form_input_types.asp)

```
<label for="password">Contraseña:</label>
<input type="password" id="password" name="password" required minlength="6">

```

---

### Input de Número (`number`)
Permite que los usuarios introduzcan solo números.  
**Validaciones:** `min`, `max`, `step`, `required`.

[Ver documentación oficial: Input Número - 10 min](https://www.w3schools.com/html/html_form_input_types.asp)

```
<label for="edad">Edad:</label>
<input type="number" id="edad" name="edad" min="18" max="100" step="1" required>

```

---

### Input de Fecha (`date`)
Permite seleccionar una fecha desde un calendario.  
**Validaciones:** `min`, `max`, `required`.

[Ver documentación oficial: Input Fecha - 10 min](https://www.w3schools.com/html/html_form_input_types.asp)

```
<label for="fecha_nacimiento">Fecha de nacimiento:</label>
<input type="date" id="fecha_nacimiento" name="fecha_nacimiento" required>


```

---

### Checkbox y Radio
**Checkbox:** permite seleccionar múltiples opciones.  
**Radio buttons:** solo permite una opción entre varias.

[Ver documentación oficial: Checkbox y Radio - 10 min](https://www.w3schools.com/html/html_form_input_types.asp)

```
<label for="acepto">Acepto los términos:</label>
<input type="checkbox" id="acepto" name="acepto" required>
<label>Género:</label>
<input type="radio" id="masculino" name="genero" value="masculino" required>
<label for="masculino">Masculino</label>
<input type="radio" id="femenino" name="genero" value="femenino" required>
<label for="femenino">Femenino</label>

```

---

## Botones en Formularios
- **Submit:** envía la información del formulario al servidor.
- **Reset:** restablece los campos a sus valores iniciales.
- **Button:** botón genérico, se usa con JavaScript.

[Ver documentación oficial: Botones en Formularios - 10 min](https://www.w3schools.com/html/html_form_elements.asp)

```
<input type="submit" value="Enviar">
<input type="reset" value="Reiniciar">
<button type="button">Haz clic aquí</button>

```

