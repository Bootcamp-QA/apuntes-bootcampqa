# Creación de Peticiones POST, PATCH y DELETE en Postman

Aquí te explicamos cómo crear y configurar solicitudes GET, POST, PUT/PATCH y DELETE en Postman.



### 4.1. Solicitud PUT O PATCH
[Ver clase: Peticiones PATCH - 25 min](https://bootcampqa.com/videosapi/api-patch.mp4)

Las solicitudes PUT O PATCH se utilizan para actualizar un recurso existente en el servidor. Para crear una solicitud PUT en Postman:

1. Selecciona la colección en la que deseas agregar la solicitud.
2. Haz clic en el botón "Add Request" para crear una nueva solicitud.
3. En la parte superior, selecciona "PUT/PATCH" del menú desplegable de métodos HTTP.
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

### 4.2. Solicitud POST

[Ver clase: Peticiones POST - 20 min](https://bootcampqa.com/videosapi/api-post.mp4)

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



### 4.3. Solicitud DELETE
[Ver clase: Peticiones DELETE - 15 min](https://bootcampqa.com/videosapi/api-delete.mp4)

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


