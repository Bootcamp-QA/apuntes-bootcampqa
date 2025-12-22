Grabación de Videos y Otras Opciones
------------------------------------

Playwright permite grabar videos de cada test y ajustar varias opciones. Aquí están algunas de las más útiles:

### Grabar Videos

 # Graba un video de cada test
pytest --video=on
# Solo graba si falla
pytest --video=retain-on-failure
    

### Capturas de Pantalla

 # Captura una captura de pantalla después de cada test
pytest --screenshot=on
# Solo captura si falla
pytest --screenshot=only-on-failure
    

### Opciones Adicionales

 # Ejecuta en modo visible
pytest --headed

# Emula un dispositivo
pytest --device="iPhone 12"
    
