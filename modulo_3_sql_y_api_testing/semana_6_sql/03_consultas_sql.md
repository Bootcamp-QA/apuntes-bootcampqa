# Consultas SQL

# Video de la clase


[Ver clase: Consultar Datos - Select SQL - 20 min](https://bootcampqa.com/videosapi/sql-filtrar-datos.mp4)

# Apuntes

La instrucción **SELECT** permite leer y consultar datos almacenados en una tabla.

### Consultar todos los registros

Devuelve todas las filas y columnas de la tabla.

```
SELECT * FROM usuarios;

```

---

## WHERE — Filtrar resultados por condiciones

La cláusula **WHERE** permite mostrar solo las filas que cumplen una condición.

Se puede filtrar por:

- Texto
- Números
- Valores booleanos

### Operadores comunes

- **=** igual
- **!= / <>** distinto
- **> , < , >= , <=** comparaciones
- **LIKE** coincidencia parcial
- **IN** valores dentro de una lista
- **BETWEEN** rango de valores
- **IS NULL / IS NOT NULL** valores nulos


```
SELECT * FROM usuarios WHERE ciudad = 'Madrid';
SELECT * FROM usuarios WHERE edad = 30;
SELECT * FROM usuarios WHERE activo = TRUE;
```


---

## Condiciones múltiples (AND / OR)

Permiten combinar varias condiciones dentro de una misma consulta:

- **AND**: todas las condiciones deben cumplirse.
- **OR**: basta con que se cumpla una de ellas.

```
SELECT * FROM usuarios
WHERE ciudad = 'Madrid' AND activo = TRUE;

SELECT * FROM usuarios
WHERE ciudad = 'Valencia' OR ciudad = 'Granada';
```

---

## Ordenar resultados (ORDER BY)

La cláusula **ORDER BY** permite ordenar los resultados:

- Ascendente (**ASC**)
- Descendente (**DESC**)

```
SELECT * FROM usuarios ORDER BY edad DESC;
SELECT * FROM usuarios ORDER BY nombre ASC;
```


