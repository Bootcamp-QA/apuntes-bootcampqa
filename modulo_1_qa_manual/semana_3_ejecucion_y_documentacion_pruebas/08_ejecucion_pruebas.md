# Ejecución de Pruebas

# Video de la clase


[Ver clase: Ejecución de Pruebas - 10 min](https://bootcampqa.com/videos/herramientasdegestiondepruebas.mp4)

# Apuntes

Debes ejecutar cada una de las pruebas en versión escritorio y versión móvil. Para ello sigue los siguientes pasos:

- Abre la página del proyecto en una ventana de incógnito.  
- Utiliza siempre la URL publicada en GitHub, nunca la URL de tu ordenador local.  
- Abre la historia de usuario que vas a probar, la cual contiene todas las pruebas a ejecutar.  

## Ejecución de los casos de prueba

- Para cada prueba, sigue los pasos indicados en la prueba y comprueba que los resultados obtenidos coinciden con los resultados esperados.  
- Ejecuta cada caso de prueba tanto en versión escritorio como en versión móvil.  

## Resultado de las pruebas

- Si los resultados coinciden con lo esperado en ambas versiones (escritorio y móvil), marca la prueba como **Pasada** en la herramienta de pruebas que estés utilizando.  
- Es recomendable añadir información adicional relevante, como:
  - Datos utilizados durante la prueba.  
  - Navegador y versión.  
  - Dispositivo o modelo de móvil utilizado.  
  - Sistema operativo.  

Cuanta más información se registre, mejor será la trazabilidad de la prueba.

## Gestión de pruebas fallidas

- Si al ejecutar una prueba los resultados no coinciden con lo esperado, marca la prueba como **Fallida**.  
- Crea un nuevo ticket de error o bug asociado a la prueba fallida, incluyendo:
  - Pasos para reproducir el error.  
  - Resultado esperado.  
  - Resultado obtenido.  
  - Evidencias si aplica (capturas, vídeos, logs).  

## Finalización de la historia de usuario

- Tras completar una prueba, ya sea pasada o fallida, continúa con la siguiente hasta ejecutar todas las pruebas definidas en la historia de usuario.  
- Una vez que **todas las pruebas estén ejecutadas y marcadas como Pasadas o Fallidas**, la historia de usuario puede considerarse completamente probada.  
- La historia de usuario debe cerrarse únicamente cuando todas las pruebas estén finalizadas y los resultados correctamente registrados.

