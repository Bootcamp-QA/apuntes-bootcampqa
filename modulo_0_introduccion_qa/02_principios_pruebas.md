# Tema 2 - Los 7 Principios de las Pruebas

## Video de la clase 
[Ver clase: Los 7 Principios de las Pruebas - 15 minutos](https://bootcampqa.com/videos/7principiosdepruebas.mp4)


## Apuntes
## ¿Qué son los 7 principios de las pruebas?

Son **7 principios básicos** a los que todo proceso de testing debería ajustarse.  
Están **definidos por ISTQB**.

### Objetivos
- Servir de guía para **homogeneizar el testing** a nivel global.
- Garantizar que se siguen **estándares de calidad de software**.


## Principio 1 · Las pruebas muestran la presencia de defectos, no su ausencia

- Las pruebas permiten decir **qué defectos se han encontrado**.
- Nunca se puede asegurar que el sistema **no tiene defectos**.
- Puede haber defectos que no se hayan encontrado.
- Las pruebas **reducen la probabilidad** de que existan defectos, pero no la eliminan.

## Principio 2 · Las pruebas exhaustivas no son posibles

- Probar todo **no es posible**, salvo en sistemas muy triviales.

### Pruebas exhaustivas significan:
- Probar **todas las entradas posibles**  
  Ejemplo: todas las edades posibles en un campo “edad”.
- Probar en **todos los dispositivos posibles**  
  Ejemplo: todos los móviles y sistemas operativos del mercado.

Como no es posible probar todo, es necesario **seleccionar qué casos de prueba ejecutar** (planificación).


## Principio 3 · Las pruebas tempranas ahorran tiempo y dinero

- El testing debe comenzar **desde el inicio del proceso**, no cuando el software ya está terminado.
- Encontrar defectos de forma temprana evita que se generen defectos posteriores.
- Esto **reduce el coste** de corrección.


## Principio 4 · Agrupación de defectos

- La mayoría de los defectos suelen encontrarse **agrupados en las mismas áreas**.

### Principio de Pareto
- El **80% de los defectos** se encuentra en el **20% de los módulos**.

### Motivos
- Áreas con mayor complejidad.
- Partes del sistema con implementaciones más difíciles.

Este principio es muy útil en la **planificación de pruebas**.


## Principio 5 · Desgaste de las pruebas (Paradoja del pesticida)

- Si siempre se ejecutan las mismas pruebas, su efectividad disminuye.
- El software se vuelve “resistente” a esas pruebas.

### Es necesario:
- Revisar periódicamente los casos de prueba.
- Agregar nuevos casos de prueba.
- Cambiar datos de prueba.


## Principio 6 · Las pruebas dependen del contexto

- No todos los sistemas se prueban de la misma manera.
- El enfoque de testing depende de:
  - Tipo de plataforma: móvil, web o escritorio.
  - Tipo de software: finanzas, compras, educación, sanidad, etc.

No existe una estrategia de testing universal, todo depende del **contexto**.


## Principio 7 · Falacia de la ausencia de defectos

- No se puede asegurar al 100% que un software no contiene defectos.
- Solo se puede afirmar que **no se han encontrado defectos**.
