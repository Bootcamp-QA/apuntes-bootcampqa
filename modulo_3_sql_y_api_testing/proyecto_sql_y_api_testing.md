# PROYECTO SQL Y API TESTING

## Descripción del Proyecto

En este proyecto se trabajará con **SQL y API Testing** utilizando **Supabase**, **GitHub** y **Postman**.  
El objetivo es crear una base de datos, ejecutar consultas SQL y realizar pruebas completas sobre una API REST.

Es **muy importante respetar exactamente el nombre de los campos** definidos en la base de datos y en la API, ya que cualquier cambio en los nombres puede provocar errores en las consultas y peticiones.

Puede hacerse en inglés (recomendado) o español. Importante, todo el proyecto debe mantenerse **en un solo idioma** de forma consistente.

---

## Semana 6: SQL **40%**

### 1. Configuración
1. Crear un nuevo proyecto en Supabase y realiza las siguientes consultas SQL
2. En el proyecto portafolio, actualiza el `README.md` e incluye tu enlace al proyecto de Supabase.
3. Guarda las consultas sql en la carpeta sql de tu proyecto de portfolio.

### 2. Crear Tabla `create.sql`  **5%**

1. Crear una tabla con los siguientes campos:
   1. id
   2. name (opcional)
   3. email (obligatorio)
   4. subject (obligatorio)
   5. age (numérico, opcional, mayor que 18)
   6. message (obligatorio, máximo 500 caracteres)

---

### 3. Insertar Datos `insert.sql` **5%**

Insertar **10 registros de prueba** en la tabla utilizando como referencia los siguientes datos:

| name   | email              | age   | subject       | message              |
|--------|--------------------|-------|---------------|----------------------|
| ana    | ana@gmail.com      | vacío | information   | hola testing         |
| vacío  | pedro@gmail.com    | 20    | job           | pedro mensaje        |
| maria  | maria@yahoo.com    | 25    | other         | mensaje de prueba    |
| ana    | ana.work@gmail.com | 30    | job           | test message         |
| vacío  | user1@gmail.com    | 22    | information   | mensaje testing      |
| pedro  | pedro@test.com     | 35    | other         | test mensaje largo   |
| juan   | juan@gmail.com     | vacío | job           | hola qa testing      |
| ana    | ana.test@mail.com  | 28    | information   | mensaje con test     |
| vacío  | contact@gmail.com  | 40    | job           | test email gmail     |
| laura  | laura@mail.com     | 19    | other         | mensaje final test   |

---

### 4. Consultas SQL  **20%**

1. Consultar todos los datos.
2. Filtrar por nombre `ana`.
3. Filtrar por nombre vacío.
4. Filtrar por nombre que empiece por `a`.
5. Filtrar por edad entre 20 y 30.
6. Filtrar por asunto `job` e `information`.
7. Filtrar por nombre `maria` o `ana`.
8. Filtrar por email que contenga `gmail` y asunto `job`.
9. Filtrar por edad mayor a 30 y mensaje que contenga `test`.
10. Mostrar los datos ordenados por email de la A a la Z.

---

### 5. Actualizar Datos `update.sql`  **5%**

1. Cambiar email de laura por `lauratest@gmail.com`.
2. Cambiar edad 20 por a 21.

---

### 6. Eliminar Datos `delete.sql`  **5%**

1. Eliminar todos los registros con edad 30.
2. Eliminar todos los registros con nombre `pedro`.



---

## Semana 7: API Testing  **45%**

### 1. Documentación de la API  **5%**

1. Generar una API con Supabase.
2. Crear la documentación de la API.
3. Crear una carpeta llamada `api testing` y agregar la documentación.
4. Actualizar el `README.md` con el enlace al proyecto de Postman.

---

### 2. Peticiones GET **10%**

#### Casos Positivos
1. GET con nombre válido.
2. GET con asunto válido.
3. GET con edad válida.
4. GET con email válido.

Agrega test para validar códigos de respuesta y contenido de respuesta.

#### Casos Negativos
5. GET sin autenticación.
6. GET con nombre que no exista.
7. GET con asunto que no exista.
8. GET con edad inválida.
9. GET con email que no exista.

Agrega test para validar códigos de respuesta.

---

### 3. Peticiones PATCH (Editar) **10%**

Usar siempre el mismo registro identificado por `id`:

1. PATCH editar nombre válido.
2. PATCH editar asunto válido.
3. PATCH editar edad válida.
4. PATCH editar email válido.
5. PATCH sin autenticación.
6. PATCH editar nombre vacío.
7. PATCH editar asunto vacío.
8. PATCH editar edad vacía.
9. PATCH editar email vacío.
10. PATCH editar edad inválida (menor a 18).
11. PATCH restaurar todos los valores originales (nombre, asunto, edad, email).

Agrega test para validar códigos de respuesta.

---

### 4. Peticiones POST **10%**

1. POST con todos los campos obligatorios y opcionales válidos (nombre `apitest`).
2. POST solo con campos obligatorios, sin nombre ni edad (nombre `apitestoptional`).
3. POST sin autenticación.
4. POST sin campo obligatorio email.
5. POST sin campo obligatorio asunto.
6. POST sin campo obligatorio mensaje.

Agrega test para validar códigos de respuesta.

---

### 5. Peticiones DELETE **10%**

1. DELETE por nombre `apitest`.
2. DELETE por nombre `apitestoptional`.
3. DELETE sin autenticación.
4. DELETE por email vacío.
5. DELETE por asunto vacío.
6. DELETE por edad inválida (valor texto).

Agrega test para validar códigos de respuesta.

---

## Semana 8: Integración Continua con GitHub **15%**

### 1. Integración con Proyecto HTML  **5%**

1. Integrar la API con el proyecto HTML.
2. Modificar el script incluyendo el enlace y la contraseña.
3. Comprobar que la integración funciona correctamente.

### 2. Ejecución de Postman desde GitHub  **10%**

1. Configurar el proyecto de GitHub para ejecutar automáticamente las colecciones de Postman.


