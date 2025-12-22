# Tema 1.5 Técnicas de Pruebas  
Basado en el estándar ISTQB

## Video de la clase

[Ver clase: Técnicas de Pruebas - 10 min](https://bootcampqa.com/videos/tecnicasdepruebas.mp4)

[Ver clase: Técnicas de Pruebas de caja negra - 15 min](https://bootcampqa.com/videos/tecnicasdepruebadecajanegra.mp4)

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


# Técnicas de Pruebas de Caja Negra

## Introducción

Las pruebas de caja negra son una técnica de prueba de software que se centra en la **funcionalidad del sistema**, sin tener en cuenta su estructura interna o el código fuente.  
El objetivo es validar que el sistema cumple con los **requisitos especificados**.

El probador no necesita conocer cómo está implementado el sistema, solo qué entradas recibe y qué salidas debe producir.

---

## Características de las Pruebas de Caja Negra

- Se basan en los requisitos y especificaciones
- No consideran la lógica interna del sistema
- Se enfocan en entradas y salidas
- Pueden ser realizadas por testers, analistas o usuarios
- Detectan errores funcionales y de comportamiento

---

## Objetivos

- Verificar que el software hace lo que debe hacer
- Detectar errores de funcionalidad
- Validar reglas de negocio
- Comprobar el comportamiento ante entradas válidas e inválidas

---

## Tipos de Errores Detectados

- Funcionalidades incorrectas o ausentes
- Errores en interfaces
- Problemas de rendimiento
- Errores en el manejo de datos
- Fallos en la validación de entradas

---

## Técnicas de Pruebas de Caja Negra

### 1. Partición de Equivalencia

Consiste en dividir el conjunto de datos de entrada en **clases de equivalencia** que se espera que tengan un comportamiento similar.

#### Tipos de Clases
- Clases válidas
- Clases inválidas

#### Ventajas
- Reduce el número de casos de prueba
- Mejora la cobertura funcional

#### Ejemplo
Si un campo acepta valores entre 1 y 100:
- Clase válida: 1–100
- Clases inválidas: <1, >100

---

### 2. Análisis de Valores Límite

Se basa en probar los valores **en los límites** de las clases de equivalencia, ya que es donde suelen aparecer más errores.

#### Valores típicos
- Valor mínimo
- Valor máximo
- Justo por debajo del mínimo
- Justo por encima del máximo

#### Ejemplo
Rango válido: 1–100  
Valores a probar:
- 0, 1, 100, 101

---

### 3. Tablas de Decisión

Se utilizan cuando el comportamiento del sistema depende de **combinaciones de condiciones**.

#### Componentes
- Condiciones
- Acciones
- Reglas (combinaciones)

#### Ventajas
- Claridad en reglas complejas
- Cobertura completa de combinaciones

#### Ejemplo
Condiciones:
- Usuario válido
- Contraseña válida

Acciones:
- Permitir acceso
- Denegar acceso

---

### 4. Pruebas de Transición de Estados

Se emplean cuando el sistema cambia de comportamiento según su **estado actual**.

#### Elementos
- Estados
- Eventos
- Transiciones

#### Ejemplo
Estados de una cuenta:
- Activa
- Bloqueada
- Cancelada

---

### 5. Casos de Uso

Las pruebas se derivan de los **casos de uso**, verificando escenarios completos de interacción.

#### Tipos de escenarios
- Flujo principal
- Flujos alternativos
- Flujos de error

#### Ventajas
- Visión desde el punto de vista del usuario
- Pruebas realistas

---

### 6. Pruebas Exploratorias

El tester diseña y ejecuta pruebas de forma dinámica, basándose en su experiencia y conocimiento del sistema.

#### Características
- No siguen scripts estrictos
- Se adaptan durante la ejecución
- Útiles para detectar errores no previstos

---

### 7. Pruebas Basadas en Requisitos

Cada requisito debe tener al menos un caso de prueba asociado.

#### Objetivo
- Asegurar que todos los requisitos están cubiertos
- Facilitar la trazabilidad

---

## Ventajas de las Pruebas de Caja Negra

- No requieren conocimiento técnico profundo
- Simulan el uso real del sistema
- Ideales para validación funcional
- Útiles en fases tempranas y finales

---

## Desventajas

- No cubren el código interno
- Posible redundancia de pruebas
- Dependencia de la calidad de los requisitos

---

## Comparación con Caja Blanca

| Caja Negra | Caja Blanca |
|----------|-------------|
| No ve el código | Analiza el código |
| Enfoque funcional | Enfoque estructural |
| Basada en requisitos | Basada en implementación |

---

## Conclusión

Las técnicas de pruebas de caja negra son fundamentales para garantizar que el software cumple con los requisitos funcionales y las expectativas del usuario.  
Combinadas con otras técnicas, permiten lograr una mayor calidad del producto final.

¡
