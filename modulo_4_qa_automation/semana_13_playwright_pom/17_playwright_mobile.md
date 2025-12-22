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