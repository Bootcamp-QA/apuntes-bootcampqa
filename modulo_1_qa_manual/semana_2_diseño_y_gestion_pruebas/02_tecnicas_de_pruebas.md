# Tema 2.2.1 Técnicas de Pruebas  
Basado en el estándar ISTQB

## Video de la clase

[Ver clase: Técnicas de Pruebas - 10 min](https://bootcampqa.com/videos/tecnicasdepruebas.mp4)

## Apuntes

## ¿Qué son las técnicas de pruebas?

Las técnicas de prueba son mecanismos que se utilizan con el objetivo de identificar los casos de prueba con mayor probabilidad de encontrar defectos y obtener la mayor cobertura posible en cuanto a las pruebas de un sistema.

## Técnicas de pruebas de caja blanca

Las técnicas de pruebas de caja blanca se basan en el conocimiento interno del código de un programa o sistema. Son muy útiles para encontrar errores en el código y garantizar que no exista código muerto o partes del sistema sin probar.

### Técnica de cobertura de sentencia

La cobertura de sentencia tiene como objetivo asegurar que todas las sentencias de código del programa hayan sido ejecutadas al menos una vez durante las pruebas.

Es importante porque:
- Ayuda a identificar sentencias que no han sido ejecutadas.
- Permite detectar código muerto o secciones no utilizadas.
- Puede indicar funcionalidades que no se han probado adecuadamente.

### Prueba y cobertura de rama

La técnica de cobertura de decisión se utiliza para medir cuántas decisiones dentro de una estructura de control han sido probadas.

Cada estructura puede tener múltiples opciones o caminos.  
El objetivo principal es asegurar que todas las posibles opciones dentro de una estructura de control sean probadas.

## Técnicas de pruebas basadas en la experiencia

Cuando hablamos de estas técnicas, nos centramos únicamente en los datos de entrada y los resultados obtenidos, sin analizar la estructura interna de la funcionalidad.

### Predicción de errores

Se utiliza para predecir la cantidad de errores que pueden existir en el software antes de realizar pruebas formales.

Se basa en:
- Información histórica de pruebas anteriores.
- Experiencias en proyectos similares.
- Complejidad del software.

### Pruebas exploratorias

Su objetivo principal es la detección de posibles defectos.  
Dependen en gran medida de la habilidad del QA para identificar problemas que pueden ser difíciles de encontrar con otros enfoques de prueba.

### Lista de comprobación

En esta técnica, el QA utiliza su experiencia previa para elaborar una lista de comprobación que sirve como guía para dirigir las pruebas.

La lista:
- Establece un estándar.
- Ayuda a recordar qué debe ser probado.
- Permite identificar qué ya fue probado.

## Técnicas de pruebas de caja negra

Son grupos de actividades de pruebas realizadas en relación con el producto en una etapa determinada del desarrollo.

### Partición de equivalencia

Los datos de entrada se dividen en particiones o clases de equivalencia.

Los datos que producen el mismo resultado se agrupan en una misma clase, esperando que todos los miembros de una partición sean procesados de la misma manera.

### Análisis de valor límite o valor frontera

Es una extensión de la partición de equivalencia y se utiliza solo para valores numéricos.

En esta técnica:
- Se toman como mínimo los dos valores límite.
- Opcionalmente, se prueba un valor entre los límites.

### Tabla de decisión

Se utiliza para probar el comportamiento del sistema usando diferentes combinaciones de entrada.

Las combinaciones de entrada y los resultados esperados se representan en forma tabular.

### Transición de estado

En esta técnica, las condiciones de entrada provocan cambios de estado.

Es ideal para:
- Sistemas que dependen de eventos pasados.
- Sistemas que funcionan mediante una secuencia de eventos.

## Enfoque basado en la colaboración

Las técnicas anteriores se enfocan principalmente en la detección de defectos.  
Este enfoque, además, busca prevenir defectos.

BDD es un ejemplo de enfoque basado en la colaboración.

### Redacción colaborativa de historias de usuario

La historia de usuario se redacta de forma conjunta con todo el equipo.

En BDD, este proceso se realiza en la llamada **Three Amigos Meeting**.

### Criterios de aceptación

Los criterios de aceptación son las condiciones que una historia de usuario debe cumplir para ser aceptada.

- Son el resultado de la conversación del equipo.
- Pueden verse como condiciones de prueba.
- En BDD, equivalen a los escenarios de prueba.

### Desarrollo guiado por pruebas de aceptación

Es el equivalente en ISTQB a BDD.

En ISTQB se denomina desarrollo guiado por pruebas de aceptación, que equivale a desarrollo guiado por comportamiento.

Los casos de prueba se crean antes de la implementación y en colaboración con los diferentes roles del equipo.

# Tema 2.2.2 Técnicas de Pruebas de Caja Negra

## Video de la clase

[Ver clase: Técnicas de Pruebas de caja negra - 15 min](https://bootcampqa.com/videos/tecnicasdepruebadecajanegra.mp4)

## Apuntes


