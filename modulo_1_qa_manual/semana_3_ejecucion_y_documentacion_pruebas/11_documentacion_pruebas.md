# Documentación de plan de pruebas

Antes de cada release, se documentan las pruebas realizadas para registrar los resultados, los errores encontrados y permitir tomar decisiones informadas sobre la calidad del producto y los próximos pasos. Esta documentación se centraliza en **Confluence** para que todo el equipo tenga acceso a la información.  

A continuación se presenta una **plantilla basada en ISTQB** para documentar las pruebas de manera estándar. La plantilla incluye:  

- **Objetivos de la prueba:** Qué se busca validar y asegurar en la versión probada.  
- **Alcance de la prueba:** Funcionalidades incluidas, navegadores y dispositivos a probar.  
- **Criterios de entrada y salida:** Condiciones necesarias para empezar y criterios para considerar la prueba completada.  
- **Tipos de prueba:** Funcionales, de regresión y exploratorias.  
- **Responsabilidades:** Quién realiza las pruebas y quién corrige los errores.  
- **Herramientas y datos de prueba:** Herramientas usadas para gestión, reporte y automatización.  
- **Comunicación y reporte:** Cómo se documentan los resultados y errores.  
- **Resultados y errores encontrados:** Resumen de la ejecución de pruebas y lista de incidencias detectadas.  

Esta estructura garantiza que las pruebas estén documentadas de manera clara, completa y estandarizada, facilitando la toma de decisiones sobre la calidad del producto y la planificación de futuras pruebas.


## Plantilla de Plan de pruebas basado en ISTQB

# Plan de Pruebas - [Nombre del Proyecto]

## Información General
**Proyecto:** [Nombre del proyecto]  
**Entorno de pruebas:** [Url de la web a probar]  
**Release Version:** [Enlace a la release]  
**Responsable de Pruebas:** [Nombre del QA]  


## Objetivos de la Prueba
- Validar las funcionalidades de la web.  
- Asegurar que los cambios recientes no rompan el sistema.  



## Alcance de la Prueba

- **Dispositivos y navegadores:**  
  - Desktop: Chrome  
  - Móvil: Simulación básica de iPhone SE (opcional)
-  **Funcionalidades a probar:**
[Enlace a las historias de usuario probadas]



## Criterios de Entrada
- Las historias de usuario debes estar desplegadas en el entorno de pruebas.  



## Criterios de Salida
- Todas las pruebas funcionales han sido ejecutadas.
- No hay errores críticos en la web.  
- Todas las pruebas de regresión han pasado.  



## Tipos de Prueba
- **Pruebas Funcionales:** Por cada historia de usuario.  
- **Pruebas de Regresión:** Antes de cada release y después de cada cambio, para asegurar que las funcionalidades existentes no se rompan.  
- **Pruebas Exploratorias:** Antes de cada release, para detectar errores no previstos por los casos de prueba formales.  



## Responsabilidades
- **QA:** Diseña y ejecuta las pruebas, reporta los errores y documenta los resultados.  
- **Desarrollo:** Implementa la web y corrige los errores detectados.  



## Herramientas y Datos de Prueba
- **Gestión de pruebas:** AssertThat  
- **Reporte de errores:** Jira  
- **Automatización:** Playwright  
- **Datos de prueba:** No se requieren datos adicionales



## Comunicación y Reporte
- Todos los errores se gestionan en Jira.  
- El resumen de resultados de pruebas y errores encontrados se documenta en Confluence.  



## Resultados de las Pruebas 
- Resultados de pruebas funcionales ejecutadas: [URL a pruebas funcionales]  
- Resultados de pruebas de regresión ejecutadas: [URL a pruebas de regresión]  



## Reporte de Errores
Se registraron todos los errores detectados durante las pruebas funcionales, de regresión y exploratorias.  

 [URL a errores]    

