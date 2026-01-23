Test en Moviles
---------------


[VER CLASE: Playwright - Tests en Móviles - 15 min](https://bootcampqa.com/videosauto/playwrightmobile.mp4)

 # Ejecutar con Device telefono movil

 Por defecto playwright ejecuta los tests en tamaño escritorio, pero con el comando Device puedes elegir en que tamaño quieres que se ejecute.

    pytest --device='iPhone 12'


[Lista de Devices Disponibles](https://github.com/microsoft/playwright/blob/main/packages/playwright-core/src/server/deviceDescriptorsSource.json)

 # Comprobar el tamaño de la pantalla en playwright
 En general, los tests van a funcionar en cualquier tamaño, entonces los tests funcionan sin ninguna modificación.
 Pero hay algunos casos específicos en que se muestra diferente en móvil que en escritorio, como por ejemplo el menú. 
 En esos casos, debemos indicar en el test que actue diferente según el tamaño de la pantalla.
 Puedes utilizar playwright para saber el tamaño de la pantalla.
 Si el ancho de la pantalla (width) es mayor a 1024 sera un ordenador, y se hará la acción que corresponda en el ordenador, sino sera movil o tablet y se hará la acción de ese tamaño.
 
    page.viewport _size ['width' ]
    page.viewport _size ['height' ]
    




    

