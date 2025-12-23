# 3 Funciones

## Video de la clase


[Ver clase: Python Funciones - 5 min](https://bootcampqa.com/videosauto/pythonfunciones.mp4)

## Apuntes
Funciones
Las funciones en Python son bloques de código reutilizables que se ejecutan cuando son llamados. Se pueden definir funciones con o sin parámetros y también pueden devolver valores.

Definir una función básica:
```
def saludar():
    print("Hola, bienvenido!")

# Llamar a la función
saludar()  # Salida: Hola, bienvenido!

```

Funciones con parámetros y retorno:
Puedes definir funciones con varios parámetros y devolver un valor procesado.

```
def calcular_area(base, altura):
    area = base * altura / 2
    return area

# Llamar a la función con dos argumentos
area_triangulo = calcular_area(10, 5)

# Mostrar el área calculada
print(area_triangulo)  # Salida: 25.0
```