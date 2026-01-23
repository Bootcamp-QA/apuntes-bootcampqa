# API Testing con Postman

[Ver clase: Configurar cuenta en POSTMAN - 5 min](https://bootcampqa.com/videosapi/api-crear-proyecto-postman-coleccion.mp4)

[Ver clase: Peticiones GET: Autentificación - 10 min](https://bootcampqa.com/videosapi/api-get-y-autentificacion.mp4)

[Ver clase: Peticiones GET: Variables y Tests- 30 min](https://bootcampqa.com/videosapi/api-get-variables-tests.mp4)

[Ver clase: Peticiones GET: Casos negativos - 10 min](https://bootcampqa.com/videosapi/api-get-casos-negativos.mp4)

[Ver clase: Peticiones PATCH - 25 min](https://bootcampqa.com/videosapi/api-patch.mp4)

[Ver clase: Peticiones POST - 20 min](https://bootcampqa.com/videosapi/api-post.mp4)

[Ver clase: Peticiones DELETE - 15 min](https://bootcampqa.com/videosapi/api-delete.mp4)

## 1. Creación de Cuenta en Postman

Para empezar a usar Postman, primero necesitas crear una cuenta en la plataforma. Sigue estos pasos:

1. Visita Postman y haz clic en "Sign Up" en la esquina superior derecha.  
2. Elige registro con Google (recomendado) o rellena el formulario con tu dirección de correo electrónico, nombre y una contraseña segura.  
3. Si te has registrado con tu correo, confirma tu correo electrónico siguiendo el enlace que Postman te enviará.  
4. Inicia sesión en tu cuenta de Postman con tus credenciales.

## 2. Creación de un Workspace Público

Un Workspace en Postman es un espacio donde puedes organizar tus colecciones de peticiones. Para crear un Workspace público:

1. Haz clic en el icono de tu perfil en la esquina superior derecha y selecciona "Workspaces".  
2. Haz clic en el botón "Create Workspace".  
3. Ingresa un nombre para tu workspace y elige la opción "Public" para que otros puedan verlo.  
4. Haz clic en "Create Workspace" para finalizar.

Los Workspaces públicos te permiten colaborar con otros usuarios y compartir tus colecciones.

## 3. Creación de una Colección

Las colecciones en Postman te permiten agrupar tus solicitudes. Para crear una colección:

1. En el panel izquierdo, haz clic en "Collections".  
2. Haz clic en el botón "New Collection" (ícono de carpeta con un signo más).  
3. Introduce un nombre para tu colección y una descripción opcional.  
4. Haz clic en "Create" para guardar la colección.

Una colección te ayuda a organizar y ejecutar solicitudes relacionadas.

## 4. Creación de Peticiones GET, POST, PUT y DELETE en Postman

Aquí te explicamos cómo crear y configurar solicitudes GET, POST, PUT y DELETE en Postman.

### 4.1. Solicitud GET

Las solicitudes GET se utilizan para obtener datos del servidor. Para crear una solicitud GET en Postman:

1. Selecciona la colección en la que deseas agregar la solicitud.  
2. Haz clic en el botón "Add Request" para crear una nueva solicitud.  
3. En la parte superior, selecciona "GET" del menú desplegable de métodos HTTP.  
4. Introduce la URL de la solicitud en el campo URL.  
5. Haz clic en "Send" para enviar la solicitud.

```
Ejemplo: Obtener detalles del usuario con ID 1.  
URL: https://api.example.com/users/1  
Método: GET
```

### 4.2. Solicitud POST

Las solicitudes POST se utilizan para enviar datos al servidor y crear nuevos recursos. Para crear una solicitud POST en Postman:

1. Selecciona la colección en la que deseas agregar la solicitud.  
2. Haz clic en el botón "Add Request" para crear una nueva solicitud.  
3. En la parte superior, selecciona "POST" del menú desplegable de métodos HTTP.  
4. Introduce la URL de la solicitud en el campo URL.  
5. Haz clic en la pestaña "Body".  
6. Selecciona "raw" y elige "JSON" en el menú desplegable de tipo de contenido.  
7. Introduce el cuerpo de la solicitud en el campo de texto.  
8. Haz clic en "Send" para enviar la solicitud.

Ejemplo: Crear un nuevo usuario con nombre "Jane Doe" y correo electrónico "jane@example.com".  
```
URL: https://api.example.com/users  
Método: POST  
```

Cuerpo:
```
{
  "name": "Jane Doe",
  "email": "jane@example.com"
}
```

### 4.3. Solicitud PUT

Las solicitudes PUT se utilizan para actualizar un recurso existente en el servidor. Para crear una solicitud PUT en Postman:

1. Selecciona la colección en la que deseas agregar la solicitud.
2. Haz clic en el botón "Add Request" para crear una nueva solicitud.
3. En la parte superior, selecciona "PUT" del menú desplegable de métodos HTTP.
4. Introduce la URL de la solicitud en el campo URL.
5. Haz clic en la pestaña "Body".
6. Selecciona "raw" y elige "JSON" en el menú desplegable de tipo de contenido.
7. Introduce el cuerpo de la solicitud en el campo de texto.
8. Haz clic en "Send" para enviar la solicitud.

Ejemplo: Actualizar los detalles del usuario con ID 1.
```
URL: [https://api.example.com/users/1](https://api.example.com/users/1)
Método: PUT
```

Cuerpo:

```
{
  "name": "John Smith",
  "email": "john.smith@example.com"
}
```

### 4.4. Solicitud DELETE

Las solicitudes DELETE se utilizan para eliminar un recurso del servidor. Para crear una solicitud DELETE en Postman:

1. Selecciona la colección en la que deseas agregar la solicitud.
2. Haz clic en el botón "Add Request" para crear una nueva solicitud.
3. En la parte superior, selecciona "DELETE" del menú desplegable de métodos HTTP.
4. Introduce la URL de la solicitud en el campo URL.
5. Haz clic en "Send" para enviar la solicitud.

Ejemplo: Eliminar el usuario con ID 1.
```
URL: [https://api.example.com/users/1](https://api.example.com/users/1)
Método: DELETE
```

## 5. Autenticación

Algunas APIs por seguridad requiren autorización. Hay varios tipos, depende de la API. En el caso de Supabase, usa de tipo API KEY. Para agregar la autentificación en postman sigue estos pasos:

1. Selecciona la solicitud en tu colección.
2. Haz clic en la pestaña "Authorization".
3. En el menú desplegable de tipo, selecciona "API KEY".
4. Rellena los campos con los siguientes datos:
   - Key: apikey
   - Value: API KEY de tu API. (Puedes encontrarlo en supabase, settings, api key)
   - Add to: selecciona HEADER
6. Haz clic en "Save" para guardar los cambios.

Con estos pasos, tu solicitud incluirá automáticamente las credenciales de autenticación básica.

## 6. Agregar Tests o Pruebas a las Solicitudes

Los tests en Postman te permiten validar la respuesta de una solicitud. Para agregar un test:

1. Selecciona la solicitud en tu colección.
2. Haz clic en la pestaña "Scripts".
3. Introduce el código del test en el campo de texto.
4. Haz clic en "Save" para guardar los cambios.

Ejemplo:

```
pm.test("Estado es 200", function () {
  pm.response.to.have.status(200);
});
pm.test("El nombre del usuario es John Doe", function () {
  var jsonData = pm.response.json();
  pm.expect(jsonData.name).to.eql("John Doe");
});
```

## 7. Uso y Guardado de Variables

Las variables en Postman te permiten reutilizar valores en tus solicitudes. Para guardar una variable de respuesta:

1. Selecciona la solicitud en tu colección.
2. Haz clic en la pestaña "Tests".
3. Introduce el código para guardar la variable en el campo de texto.
4. Haz clic en "Save" para guardar los cambios.

Ejemplo:

```
let responseData = pm.response.json();
pm.environment.set("userId", responseData.id);
```

Ahora puedes usar la variable `{{userId}}` en otras solicitudes.

## 8. Ejecución de Colecciones con Postman Runner

Puedes ejecutar todas las solicitudes de una colección en secuencia usando Postman Runner.

1. Haz clic en el botón "Runner" en la esquina superior izquierda.
2. Selecciona la colección que deseas ejecutar.
3. Configura los parámetros de ejecución, como el entorno y el número de iteraciones.
4. Haz clic en "Start Run" para ejecutar la colección.

Postman Runner te permite automatizar la ejecución de pruebas y revisar los resultados en un solo lugar.

## 9. Exportar Resultados con Postman

Puedes exportar los resultados de tus pruebas para su análisis o informes.

1. Después de ejecutar una colección en Postman Runner, haz clic en el botón "Export Results".
2. Selecciona el formato de exportación, como JSON o CSV.
3. Descarga el archivo con los resultados y guárdalo en tu ordenador.

Exportar resultados te permite guardar un registro de tus pruebas y compartir los resultados con otros.
