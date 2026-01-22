# Proyecto QA Manual
El proyecto consiste en crear y ejecutar un plan de pruebas manuales para una página web tanto en escritorio como en movil en base a los siguientes requisitos. Utilizando JIRA, Herramientas de gestión de pruebas y metodologías ágiles scrum.
- El proyecto se realiza en equipo. 
- Debe entregarse cada semana la parte correspondiente.




## Entrega 1 - Crear proyecto e historias de usuario en Jira


**Objetivo**: Crear proyecto de equipo SCRUM en JIRA
Requisitos:
1. Crea una cuenta en JIRA
2. Crea un proyecto SCRUM en JIRA con nombre de la web a probar, miembros del equipo, y tablero scrum con columnas to do, in progress, qa y done.

**Objetivo**: Crear las siguientes historias de usuario en JIRA con criterios de aceptación. Puedes hacerlo en inglés o en español.

### Historias de Usuario con Criterios de Aceptación

1. **Menú de navegación**

* **Historia:** Como usuario quiero ver un menú con enlaces a Inicio, Sobre Nosotros, Viajes y Reservas para navegar fácilmente por el sitio.
* **Criterios de aceptación:**

  * El menú muestra los enlaces: Inicio, Sobre Nosotros, Viajes y Reservas.
  * Cada enlace lleva a su sección correspondiente.
  * El menú está visible en todas las páginas.
  * Debe ser responsive.

2. **Página de inicio**

* **Historia:** Como usuario quiero ver un título, una descripción y una imagen de la tienda para entender rápidamente de qué trata el sitio.
* **Criterios de aceptación:**

  * Se muestra un título claro.
  * Se incluye una descripción informativa.
  * Hay una imagen representativa de la agencia.
  * Debe ser responsive.

3. **Lista de viajes**

* **Historia:** Como usuario quiero ver una lista de viajes con nombre, precio y categoría para conocer lo que la agencia ofrece.
* **Criterios de aceptación:**

  * La lista muestra todos los viajes disponibles.
  * Cada producto contiene nombre, precio y categoría.
  * Debe ser responsive.

4. **Filtros de viajes**

* **Historia:** Como usuario quiero filtrar la lista de viajes  para encontrar fácilmente los que cumplen mis criterios de búsqueda.
* **Criterios de aceptación:**

  * Filtrar por nombre, mostrando productos que contengan el texto ingresado.
  * Filtrar por rango de precio.
  * Filtrar por categoría desde un desplegable.
  * Resultados actualizados mostrando solo productos que cumplan los filtros.
  * Si no existen coincidencias, mostrar mensaje informativo.

5. **Página Sobre Nosotros**

* **Historia:** Como usuario quiero ver un título, descripción e imagen sobre la empresa para conocer más sobre la tienda.
* **Criterios de aceptación:**

  * Sección incluye título claro.
  * Contiene descripción informativa.
  * Muestra imagen representativa.
  * Debe ser responsive.

6. **Formulario de reserva**

* **Historia:** Como usuario quiero enviar mis datos mediante un formulario con nombre, email, teléfono (opcional), mensaje para comunicarme con la tienda.
* **Criterios de aceptación:**

  * Campos: nombre (obligatorio), email (obligatorio), teléfono (opcional), mensaje (obligatorio).
  * Validación de campos obligatorios.
  * Formato de email válido.
  * Mensaje de confirmación al enviar correctamente.
  * Indicaciones si hay errores.
  * Debe ser responsive.

## Entrega 2 - Diseño de pruebas
**Objetivo:** Diseñar pruebas para cada historia de usuario creada aplicando técnicas de prueba adecuadas.
Requisitos:
1. Crear un sprint en JIRA de una semana con todas las historias de usuario, en la columna to do.
2. Configurar herramienta de gestión de pruebas Asserthat en el proyecto de JIRA
3. Para todas las historias de usuario, crear sus casos de prueba en lenguaje gherkin usando las técnicas de pruebas. Una vez creadas, pasar la tarea a QA.


## Entrega 3 - Ejecución de pruebas, reporte de errores y generación de reportes (45%)

**Objetivo:** Ejecutar pruebas en web y móvil y registrar resultados en JIRA

Requisitos:

1. Ejecutar las pruebas de cada historia de usuario en web y móvil
2. Registrar los resultados de las pruebas en JIRA pass/failed
3. Pasar a done las historias de usuario una vez finalizadas las pruebas.
  
**Objetivo:** Identificar y reportar errores en Jira
Requisitos:
1. Si alguna prueba de una historia de usuario falla, crear un ticket de error asociado a la historia de usuario
2. Incluir todos los detalles en el ticket de error: pasos para reproducir, resultado actual con captura, resultado esperado, navegador y resolución.
   
**Objetivo:** Crear una release en Jira
Requisitos:
1. Crear una release en JIRA
2. Incluir en la release todas las historias de usuario con estado done.


**Objetivo: Crear un plan de pruebas de regresión**
Requisitos:
1. Identificar los casos de prueba críticos y agregar la etiqueta regresion.
2. Crear una tarea con todas las pruebas marcadas como regresión (será referencia para su posterior automatización).

 **Objetivo: Documentar un plan de pruebas**  
 Requisitos:
 1. Crear una nueva página en Confluence de Plan de Pruebas con la plantilla propuesta
 2. Modificar la plantilla incluyendo todos los datos de historias de usuario probadas, resultados de pruebas y errores.

## CRITERIOS DE EVALUACIÓN

Completo: Todos los requisitos completados.

Casi completo: 2 requisitos incompletos o 1 requisito sin realizar.

Parcialmente completo: Más de 2 requisitos incompletos o más de 1 requisito sin realizar.

Incompleto: no realizado.

| Objetivo de aprendizaje                                                           | Completo | Casi completo | Parcialmente completo | Incompleto |
| --------------------------------------------------------------------------------- | -------- | ------------- | --------------------- | ---------- |
| **1.Configurar un proyecto ágil Scrum en Jira**                                   | 5%       | 4%            | 3%                    | 0%         |
| **2.Crear historias de usuario en Jira con criterios de aceptación**              | 15%      | 10%           | 5%                    | 0%         |
| **3. Diseñar pruebas en lenguaje Gherkin usando herramientas de gestión de pruebas**| 35%      | 30%           | 20%                   | 0%         |
| **Ejecutar pruebas en web y móvil y registrar resultados**                        | 20%      | 15%           | 10%                   | 0%         |
| **Identificar y reportar errores en Jira**                                        | 10%      | 8%            | 5%                    | 0%         |
| **Crear una release en Jira**                                                     | 5%       | 4%            | 2%                    | 0%         |
| **Crear un plan de pruebas de regresión**                                         | 5%       | 4%            | 2%                    | 0%         |
| **Documentar un plan de pruebas**                                                 | 5%       | 4%            | 2%                    | 0%         |

Para superar el módulo, el proyecto debe obtener una calificación final igual o superior al 65%.

El proyecto se realiza en equipo de entre 2 y 3 miembros.

Cada integrante es responsable de cumplir sus tareas asignadas.

Si un miembro del equipo no cumple con sus responsabilidades, se le restará un 10% de la nota final, será excluido del equipo y deberá realizar el proyecto completo de forma individual para superar el módulo. 
