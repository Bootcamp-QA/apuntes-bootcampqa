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