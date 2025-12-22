
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