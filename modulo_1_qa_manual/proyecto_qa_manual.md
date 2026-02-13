# Proyecto QA Manual
El proyecto consiste en crear y ejecutar un plan de pruebas manuales para una página web tanto en escritorio como en movil en base a los siguientes . Utilizando JIRA, Herramientas de gestión de pruebas y metodologías ágiles scrum.
- El proyecto se realiza en equipo. 
- Debe entregarse cada semana la parte correspondiente.




## Entrega 1 - Crear proyecto e historias de usuario en Jira


**Objetivo 1**: Crear proyecto de equipo SCRUM en JIRA
1. Crea una cuenta en JIRA
2. Crea un proyecto SCRUM en JIRA con nombre de la web a probar, miembros del equipo, y tablero scrum con columnas to do, in progress, qa y done.

**Objetivo 2**: Crear las siguientes historias de usuario en JIRA con criterios de aceptación. Puedes hacerlo en inglés o en español.

### Historias de Usuario con Criterios de Aceptación

1. **Menú de navegación**

* **Historia:** Como usuario quiero ver un menú con enlaces a Inicio, Sobre Nosotros, Productos y Contacto para navegar fácilmente por el sitio.
* **Criterios de aceptación:**

  * El menú muestra los enlaces: Inicio, Sobre Nosotros, Contacto y Reservas.
  * Cada enlace lleva a su sección correspondiente.
  * El menú está visible en todas las páginas.
  * Debe ser responsive.

2. **Página de inicio**

* **Historia:** Como usuario quiero ver una página de inicio para saber la información relevante de la tienda.
* **Criterios de aceptación:**

  * Se muestra un título con el nombre de la tienda.
  * Se muestra una descripción.
  * Hay una imagen de la tienda.
  * Hay un botón para abrir la página de productos de la tienda.
  * Debe ser responsive.
 
3. **Página Sobre Nosotros**

* **Historia:** Como usuario quiero ver una página sobre nosotros para conocer más sobre la tienda.
* **Criterios de aceptación:**

  * La página incluye un título "Sobre Nosotros"
  * La página incluye información sobre la historia y los valores de la tienda.
  * La página muestra una imagen del equipo.
  * Debe ser responsive.

4. **Página de productos**

* **Historia:** Como usuario quiero ver una página de productos para ver los productos que ofrece la tienda.
* **Criterios de aceptación:**

  * La página muestra el título "Nuestros Productos".
  * Debe mostrarse una lista de productos con la siguiente información: Categoría, Nombre, Precio 
  * Debe ser responsive.

5. **Filtros de productos**

* **Historia:** Como usuario quiero filtrar los productos para encontrar fácilmente el que se ajuste a mis necesidades.
* **Criterios de aceptación:**

  La página debe tener los siguientes filtros disponibles:

  * Filtrar por nombre: Debe mostrar los productos cuyo nombre contenga el texto introducido.
  * Filtrar precio: Puede filtrar por precio mínimo, precio máximo, o rango de precio mínimo y máximo. Debe mostrar los productos que estén dentro del rango de precio introducido.
  * Filtrar por categoría: Plantas, herramientas o macetas. Debe mostrar los productos que tengan la categoría seleccionada.
  * Los filtros pueden combinarse.
  * Si no existen coincidencias, se debe mostrar un mensaje informativo.



6. **Página de contacto**

* **Historia:** Como usuario quiero tener un formulario de contacto para comunicarme con la tienda.
* **Criterios de aceptación:**
La página de contacto debe tener in formulario con los siguientes campos:
  * nombre (obligatorio)
  * email (obligatorio), con formato email válido.
  * teléfono (opcional), con formato teléfono valido (solo números o prefijo +)
  * mensaje (obligatorio, con máximo 500 caracteres).
  * Mensaje de confirmación al enviar correctamente.
  * Indicaciones si hay errores.
  * Debe ser responsive.
 
7. **Carrito de la compra**

* **Historia:** Como usuario quiero tener un carrito de la compra para poder visualizar mi pedido.
* **Criterios de aceptación:**
  - En el menú habrá un icono de un carrito que abrirá la página carrito de la compra.
  - El usuario puede agregar productos al carrito desde la página de productos. Cuando agrege un producto al carrito, aparecerá en la página de carrito el nombre, la imagen, la categoría y el precio del producto añadido.
  - El usuario puede quitar productos del carrito de dos formas: Desde la página de producto o En la página del carrito. Cuando quite un producto del carrito, desaparecerá de la página de carrito.
  - Cuando haya productos en el carrito aparecerá:
  - Un resumen de la compra que incluirá:
    1. El precio total de los productos añadidos.
    2. El importe del 21% de IVA
    3. El coste de envío que será de 5€
    4. El total de la compra que será la suma los productos mas el iva mas el envio.
    5. Cuando se agregen o eliminen productos del carrito el precio debe actualizarse.

  - Un botón vaciar carrito, que dejará la página de carrito vacio. Estará disponible solo cuando haya productos en el carrito.
  - Habrá un enlace seguir comprando, que abrirá la página de productos para seguir agregando productos al carrito.
  - Cuando el carrito esté vacio, se verá un botón "Ver productos" que abrirá la página de productos.
 
  8. **Finalizar compra**
 * **Historia:** Como usuario quiero completar la compra de mi pedido.
