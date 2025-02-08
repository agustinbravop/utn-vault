Un ***bridge*** o puente de red es un dispositivo de interconexión de redes para interconectar varias LAN individuales, algo muy útil para la [[Conmutación en Redes LAN]].

El *dominio de colisión* es el segmento de la red donde las tramas pueden colisionar.

Un **no-frills bridge** es un bridge transparente que se conecta a dos o más LANs. Escucha *promiscuamente* cada trama transmitida y la almacena hasta que la LAN del otro lado esté ociosa. Evita colisiones entre las LANs, osea que un puente es la **frontera** de los dominios de colisión.

![[Puentes de Red.png]]

Un **learning bridge** escucha de forma promiscua y almacena la dirección de origen de la trama en una caché de estación junto con el puerto que recibió la trama.

Para cada trama recibida, el learning bridge busca en la *caché de estación* la dirección de destino para enviar la trama solo por el puerto asociado a esa dirección. Si no la encuentra, entonces difunde la trama por todas las interfaces. Cada entrada de la caché se borra luego de un tiempo de envejecimiento.

El concepto de learning bridge funciona con cualquier número de puertos.

![[Puentes de Red (3 Puertos).png]]

Un puente sirve para:

- **Filtrar** las tramas, evitando colisiones entre LANs.
- **Conmutar** las tramas, para comunicación entre LANs.

Mientras que un simple repetidor reexpide cada bit a medida que lo recibe, un bridge recibe la trama entera antes de almacenarla y retransmitirla. Por ende, es un dispositivo que opera a nivel de [[Capa de Enlace]].

## Bucles entre Puentes

Los **bucles entre puentes** son un problema que sucede cuando hay más de un camino entre dos redes. Un bucle entre 2 redes LAN produce un bucle de retransmisión infinito, creando un *broadcast storm* que satura la red.

![[Bucles entre Puentes de Red.png]]

*Spanning Tree* es un [[Protocolo]] de difusión que busca **prevenir bucles** en la red.

Los puentes intercambian información sobre sus conexiones regularmente siguiendo un Bridge Protocol. Los mensajes se llaman BPDUs y se envían a una dirección multicast reservada.

Cada *puerto* de cada puente tiene un identificador y un costo (inverso a su velocidad). Cada puente calcula el grafo de la red y desactiva interfaces hasta cortar todos los bucles y construir un **árbol de expansión**.

Los puentes eligen como raíz del árbol a aquel que tiene el ID más bajo.

El puerto de un puente debe aprender toda la red de puentes y calcular el grafo antes de comenzar a reenviar tramas. Este proceso es lento, y un cambio en la topología significa recalcular el árbol.

![[Estados de un Puerto Spanning Tree.png]]

El tiempo de reacción ante fallos es lento, y no es fácil reducir el tiempo de convergencia, por lo que este protocolo no es adecuado en redes de alta disponibilidad.
