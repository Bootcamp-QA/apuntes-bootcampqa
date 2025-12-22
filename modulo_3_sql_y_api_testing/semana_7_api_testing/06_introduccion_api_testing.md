# Introducción a Api testing

# Video de la clase


[Ver clase: Herramientas de Gestión de Pruebas - 10 min](https://bootcampqa.com/videos/herramientasdegestiondepruebas.mp4)

# Apuntes

# Qué es una API

## Qué es una API y para qué sirve

Una **API** permite que diferentes sistemas se comuniquen entre sí de forma estandarizada.  
Gracias a las APIs, una aplicación puede solicitar información o ejecutar acciones en otra sin necesidad de conocer cómo está implementada internamente.

---

## Qué es una API

**API** son las siglas de **Application Programming Interface**, que significa *Interfaz de Programación de Aplicaciones*.

Una API es un conjunto de funciones, reglas y procedimientos que permiten la comunicación e integración entre distintos sistemas o aplicaciones.

---

## Ventajas de usar APIs

- Permiten reutilizar funcionalidades ya existentes.
- Reducen la complejidad, ya que no es necesario conocer la implementación interna.
- Son independientes del lenguaje de programación.
- Permiten separar la lógica de negocio (backend) del diseño (frontend).
- Facilitan que un mismo backend sea utilizado por distintos frontends (web, móvil, desktop).

---

## Qué es una API REST

Una **API REST** (Representational State Transfer) es un tipo de API que sigue la arquitectura REST, basada en un conjunto de reglas estándar para la creación de servicios web.

Las APIs REST son más simples, ligeras y flexibles que arquitecturas más antiguas como SOAP, por lo que son las más utilizadas actualmente.

---

## Arquitectura Cliente-Servidor

La arquitectura REST se basa en un modelo **cliente-servidor**:

- **Cliente (Frontend)**: realiza peticiones.
- **Servidor (Backend)**: procesa las peticiones y devuelve respuestas.

La comunicación se realiza mediante peticiones (*request*) y respuestas (*response*).

---

## Protocolo HTTP y HTTPS

Las APIs REST utilizan el protocolo **HTTP** o **HTTPS**.

- **HTTP (Hypertext Transfer Protocol)**: protocolo estándar para la transferencia de datos en la web.
- **HTTPS (HTTP Secure)**: versión segura de HTTP que cifra la información mediante SSL/TLS.

HTTPS es el protocolo recomendado para APIs por motivos de seguridad.

---

## Métodos de una API REST

Las APIs REST exponen recursos a través de URLs y utilizan métodos HTTP estándar para operar sobre ellos.

- **GET**: obtener información de un recurso.
- **POST**: crear un nuevo recurso.
- **PUT**: actualizar un recurso existente.
- **DELETE**: eliminar un recurso.

Existen otros métodos como **OPTIONS**, **HEAD**, **PATCH**, entre otros.

---

## Formatos de respuesta: JSON y XML

Una API REST recibe y devuelve información en formatos estructurados:

- **JSON (JavaScript Object Notation)**  
  Es ligero, sencillo y fácil de interpretar.
- **XML (eXtensible Markup Language)**  
  Es más extenso y flexible, adecuado para estructuras complejas.

Actualmente, **JSON** es el formato más utilizado en APIs REST.

---

## Códigos de respuesta HTTP

Cada petición a una API REST devuelve un **código de estado HTTP**, que indica el resultado de la operación.

### Clasificación de códigos

- **1xx**: respuestas informativas.
- **2xx**: éxito.
- **3xx**: redirecciones.
- **4xx**: errores del cliente.
- **5xx**: errores del servidor.

---

## Códigos de respuesta más comunes

- **200 OK**: solicitud exitosa.
- **201 Created**: recurso creado correctamente.
- **204 No Content**: solicitud exitosa sin contenido en la respuesta.
- **400 Bad Request**: solicitud incorrecta.
- **401 Unauthorized**: autenticación requerida o inválida.
- **403 Forbidden**: acceso no permitido.
- **404 Not Found**: recurso no encontrado.
- **500 Internal Server Error**: error interno del servidor.
- **503 Service Unavailable**: servicio no disponible temporalmente.
