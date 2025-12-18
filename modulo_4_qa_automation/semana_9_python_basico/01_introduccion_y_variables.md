# Tema 4.1 - Introducción y Variables Python

## Video de la clase


[Ver clase: JIRA - 15 min](https://bootcampqa.com/videos/jira.mp4)

## Apuntes

### 1.Introducción

Python es un lenguaje de programación fácil de aprender y muy poderoso. Es ideal para principiantes, y también es usado en una gran variedad de proyectos profesionales.

### 1. Instalando Python en VS Code
Si aún no tienes Python instalado, asegúrate de instalarlo desde python.org y selecciona la opción "Agregar Python a la variable PATH" durante la instalación.

### 2. Usando la terminal integrada de VS Code
Para ejecutar Python desde la terminal de VS Code:

Abre VS Code y crea un nuevo archivo con la extensión .py.
Escribe tu código Python en el archivo.
Abre la terminal integrada en VS Code. Puedes hacerlo con el atajo de teclado Ctrl + ` o desde el menú superior seleccionando Terminal > Nueva Terminal.
En la terminal integrada, navega hasta el directorio donde se encuentra tu archivo usando el comando cd (si es necesario).
Para ejecutar tu archivo Python, escribe el siguiente comando en la terminal integrada: 
`python nombre_del_archivo.py`
Por ejemplo, si tu archivo se llama hola_mundo.py, ejecuta:
`python hola_mundo.py`

### 2.Variables
2. Variables
Las variables en Python no necesitan ser declaradas explícitamente. Puedes asignarles cualquier tipo de dato.
```
# Cadenas
nombre = "Juan"
# Números enteros (int)
edad = 25
# Booleanos
es_mayor = True
# Decimales (float)
PI = 3.14159
```
Para obtener datos de entrada del usuario, puedes usar la función input(). El valor devuelto por input() es siempre una cadena (string), por lo que si esperas un número, tendrás que convertirlo usando int() o float().

```
# Obtener un valor del usuario
nombre = input("¿Cómo te llamas? ")
print("Hola ", nombre)

# Convertir la entrada a un número
edad = int(input("¿Cuántos años tienes? "))
print("Tienes  edad, "años.")
```