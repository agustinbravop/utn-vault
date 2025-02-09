*Internet Protocol* (IP) es un [[Protocolo]] de la [[Capa de Red]] para el:

- **Enrutamiento**: conjunto de reglas y algoritmos usados por los [[Enrutadores]] para construir y mantener sus tablas de enrutamiento, para determinar la mejor ruta.
- **Enrutado**: definen cómo se debe empaquetar y direccionar los datos para ser enviados a través de la red. Especifican estructuras de datos y cómo manejarlas.

IP es el protocolo de enrutado más utilizado. Implementa un **[[Redes de Datos|servicio]] de entrega sin conexión no confiable**. Debido al **encapsulamiento**, el *datagrama IP* cuenta con un *encabezado* de mínimo 20 bytes:

![[Datagrama IP.png]]

El campo TOS se consideraba muerto hace décadas, pero actualmente es vital para cuestiones de [[Calidad de Servicio]]. Este encabezado permite la [[Fragmentación en IP]] y el uso de [[Opciones en IP]].

Las redes IP utilizan como identificadores de redes y hosts las *direcciones IP*, que son **únicas** en toda la red. La dirección IP refiere a la interfaz del host con la red.

## Direcciones IP

Las direcciones IP se implementan como un número de 32 bits. Por convención, se suelen separan los 32 bits en cuatro octetos de 8 bits representados en decimal (de 0 a 255). Ejemplo:

![[Dirección IP.png]]

El significado de una dirección IP es una convención de diseño. El mecanismo que separa entre el `netID` y el `hostID` es la *máscara de subred*: otro número de 32 bits que permite extraer las distintas porciones al hacer un AND bit a bit. Por lo general, una dirección con `hostID = 0` refiere a la dirección de la red.

La IANA (*Internet Assigned Numbers Authority*) era un registro central de IPs. Se sustituye en 1998 por la ICANN (*Internet Corporation for Assigned Names and Numbers*), la cual asigna espacios de direcciones IP y otros identificadores.

También existen registros regionales de internet, que revisan el cumplimiento de normas.

Convenciones especiales para las direcciones IP que todo el mundo utiliza y respeta:

1. `0.0.0.0`: refiere a este host. Solo está permitido durante el arranque del sistema.
2. `0.0.<host>.<host>`: host de esta red. Solo permitido durante el arranque del sistema.
3. `255.255.255.255`: broadcast local. Nunca es una dirección válida de origen.
4. `<red>.<red>.255.255`: broadcast dirigido. Nunca es una dirección válida de origen.
5. `127.<any>.<any>.<any>`: loopback. Nunca debe aparecer en una red.

### Clases de Direcciones IP

Se clasificaron las direcciones IP para facilitar el trabajo de los administradores. Clases:

6. **A**: reservadas para los gobiernos y grandes empresas del mundo.
7. **B**: para empresas medianas.
8. **C**: para todos los demás solicitantes.
9. **D**: para redes de multidifusión.
10. **E**: de uso experimental.

Las direcciones otorgadas por ICANN son públicas y otorgadas a gobiernos y empresas. Hay **direcciones privadas** que se pueden usar arbitrariamente y sin necesidad de solicitud alguna.

### Agotamiento de Direcciones

En la realidad, las redes crecieron exponencialmente y muy rápido estas clases se quedaron sin direcciones disponibles para asignar. Esto se conoce como el **agotamiento de direcciones**. 

Actualmente, la cantidad de direcciones IP que pueden existir con 32 bits es también un recurso agotado.

La idea original de las direcciones IP era que cada parte de red identificara una red física. Este enfoque requiere que a cada red interna se le asigne al menos una dirección de clase C, pero no suele necesitar 255 hosts. Por esto, se genera un gran **desperdicio** de direcciones, culpa de una asignación ineficiente. Esto se puede solucionar con [[Subnetting]].

El problema del agotamiento de direcciones da origen a [[IPv6]].
