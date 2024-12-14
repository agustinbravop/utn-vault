En un [[Sistema Operativo]], la ejecución de un [[Proceso]] o trabajo se compone de secuencias de procesador y secuencias de espera. La planificación busca **maximizar el uso de la CPU**.

El **repartidor** o _dispatcher_ conmuta el procesador de un trabajo a otro. Hace los **cambios de contexto** (intercambia estados de la CPU y transfiere el control al trabajo siguiente).

El **planificador** o _scheduler_ determina el siguiente proceso al que asignar el CPU. Hay 3 tipos de planificador según su plazo:

1. **Largo**: es el que admite procesos.
2. **Medio**: es el que suspende y activa procesos. Relacionado a la [[Memoria Virtual]].
3. **Corto**: es el que agrega y quita (por timeout) procesos a la CPU.

Tiempos relevantes para la planificación de procesos:

1. **Retorno promedio**: $\text{TRP}$. Promedio que los procesos pasan en Listo y Ejecución.
2. **Espera promedio**: $\text{TEP}$. Promedio que los procesos pasan en Listo.
3. **Irrupción**: $\text{TI}$. Tiempo que el proceso usa la CPU antes de cambiar de estado.
4. **Arribo**: $\text{TA}$. Tiempo que el proceso demora en llegar a Listo.

## Algoritmos de Planificación

Para el procesamiento por lotes:

1. **FIFO**: Fist In, First Out. Se atiende en orden de llegada. Es simple, pero un proceso puede monopolizar la CPU.
2. **SJF**: Shortest Job First. Reduce el $\text{TEP}$ pero produce inanición en procesos largos.
3. **SRTF**: Shortest Remaining Time First. Es similar a SJF pero permite desalojar procesos (es **apropiativo**). Prioriza los procesos que están más cerca de terminar.

Para **sistemas interactivos**, donde el tiempo de espera es importante:

1. **Round Robin**: a todos los procesos se les asigna el mismo tiempo **_quantum_** $q$ para usar la CPU. Cuando el tiempo $q$ se acaba sin que el proceso haya terminado, el proceso vuelve al final de la cola. Si $q$ es pequeño hay demasiados cambios de contexto. Si $q$ es grande entonces aumentan los tiempos de respuesta. Por ende, el valor de $q$ requiere _fine-tuning_.
2. **Por Prioridades**: se asigna al CPU el trabajo con mayor **prioridad**. Hay prioridades internas o externas, estáticas o dinámicas. En general, produce inanición en procesos de baja prioridad. Esto se puede solucionar con **envejecimiento**, aumentando la prioridad de los procesos que llevan esperando mucho tiempo.
3. **Colas Multinivel**: diferencia tipos de trabajos, y cada tipo tiene una cola distinta. Cada cola tiene su propio algoritmo de planificación. Otro algoritmo prioriza a qué cola asignar el CPU.
4. **Colas Multinivel Adaptativas**: los trabajos cambian de prioridad y de cola.
