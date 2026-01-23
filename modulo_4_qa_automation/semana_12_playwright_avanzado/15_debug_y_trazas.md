# Playwright Debug y Trazas
[VER CLASE: Playwright - Debug y Trazas - 20 min](https://bootcampqa.com/videosauto/playwrightdebugtrazas.mp4)

## Debug
Para depurar los tests, puedes usar page.pause() para parar justo en el punto que quieras y desde ahi inspeccionar los elementos que necesites.

page.pause()
    
Esto abrirá el navegador en modo interactivo para inspeccionar paso a paso lo que sucede durante la prueba.

## Grabar y Ver Trazas
-------------------

Las trazas te permiten revisar exactamente lo que sucedió en cada test, especialmente útil cuando una prueba falla en github que no puedes verla.

### Guardar Trazas

- Ejecuta pruebas y guarda las trazas de todas las pruebas:
  
    pytest --tracing=on
  
- Ejecuta pruebas y guarda traza solo de las pruebas que fallen:

    pytest --tracing=retain-on-failure
    

### Ver las Trazas
Una vez que hayas grabado o descargado una traza, puedes verla usando el siguiente comando:

playwright show-trace trace.zip
