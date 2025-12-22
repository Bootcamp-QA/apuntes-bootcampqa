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
    