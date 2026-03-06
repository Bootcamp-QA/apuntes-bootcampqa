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
