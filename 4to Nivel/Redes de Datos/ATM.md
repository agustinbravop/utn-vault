**Asynchronous Transfer Mode** (ATM) es un [[Protocolo]] que ofrece circuitos virtuales.

Permite transportar distintos tipos de tráfico. Tuvo gran adopción en telefónicas. Es un poco más veloz que [[Frame Relay]], ofreciendo velocidades desde OC-3 (155 Mbps) hasta OC-12 (622 Mbps).

Está basado en SONET/SDH como capa física, y permite la [[Multiplexación]] de varios circuitos virtuales sobre las conexiones físicas. Cada circuito virtual se identifica con un VCVI. Varios VCIs con destino común se pueden multiplexar en un único VPI.

Las _ATM Adaptation Layers_ (AAL):

![[ATM.png]]

1. AAL1: para audio y video.
2. AAL2: para videos comprimidos.
3. AAL3.
4. AAL4.
5. AAL5: existe específicamente para la transferencia de datos.

Categorías de servicio en ATM, de más a menos prioritario:

$$\text{CBR} \gt \text{VBR} \gt \text{ABR} \gt \text{UBR}$$
