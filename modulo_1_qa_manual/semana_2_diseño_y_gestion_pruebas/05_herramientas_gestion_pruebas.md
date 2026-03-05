# Herramientas de Gestión de Pruebas

# Video de la clase
[Ver clase: Herramientas de Gestión de Pruebas - 10 min](https://bootcampqa.com/videos/herramientasdegestiondepruebas.mp4)

# Apuntes

## ¿Qué es una herramienta de Gestión de Pruebas?

Una herramienta de gestión de pruebas es una herramienta de calidad de software que permite gestionar de forma centralizada todo el proceso de testing.

Permite:

- Organizar y almacenar casos de prueba y sus resultados  
- Generar informes de pruebas  
- Planificar y organizar la ejecución de pruebas  

## Herramientas de gestión de pruebas más utilizadas

- TestRails  
- XRay  
- Zephyr  
- TestLink  
- HP Quality Center  
- AIO Tests  
- Asserthat  

## Funcionalidades de las herramientas de gestión de pruebas

- Creación de casos de prueba  
- Almacenamiento de resultados de ejecución de pruebas  
- Creación de planes de pruebas  
- Organización de casos de prueba  
- Generación de documentación de las pruebas  

## Instalar una herramienta de Gestión de Pruebas en Jira

Permisos y roles de JIRA, JIRA ahora distingue entre 2 roles:
Administrador de JIRA: Esta persona tiene permiso para instalar aplicaciones y agregar miembros al equipo, es por defecto la persona que creó el equipo de JIRA la primera vez y luego invitó al resto.
Administrador de Espacio: Esta persona tiene permiso para hacer cambios solo en el Proyecto (agregar usuarios al Proyecto, ver y crear tareas, etc). Este permiso es el que teneis las demás del equipo por defecto.
 
Entonces la persona que creo el equipo de JIRA es la unica que puede instalar Asserthat o cualquier otra aplicación.

La persona Administradora de JIRA debe seguir los siguientes pasos para instalar la aplicación:

1. En el menú principal de Jira, selecciona **Aplicaciones** y luego **Explorar más aplicaciones**  
2. En la barra de búsqueda, busca la herramienta de gestión de pruebas que prefieras  
3. Haz clic en **Instalar**  
4. Sigue las instrucciones para habilitar la herramienta en tu proyecto  
   Cada herramienta tiene un proceso ligeramente diferente  
5. Comienza a utilizar la herramienta de gestión de pruebas en tu proyecto

## Herramienta de Administración de pruebas AssertThat

### 1. Activar Herramienta AsserThat en el Proyecto
Una vez el administrador ha instalado la herramienta de gestión de pruebas, debéis activarla en vuestro proyecto siguiendo estos pasos:
2. Ve a aplicaciones, y debe aparecer Asserthat integration.
3. Activa lo siguiente:
- Activa todos (todos en verde)
- Idioma: IMPORTANTE INGLÉS. No funciona bien en otro idioma la validación, para quienes lo hacéis en ingles no hay problema, para quienes lo hagáis en español, podéis poner todo en español menos las palabras GIVEN, WHEN, THEN, AND, EXAMPLES que son las que da el estándar y para validar bien teneis que usar las mismas exactamente.
4. Haz clic en el boton del final reindexar para aplicar los cambios.
5. Vuelve al tablero de la aplicación, la aplicación Asserthat (Características si está en Español) aparecerá en la barra superior, y también como opción dentro de las historias de usuario.
jira-asserthat
tablero-asserthat

### 2. Agregar pruebas/escenarios en Asserthat
Asserthat deberia permitir crear varios escenarios para la misma feature/característica desde la historia de usuario pero por un error en la aplicación no te permite hacerlo desde historia de usuario, asi que debes crear las pruebas en su lugar desde la pestaña asserthat:

1. Abre la pestaña Asserthat
2. Haz clic en la pestaña feature/caracteristicas
asserthat-featurse
4. Crea una nueva feature/característica con el mismo nombre de la historia de usuario o pincha en la que tengas creada a la que quieras agregar algún escenario
asserthat-crearfeature
6. Agrega los escenarios haciendo clic en crear escenario, poniendo titulo y pasos (importante los pasos aunque los pongas en español usa las palabras clave en inglés GIVEN, WHEN, THEN, AND y EXAMPLES)
asserthat-crearescenario
7. Una vez creados los escenarios, asocialos a la historia de usuario, para ello rellena el campo related-to de cada escenario con el id de la historia de usuario a la que lo quieras asociar.
8. Por ultimo abre la historia de usuario y veras los escenarios creados.

### 3. Mover pruebas/escenarios en Asserthat
Si has creado algun escenario en un feature/caracteristica diferente y quieres moverlo sin tener que borrarlo, puedes seguir los siguientes pasos:
1. Abre la pestaña Asserthat
2. Haz clic en la pestaña feature/caracteristicas
3. Entra en la feature en la que tengas el escenario
4. Haz clic en los 3 puntitos del escenario y elige la opcion move
5. Selecciona el nuevo feature al que quieres moverlo

### 4. Eliminar Features/caracteristicas en Asserthat
Si has creado por error algun feature/caracteristicas en asserthat, puedes borrarlo siguiendo los siguientes pasos.
1. Abre la pestaña Asserthat
2. Haz clic en la pestaña feature/caracteristicas
3. Haz clic en los 3 puntitos de la caracteristica/feature que quieras eliminar
4. Selecciona la opcion borrar y se eliminará la feature

### 5. Agregar Resultados de Pruebas en Asserthat
Una vez creadas las pruebas, puedes agregar los resultados de prueba desde la historia de usuario de JIRA. Sigue los siguientes pasos.
Si es un escenario/prueba normal (sin examples):
1. Haz clic en ejecutar
2. Elige agregar ejecución
3. Selecciona el resultado de la prueba (passed/failed) y comentario (recomendado agregar navegadores en los que se ha probado)
4. Guardar

Si es un escenario outline (con examples):
1. Haz clic en ejecutar
2. Elige agregar ejecución
3. Elige el example (debes poner un resultado para cada example)
4. Selecciona el resultado de la prueba y comentario
5. Guardar
6. Agrega otra ejecución para el siguiente example y repite los pasos hasta poner los resultados de todos los examples.
   
