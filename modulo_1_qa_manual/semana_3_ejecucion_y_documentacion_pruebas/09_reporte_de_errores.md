# Reporte de errores

# Video de la clase


[Ver clase: Reporte y verificación de Errores - 15 min](https://bootcampqa.com/videos/manual-reporte-de-errores.mp4)

# Apuntes
## Reporte de errores

En Jira haz click en crear issue o tarea y elige el tipo de tarea **ERROR** o **BUG**.

### Título  
Agrega un título del error. Debe ser breve pero descriptivo. No indiques algo genérico como “error en la página”, ya que será difícil entender qué está fallando.

### Descripción  
Agrega una descripción del error siguiendo el siguiente esquema:

**Pasos para reproducir / Steps to reproduce**  
Incluye los pasos necesarios para reproducir el error. Normalmente coinciden con los pasos *Given* y *When* de tus pruebas, ya que son las acciones a llevar a cabo.

**Resultado Actual / Actual Result**  
Describe el resultado de error no esperado que has obtenido al seguir esos pasos.  
Incluye una captura de pantalla o vídeo del error.

**Resultado Esperado / Expected Result**  
Describe el resultado que se espera obtener una vez se arregle el fallo.

**Plataforma**  
Indica si el error ocurre en:
- Móvil  
- Escritorio  
- Ambos  

**Información Adicional**  
Cualquier información que pueda ayudar a entender o solucionar el error, por ejemplo:
- Versión del navegador  
- Sistema operativo  
- Logs de error en la consola  

### Enlace a Historia de Usuario

Indica con qué historia de usuario está relacionado el error siguiendo estos pasos:

- En la sección de incidencias enlazadas, elige la opción **relates to** (relacionado con).  
- Agrega el ID de la historia de usuario que tiene el error.  

Pulsa el botón **Crear**.

## Pruebas de Verificación o Validación

- Abre en Jira el backlog del proyecto donde debe aparecer el error que has creado.  
- Arrastra el ticket de error al sprint.  
- Vuelve al tablero y mueve el error a la columna **In Progress**.  
- Una vez arreglado el error mueve el error a la columna **QA** para volver a probarlo.  
- Vuelve a ejecutar únicamente ese caso de prueba fallado tanto en **Desktop** como en **Mobile**.  
- Si obtienes el resultado esperado, marca el test como **Passed** y mueve el bug a la columna **Done**.
- Ejecuta las pruebas de regresión tras validar los errores, para asegurar que con el arreglo no ha sido afectada ninguna funcionalidad importante.
- Si no obtienes el resultado esperado, vuelve a marcar el test como **Failed**, mueve el bug a la columna **In Progress** y repite el proceso.
