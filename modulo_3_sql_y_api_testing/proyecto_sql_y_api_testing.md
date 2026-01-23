# PROYECTO SQL Y API TESTING

## Descripción del Proyecto

En este proyecto se trabajará con **SQL y API Testing** utilizando **Supabase**, **GitHub** y **Postman**.  
El objetivo es crear una base de datos para almacenar los datos del formulario de tu portafolio, ejecutar consultas SQL y realizar pruebas completas sobre una API REST.

Es **muy importante respetar exactamente el nombre de los campos** definidos en la base de datos y en la API, ya que cualquier cambio en los nombres puede provocar errores en las consultas y peticiones.

Puede hacerse en inglés (recomendado) o español. Importante, todo el proyecto debe mantenerse **en un solo idioma** de forma consistente.

---

## Entrega 1: SQL 

### Objetivo 1: Configurar proyecto Base de Datos en Supabase
1. Crear un nuevo proyecto en Supabase
2. En tu proyecto portafolio, actualiza el `README.md` e incluye tu enlace al proyecto de Supabase.
3. Comparte el proyecto supabase con mybootcampqa@gmail.com para su corrección.


### Objetivo 2: Crear Tabla SQL

1. Crear en supabase una tabla con los siguientes campos y agrega a la carpeta sql un archivo create.sql con la query en tu proyecto de github.
   1. id autoincremento
   2. name (opcional)
   3. email (obligatorio)
   4. subject (obligatorio)
   5. age (numérico, opcional, mayor que 18)
   6. message (obligatorio, máximo 500 caracteres)
  

---

### Objetivo 3: Insertar Datos SQL

1. Insertar los siguientes **10 registros de prueba** en la tabla y agrega a la carpeta sql de tu proyecto de github un archivo insert.sql con las consultas.
   
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

### Objetivo 4. Consultas SQL 

1. Realiza las siguientes consultas SQL,y agrega a la carpeta sql de tu proyecto de github un archivo select.sql con las consultas.
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

### Objetivo 5:Actualizar y eliminar datos en SQL

Realiza las siguientes consultas SQL, y agrega a la carpeta sql de tu proyecto de github un archivo update.sql con las consultas.

1. Cambiar email de laura por `lauratest@gmail.com`.
2. Cambiar edad 20 por a 21.
3. Eliminar todos los registros con edad 30.
4. Eliminar todos los registros con nombre `pedro`.



---

## Entrega 2: API Testing  

### Objetivo 6: Generar API y su Documentación:
1. Generar una API con Supabase a partir de la base de datos creada.
2. Genera la documentación de la API y agregala a tu proyecto de github.
3. Crea una cuenta y una colección en postman para probar la API.
4. Actualizar el `README.md` con el enlace al proyecto de Postman.
5. Comparte el proyecto postman con mybootcampqa@gmail.com para su corrección.

---

### Objetivo 7: Peticiones GET

#### Casos Positivos
Crea las peticiones y agrega test para validar códigos de respuesta y contenido de respuesta. Usa variables.
1. GET con nombre válido.
2. GET con asunto válido.
3. GET con edad válida.
4. GET con email válido.

#### Casos Negativos
Crea las peticiones y agrega test para validar códigos de respuesta. Usa variables.
5. GET sin autenticación.
6. GET con nombre que no exista.
7. GET con asunto que no exista.
8. GET con edad inválida.
9. GET con email que no exista.

---

### Objetivo 8: Peticiones PATCH (Editar)
Crea las peticiones y agrega test para validar códigos de respuesta. Usa variables.
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



---

### Objetivo 9: Peticiones POST
Crea las peticiones y agrega test para validar códigos de respuesta. Usa variables.
1. POST con todos los campos obligatorios y opcionales válidos (nombre `apitest`).
2. POST solo con campos obligatorios, sin nombre ni edad (nombre `apitestoptional`).
3. POST sin autenticación.
4. POST sin campo obligatorio email.
5. POST sin campo obligatorio asunto.
6. POST sin campo obligatorio mensaje.


---

### Objetivo 10: Peticiones DELETE
Crea las peticiones y agrega test para validar códigos de respuesta. Usa variables.
Usa para borrar los nombres que usaste para crear en POST. Es decir, si creaste un nombre apitest en delete borra por nombre apitest.
1. DELETE por nombre `apitest`.
2. DELETE por nombre `apitestoptional`.
3. DELETE sin autenticación.
4. DELETE por email vacío.
5. DELETE por asunto vacío.
6. DELETE por edad inválida (valor texto).

Agrega test para validar códigos de respuesta.

---

## Semana 8: Integración Continua con GitHub

### Objetivo 11: Integración con Proyecto Web 

1. Integrar la API con el proyecto HTML.
2. Modificar el script incluyendo el enlace y la contraseña.
3. Comprobar que la integración funciona correctamente.

### Objetivo 12: Ejecución de Postman desde GitHub

1. Configurar el proyecto de GitHub para ejecutar automáticamente las colecciones de Postman.


# CRITERIOS DE EVALUACIÓN

- Completo: Todos los requisitos completados.
- Casi completo: 2 requisitos incompletos o 1 requisito sin realizar.
- Parcialmente completo: Más de 2 requisitos incompletos o más de 1 requisito sin realizar.
- Incompleto: No realizado.


| Objetivo de aprendizaje                                                      | Completo | Casi completo | Parcialmente completo | Incompleto |
| ---------------------------------------------------------------------------- | -------- | ------------- | --------------------- | ---------- |
| **1.Configurar proyecto Base de Datos en Supabase **                                          | 5%       | 4%            | 2%                    | 0%         |
| **2.Crear tabla SQL**                                                          | 5%       | 4%            | 2%                    | 0%         |
| **3.Insertar datos en SQL**                                                    | 10%      | 8%            | 5%                    | 0%         |
| **4.Crear consultas SQL**                                                      | 15%      | 10%           | 5%                    | 0%         |
| **5.Actualizar y eliminar datos en SQL**                                       | 5%       | 4%            | 2%                    | 0%         |
| **6.Generar API y documentación de la API y configurar POSTMAN **                        | 5%       | 4%            | 2%                    | 0%         |
| **7.Pruebas de peticiones API GET con Postman (tests y variables)**            | 10%      | 8%            | 5%                    | 0%         |
| **8.Pruebas de peticiones API PATCH con Postman (tests y variables)**          | 10%      | 8%            | 5%                    | 0%         |
| **9.Pruebas de peticiones API POST con Postman (tests y variables)**           | 10%      | 8%            | 5%                    | 0%         |
| **10.Pruebas de peticiones API DELETE con Postman (tests y variables)**         | 10%      | 8%            | 5%                    | 0%         |
| **11.Integrar la API en un proyecto web**                                       | 5%       | 4%            | 2%                    | 0%         |
| **12.Configurar CI con GitHub Actions para ejecutar pruebas de API con Newman** | 10%      | 8%            | 5%                    | 0%         |


Para superar el módulo, el proyecto debe obtener una calificación final igual o superior al 65%.

El proyecto se realiza de forma individual.
