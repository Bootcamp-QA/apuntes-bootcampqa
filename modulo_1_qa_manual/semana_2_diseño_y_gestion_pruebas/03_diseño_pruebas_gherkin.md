# Tema 2.3 Diseño Pruebas en Gherkin

## Videos de la clase

[Ver clase: Diseño de pruebas en gherkin para menu - 25 min](https://bootcampqa.com/videos/manual-creacion-pruebas-gherkin.mp4)

[Ver clase: Diseño de pruebas en gherkin para menu - 25 min](https://bootcampqa.com/videos/manual-creacion-pruebas-gherkin.mp4)

[Ver clase: Diseño de pruebas en gherkin para menu - 25 min](https://bootcampqa.com/videos/manual-creacion-pruebas-gherkin.mp4)

[Ver clase: Diseño de pruebas en gherkin para menu - 25 min](https://bootcampqa.com/videos/manual-creacion-pruebas-gherkin.mp4)

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
