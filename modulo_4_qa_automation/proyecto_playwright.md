# PROYECTO AUTOMATIZACIÓN DE PRUEBAS CON PLAYWRIGHT (PYTHON)

## Descripción del Proyecto

En este proyecto se automatizarán pruebas de regresión sobre una aplicación web utilizando **Playwright con Python**.  
Se trabajará con una estructura basada en **Page Object Model**, integración continua con **GitHub Actions** y adaptación de las pruebas para versión móvil.


## Entrega 1: Creación del Proyecto y Automatización Básica

### Objetivo 1: Crear un proyecto de Playwright con Python en GitHub y actualizar README
1. Crear un proyecto en GitHub usando la plantilla:  
   https://github.com/Bootcamp-QA/playwright-python-template
2. Actualizar el archivo `README.md`:
   1. Descripción del proyecto.
   2. URL de la web.
3. Configurar el entorno básico de Playwright con Python.

### Objetivo 2: Automatizar pruebas de regresión básicas de navegación y páginas informativas
Automatizar las pruebas de regresión para las siguientes secciones de la web:

1. Menú de navegación.
2. Página de inicio.
3. Página “Sobre nosotros”.

---

## Entrega 2: Automatización de Pruebas Avanzadas y Github Actions

### Objetivo 3: Automatizar pruebas del formulario de contacto (escenarios válidos e inválidos)

Automatizar las siguientes pruebas:

1. Enviar formulario con campos obligatorios.
2. Enviar formulario con campos opcionales.
3. Enviar formulario con el campo email vacío.
4. Enviar formulario con el campo email inválido.
5. Enviar formulario con el campo mensaje vacío.

---

### Objetivo 4: Automatizar pruebas de filtros (escenarios válidos y no válidos)

Automatizar las pruebas de filtros:

1. Filtro por nombre válido.
2. Filtro por categoría válida.
3. Filtro por rango de precio válido.
4. Filtro por nombre que no exista.

---

### Objetivo 5: Configurar y ejecutar pruebas en GitHub Action 
1. Revisar el workflow de GitHub Actions.
2. Ejecutar las pruebas en el entorno de GitHub Actions.
3. Analizar los errores utilizando trazas, logs o reportes de Playwright.
4. Corregir los fallos hasta que todas las pruebas pasen correctamente en GitHub Actions.

## Entrega 3: Page Object Model y Pruebas en version Movil 

### Objetivo 6: Reorganizar el proyecto utilizando el patrón Page Object Model
1. Reorganizar el proyecto utilizando el patrón **Page Object Model**.
2. Crear una carpeta `pages` que contenga las clases de cada página.
3. Crear una carpeta `tests` que contenga los tests agrupados por funcionalidad.
4. Los tests deben importar y utilizar las páginas definidas en la carpeta `pages`.

### Objetivo 7:Adaptar las pruebas automatizadas para su ejecución en versión móvil
1. Modificar las pruebas necesarias para que funcionen correctamente en versión móvil.
2. Ajustar selectores, resoluciones y comportamientos específicos de dispositivos móviles.
3. Actualizar el workflow de GitHub Actions para ejecutar las pruebas en versión movil

# CRITERIOS DE EVALUACIÓN

- Sobresaliente: 100% del objetivo completado.
- Notable: Más del 80% del objetivo completado.
- Cumple Objetivos: Más del 60% del objetivo completado.
- Próximo al objetivo: Más del 45% del objetivo completado.

| Objetivo de aprendizaje                                                                 | Sobresaliente | Notable | Cumple Objetivos | Próximo al objetivo |
|-----------------------------------------------------------------------------------------|---------------|---------|------------------|---------------------|
| 1. Configurar proyecto Base de Datos en Supabase                                         | 5%            | 4%      | 3%               | 2%                  |
| 2. Crear tabla SQL                                                                       | 5%            | 4%      | 3%               | 2%                  |
| 3. Insertar datos en SQL                                                                 | 10%           | 8%      | 6%               | 5%                  |
| 4. Crear consultas SQL                                                                   | 15%           | 12%     | 10%              | 8%                  |
| 5. Actualizar y eliminar datos en SQL                                                    | 5%            | 4%      | 3%               | 2%                  |
| 6. Generar API y documentación de la API y configurar Postman                            | 5%            | 4%      | 3%               | 2%                  |
| 7. Pruebas de peticiones API GET con Postman (tests y variables)                         | 10%           | 8%      | 6%               | 5%                  |
| 8. Pruebas de peticiones API PATCH con Postman (tests y variables)                       | 10%           | 8%      | 6%               | 5%                  |
| 9. Pruebas de peticiones API POST con Postman (tests y variables)                        | 10%           | 8%      | 6%               | 5%                  |
| 10. Pruebas de peticiones API DELETE con Postman (tests y variables)                     | 10%           | 8%      | 6%               | 5%                  |
| 11. Integrar la API en un proyecto web                                                   | 5%            | 4%      | 3%               | 2%                  |
| 12. Configurar CI con GitHub Actions para ejecutar pruebas de API con Newman             | 10%           | 8%      | 6%               | 5%                  |


Para superar el módulo, el proyecto debe obtener una calificación final igual o superior al 60%.

El proyecto se realiza en equipo. Cada integrante es responsable de cumplir sus tareas asignadas.

Si un miembro del equipo no cumple con sus responsabilidades, se le restará un 10% de la nota final, será excluido del equipo y deberá realizar el proyecto completo de forma individual.

