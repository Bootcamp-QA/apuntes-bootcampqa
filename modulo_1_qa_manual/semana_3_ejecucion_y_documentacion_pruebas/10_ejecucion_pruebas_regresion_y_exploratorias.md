# Tema 1.10 Release y ejecución de pruebas de regresión y exploratorias

# Video de la clase


[Ver clase: Herramientas de Gestión de Pruebas - 10 min](https://bootcampqa.com/videos/herramientasdegestiondepruebas.mp4)

# Apuntes
## Control de release version y Ejecución de pruebas de Regresión

## Pruebas de Regresión

Las pruebas de regresión sirven para comprobar que la funcionalidad ya existente sigue funcionando después de introducir un nuevo cambio.

1. Es importante ejecutar las pruebas de regresión después de introducir cambios en nuestro proyecto, para asegurar que estos cambios no afectan a la funcionalidad existente.

2. Identificar las pruebas de regresión.  
No será posible probar a fondo toda la funcionalidad del sistema, por lo que debes identificar en primer lugar cuáles son las pruebas más importantes para marcarlas como pruebas de regresión y así encontrar un equilibrio entre tiempo de pruebas y calidad asegurada.

1. Como prueba de regresión debes siempre incluir los casos más críticos e importantes desde el punto de vista de negocio y experiencia de usuario.

2. Generalmente incluye las áreas de pagos, registro de usuarios, búsquedas y filtros más comunes, formularios más usados y enlaces e información más relevante. Hazte la pregunta: ¿podría el usuario seguir usando mi web sin esta funcionalidad? Si la respuesta es no, definitivamente debes incluirla.

3. También es importante asegurar que las pruebas de regresión se ejecutan en los navegadores web y móviles más comunes entre nuestros usuarios.

## Cuándo Ejecutar las Pruebas de Regresión

Idealmente, las pruebas de regresión se deben ejecutar cada vez que introducimos un nuevo cambio en nuestra web, es decir, cada vez que se agrega una nueva historia de usuario o arreglo de error a la aplicación.

1. Debido al tiempo necesario para ejecutar las pruebas de regresión, esto es solo posible cuando las pruebas están automatizadas.

2. Si ejecutas las pruebas de regresión de forma manual, deberías hacerlo al menos:
   - Al final de cada Sprint, para asegurar que las funcionalidades nuevas que ha hecho el equipo durante el sprint no han introducido ningún error.
   - Antes de cada Release.

## Ejecutar las Pruebas de Regresión

Una vez terminas todas las historias de usuario de tu sprint, crea una nueva tarea de pruebas de regresión.

1. Para ello, selecciona todas las pruebas que has marcado como regresión, tanto de las nuevas funcionalidades como de las ya existentes. Lo único que no debes incluir son las pruebas de regresión de historias de usuario que no están aún hechas.

2. Ejecuta las pruebas de regresión en escritorio y móvil.

3. Si alguna prueba falla, crea un ticket de error para solucionarlo.

4. Arregla los fallos encontrados y vuelve a ejecutar la prueba fallida.

5. Una vez pasadas todas las pruebas, puedes completar la tarea de pruebas de regresión.

## Qué es una Release o Versión

Una release es una puesta en producción (entrega al usuario final) de una nueva versión de nuestra web o aplicación.

1. Normalmente la funcionalidad nueva se despliega y prueba en un entorno de pruebas, que no está disponible para nuestro cliente o usuario.

2. Cuando las funcionalidades están listas y probadas, se hace un despliegue a producción, que consiste en agregar estos cambios a la web que usa el cliente, es decir, nuestros cambios estarán disponibles y visibles para nuestros usuarios.

3. Esto puede hacerse al final de cada sprint, de forma mensual, semanal, cada dos días o incluso a diario o varias veces al día si se tiene un proceso automatizado de control de calidad y despliegue.

## Crear una Release o Versión en JIRA

Una release o versión en Jira sirve para agrupar las nuevas funcionalidades o user stories que van a desplegarse en producción, es decir, las nuevas funcionalidades que verán nuestros usuarios.

1. Para crear una nueva versión, ve a la pestaña versiones y haz click en crear versión.

2. En nombre, incluye el nombre de la versión. Se puede poner el nombre que se quiera. Generalmente suele nombrarse como versión 1.0 la primera, 1.1 la segunda y así sucesivamente.

## Agregar la Versión a Historias de Usuario y Bugs Finalizados

Una historia de usuario o un error debe estar terminado para incluirse en una release. Esto quiere decir que ha sido desarrollada y probada, lo que indica que cumple los estándares de calidad necesarios para ser entregado al usuario.

1. Para agregar la versión, abre la historia de usuario o error que tienes en Done.

2. En el campo Versiones Corregidas elige la que acabas de crear, por ejemplo 1.1.

3. Repite el proceso por todas las historias y errores completos (columna Done).

## Completar la Release y Cerrar el Sprint

En releases, marca la release como released (entregada). Esto significa que se ha desplegado en producción.

Cierra el Sprint al completar las dos semanas.
