# Tema 1.3 - BDD (Behaviour-Driven Development)

## Video de la clase


[Ver clase: BDD - 15 min](https://bootcampqa.com/videos/bdd.mp4)

## Apuntes

### ¿Qué es BDD?

BDD (Behaviour-Driven Development) es un proceso de software ágil que busca la colaboración y entendimiento entre desarrolladores, QAs y Product Owners. Surge del TDD (Test-Driven Development), pero a diferencia de este, BDD define las pruebas centradas en el **usuario y el comportamiento del sistema**, no solo en las funcionalidades.

El objetivo principal es que el equipo describa los detalles de cómo se debe comportar la aplicación de manera que sea comprensible para todos.

### Fases del BDD

1. **Discovery**

   * Se elige una User Story.
   * Se discuten ejemplos concretos para acordar cómo se espera que se comporte la aplicación en cada caso.
2. **Formulation**

   * Se documentan esos ejemplos de forma que sirvan como guía para la automatización.
   * Se busca confirmación por parte de todo el equipo.
3. **Automation**

   * Se implementa el comportamiento descrito en los ejemplos.
   * Se crean primero los tests que guiarán la implementación.

### Beneficios del BDD

* **Mejora la colaboración:** Todos usan un lenguaje común, lo que facilita la comunicación y el trabajo en equipo.
* **Se prioriza el valor del negocio:** Permite a los desarrolladores entender los objetivos del negocio y alinearse con las necesidades del cliente.
* **Reducción de riesgos:** Al detallar todos los requerimientos y escenarios posibles, se minimizan errores y malentendidos durante el desarrollo.

### Mitos sobre BDD

* Todas las fases son igual de importantes: la comunicación y discovery son esenciales antes de documentation y automation.
* Puedes automatizar un escenario después de implementarlo, pero ya no sería BDD puro.
* Usar Gherkin no significa que estés aplicando BDD; es solo un formato para escribir pruebas.

### Características de BDD

* **Ejemplos concretos:** Describe la funcionalidad con ejemplos reales, no abstractos. Ejemplo: "el usuario Juan hace login" en lugar de "el usuario hace login".
* **No técnico:** Se enfoca en comportamientos del sistema, sin especificaciones técnicas.
* **Cada ejemplo corresponde a un comportamiento:** Cada comportamiento diferente se define como un ejemplo concreto.

### Resumen

BDD permite desarrollar, probar y pensar el código desde la perspectiva del usuario. La clave es implementar "ejemplos del mundo real" en lugar de solo "funcionalidades", promoviendo la colaboración del equipo y empatía con el usuario final.
