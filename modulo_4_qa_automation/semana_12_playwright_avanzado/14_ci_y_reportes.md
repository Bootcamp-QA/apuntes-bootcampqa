Configuración en integración continua y reportes
------------------------------------
[VER CLASE: Reportes e Integración Contínua Github Actions - 20 min](https://bootcampqa.com/videosauto/playwrightci.mp4)

Perfecto, te agrego **solo lo básico**, para que entiendan **qué es integración continua** y **qué pinta GitHub Actions aquí**, sin entrar en demasiado detalle y alineado con el workflow que pasas.

---

## Configuración en integración continua y reportes

[VER CLASE: Reportes e Integración Contínua Github Actions - 20 min](https://bootcampqa.com/videosauto/playwrightci.mp4)

## Integración continua (CI)

La integración continua es una práctica que consiste en **ejecutar los tests automáticamente** cada vez que hay cambios en el código o en momentos programados.

El objetivo principal es:

* Detectar errores lo antes posible
* Validar que los tests siguen funcionando después de cada cambio
* Evitar que código con fallos llegue a producción

En este curso, la integración continua se hace usando **GitHub Actions**.

---

## GitHub Actions y ejecución de tests

GitHub Actions permite definir **workflows** que se ejecutan automáticamente en servidores de GitHub.

No es necesario entender todo el workflow en detalle, solo saber que **GitHub se encarga de ejecutar los tests por nosotros**.

---

## Qué hace el workflow de Playwright (resumen)

De forma general, el flujo es el siguiente:

1. Descarga el código del repositorio en el servidor de github
2. Instala Python
3. Instala las dependencias del proyecto
4. Instala los navegadores de Playwright
5. Ejecuta los tests con Pytest con las configuraciones que le indiquemos.
6. Genera reportes HTML
7. Guarda videos y resultados como artefactos, que son archivos que pueden descargarse desde github.

---

## Reportes y evidencias en Playwright

Playwright permite grabar videos de cada test y ajustar varias opciones. Aquí están algunas de las más útiles:

### Grabar Videos

Graba un video de cada test:

```bash
pytest --video=on
```

Solo graba si falla:

```bash
pytest --video=retain-on-failure
```

---

### Capturas de Pantalla

Captura una captura de pantalla después de cada test:

```bash
pytest --screenshot=on
```

Solo captura si falla:

```bash
pytest --screenshot=only-on-failure
```

---

### Opciones Adicionales

Ejecuta en modo visible:

```bash
pytest --headed
```

Emula un dispositivo:

```bash
pytest --device="iPhone 12"
```


