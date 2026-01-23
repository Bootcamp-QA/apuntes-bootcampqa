# Introducción a Playwright

[Ver clase: Playwright Configuración Inicial - 15 min](https://bootcampqa.com/videosauto/configurarproyectoplaywright.mp4)


Para más detalles y ejemplos, consulta la [documentación oficial de Playwright para Python](https://playwright.dev/python/docs/intro).

Instalación y Ejecución de Tests
--------------------------------

Para comenzar, asegúrate de tener Python instalado y las dependencias necesarias.

### Instalación de Python

1 . Descarga e instala Python 12 desde su [página oficial](https://www.python.org/downloads/).
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
