Aserciones Playwright
------------------
[Ver clase: Playwright - Asserciones - 20min](https://bootcampqa.com/videosauto/pwasserciones.mp4)

Las aserciones son fundamentales para validar los resultados de las pruebas, te permite comprobar que los elementos que aparecen en la pagina son los esperados, puedes validar textos, urls, si estan o no visibles botones, imagenes o el numero de elementos mostrados entre muchas otras opciones. 

Puedes consultar la lista completa de aserciones en la documentación oficial de playwright: https://playwright.dev/python/docs/test-assertions

A continuación tienes un resumen de las más comunes:

### Verificar que un Elemento Contenga un Texto Específico

    expect(locator).to _contain _text("Texto parcial")
    

### Comprobar que un Elemento NO esté Visible

    expect(locator).not.to_be _visible()
    

### Comprobar que una URL Contenga un Texto

    import re
    expect(page).to _have _url("dashboard")
    

### Comprobar que un Elemento tenga un Color Específico

    expect(locator).to _have _css("color", "rgb(255, 0, 0)")  # rojo
    

### Comprobar que una Lista Contiene un Número de Elementos

    expect(locator).to _have_count(5)
