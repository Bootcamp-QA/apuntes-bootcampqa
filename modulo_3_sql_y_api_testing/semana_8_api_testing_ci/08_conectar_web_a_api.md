# COMO CONECTAR TU WEB A UNA API

Aquí aprenderás paso a paso cómo conectar tu web con una API usando el siguiente script de la plantilla: https://github.com/Bootcamp-QA/template-portfolioqa/blob/main/script.js

---

## 1. Agregar el script a tu página

Agrega a tu proyecto el archivo `script.js` disponible en la plantilla, e inclúyelo en la página HTML en la que lo quieras usar:

```html
<script src="script.js" defer></script>
```

---

## 2. Incluye los datos de tu API

Modifica en `script.js` la URL y el API key, y pon los de la API que quieras usar.

```javascript
// Ejemplo
const SUPABASE_URL = 'https://tu-api-url';
const SUPABASE_API_KEY = 'tu_api_key';
```

---

## 3. Enviar datos de formulario a API con POST

Para enviar los datos de tu formulario:

1. Asegúrate de que el formulario llama a la función `enviarFormulario`. Esta función envía los datos del formulario a la API.

2. Inclúyelo en tu `<form>` así, y asegúrate de que cada `input` tenga un **ID único** en toda la página:
3. Incluye tambien un parrafo con id **formMessage** para poder mostrar el mensaje de error o exito cuando envia el formulario

```html
<form onsubmit="return enviarFormulario(event)">
    <input id="nombre" type="text" placeholder="Nombre" />
    <input id="email" type="email" placeholder="Email" required />
    <select id="asunto" required>
      <option value="">---</option>
      <option value="info">Información</option>
      <option value="job">Oferta Trabajo</option>
      <option value="other">Otro</option>
    </select>
    <textarea id="mensaje" rows="4" placeholder="Mensaje"></textarea>
    <button type="submit">Enviar</button>
</form>

<!-- Elemento donde se mostrarán los mensajes de éxito o error -->
<p id="formMessage"></p>
```

3. En el script modifica la función `enviarFormulario`,e indica los campos que debe enviar a tu API y los valores de los inputs del formulario:

```javascript
const data = {
    nombre: document.getElementById('nombre').value,
    email: document.getElementById('email').value,
    asunto: document.getElementById('asunto').value,
    mensaje: document.getElementById('mensaje').value
};
```

> 🔹 **Importante:** Los nombres de los campos corresponden a los de la API, los valores a los IDs de los inputs de tu formulario.

---

## 4. Mostrar datos en la web de una API con GET

Si quieres mostrar los datos de tu API en la página web:

1. Agrega el script a tu proyecto, igual que antes:

```html
<script src="script.js" defer></script>
```

2. Incluye un botón que llame a la función `mostrarDatos` para cargar los datos:

```html
<button id="verMensajes" onclick="mostrarDatos()">Ver mensajes</button>
```

3. Por último, agrega una tabla con id **formsTable** donde se mostrarán los datos:

```html
<table id="formsTable">
</table>
```


