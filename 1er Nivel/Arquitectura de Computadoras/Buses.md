Un **bus** significa transporte y consiste en un arreglo de líneas lógicas dedicadas a interconectar órganos de la [[Computadora]] entre sí.

![[Buses.png]]

Cada línea del bus une un [[Biestables|flip-flop]] fuente con su flip-flop destino del mismo peso (es decir la misma posición en los [[Registros]] de cada extremo del bus). Cada órgano tiene un **registro dedicado** a recibir y enviar información del bus (uno por cada bus al cual el órgano se conecta).

![[Registros Situados entre Dos Buses.png]]

La señal de nivel $SR_1$ (salida de $R_1$) se mantiene durante un ciclo de reloj completo para estabilizar el bus (cargar el voltaje de los hilos del bus) y cargar el contenido del registro 1. En el tick de reloj (_clock_) $\theta$ siguiente se manda la señal impulsional $ER_2$ (entrada a $R_2$) para leer el bus mientras $SR_1$ sigue activa.
