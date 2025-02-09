Es importante que una nueva conexión [[TCP]] inyecte segmentos de forma gradual a la subred, para hacer un [[Control de Congestión]].

Para evitar la congestión de la red, TCP usa el mecanismo de arranque lento (*slow start*). En cada conexión se agrega una ventana de congestión (`cwnd`) que se inicializa en 1 y se aumenta con cada ACK recibido.

El extremo emisor puede enviar, como máximo, `min(W, cwnd)` paquetes antes de esperar un acuse. Por cada *round-trip*, se duplica el valor de `cwnd` hasta superar el límite `ssthresh`, y luego su valor solo se incrementa de 1 en 1.

TCP también interviene activamente en la prevención de la congestión durante la transmisión de datos.

Este manejo de la congestión por TCP impone una visión de [[Sistema de Caja Negra]] de la red. Se basa en la expiración de los temporizadores de TCP.

Dos eventos indican que puede existir congestión:

- **Timer RTO**: congestión grave.
- **ACKs duplicados**: congestión leve.

## Congestión Grave

Se usa el parámetro `ssthresh`. Se hace *slow start* hasta cruzar ese límite, a partir del cual se incrementa linealmente la ventana.

Si ocurre un RTO, también se deja de aplicar slow start.

## Congestión Leve

La llegada de varios acuses duplicados puede implicar una congestión.

Si TCP detecta tres ACKs duplicados seguidos, retransmite el segmento faltante (FAST RETRANSMIT). También se invoca la etapa de Congestion Avoidance del algoritmo de control de congestión (FAST RECOVERY).