* **Criterios de aceptación:**
* Cuando haya productos en el carrito, aparecerá un botón realizar pago, que llevará a la página de realizar pedido que tendrá lo siguiente:
* Resumen del pedido que incluirá:
  - Nombre de los productos con sus precios
  - Subtotal, suma del precio de todos los productos
  - IVA 21%, total de iva aplicado.
  - Envio, 5€
  - Total, suma total de todas las cantidades.
* Formulario de datos de envio y pago con los siguientes campos y botones:
- Nombre Completo, obligatorio
- Email, obligatorio
- Dirección, obligatoria
- Número de tarjeta, válida, obligatoria. (Tarjeta de prueba válida 4242 4242 4242 4242)
- Botón volver al carrito, que volverá a la página de carrito
- Botón completar compra que si todos los datos del formulario son correctos aparecerá una página de pedido completado con los siguientes datos:
- Resumen del pedido con:
  - Nombre y precio de cada producto
  - Subtotal (suma del precio de todos los productos)
  - IVA 21%
  - Envío 5€
  - Total: La suma de todos los importes.
  - Botón Volver a la tienda, que abrirá la página de productos
  - Botón ir al inicio, que abrirá la página de inicio.
  - Si algún campo del formulario es incorrecto aparecerá un mensaje de error.

## Entrega 2 - Diseño de pruebas
**Objetivo 3:** Diseñar pruebas para cada historia de usuario creada aplicando técnicas de prueba adecuadas.
1. Crear un sprint en JIRA de una semana con todas las historias de usuario.
2. Configurar herramienta de gestión de pruebas Asserthat en el proyecto de JIRA
3. Para todas las historias de usuario, crear sus casos de prueba en lenguaje gherkin usando las técnicas de pruebas.
4. Una vez creadas las pruebas, pasar la tarea a QA.


## Entrega 3 - Ejecución de pruebas, reporte de errores y generación de reportes (45%)

**Objetivo 4:** Ejecutar pruebas en web y móvil y registrar resultados en JIRA
1. Ejecutar las pruebas de cada historia de usuario en web y móvil
2. Registrar los resultados de las pruebas
3. Pasar a done las historias de usuario una vez finalizadas las pruebas.
  
**Objetivo 5:** Identificar y reportar errores en Jira
1. Si alguna prueba de una historia de usuario falla, crear un ticket de error asociado a la historia de usuario
2. Incluir todos los detalles en el ticket de error: pasos para reproducir, resultado actual con captura, resultado esperado, navegador y resolución.
   
**Objetivo 6:** Crear una release en Jira
1. Crear una release en JIRA
2. Incluir en la release todas las historias de usuario con estado done.


**Objetivo 7: Crear un plan de pruebas de regresión**
1. Identificar los casos de prueba críticos y agregar la etiqueta regresion.
2. Crear una tarea con todas las pruebas marcadas como regresión (será referencia para su posterior automatización).

 **Objetivo 8: Documentar un plan de pruebas**  
 1. Crear una nueva página en Confluence de Plan de Pruebas con la plantilla propuesta
 2. Modificar la plantilla incluyendo todos los datos de historias de usuario probadas, resultados de pruebas y errores.

## CRITERIOS DE EVALUACIÓN

Sobreasliente: 100% del objetivo completado.

Notable:  Más del 80% del objetivo completado.

Cumple Objetivos: Más del 60% del objetivo completado.

Próxima al objetivo: Más del 45% del objetivo completado.



| Objetivo de aprendizaje                                                           | Sobresaliente | Notable |  Cumple Objetivos  | Próxima al objetivo |  
| --------------------------------------------------------------------------------- | -------- | ------------- | --------------------- | ---------- |
| **1.Configurar un proyecto ágil Scrum en Jira**                                   | 5%       | 4%            | 3%                    | 2%         |
| **2.Crear historias de usuario en Jira con criterios de aceptación**              | 15%      | 12%           | 10%                    | 5%         |
| **3. Diseñar pruebas en lenguaje Gherkin usando herramientas de gestión de pruebas**| 35%      | 30%           | 25%                   | 20%         |
| **4.Ejecutar pruebas en web y móvil y registrar resultados**                        | 20%      | 15%           | 12%                   | 10%         |
| **5.Identificar y reportar errores en Jira**                                        | 10%      | 8%            | 6%                    | 4%         |
| **6.Crear una release en Jira**                                                     | 5%       | 4%            | 3%                    | 2%         |
| **7.Crear un plan de pruebas de regresión**                                         | 5%       | 4%            | 3%                    | 2%         |
| **8.Documentar un plan de pruebas**                                                 | 5%       | 4%            | 3%                    | 2%         |

Para superar el módulo, el proyecto debe obtener una calificación final igual o superior a suficiente 60% completado.

El proyecto se realiza en equipo de entre 3 y 4 miembros.

Cada integrante es responsable de cumplir sus tareas asignadas.

Si un miembro del equipo no cumple con sus responsabilidades, se le restará un 10% de la nota final, será excluido del equipo y deberá realizar el proyecto completo de forma individual para superar el módulo. 
