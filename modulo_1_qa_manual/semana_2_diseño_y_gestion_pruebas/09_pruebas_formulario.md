# Diseño de pruebas para formularios

[Ver clase: Diseño de pruebas en gherkin para formularios - 30 min](https://bootcampqa.com/videos/manual-pruebas-formulario.mp4)

Cuando una web tiene un formulario, para probarlo debes rellenar los campos del formulario y enviarlo.
 

## Casos positivos:
En los casos positivos, rellenas el formulario con datos válidos, que te permiten enviar el formulario. 
En este puedes validar todos los campos a la vez, es decir enviar con todos los valores válidos. 

- Enviar todos los campos obligatorios sin opcionales.  
- Enviar todos los campos obligatorios y opcionales. 

Ejemplos:

Scenario: Enviar formulario con los campos obligatorios
Given el usuario esta en la pagina de reserva
When rellena el formulario con campos obligatorios validos <email>,<mensaje>
And envia el formulario
Then debe ver un mensaje de reserva enviada

Examples:

| email | mensaje |

| test@gmail.com | Mensaje de Prueba 1 |

| test_23ñ-sk@email.es | Mensaje carácteres especiales()? |

Scenario: Enviar formulario con los campos obligatorios y opcionales
Given el usuario esta en la pagina de reserva
When rellena el formulario con campos obligatorios validos <email>,<mensaje>, <telefono>
And envia el formulario
Then debe ver un mensaje de reserva enviada

Examples:

| email | mensaje | telefono |

| test@gmail.com | Mensaje de Prueba 1 | 666777888 |

| test_23ñ-sk@email.es | Mensaje carácteres especiales()? | +34666777888|

## Casos negativos:
En los casos negativos, rellenas el formulario con datos no válidos, es decir los que te mostrarán un mensaje de error y no te dejará enviar el formulario.
Estos casos debes validarlos por separado, es decir, enviar todos los valores bien excepto el que estás probando, que lo envías con el valor no válido.

### Dejar vacíos campos obligatorios. Un caso de prueba por cada campo vacío.  
 Ejemplo:
Scenario: Enviar formulario con los campos obligatorios
Given el usuario esta en la pagina de reserva
When rellena el formulario con campos obligatorios vacios <email>,<mensaje>
And envia el formulario
Then debe ver un mensaje error
And el formulario no debe enviarse

Examples:
| email | mensaje |

| vacio | Mensaje de Prueba 1 |

| test_23ñ-sk@email.es | vacio |

### Validación adicional de campos:

- Formato: Comprobar que valida que se introducen los datos en el formato correcto.  
  Ejemplo: Emails, Cuenta Bancaria.  
- Tamaño: Comprobar que valida el máximo de caracteres permitidos en un campo.  
  Ejemplo: Nombre, Mensaje.  
- Rango: Comprobar que valida el rango permitido.  
  Ejemplo: Cantidades, Fechas, números.  

Scenario: Enviar formulario con email invalido
Given el usuario esta en la pagina de reserva
When rellena el formulario con campo email invalido "testgmail.com"
And envia el formulario
Then debe ver un mensaje error
And el formulario no debe enviarse



