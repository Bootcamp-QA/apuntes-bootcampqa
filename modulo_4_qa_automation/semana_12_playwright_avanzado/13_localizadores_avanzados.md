#Localizadores Avanzados
-----------------------

[VER CLASE: Localizadores Avanzados - 30 min](https://bootcampqa.com/videosauto/playwrightlocalizadoresavanzados.mp4)

Playwright también proporciona localizadores avanzados para escenarios más específicos. Estos métodos permiten mayor precisión y flexibilidad al interactuar con elementos en la página. Algunos de los más comunes son:

### 1 . Filter (Filtrado)

Utiliza `filter()` para aplicar filtros adicionales a un locator existente. Esto permite encontrar un subconjunto específico de elementos dentro de un conjunto más grande.

locator = page.locator(".item").filter(has _text="Producto Destacado")
    

### 2 . First, Last, Nth

Usa `first`, `last`, o `nth()` para seleccionar un elemento específico de una lista de elementos encontrados. Esto es útil cuando necesitas interactuar con el primero, último, o un elemento en una posición específica.

 Ejemplo Seleccionar el primer elemento
locator = page.locator(".item").first

Ejemplo Seleccionar el último elemento
locator = page.locator(".item").last

Ejemplo Seleccionar el tercer elemento (índice 2)
locator = page.locator(".item").nth(2)
    

### 3 . Locator Anidado

Los localizadores pueden anidarse para interactuar con elementos dentro de un contenedor específico. Este enfoque permite limitar el alcance de búsqueda a un contexto particular.

locator = page.locator("div.contenedor").get _by _role("heading", name="Título Principal")
    

### 4 . Selector CSS

Utiliza `locator()` con selectores CSS para localizar elementos basados en sus etiquetas, clases, o atributos específicos. Este enfoque es muy flexible pero puede ser menos robusto si los selectores cambian frecuentemente.

 Ejemplo Localizar un elemento por etiqueta
locator = page.locator("h1")

Ejemplo Localizar un elemento por etiqueta y clase
locator = page.locator("h1.updite")

Ejemplo Localizar un elemento con un atributo específico
locator = page.locator("button [data-action='submit' ]")
