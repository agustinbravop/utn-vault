**Representational State Transfer** (REST) es un estilo de arquitectura de un [[Web Services|web service]] cuya API cumple con un conjunto de restricciones. Si bien REST surge en el ámbito académico, creado por Roy Fielding, actualmente se usa ampliamente en la industria. Se basa en URIs y el protocolo HTTP.

Criterios para que una API sea RESTful:

1. **Arquitectura cliente-servidor**: por ejemplo, usando HTTP.
2. **Sin estado**: cada petición está separada y aislada de otras peticiones anteriores o posteriores.
3. **Cacheable**.
4. **Sistema de capas**: existe una jerarquía y abstracción de middlewares.
5. **Interfaz uniforme**: que toda la información necesaria para manipular o usar el recurso se encuentre en el mensaje. Esto requiere que los recursos sean _identificables_ y _solicitables_, que se pueda manipular recursos mediante sus _representaciones_, y que haya _hypermedia_ disponible para usar hyperlinks.

Una API es RESTful solo si cumple con estos criterios o restricciones.

**URI**: identifica un recurso con un nombre en una jerarquía. Conviene usar sustantivos, no verbos. Ej: `/users/1234`, `/player/johndoe`.

## HTTP

HTTP es el protocolo de comunicación por excelencia para las API REST. Sus métodos se utilizan para manipular recursos. Listado de métodos (o verbos) HTTP disponibles:

1. `GET`.
2. `DELETE`.
3. `POST`.
4. `PUT`.
5. `HEAD`.
6. `OPTIONS`.
7. `PATCH`.
8. `CONNECT`.
9. `TRACE`.

Códigos de respuesta HTTP:

1. `1xx`: informativo.
2. `2xx`: respuesta exitosa.
3. `3xx`: redirección.
4. `4xx`: error en el cliente.
5. `5xx`: error en el servidor.

Ejemplo:

```
# La siguiente petición...
GET /ffilms/2 HTTP/1.1
Host: localhost
User-agent Mozilla/4.0
Connection: keep-alive
Authorization: Basic qhWadbQ...

# Provoca la siguiente respuesta
HTTP/1.1 200 OK
Date: Sun, 08 Feb 2000 01:11:12 GMT.
Content-Type: application/json

{...}
```

Una alternativa a REST es usar gRPC, que es más nuevo y performante, aunque menos utilizado. REST es un estándar masivo y compatible con la mayoría de internet.
