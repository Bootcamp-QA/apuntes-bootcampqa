# Cómo obtener los datos necesarios en Postman para GitHub Actions

Para ejecutar una colección privada de Postman en GitHub Actions con Newman, necesitas tres datos: URL de la colección, API Key y URL del environment. A continuación se explica cómo obtener cada uno.

---

## 1. URL de la colección

1. Abre Postman y ve a la pestaña **Collections** en el panel izquierdo.
2. Selecciona la colección que quieres usar.
3. Haz clic en los **tres puntos (⋮)** al lado del nombre de la colección y elige **Share Collection**.
4. Selecciona **Get a public link** o **Get a link via API** (si la colección es privada, necesitarás la API Key para autenticación).
5. Copia la URL que aparece; esta será la URL que usarás en el workflow de GitHub Actions.

> Nota: Aunque tu colección sea privada, la URL combinada con la API Key permitirá que Newman acceda a ella sin exponer tu colección públicamente.

---

## 2. Postman API Key

1. Abre Postman y haz clic en tu avatar (esquina superior derecha) y selecciona **Settings**.
2. Ve a la pestaña **API Keys**.
3. Haz clic en **Generate API Key**.
4. Pon un nombre descriptivo a la API Key (por ejemplo: `GitHub Actions`).
5. Haz clic en **Generate Key**.
6. Copia la clave generada; esta se usará como secreto en GitHub (`POSTMAN_API_KEY`).

> Nota: Nunca compartas esta clave en repositorios públicos. Siempre guárdala como **Secret** en GitHub Actions.

---

## 3. URL del Environment

1. En Postman, ve a la pestaña **Environments**.
2. Selecciona el environment que deseas usar con la colección.
3. Haz clic en **⋮** al lado del nombre del environment y selecciona **Share Environment**.
4. Elige **Get a link via API** para obtener la URL del environment.
5. Copia esta URL; será usada en el workflow de GitHub Actions (`POSTMAN_ENV_URL`).

> Nota: Esto permite que Newman descargue el environment completo con todas las variables definidas (como tokens, base URL, credenciales de prueba, etc.) sin necesidad de exportar manualmente.

---

Con estos tres datos:  

- **POSTMAN_COLLECTION_URL** → URL de la colección  
- **POSTMAN_API_KEY** → clave privada de Postman  
- **POSTMAN_ENV_URL** → URL del environment  

Ya puedes configurar GitHub Actions para ejecutar la colección automáticamente y generar reportes cada vez que haya cambios.

## Cómo usar estos datos en GitHub Actions

Para ejecutar tu colección de Postman automáticamente desde GitHub y generar reportes, sigue estos pasos:

---

### 1. Guardar cada dato como secreto en GitHub

1. Ve a tu repositorio en GitHub.
2. Haz clic en **Settings** → **Secrets and variables** → **Actions** → **New repository secret**.
3. Crea los siguientes secretos:

   - `POSTMAN_API_KEY` → tu API Key de Postman.
   - `POSTMAN_COLLECTION_URL` → URL de la colección.
   - `POSTMAN_ENV_URL` → URL del environment.

> Nota: Los secretos se mantienen privados y no se exponen en los logs de GitHub Actions.

---

### 2. Usar los secretos en el workflow de GitHub Actions

1. Crea un archivo de workflow en `.github/workflows/run_postman.yml`.
2. Dentro del workflow, configura los pasos para ejecutar Newman usando los secretos:

   - Descargar la colección desde la URL usando la API Key.
   - Descargar el environment desde la URL usando la API Key.
   - Ejecutar los tests de la colección aplicando las variables del environment.

> Esto permite ejecutar automáticamente los tests sin necesidad de exportar manualmente la colección o el environment cada vez que haya cambios.

---

### 3. Generar un reporte HTML automáticamente

1. Configura Newman para generar un reporte en HTML usando la opción `--reporters html`.
2. Cada vez que el workflow se ejecute (automáticamente o manualmente), Newman generará el reporte.
3. Puedes configurar el workflow para guardar el reporte como **artifact** o publicarlo en un directorio accesible dentro del repositorio.

> Esto permite que cualquier miembro del equipo descargue y revise el reporte directamente desde GitHub Actions, sin necesidad de ejecutar Newman localmente.
