El **software de redes** para la [[Comunicación de Datos]] está muy estructurado y tiene una **jerarquía de protocolos** clara.

![[Software de Redes.png]]

Cada **capa** de la red se construye a partir de la capa inferior. Los _pares_ (capas del mismo nivel) se comunican mediante _protocolos_, que son un idioma común entre ellos. Estos protocolos tienen una sintaxis, semántica, y temporización. Cada uno determina una PDU (Protocol Data Unit).

Un **servicio** que una capa ofrece puede estar:

- **Orientado a la conexión**: garantiza la secuencia de llegada de los mensajes. Ej: TCP.
- **NO orientado a la conexión**: cada mensaje "llega cuando llega". Ej: UDP.

Las _primitivas_ de servicios son operaciones básicas que ordenan que el servicio ejecute una acción o informe el estado de algún par. Ejemplos para un socket: `LISTEN`, `CONNECT`, `RECIEVE`, `SEND`, `DISCONNECT`.

El servicio define las operaciones que la capa puede realizar, y el protocolo indica cómo implementar un servicio, definiendo un _formato_.

## Modelo OSI

El modelo de referencia OSI (Open Systems Interconnection), propuesto por la ISO (International Standards Organization), es una propuesta académica de cómo organizar las responsabilidades de cada capa.

![[Modelo OSI.png]]

El modelo solo dice lo que cada capa debería hacer, no cómo hacerlo. No es una arquitectura de red porque no especifica servicios y protocolos exactos. Sirve como un buen caso de estudio.

## TCP/IP

TCP/IP es el modelo de referencia de Arpanet e Internet. Ofrece protocolos específicos para utilizar, pero mezcla entre sus capas algunas de las responsabilidades que el modelo OSI organiza de manera más clara.

![[Modelo TCP-IP.png]]
