# Acciones en Playwright

[Ver Clase: Acciones y Formularios 25 min](https://bootcampqa.com/videosauto/pwrellenarformularios.mp4)

## Acciones
Las acciones sirven para interactuar con los elementos de la web. 
Puedes ver la lista completa de acciones en la documentación oficial de playwright: https://playwright.dev/python/docs/input

A continuación se detallan las más usadas:

### Hacer Clic

```python
locator.click()
```

### Escribir Texto

```python
locator.fill("Texto a escribir")
```

### Seleccionar una Opción en un Select

```python
locator.select_option("value _opcion")
```

### Marcar o Desmarcar un Checkbox

```python
# Marcar un checkbox
locator.check()

# Desmarcar un checkbox
locator.uncheck()
```

### Esperar que un Elemento Sea Visible

```python
locator.wait _for(state="visible")
```

