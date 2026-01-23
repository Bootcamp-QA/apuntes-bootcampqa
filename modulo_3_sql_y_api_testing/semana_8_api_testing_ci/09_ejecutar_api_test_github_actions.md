# Ejecución de Tests de Postman en GitHub Actions

Este documento explica cómo configurar y entender un workflow de GitHub Actions que ejecuta automáticamente tests de Postman usando Newman, descarga la colección y el environment desde la API de Postman y genera un reporte HTML.

## 1. Configuración previa en Postman

Antes de tocar GitHub, necesitamos obtener tres cosas desde Postman:

### 1.1 Obtener la URL (ID) de la colección

Abre Postman y selecciona la colección que quieres ejecutar.

Haz clic en los tres puntos (⋮) → Share.

Copia el id de la colección de la url:

Formato de la URL:

https://api.getpostman.com/collections/33801345-181c803c-a263-4988-9141-4482d833ab13

### 1.2 Obtener el ID del Environment

En Postman, ve a Environments y Selecciona el environment.

Haz clic en Share y copia el ID del Environment:

Formato:

https://api.getpostman.com/environments/33801345-181c803c-a263-4988-9141-4482d833eb4c

### 1.3 Obtener el API Key de Postman

Ve a Postman → Settings.

Abre la pestaña API Keys.

Genera una nueva clave.

Guarda el valor, lo necesitaremos en GitHub.

## 2. Configurar el secreto en GitHub

En el repositorio de github ve a Settings
Luego a Secrets and variables → Actions
Y luego a New repository secret

Crear este secreto:

Nombre: POSTMAN_API_KEY

Valor: tu API Key de Postman

## 3. Agrega la url de la colección y el environment de POSTMAN a github workflow

Abre el archivo de github workflow que estará en la carpeta .github/workflow.
Busca en el archivo del workflow la url de la colección y cambiala por por la de tu colección de postman: **"https://api.getpostman.com/collections/33801345-181c803c-a263-4988-9141-4482d833eb4c"**

Busca en el archivo del workflow la url del environment y cambiala por la de tu environment de postman: **https://api.getpostman.com/environments/33801345-181c803c-a263-4988-9141-4482d833eb4c**

## 4. Qué hace el workflow

- Se ejecuta al hacer push a main, manualmente o de forma programada

- Descarga la colección y el environment desde Postman

- Ejecuta los tests con Newman

- Genera un reporte HTML

- Guarda el reporte como artefacto en GitHub Actions para que puedas descargarlo.
