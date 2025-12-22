Navegación en Playwright
------------------------

La navegación es una parte fundamental de las pruebas con Playwright. Aquí te mostramos cómo utilizar `goto()`, `wait_for_url()`, y métodos para obtener la URL y el título de la página.

### 1 . Ir a una Página con `goto()`

El método `goto()` se utiliza para navegar a una URL específica. Maneja automáticamente redirecciones y espera hasta que la página haya terminado de cargar.

 # Navegar a una URL específica
    page.goto("https://bootcampqa.com")
    

Utiliza `goto()` como el primer paso para cargar la página que quieres probar.

### 2 . Esperar a una URL Específica con `wait_for_url()`

El método `wait_for_url()` se utiliza para esperar a que la URL cambie a una dirección específica. Es útil cuando hay una redirección después de una acción, como hacer clic en un botón o enviar un formulario.

 # Esperar hasta que la URL contenga "dashboard"
     page.wait _for _url(" * */dashboard")
    

Esta técnica permite asegurarte de que la redirección ha ocurrido antes de continuar con las siguientes acciones del test.

### 3 . Obtener la URL Actual con `page.url`

El atributo `page.url` devuelve la URL actual de la página. Es útil para validar que la navegación ha sido exitosa y para hacer aserciones.

 # Obtener la URL de la página actual
current _url = page.url
print(f"La URL actual es: {current _url}")
    

Úsalo para comprobar que estás en la página correcta después de una acción de navegación.

### 4 . Obtener el Título de la Página con `page.title()`

El método `page.title()` devuelve el título de la página actual. Es útil para validar que se ha cargado la página correcta y para verificar el contenido de la pestaña del navegador.

 # Obtener el título de la página
page _title = page.title()
print(f"El título de la página es: {page _title}")
    

El título suele ser un buen indicador para confirmar que la página cargada es la esperada.

### 5 . Esperar a que la Página se Cargue Completamente con `wait_for_load_state()`

El método `wait_for_load_state()` asegura que la página esté completamente cargada antes de continuar. Esto reduce errores por intentar interactuar con elementos que aún no están disponibles.

 # Esperar hasta que la página esté completamente cargada
 page.wait _for _load _state("load")
    

Usa esta función cuando necesites estar seguro de que todos los recursos (como imágenes y scripts) se han cargado antes de proceder.

Localizadores
-------------

Playwright ofrece una variedad de localizadores para interactuar con elementos en la página. A continuación, se presentan ordenados de más a menos recomendados, basándonos en accesibilidad, facilidad de mantenimiento y robustez:

### 1 . Por Rol (Recomendado para accesibilidad)

Utiliza `get_by_role()` para localizar elementos basados en su rol. Este enfoque es ideal para pruebas accesibles y es menos propenso a fallos debido a cambios en el diseño de la página.

locator = page.get _by _role("button", name="Enviar")
    

### 2 . Por Texto

Utiliza `get_by_text()` para localizar elementos basados en su contenido de texto. Es útil cuando el texto es estable y no cambia frecuentemente.

locator = page.get _by _text("Iniciar sesión")
    

### 3 . Por Etiqueta Asociada (Label)

Utiliza `get_by_label()` para localizar controles de formulario asociados a un texto de etiqueta. Esto facilita la interacción con formularios y mejora la legibilidad del código.

locator = page.get _by _label("Correo Electrónico")
    

### 4 . Por Placeholder

Utiliza `get_by_placeholder()` para localizar un campo de entrada basado en el texto de sugerencia (placeholder). Es útil para identificar campos de texto que tienen un placeholder único.

locator = page.get _by _placeholder("Introduce tu correo")
    

### 5 . Por Texto Alternativo (Alt Text)

Utiliza `get_by_alt_text()` para localizar elementos, generalmente imágenes, basados en su texto alternativo. Es útil para verificar imágenes o elementos gráficos en la página.

locator = page.get _by _alt _text("Logo de la empresa")
    

### 6 . Por Atributo de Título

Utiliza `get_by_title()` para localizar elementos basados en su atributo de título. Es útil cuando el elemento tiene un atributo `title` claro y único.

locator = page.get _by _title("Cerrar ventana")
    

### 7 . Por `data-testid` (Para pruebas específicas)

Utiliza `get_by_test_id()` para localizar elementos basados en el atributo `data-testid`. Esto es útil cuando se controlan los atributos de prueba en el código de la aplicación.

locator = page.get _by _test _id("submit-button")
    
