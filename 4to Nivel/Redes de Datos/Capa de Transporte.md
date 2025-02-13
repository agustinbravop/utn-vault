La **capa de transporte** busca la conectividad extremo-extremo entre procesos. Ocupa los servicios de la [[Capa de Red]].

Provee conectividad y sincronización de datos (entre aplicaciones finales). Permite la [[Multiplexación]] de varias aplicaciones sobre uno o varios enlaces.

Suele ser la última capa "obligatoria" a implementar en un stack de [[Protocolo|protocolos]] de [[Redes de Datos]]. En el modelo OSI le siguen las capas de sesión y de presentación, pero estas dos no existen en el modelo TCP/IP, por lo que la capa de transporte suele ofrecer sus servicios a la capa de aplicación.

![[Capa de Transporte.png]]

Debe proveer confiabilidad, abstracción, y aislación de problemas de la subred.

Es la última capa que realiza control de errores, y soluciona (de nuevo) algunos problemas ya vistos en la [[Capa de Enlace]].
