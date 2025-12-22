# Editar y eliminar datos SQL

# Video de la clase


[Ver clase: Editar o Eliminar datos SQL - 10 min](https://bootcampqa.com/videosapi/sql-editar-eliminar-datos.mp4)

# Apuntes

## Editar datos (UPDATE)

La instrucción **UPDATE** permite modificar uno o varios campos de registros existentes.  
Es fundamental usar **WHERE** para evitar modificar todos los registros de la tabla.

```
UPDATE usuarios
SET ciudad = 'Valencia', edad = 35
WHERE id = 2;

```

---

## Eliminar datos (DELETE)

La instrucción **DELETE** permite eliminar registros de una tabla.  
Al igual que con UPDATE, se debe usar **WHERE** para evitar borrar todos los datos.

```
DELETE FROM usuarios WHERE id = 4;
DELETE FROM usuarios WHERE activo = FALSE;
```
