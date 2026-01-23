Grabación de Tests
------------------

Playwright permite grabar tests automáticamente mediante el comando `codegen`.

 # Graba un test interactivo en Playwright
 1. Abre tu proyecto en visual studio
 2. En el terminal de visual studio ejecuta este comando:
 `
playwright codegen https://bootcampqa.com
`
3. Esto abrirá un navegador donde puedes realizar interacciones, y Playwright generará automáticamente el código de test.
4. En la carpeta test crea un archivo por cada historia de usuario por ejemplo login.py
5. Dentro del archivo menu.py crea un nuevo test, debe empezar siempre por la palabra test, por ejemplo test_login_valido
6. Pega el código
7. Prueba el test ejecutando en la terminal:

    `
pytest --headed
`

Repite los pasos para nuevos tests.
