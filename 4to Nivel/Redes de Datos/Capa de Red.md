La **capa de red** convierte un conjunto de enlaces locales en una red (entidad lógica que interconecta enlaces). Usa los servicios de la [[Capa de Enlace]] para ofrecer servicios a la [[Capa de Transporte]].

La capa de red se encarga de llevar los *paquetes* desde el origen hasta el destino, y su trabajo es **hallar el camino**. Para esto, debe conocer la *topología* de la subred de comunicación, lo que implica conocer el grupo de [[Enrutadores]] para elegir las rutas adecuadas. Esto presenta ciertos problemas a resolver.

Siguiendo el principio de interoperabilidad de las [[Redes de Datos]], los servicios deben ser independientes de la tecnología del enrutador.

![[Capa de Red.png]]

El *host* transmite al *router* más cercano un paquete para enviar mediante un enlace. El paquete se almacena hasta que haya llegado por completo para que la suma de verificación (*checksum*) pueda comprobarse. Luego, reenvía el paquete al siguiente router de la ruta hasta llegar al destino.

## Modelos de Servicio

Hay dos opciones:

- **Circuitos Virtuales**: servicio orientado a la conexión. Antes de poder enviar cualquier paquete de datos, se debe establecer una ruta del enrutador de origen al de destino: un *circuito*. Esto evita la necesidad de elegir una nueva ruta para cada paquete enviado. El problema es que si un router de la ruta se cae, se rompe el circuito.

![[Circuitos Virtuales.png]]

- **Datagramas**: servicio no orientado a la conexión. Los paquetes se colocan individualmente en la subred y se enrutan de manera independiente. Así, ante un cambio en la topología, el datagrama pueda lograr a destino usando un camino distinto al de los datagramas previos. La desventaja es que los paquetes pueden legar fuera de orden o duplicados.

![[Datagramas.png]]

|                            | Circuitos Virtuales        | Datagramas                              |
| -------------------------- | -------------------------- | --------------------------------------- |
| Configuración del circuito | Requerida                  | No necesaria                            |
| Direccionamiento           | El paquete indica n° de CV | El paquete indica dir. origen y destino |
| Enrutamiento               | Misma ruta para todos      | Cada paquete viaja por separado         |
| Efecto de fallas           | Terminan todos los CVs     | Solo se pierden paquetes en el router   |
| Calidad del servicio       | Fácil                      | Difícil                                 |
| Control de congestión      | Fácil                      | Difícil                                 |
