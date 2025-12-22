#Introducción a Playwright
==========================

Para más detalles y ejemplos, consulta la [documentación oficial de Playwright para Python](https://playwright.dev/python/docs/intro).

Instalación y Ejecución de Tests
--------------------------------

Para comenzar, asegúrate de tener Python instalado y las dependencias necesarias.

### Instalación de Python

1 . Descarga e instala Python desde su [página oficial](https://www.python.org/downloads/).
2. Añade Python a tu `PATH` durante la instalación.
    

### Crear Proyecto en GitHub con Template de Playwright Python

Primero, utiliza el [template de Playwright Python](https://github.com/Bootcamp-QA/playwright-python-template). Haz clic en el botón **"Use this template"**, selecciona la opción **Public** y crea tu nuevo repositorio.

Una vez creado el repositorio, sigue estos pasos:

1.  Descarga el proyecto en tu equipo utilizando GitHub Desktop.
2.  Abre el proyecto en **Visual Studio Code**.

### Instalar Dependencias

Una vez abierto tu proyecto. Abre una terminal dentro de Visual Studio Code. Luego, instala las dependencias con:

pip install -r requirements.txt
playwright install
    

### Ejecución de Tests

Para ejecutar las pruebas en local:

pytest
# O si no reconoce el comando pytest
python -m pytest
    

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
    

Localizadores Avanzados
-----------------------

Playwright también proporciona localizadores avanzados para escenarios más específicos. Estos métodos permiten mayor precisión y flexibilidad al interactuar con elementos en la página:

### 1 . Filter (Filtrado)

Utiliza `filter()` para aplicar filtros adicionales a un locator existente. Esto permite encontrar un subconjunto específico de elementos dentro de un conjunto más grande.

locator = page.locator(".item").filter(has _text="Producto Destacado")
    

### 2 . First, Last, Nth

Usa `first`, `last`, o `nth()` para seleccionar un elemento específico de una lista de elementos encontrados. Esto es útil cuando necesitas interactuar con el primero, último, o un elemento en una posición específica.

 # Seleccionar el primer elemento
locator = page.locator(".item").first

# Seleccionar el último elemento
locator = page.locator(".item").last

# Seleccionar el tercer elemento (índice 2)
locator = page.locator(".item").nth(2)
    

### 3 . Locator Anidado

Los localizadores pueden anidarse para interactuar con elementos dentro de un contenedor específico. Este enfoque permite limitar el alcance de búsqueda a un contexto particular.

locator = page.locator("div.contenedor").get _by _role("heading", name="Título Principal")
    

### 4 . Selector CSS

Utiliza `locator()` con selectores CSS para localizar elementos basados en sus etiquetas, clases, o atributos específicos. Este enfoque es muy flexible pero puede ser menos robusto si los selectores cambian frecuentemente.

 # Localizar un elemento por etiqueta
locator = page.locator("h1")

# Localizar un elemento por etiqueta y clase
locator = page.locator("h1.updite")

# Localizar un elemento con un atributo específico
locator = page.locator("button [data-action='submit' ]")
    

Acciones Comunes
----------------

Aquí tienes algunas de las acciones más comunes que puedes realizar con Playwright:

### Hacer Clic

locator.click()
    

### Escribir Texto

locator.fill("Texto a escribir")
    

### Seleccionar una Opción en un Select

locator.select _option("value _opcion")
    

### Marcar o Desmarcar un Checkbox

 # Marcar un checkbox
locator.check()

# Desmarcar un checkbox
locator.uncheck()
    

### Esperar que un Elemento Sea Visible

locator.wait _for(state="visible")
    

Aserciones Comunes
------------------

Las aserciones son fundamentales para validar los resultados de las pruebas. Aquí tienes algunas comunes y avanzadas:

### Verificar que un Elemento Contenga un Texto Específico

expect(locator).to _contain _text("Texto parcial")
    

### Comprobar que un Elemento NO esté Visible

        expect(locator).not.to _be _visible()
    

### Comprobar que una URL Contenga un Texto

import re
expect(page).to _have _url("dashboard")
    

### Comprobar que un Elemento tenga un Color Específico

expect(locator).to _have _css("color", "rgb(255, 0, 0)")  # rojo
    

### Comprobar que una Lista Contiene un Número de Elementos

expect(locator).to _have _count(5)
    

Grabación de Tests
------------------

Playwright permite grabar tests automáticamente mediante el comando `codegen`.

 # Graba un test interactivo en Playwright
playwright codegen https://bootcampqa.com
    

Esto abrirá un navegador donde puedes realizar interacciones, y Playwright generará automáticamente el código de test.

Test en Moviles
---------------

Puedes utilizar playwright para saber el tamaño de la pantalla.Si el ancho de la pantalla (width) es mayor a 1024 sera un ordenador, sino sera movil o tablet.

 # Comprobar el tamaño de la pantalla en playwright
    page.viewport _size ['width' ]
    page.viewport _size ['height' ]
    

Por defecto playwright ejecuta los tests en tamaño escritorio, pero con el comando Device puedes elegir en que tamaño quieres que se ejecute.

 # Ejecutar con Device telefono movil
    pytest --device='iPhone 12'
    

[Lista de Devices Disponibles](https://github.com/microsoft/playwright/blob/main/packages/playwright-core/src/server/deviceDescriptorsSource.json)

Grabación de Videos y Otras Opciones
------------------------------------

Playwright permite grabar videos de cada test y ajustar varias opciones. Aquí están algunas de las más útiles:

### Grabar Videos

 # Graba un video de cada test
pytest --video=on
# Solo graba si falla
pytest --video=retain-on-failure
    

### Capturas de Pantalla

 # Captura una captura de pantalla después de cada test
pytest --screenshot=on
# Solo captura si falla
pytest --screenshot=only-on-failure
    

### Opciones Adicionales

 # Ejecuta en modo visible
pytest --headed

# Emula un dispositivo
pytest --device="iPhone 12"
    

4 . Depuración
--------------

Para depurar los tests, puedes usar page.pause() para parar justo en el punto que quieras y desde ahi inspeccionar los elementos que necesites.

page.pause()
    

Esto abrirá el navegador en modo interactivo para inspeccionar paso a paso lo que sucede durante la prueba.

Grabar y Ver Trazas
-------------------

Las trazas te permiten revisar exactamente lo que sucedió en cada test, especialmente útil cuando una prueba falla.

### Grabar Trazas

 # Graba una traza de cada prueba
pytest --tracing=on
# Solo graba traza si falla
pytest --tracing=retain-on-failure
    

### Ver las Trazas

Una vez que hayas grabado una traza, puedes verla usando el siguiente comando:

playwright show-trace trace.zip