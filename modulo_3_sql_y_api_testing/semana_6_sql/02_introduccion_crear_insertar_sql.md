# Introducción a SQL, crear tablas e insertar datos

# Video de la clase


[Ver clase: Herramientas de Gestión de Pruebas - 10 min](https://bootcampqa.com/videos/herramientasdegestiondepruebas.mp4)

# Apuntes

## ¿Qué es SQL?

**SQL (Structured Query Language)** es un lenguaje estándar para trabajar con bases de datos.

Permite:

- Consultar datos  
- Insertar información  
- Modificar registros existentes  
- Eliminar datos  

### ¿Por qué es útil para QA?

- Verificar que los datos se guardan correctamente.
- Preparar datos antes de ejecutar pruebas.
- Consultar si los datos se han insertado bien (registro, login, compras, etc.).

---

## Crear una tabla (CREATE TABLE)

La instrucción **CREATE TABLE** permite definir la estructura de una nueva tabla indicando:

- Columnas
- Tipos de datos
- Restricciones o reglas

```
CREATE TABLE usuarios (
  id SERIAL PRIMARY KEY,
  nombre VARCHAR(100) NOT NULL,
  ciudad VARCHAR(100),
  edad INTEGER CHECK (edad >= 0),
  activo BOOLEAN NOT NULL DEFAULT TRUE,
  created_at TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP
);
```


### Tipos de datos comunes

- **VARCHAR(n)**: cadena de texto variable con un máximo de caracteres.
- **INTEGER**: número entero.
- **BOOLEAN**: valor lógico (`TRUE` o `FALSE`).
- **DATE**: fecha sin hora.
- **TIMESTAMP**: fecha y hora.
- **NUMERIC(p,s)**: número decimal con precisión.


---

### Restricciones / Reglas comunes

- **NOT NULL**: el valor es obligatorio.
- **PRIMARY KEY**: identificador único de la tabla.
- **UNIQUE**: no permite valores repetidos.
- **CHECK (condición)**: valida una condición específica.
- **DEFAULT valor**: asigna un valor por defecto.
- **DEFAULT CURRENT_TIMESTAMP**: guarda la fecha y hora en la que se inserta un registro.
- **SERIAL**: entero autoincremental.



---

## Insertar datos (INSERT)

La instrucción **INSERT** permite agregar nuevos registros a una tabla.  
Los campos con valores por defecto o automáticos no necesitan indicarse explícitamente.

```
INSERT INTO usuarios (nombre, ciudad, edad, activo)
VALUES
('Ana', 'Madrid', 30, TRUE),
('Luis', NULL, 25, TRUE),
('Elena', 'Sevilla', 42, FALSE);

```

