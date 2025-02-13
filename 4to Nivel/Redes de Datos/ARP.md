_Address Resolution Protocol_ (ARP) es un [[Protocolo]] que responde la siguiente pregunta: ¿Cómo averiguar la dirección [[Subcapa de Control de Acceso al Medio|MAC]] de un destino [[IP]]?

La [[Capa de Red]] conoce la dirección lógica IP, y la [[Capa de Enlace]] conoce la dirección física MAC. ARP asocia una dirección lógica conocida a una dirección física desconocida.

![[ARP.png]]

La capa de enlace envía un broadcast, consultando a quién de sus direcciones MAC le corresponde cierta dirección IP, y la estación correspondiente responde con su dirección IP.

## RARP

Reverse ARP responde la pregunta inversa: ¿Y si la estación no conoce su propia dirección IP?

Esto requiere un servidor que asigne direcciones IP.
