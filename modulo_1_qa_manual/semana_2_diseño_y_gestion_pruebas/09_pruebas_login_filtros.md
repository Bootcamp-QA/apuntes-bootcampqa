#Diseño de pruebas para Login y Filtros

[Ver clase: Diseño de pruebas en gherkin para login, registros y filtros - 20 min](https://bootcampqa.com/videos/manual-pruebas-login-filtros.mp4)

## Validación de registros de usuarios

Si la página web tiene un sistema de registro de usuarios y login debes validar lo siguiente:

Usando la técnica de transición de estados, debemos cubrir todos los estados posibles

USUARIO NO REGISTRADO -- Registro --> USUARIO REGISTRADO -- Bloqueo --> USUARIO BLOQUEADO

Teniendo en cuenta la tabla de decision, tendriamos 2 pruebas positivas, que serian las transiciones válidas (Registro y Bloqueo)
1. USUARIO NO REGISTRADO -- Registro --> USUARIO REGISTRADO
2. USUARIO REGISTRADO -- Bloqueo --> USUARIO BLOQUEADO
Tendriamos por otro lado 3 pruebas negativas, que serian las trancisiones no válidas
1. USUARIO REGISTRADO no puede Registrarse de nuevo.
2. USUARIO BLOQUEADO no puede registrarse de nuevo.
3. USUARIO NO REGISTRADO no puede bloquearse

A su vez, habría que añadir las mismas pruebas negativas que en formularios, es decir, enviar con campos obligatorios vacios, y validar el formato de los campos.

Ejemplo:
Scenario: Registrar un usuario no registrado
Given el usuario "pepe@gmail.com" no esta registrado en la web
When completa el formulario de registro con campos obligatorios validos "pepe@gmail.com", "contraseñatest"
Then el usuario se registra correctamente
And puede acceder a la página

## Validación de login de usuarios
En el caso de login se debe también tener en cuenta como precondición que el usuario para hacer login debe estar registrado en la plataforma y no debe estar bloqueado.
En este caso se puede usar la técnica de tabla de decisiones:
                      
|                      | PRUEBA 1 | PRUEBA 2 | PRUEBA 3 | PRUEBA 4 |
|----------------------|---------|---------|---------|---------|
| Usuario Registrado   | V | V | F | F |
| Usuario No registrado| F | F | V | F |
| Usuario Bloqueado    | F | F | F | V |
| Contraseña correcta  | V | F | - | V |
| Contraseña incorrecta| F | V | - | F |
| RESULTADO            | LOGIN VALIDO | ERROR | ERROR | ERROR |

En resumen tendriamos 4 posibles pruebas:
Login con usuario registrado y contraseña valida
Login con usuario registrado y contraseña invalida
Login con usuario no registrado
Login con usuario bloqueado y contraseña valida

Se debe agregar también la prueba con campos vacios
Login con usuario vacio
Login con usuario regisrado y contraseña vacia

Y si el sistema bloquea despues de un numero de intentos al usuario se debe probar ese caso también
Login con contraseña invalida 3 veces (Bloqueo)

Estas son las pruebas posibles, son siempre las mismas en todos los sistemas de login, en el caso que el sistema no bloquee usuarios se quitarian las de bloqueo de usuario quedando más simplificado.


## Validación de filtros
Un sistema puede tener muchos filtros y combinaciones de esos filtros, el numero de casos de pruebas positivos de todas las combinaciones siguiendo la técnica de prueba de tabla de decisiones es 2 elevado al número de filtros.
Es decir, si tienes 2 filtros, necesitarás 4 pruebas, pero si tienes 6 filtros necesitaras 32 pruebas para probar todas las combinaciones posibles.

En el caso de que haya pocos filtros (2 o 3 filtros) se pueden probar todas las combinaciones.
Cuando hay mas, en vez de todas las combinaciones, se prueba cada filtro por separado y luego todos combinados a la vez, esto da una cobertura aceptable. 
En el caso de que haya muchos filtros (8 o más) se pueden elegir sólo los más relevantes para probar de forma individual, es decir los que el usuario suele usar más a menudo.
Es decir tendriamos:
Casos positivos:
Una prueba por cada filtro con valor invalido
Una prueba con todos los filtros aplicados con resultados
Caso negativo:
Una prueba por cada filtro con valor invalido
Una prueba con todos los filtros aplicados sin resultados.

Ejemplo:
Scenario: Filtrar por precio invalido
Given el usuario esta en la pagina de producto
When introduce un precio invalido "-1"
Then debe ver un mesaje de error
And el filtro no debe aplicarse

Scenario: Filtrar por todos los filtros validos

Given el usuario esta en la pagina de producto

When filtra por todos los campos valido:

| precio | 10 |

| nombre | camiseta |

| color | verde |

| talla | M |

Then debe ver sólo productos que coincidan con los filtros
