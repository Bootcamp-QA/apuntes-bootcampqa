# API Testing con Postman

[Ver clase: Configurar cuenta en POSTMAN - 5 min](https://bootcampqa.com/videosapi/api-crear-proyecto-postman-coleccion.mp4)

[Ver clase: Peticiones GET: Autentificación - 10 min](https://bootcampqa.com/videosapi/api-get-y-autentificacion.mp4)

[Ver clase: Peticiones GET: Variables y Tests- 30 min](https://bootcampqa.com/videosapi/api-get-variables-tests.mp4)

[Ver clase: Peticiones GET: Casos negativos - 10 min](https://bootcampqa.com/videosapi/api-get-casos-negativos.mp4)



## 1. Creación de Peticiones GET en Postman

Aquí te explicamos cómo crear y configurar solicitudes GET en Postman. Las solicitudes GET se utilizan para obtener datos del servidor. Para crear una solicitud GET en Postman:

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

## 2. Autenticación

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

## 3. Agregar Tests o Pruebas a las Solicitudes

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

## 4. Uso y Guardado de Variables

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

## 5. Ejecución de Colecciones con Postman Runner

Puedes ejecutar todas las solicitudes de una colección en secuencia usando Postman Runner.

1. Haz clic en el botón "Runner" en la esquina superior izquierda.
2. Selecciona la colección que deseas ejecutar.
3. Configura los parámetros de ejecución, como el entorno y el número de iteraciones.
4. Haz clic en "Start Run" para ejecutar la colección.

Postman Runner te permite automatizar la ejecución de pruebas y revisar los resultados en un solo lugar.

## 6. Exportar Resultados con Postman

Puedes exportar los resultados de tus pruebas para su análisis o informes.

1. Después de ejecutar una colección en Postman Runner, haz clic en el botón "Export Results".
2. Selecciona el formato de exportación, como JSON o CSV.
3. Descarga el archivo con los resultados y guárdalo en tu ordenador.

Exportar resultados te permite guardar un registro de tus pruebas y compartir los resultados con otros.
