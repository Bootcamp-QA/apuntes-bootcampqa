# Diseño Pruebas en Gherkin

## Videos de la clase

[Ver clase: Diseño de pruebas en gherkin para menu - 25 min](https://bootcampqa.com/videos/manual-creacion-pruebas-gherkin.mp4)

[Ver clase: Diseño de pruebas en gherkin para verificar información - 10 min](https://bootcampqa.com/videos/manual-creacion-pruebas-verificar-informacion.mp4)

[Ver clase: Diseño de pruebas en gherkin para formularios - 30 min](https://bootcampqa.com/videos/manual-pruebas-formulario.mp4)

[Ver clase: Diseño de pruebas en gherkin para login, registros y filtros - 20 min](https://bootcampqa.com/videos/manual-pruebas-login-filtros.mp4)

## Apuntes

## Lenguaje Gherkin

El lenguaje Gherkin define la estructura y sintaxis básica para la descripción de pruebas que pueden ser entendidas tanto por los integrantes técnicos del equipo como por los Product Owners. De esta manera, mientras se generan pruebas, se crea documentación actualizada que describe cómo se comporta el sistema.

## Feature

Feature (Funcionalidad) es equivalente a la historia de usuario.  
Es una descripción breve de la funcionalidad que se va a desarrollar desde el punto de vista del usuario.

**Ejemplo:**

Feature: Contacto
Como recruiter
Quiero ver la información de contacto
Para poder contactar con el candidato


## Scenario

Un escenario describe un ejemplo concreto de la funcionalidad a desarrollar (feature). Una misma feature puede tener varios escenarios, uno por cada ejemplo diferente.

**Ejemplo:**

Feature: Ver info de Contacto
Como recruiter
Quiero ver la información de contacto
Para poder contactar con el candidato

Scenario: Ver teléfono
Scenario: Ver email
Scenario: Ver dirección


## Steps (Given, When, Then)

Los steps describen los pasos a seguir para llevar a cabo cada escenario:

- **Given (Dado):** Precondición  
- **When (Cuando):** Acción  
- **Then (Entonces):** Resultado esperado  

**Ejemplo:**

Scenario: Ver teléfono
Given el recruiter abre mi cv web
When comprueba la sección de contacto
Then debe ver el teléfono 666 777 888


## Steps (And, But)

Se usan para continuar pasos del mismo tipo sin repetir la palabra clave.

**Ejemplo:**

Scenario: Ver habilidades (skills)
Given el recruiter abre mi cv web
When comprueba la sección de habilidades
Then debe ver trabajo en equipo
And debe ver comunicación
And debe ver atención al detalle


## Background

Cuando un mismo step se repite en todos los escenarios de una feature, se utiliza la sección `Background` para evitar repetir los pasos en cada escenario.

**Ejemplo:**

Feature: Ver Contacto
Como recruiter
Quiero ver la sección de contacto
Para poder contactar al candidato

Background:
Given el recruiter abre el CV Web
When el recruiter consulta la sección contacto

Scenario: Ver teléfono
Then el recruiter ve el teléfono 666 777 888

Scenario: Ver email
Then el recruiter ve el email info@gmail.com


## Scenario Outline

Se utiliza para ejecutar el mismo scenario varias veces con diferentes combinaciones de valores.

Scenario Outline: Ver formación
Given el recruiter abre el cv
When consulta la sección de educación
Then debe ver <formación>, <centro>, <fecha>

Examples:
| Formación | Centro | Fecha |
| Ing. Informática | Uni. Sevilla | 2008 |
| Máster Profesorado | Uned | 2018 |


## Data Tables

Se usan para pasar una lista de valores a un step.

Scenario: Ver habilidades (skills)
Given el recruiter abre mi cv web
When comprueba la sección de habilidades
Then debe ver las habilidades:
| habilidad |
| trabajo en equipo |
| comunicación |
| atención al detalle |


## Tags y Comments

- **Tags:** Se usan para agrupar escenarios o features. Se colocan sobre el escenario o feature, no a nivel de steps.  
- **Comments:** Se agregan en nuevas líneas y deben ser de una sola línea para aclarar algo específico.

@cv @habilidades
Feature: Ver habilidades
Como recruiter
Quiero ver la sección de habilidades
Para poder saber las habilidades del candidato

@regression
Scenario: Ver habilidades
Given el recruiter abre mi cv web
When comprueba la sección de habilidades
Then debe ver las habilidades:
| habilidad |
| trabajo en equipo |
| comunicación |
| atención al detalle |

## BUENAS PRÁCTICAS LENGUAJE GHERKIN

# Gherkin  
## Buenas Prácticas  

### Guía de Buenas Prácticas.  

### Que son las buenas prácticas  
Escribir buenos escenarios en Gherkin no es fácil a la primera.  

**La regla de oro:**  
Trata a otros lectores como te gustaría que te trataran. Escribe Gherkin de modo que  
las personas que no conocen la funcionalidad, la entiendan.  

Esta guía de buenas prácticas, te ayudarán a escribir escenarios de Gherkin más  
entendibles.  

### Steps en forma declarativa  
Evita describir de forma técnica los pasos, céntrate en explicar comportamiento.  

Para hablar del login, indica que el usuario hace login, en lugar de decir que introduce  
el usuario, luego la contraseña y luego hace click en el botón login.  

### Una acción por step  
Cada step debe describir una sola acción, esto quiere decir que si un step  
describe varias cosas, mejor dividirlo en dos.  

### Background cortos  
El background debería tener como mucho 4 steps, idealmente 2, para evitar  
hacer demasiado compleja la funcionaidad.  

### Escenarios con un sólo propósito  
Cada escenario debe describir un único comportamiento. Si describe varios,  
debes dividirlo en dos diferentes.  

### Respeta el orden Given,When,Then  
Los steps siempre deben ir en el orden Given (Opcional), When,  
Then.  

### Máximo 7 steps por escenario.  
Idealmente debe tener no más de 5 y máximo 7. Si son mas, es posible que  
puedas dividir el escenario o el feature en funcionalidades más pequeñas.  

### Formato Steps  
Siempre en tercera persona. El usuario, el administrador, el recruiter...  
Siempre en presente. El usuario hace click  
Incluye siempre sujeto y predicado en las frases.  

### Título de Scenarios  
Deben ser cortos; Una sola línea.  
Describe qué hace. No incluyes el cómo o el por qué.  
No incluyas Y, O (Esto significa que puedes dividir el escenario, un escenario,  
una cosa, no lo olvides).  

Evita el lenguaje de testing; Verifica, debe... todos comprueban cosas, no  
aporta nada agregar verifica que se ve el teléfono, indica ver teléfono en su  
lugar.

## IDENTIFICACIÓN DE CASOS DE PRUEBA
## TIPOS DE CASOS DE PRUEBA

### Caso de prueba positivo
El usuario elige o introduce valores dentro del rango permitido.  
Da un resultado positivo.

**Ejemplo:**  
Introducir contraseña correcta.

---

### Caso de prueba negativo
El usuario elige o introduce valores erróneos o no permitidos.  
Se espera como resultado un mensaje de error.

**Ejemplo:**  
Introducir contraseña incorrecta.

## Verificar información

Visitar las diferentes secciones de la página y comprobar que muestra la información correcta.

- Títulos  
- Descripciones  
- Imágenes  

Si tiene varios idiomas, probar en los diferentes idiomas.  
En este caso solo tendrías que hacer un caso de prueba positivo por cada idioma para validar la información de cada sección.

## Verificar enlaces o menús

Si la página web contiene enlaces, debes verificar que funcionan correctamente los enlaces en cada sección en los que aparecen.  
En este caso solo tendrías que hacer un caso de prueba positivo por cada enlace.

## Validación de formularios y filtros

En los formularios siempre debes verificar:

- Campos obligatorios y opcionales  

Casos positivos:
- Enviar todos los campos obligatorios sin opcionales.  
- Enviar todos los campos obligatorios y opcionales.  

Casos negativos:
- Dejar vacíos campos obligatorios. Un caso de prueba por cada campo vacío.  

Validación adicional de campos:

- Formato: Comprobar que valida que se introducen los datos en el formato correcto.  
  Ejemplo: Emails, Cuenta Bancaria.  
- Tamaño: Comprobar que valida el máximo de caracteres permitidos en un campo.  
  Ejemplo: Nombre, Mensaje.  
- Rango: Comprobar que valida el rango permitido.  
  Ejemplo: Cantidades, Fechas, números.  

En los casos positivos puedes validar todos los campos a la vez, es decir enviar con todos los valores válidos.  
En los casos negativos debes validarlos por separado, es decir, enviar todos los valores bien excepto el que estás probando, que lo envías con el valor no válido.

## Validación de registros de usuarios y logins

Si la página web tiene un sistema de registro de usuarios y login debes validar lo siguiente:

Registro de usuario y login usando la técnica de transición de estados.

Usuario registrado:
- Pasar de no registrado a registrado (positivo).  
- Usuario ya registrado no puede registrarse (negativo).  
- Usuario bloqueado no puede registrarse (negativo).  

Usuario bloqueado:
- Usuario registrado pasa a bloqueado (positivo).  

Validación de formulario de registro:
- Igual que cualquier formulario.  

Técnica de tabla de decisión, combinar las posibles opciones de usuario y contraseña:

- Usuario: Registrado, No registrado o Bloqueado.  
- Contraseña: Correcta o Incorrecta.


