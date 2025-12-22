# Pruebas de Api

# Apuntes

# Manual de API Testing - Bootcamp QA

## ¿Qué es API Testing?

El **API Testing** consiste en verificar que una API funcione correctamente enviando peticiones como GET, POST, PUT, PATCH o DELETE y comprobando que las respuestas sean correctas, tanto en escenarios normales como en situaciones inesperadas.

El objetivo es validar la lógica del backend sin depender de la interfaz gráfica.

---

## ¿Qué se debe probar siempre?

Por cada endpoint se deben cubrir, como mínimo, los siguientes casos:

### 1. Caso válido (happy path)

- Todos los datos enviados son correctos.
- Autenticación correcta, si aplica.
- Se espera una respuesta exitosa con código **2XX** (200, 201, etc.).

---

### 2. Sin autenticación

- No enviar token, API key o credenciales.
- Se espera un código **401** o **403** indicando que no está autorizado o no tiene permisos.

---

### 3. Con datos inválidos

Probar cada campo individualmente con datos incorrectos.

- Texto donde se espera un número.
- Formato de email incorrecto.
- Valores booleanos inválidos.
- En peticiones GET, usar IDs inexistentes o filtros incorrectos.
- En POST, PUT o PATCH, enviar datos erróneos en el body.

Se espera un error controlado con código **4XX** (400, 422, etc.).

---

### 4. Con campos vacíos

Probar los campos obligatorios sin enviarlos o enviándolos vacíos.

- En POST, omitir campos del body o dejarlos vacíos.
- En GET, omitir parámetros obligatorios en la URL si existen.

Se espera un error controlado con código **4XX**.

---

## Organización por tipo de petición

Organizar los tests por tipo de petición ayuda a no olvidar casos importantes.

Se recomienda crear una carpeta para cada tipo de petición:

- GET
- POST
- PUT / PATCH
- DELETE

---

## Buenas prácticas de API Testing

- Probar un solo dato inválido o vacío por test, no todos a la vez.
- Utilizar datos conocidos para poder comparar resultados.
- Los datos creados o modificados durante un test deben eliminarse al finalizar.
- Verificar la base de datos siempre que sea posible para validar el resultado real.

