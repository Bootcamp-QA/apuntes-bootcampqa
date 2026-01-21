# PROYECTO AUTOMATIZACIÓN DE PRUEBAS CON PLAYWRIGHT (PYTHON)

## Descripción del Proyecto

En este proyecto se automatizarán pruebas de regresión sobre una aplicación web utilizando **Playwright con Python**.  
Se trabajará con una estructura basada en **Page Object Model**, integración continua con **GitHub Actions** y adaptación de las pruebas para versión móvil.


## Entrega 1: Creación del Proyecto y Automatización Básica

### 1. Creación del Proyecto en GitHub
1. Crear un proyecto en GitHub usando la plantilla:  
   https://github.com/Bootcamp-QA/playwright-python-template
2. Actualizar el archivo `README.md`:
   1. Descripción del proyecto.
   2. URL de la web.
3. Configurar el entorno básico de Playwright con Python.

### 2. Automatización de Pruebas de Regresión Básicas **15%**
Automatizar las pruebas de regresión para las siguientes secciones de la web:

1. Menú de navegación.
2. Página de inicio.
3. Página “Sobre nosotros”.

---

## Entrega 2: Automatización de Pruebas Avanzadas y Github Actions

### 1. Formulario de Contacto **25%**

Automatizar las siguientes pruebas:

1. Enviar formulario con campos obligatorios.
2. Enviar formulario con campos opcionales.
3. Enviar formulario con el campo email vacío.
4. Enviar formulario con el campo email inválido.
5. Enviar formulario con el campo mensaje vacío.

---

### 2. Filtros

Automatizar las pruebas de filtros:

1. Filtro por nombre válido.
2. Filtro por categoría válida.
3. Filtro por rango de precio válido.
4. Filtro por nombre que no exista.

---

### 3. GitHub Actions 
1. Revisar el workflow de GitHub Actions.
2. Ejecutar las pruebas en el entorno de GitHub Actions.
3. Analizar los errores utilizando trazas, logs o reportes de Playwright.
4. Corregir los fallos hasta que todas las pruebas pasen correctamente en GitHub Actions.

## Entrega 3: Page Object Model y Pruebas en version Movil 

### 1. Page Object Model
1. Reorganizar el proyecto utilizando el patrón **Page Object Model**.
2. Crear una carpeta `pages` que contenga las clases de cada página.
3. Crear una carpeta `tests` que contenga los tests agrupados por funcionalidad.
4. Los tests deben importar y utilizar las páginas definidas en la carpeta `pages`.

### 2. Adaptación a Versión Móvil
1. Modificar las pruebas necesarias para que funcionen correctamente en versión móvil.
2. Ajustar selectores, resoluciones y comportamientos específicos de dispositivos móviles.
3. Actualizar el workflow de GitHub Actions para ejecutar las pruebas en versión movil

# CRITERIOS DE EVALUACIÓN

- Completo: Todos los requisitos completados.
- Casi completo: 2 requisitos incompletos o 1 requisito sin realizar.
- Parcialmente completo: Más de 2 requisitos incompletos o más de 1 requisito sin realizar.
- Incompleto: No realizado.

| Objetivo de aprendizaje                                                             | Completo | Casi completo | Parcialmente completo | Incompleto |
| ----------------------------------------------------------------------------------- | -------- | ------------- | --------------------- | ---------- |
| **Crear un proyecto de Playwright con Python en GitHub y actualizar README**        | 5%       | 4%            | 2%                    | 0%         |
| **Automatizar pruebas de regresión básicas de navegación y páginas informativas**   | 15%      | 10%           | 5%                    | 0%         |
| **Automatizar pruebas del formulario de contacto (escenarios válidos e inválidos)** | 25%      | 20%           | 15%                   | 0%         |
| **Automatizar pruebas de filtros (escenarios válidos y no válidos)**                | 20%      | 15%           | 10%                   | 0%         |
| **Configurar y ejecutar pruebas en GitHub Actions**                                 | 5%       | 4%            | 2%                    | 0%         |
| **Reorganizar el proyecto utilizando el patrón Page Object Model**                  | 20%      | 15%           | 10%                   | 0%         |
| **Adaptar las pruebas automatizadas para su ejecución en versión móvil**            | 10%      | 8%            | 5%                    | 0%         |

Para superar el módulo, el proyecto debe obtener una calificación final igual o superior al 65%.

El proyecto se realiza en equipo. Cada integrante es responsable de cumplir sus tareas asignadas.

Si un miembro del equipo no cumple con sus responsabilidades, se le restará un 10% de la nota final, será excluido del equipo y deberá realizar el proyecto completo de forma individual.

