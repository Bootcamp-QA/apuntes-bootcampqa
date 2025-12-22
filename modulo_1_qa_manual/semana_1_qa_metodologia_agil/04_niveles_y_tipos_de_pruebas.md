# Niveles y Tipos de Pruebas Basado en el estándar ISTQB

# Video de la clase


[Ver clase: Niveles y tipos de pruebas - 60 min](https://bootcampqa.com/videos/nivelesytiposdepruebas.mp4)

# Apuntes

## ¿A qué nivel se pueden hacer pruebas y qué tipos de pruebas existen?

Los niveles y tipos de pruebas permiten organizar las actividades de testing según la etapa del desarrollo y el objetivo de la prueba, asegurando una cobertura adecuada del sistema.

## Niveles de pruebas

Son grupos de actividades de pruebas realizadas en relación con el producto en una etapa determinada del desarrollo.

### 🔧 Pruebas de componente o unitarias

Prueban componentes de forma aislada.

Ejemplo: Palanca de cambios

Características:
- No requieren que el sistema completo esté terminado
- Son más rápidas de ejecutar
- Facilitan la identificación del fallo

Tipo asociado:
- Pruebas unitarias

### 🔩 Pruebas de integración de componentes

Combinan varios componentes para comprobar que funcionan correctamente juntos.

Ejemplo: Caja de cambios integrada con la palanca de cambios

Características:
- Requieren una versión del sistema que incluya los componentes a probar
- Son más lentas que las unitarias

Tipo asociado:
- Pruebas de integración  
- API testing

### 🚗 Pruebas de sistema

Evalúan el sistema completo como un todo.

Ejemplo: Coche completo

Características:
- Mayor coste
- Más lentas
- Más difícil identificar la causa exacta del fallo

Tipo asociado:
- Pruebas funcionales

### 🌐 Pruebas de integración de sistemas

Prueban el sistema integrado con otros sistemas externos.

Ejemplo: Conexión del coche con un sistema GPS externo

Características:
- Verifican la comunicación entre sistemas
- Suelen depender de servicios externos

### 👥 Pruebas de aceptación

El sistema es probado por los usuarios finales en condiciones reales de uso.

Ejemplo: Coche utilizado en ciudad y campo por diferentes usuarios

Características:
- Mayor coste
- Validan que el sistema cumple las expectativas del usuario

Tipo asociado:
- Pruebas de aceptación

## Tipos de pruebas

### Pruebas funcionales y no funcionales

#### ✅ Pruebas funcionales

Verifican la funcionalidad del sistema, es decir, qué hace o cómo debe comportarse.

Ejemplo:
- El coche debe poder encender las luces

#### ⚙️ Pruebas no funcionales

Evalúan cómo se comporta el sistema en aspectos no funcionales.

Ejemplo:
- Facilidad para encontrar el botón de las luces
- Rapidez de respuesta
- Seguridad para el conductor
- Facilidad de mantenimiento

## Tipos de pruebas no funcionales

### 🚀 Rendimiento o performance

Determinan:
- Velocidad
- Estabilidad
- Tiempo de respuesta
- Uso de recursos bajo una carga determinada

### 🔄 Portabilidad

Evalúa la facilidad con la que el sistema puede moverse de un entorno a otro.

### 🧠 Usabilidad

Mide la facilidad con la que un usuario aprende y utiliza el sistema.

### 🔐 Seguridad

Identifica vulnerabilidades y previene ataques internos o externos.

### 🛠️ Mantenibilidad

Evalúa la facilidad de mantenimiento del sistema y el cumplimiento de buenas prácticas de desarrollo.

## Tipos de pruebas funcionales

### 🔧 Unitarias

Prueban de forma individual las funciones del sistema.

### 🔁 Regresión

Comprueban que, tras un cambio, otras partes del sistema no se han visto afectadas y siguen funcionando correctamente.

### 🔗 Integración

Verifican que los distintos módulos y servicios del sistema funcionan correctamente en conjunto.

### 🔍 Exploratorias

Buscan descubrir errores poco evidentes o casos límite (corner cases).

### ✔️ Confirmación

Comprueban que un defecto reportado ha sido corregido con éxito.

## Tipos de pruebas según el acceso al sistema

### 📦 Pruebas de caja negra

Se basan en lo que el sistema debe hacer, sin conocer su implementación interna.

Objetivo:
- Verificar el comportamiento del sistema según sus especificaciones

### 🧩 Pruebas de caja blanca

Se basan en la estructura interna del sistema.

Objetivo:
- Cubrir la estructura del código hasta un nivel aceptable

## Tipos de pruebas según la ejecución del código

### 📄 Pruebas estáticas

No requieren ejecutar el código para evaluar la calidad.

Ejemplos:
- Revisión de requisitos
- Revisión de código (code review)
- Análisis de código estático (SonarQube)

### ▶️ Pruebas dinámicas

Requieren ejecutar el código del sistema para poder probarlo.
