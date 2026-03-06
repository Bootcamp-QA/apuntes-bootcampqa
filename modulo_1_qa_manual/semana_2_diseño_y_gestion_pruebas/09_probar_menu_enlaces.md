# Diseño Pruebas Menu y enlaces
[Ver clase: Diseño de pruebas en gherkin para menu - 25 min](https://bootcampqa.com/videos/manual-creacion-pruebas-gherkin.mp4)

## Verificar enlaces o menús

Si la página web contiene enlaces o botones con enlaces (botones que abren alguna página), debes verificar que funcionan correctamente los enlaces en cada sección en los que aparecen.  
En este caso solo tendrías que hacer un caso de prueba positivo por cada enlace. 
No debes probar que aparece, sino que funciona el enlace o boton pulsando en el y comprobando que abre la página correcta.

En el caso del menu, se suele usar examples para validar en un solo escenario todos los enlaces del menu.

Si el menu tiene muchas opciones, normalmente no se prueban todas, sino las más relevantes (las que el usuario vaya a usar más),
Ejemplos:
Scenario: Visitar enlaces del menu
Given el usuario esta en la pagina principal
When hace clic en el <menu>
Then debe ver la <pagina>

Examples:

| menu | pagina |

| Inicio | Inicio |

| Contacto | Contacto |

Scenario: Abrir enlace instagram
Given el usuario esta en la pagina principal
When hace clic en el enlace de instagram
Then debe ver la página de instagram "instagram.com/qa"

Scenario: Abrir carrito
Given el usuario esta en la página principal
When hace clic en el boton carrito
Then debe ver la página del carrito


