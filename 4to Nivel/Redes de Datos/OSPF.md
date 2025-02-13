_Open Shortest Path First_ (OSPF) es un [[Protocolo]] para el [[Ruteo IP]] que usa el [[Enrutadores#Ruteo Dinámico por Estado de Enlace|mecanismo de estado enlace]] (LS). Los mensajes OSPF se encapsulan en datagramas IP, campo protocolo n° 89.

Clasificación de routers:

1. Router interno.
2. Router backbone.
3. Area border router.
4. [[Autonomous Systems|AS]] border router.

Secuencia básica de operaciones realizadas por los [[Enrutadores]]:

5. Descubrir vecinos OSPF.
6. Elegir el router designado (opcional, depende de la topología).
7. Formar adyacencias.
8. Sincronizar bases de datos para el área al que pertenece.
9. Calcular la tabla de encaminamiento.
10. Anunciar los estados de los enlaces (esto es una inundación limitada por área).

Tipos de mensajes:

11. `HELLO`: descubre vecinos y construye adyacencias entre ellos.
12. `DBD`: controla la sincronización de la base de datos.
13. `LSR`: peticiona registros específicos de estado de enlace.
14. `LSU`: envía registros de estado de enlace solicitados.
15. `LSACK`: reconoce los demás tipos de paquetes.

Estados por los que pasa un router para formar adyacencias:

16. `DOWN`: desactivado.
17. `INIT`: envían paquetes `HELLO` para establecer relación.
18. `TWO-WAY`: bidireccionalidad entre router y router.
19. `EXSTART`: intercambian bases de datos con un `DBD`.
20. `EXCHANGE`: intercambian información de encaminamiento.
21. `LOADING`: se reciben `LSR`s y se devuelven `LSU`s.
22. `FULL`: los routers mantienen una lista de vecinos adyacentes.
