# Diseño de Pruebas de validar información

[Ver clase: Diseño de pruebas en gherkin para verificar información - 10 min](https://bootcampqa.com/videos/manual-creacion-pruebas-verificar-informacion.mp4)

Estas pruebas tienen como objetivo, visitar las diferentes secciones de la página y comprobar que muestra la información correcta como:

- Títulos  
- Descripciones  
- Imágenes  

Si tiene varios idiomas, se debe probar en los diferentes idiomas, y puedes usar examples para validar varios idiomas en un mismo escenario.  
Solo tiene casos positivos, de validar la información mostrada, no tiene casos negativos.

Ejemplos:

Scenario: Ver información página de inicio
Given el usuario abre la web "myblog.com"
When visita la página de inicio
Then debe ver el titulo "My Blog"
And debe ver una descripción del blog
And debe ver una imagen principal

Scenario: Cambiar idioma
Given el usuario abre la web "myblog.com"
When cambia el idioma a <idima>
Then debe ver la información de la página en <idioma>

Examples:
| idioma |
| inglés |
| español |
| alemán |
