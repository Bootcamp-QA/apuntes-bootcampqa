# PROYECTO AUTOMATIZACIÓN DE PRUEBAS CON PLAYWRIGHT (PYTHON)

## Descripción del Proyecto

En este proyecto se automatizarán pruebas de regresión sobre una aplicación web utilizando **Playwright con Python**.  
Se trabajará con una estructura basada en **Page Object Model**, integración continua con **GitHub Actions** y adaptación de las pruebas para versión móvil.


## Semana 11: Creación del Proyecto y Automatización Básica **20%**

### 1. Creación del Proyecto en GitHub **5%**
1. Crear un proyecto en GitHub usando la plantilla:  
   https://github.com/Bootcamp-QA/playwright-python-template
2. Actualizar el archivo `README.md`:
   1. Descripción del proyecto.
   2. URL de la web.
3. Configurar el entorno básico de Playwright con Python.

### 2. Automatización de Pruebas de Regresión Iniciales **15%**
Automatizar las pruebas de regresión para las siguientes secciones de la web:

1. Menú de navegación.
2. Página de inicio.
3. Página “Sobre nosotros”.

---

## Semana 12: Automatización de Pruebas Avanzadas y Github Actions **50%**

### 1. Formulario de Contacto **25%**

Automatizar las siguientes pruebas:

1. Enviar formulario con campos obligatorios.
2. Enviar formulario con campos opcionales.
3. Enviar formulario con el campo email vacío.
4. Enviar formulario con el campo email inválido.
5. Enviar formulario con el campo mensaje vacío.

---

### 2. Filtros **20%**

Automatizar las pruebas de filtros:

1. Filtro por nombre válido.
2. Filtro por categoría válida.
3. Filtro por rango de precio válido.
4. Filtro por nombre que no exista.

---

### 3. GitHub Actions  **5%**
1. Revisar el workflow de GitHub Actions.
2. Ejecutar las pruebas en el entorno de GitHub Actions.
3. Analizar los errores utilizando trazas, logs o reportes de Playwright.
4. Corregir los fallos hasta que todas las pruebas pasen correctamente en GitHub Actions.

## Semana 13: Page Object Model y Pruebas en version Movil  **30%**

### 1. Page Object Model **20%**
1. Reorganizar el proyecto utilizando el patrón **Page Object Model**.
2. Crear una carpeta `pages` que contenga las clases de cada página.
3. Crear una carpeta `tests` que contenga los tests agrupados por funcionalidad.
4. Los tests deben importar y utilizar las páginas definidas en la carpeta `pages`.

### 1. Adaptación a Versión Móvil **10%**
1. Modificar las pruebas necesarias para que funcionen correctamente en versión móvil.
2. Ajustar selectores, resoluciones y comportamientos específicos de dispositivos móviles.
3. Actualizar el workflow de GitHub Actions para ejecutar las pruebas en versión movil

