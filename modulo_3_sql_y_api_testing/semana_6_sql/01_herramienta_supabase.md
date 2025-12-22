# Herramienta Supabase

# Clase en directo
- Crear cuenta y proyecto en supabase.
- Generar API y documentación en proyecto de github.

# Apuntes

# Manual de Supabase - Bootcamp QA

---

## 1. ¿Qué es Supabase?

**Supabase** es una plataforma online basada en **SQL** que ofrece una solución completa para el backend de aplicaciones.

Incluye:

- Base de datos **PostgreSQL** lista para usar.
- **API REST** automática para cada tabla creada.
- Servicios de **autenticación**, **almacenamiento**, **funciones** y más.

---

## 2. Crear una cuenta

1. Visita 👉 https://supabase.com  
2. Haz clic en **"Start your project"** o **"Sign in"**.  
3. Regístrate con tu cuenta.

---

## 3. Crear un proyecto

1. Haz clic en **"New Project"**.  
2. Rellena los siguientes datos:
   - Nombre del proyecto  
   - Contraseña de la base de datos  
   - Región del servidor  
3. Espera unos segundos mientras Supabase configura el proyecto.

---

## 4. Editor SQL: crear, editar y consultar tablas

- Accede a la sección **"SQL Editor"** desde el menú lateral.
- Permite:
  - Ejecutar sentencias SQL directamente.
  - Crear tablas.
  - Editar estructuras.
  - Realizar consultas sobre tablas existentes.

---

## 5. Ver registros y tablas creadas

- Accede a **"Table Editor"**.
- Selecciona la tabla creada.
- Desde aquí puedes:
  - Ver todos los registros.
  - Insertar datos manualmente.
  - Editar registros existentes.
  - Eliminar registros desde la interfaz gráfica.

---

## 6. Ver la API generada automáticamente

Supabase genera automáticamente una **API RESTful** para cada tabla.

Para ver la documentación de la API:

1. Ve a **"Table Editor"**.
2. Selecciona una tabla (por ejemplo, `usuarios`).
3. Haz clic en la pestaña **"API Docs"** (arriba a la derecha).
4. Se abrirá la documentación autogenerada con ejemplos de:
   - **GET** (listar registros)
   - **POST** (insertar)
   - **PATCH** (editar)
   - **DELETE** (eliminar)
   - Filtros, paginación y ordenación

Las URLs pueden copiarse y probarse directamente en **Postman** o en tu aplicación.

---

## 7. Ver el endpoint base (Project URL)

1. Ve a **"Settings" → "Data API"**.
2. Copia la URL base del proyecto

---

## 8. Obtener tu API Key

1. Ve a **"Project Settings" → "API Keys"**.
2. En la pestaña **"API Keys"** encontrarás las claves dentro de **"Secret Keys"**.


## 9.Generar documentación de la API

Sigue estos pasos para generar la documentación de la API y dejarla lista para guardarla en GitHub.

### Pasos

1. Abre el generador de documentación de la API en tu navegador:  
   https://bootcamp-qa.github.io/ReportGenerator/documentacionapi.html

2. En el campo **Nombre de la tabla**, introduce el nombre de la tabla de la base de datos para la que deseas generar la documentación.

3. En el campo **Columnas**, escribe los nombres de las columnas separados por comas.  
   - Si una columna es obligatoria, añade un **asterisco (*)** junto a su nombre.  
   - Ejemplo de formato: `id*, nombre*, email, edad, activo`

4. En el campo **Base URL**, introduce la URL base de la API (endpoint principal) que utilizará la documentación.

5. Genera la documentación. El sistema creará automáticamente el contenido de la API con los datos introducidos.

6. Guarda el archivo generado en formato **HTML**.

7. Nombra el archivo como **`apidocs.html`**.

8. Sube el archivo **apidocs.html** a tu repositorio de GitHub. La documentación quedará lista para ser compartida o publicada.
