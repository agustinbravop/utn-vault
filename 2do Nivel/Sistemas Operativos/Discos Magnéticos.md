En este dispositivo de [[Entrada-Salida]], el cabezal se mueve para leer posiciones de los discos.

![[Disco Magnético.png]]

![[Cabezales de un Disco Magnético.png]]

## Algoritmos de Planificación

Dada una cola de solicitudes, hay un algoritmo que determina cómo el disco debe mover el cabezal para completar la cola.

1. **FCFS**: se resuelve en el orden en el que llegan. Presenta un movimiento del cabezal ineficiente.
2. **SSTF**: Shortest Seek Time First.
3. **SCAN**: atiende peticiones mientras se mueve de extremo a extremo constantemente.
4. **C-SCAN**: cuando alcanza un extremo, vuelve al inicio sin atender peticiones y comienza nuevamente, para asegurar un tiempo de espera uniforme.
5. **LOOK**: solo se mueve el brazo hasta el último cilindro (no los extremos) y mira si hay solicitudes pendientes antes de seguir.
6. **C-LOOK**: asegura un tiempo de espera uniforme.

Estos algoritmos consideran factores como velocidad (dada por la cantidad de movimientos del cabezal), inanición, carga del sistema, cache, [[Fragmentación]]. En simulaciones de cargas reales, los mejores resultados los tienen SSTF y LOOK.
