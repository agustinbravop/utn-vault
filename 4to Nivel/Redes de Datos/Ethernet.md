El Ethernet es un [[Protocolo]] y tecnología LAN cableada que ha reemplazado a las tecnologías LAN cableadas de la competencia.

![[Ethernet.png]]

Ethernet implementa la capa física y la [[Capa de Enlace]] de forma monolítica:

$$\text{Ethernet} \begin{cases}\text{Capa de enlace} & \begin{cases}\text{Subcapa LLC} \\ \text{Subcapa MAC} \end{cases} \\ \text{Capa física} &\begin{cases}\text{Subcapa de convergencia de transmisión} \\ \text{Subcapa dependiente del medio físico} \end{cases}\end{cases}$$

![[Stack de Ethernet.png]]

**Señal de Jam**: ante una colisión, la estación enviará un _jam_ de 32 bits para reforzar la colisión. Las estaciones notificadas reprograman la transmisión usando un algoritmo de _retroceso exponencial binario truncado_ que indica un tiempo aleatorio a esperar.

**Inter Frame Gap**: los dispositivos Ethernet deben permitir un período de reposo (IFG) entre trama y trama, para la limpieza en la tarjeta de red. El tiempo mínimo es de 96 tiempos de bit (es el tiempo necesario para enviar 96 bits).

Encapsulamiento LAN DIX Ethernet v2 (hay otros más modernos, por ejemplo para VLAN):

![[Encapsulamiento Ethernet.png]]

El estándar se ha ido adaptando a los avances tecnológicos. Tecnologías Ethernet:

1. **Fast Ethernet**: 100 Basse-TX reduce la ventana de colisión. Velocidad hasta 100 Mbps.
2. **Gigabit Ethernet**: introduce _frame bursting_, _jumbo frames_, y auto-negociación.
3. **10 Gigabit Ethernet**: solo full-duplex.
4. Más: hay hasta 40 Gbps para _data centers_ y hasta 100 Gbps para _backbones_.
