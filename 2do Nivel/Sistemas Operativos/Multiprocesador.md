En un **multiprocesador**, dos o más CPUs comparten todo el acceso a una RAM común. El SO debe solucionar las [[Comunicación entre Procesos#Condiciones de Competencia|condiciones de competencia]] (_race conditions_) que esto genera.

## Hardware de Multiprocesadores

### Uniform Memory Access

En este enfoque, cada palabra de memoria se puede leer a la misma velocidad.

Los multiprocesadores UMA con arquitecturas basadas en bus presentan un solo bus que comunica varias CPUs a varios módulos de memoria. Un problema común es que el bus se vuelve un cuello de botella.

![[Multiprocesadores UMA con Arquitecturas Basadas en Bus.png]]

Otra propuesta son los **interruptores de barras cruzadas**, la cual conecta $n$ CPUs a $k$ memorias. La desventaja es que la electrónica se vuelve compleja si $n$ o $k$ aumentan mucho, por lo cual es una propuesta poco escalable.

![[Multiprocesador UMA con Interruptores de Barras Cruzadas.png]]

Otra alternativa es usar **redes de conmutación multietapa**, donde cualquier CPU puede acceder a cualquier memoria si sus mensajes viajan por ciertos conmutadores.

![[Multiprocesador UMA con Redes de Conmutación Multietapa.png]]

### Non-Uniform Memory Access

Este enfoque NUMA permite tener más de 100 CPUs sin ser muy costoso.

![[Multiprocesador NUMA.png]]

### Chips Multinúcleo

Dado que los transistores se están haciendo cada vez más pequeños, se pueden colocar varias CPUs (núcleos) en el mismo chip o **pastilla**.

## Software de Multiprocesadores

Hay varios enfoques respecto a cómo tratar el [[Sistema Operativo]]:

1. **Cada CPU con su propio SO**: se divide estáticamente la memoria y su propia copia privada del SO: cada CPU es su propia computadora. Este modelo no es muy utilizado.
2. **Maestro-Esclavo**: cuando una CPU está inactiva, le pide al SO un proceso para ejecutar. El CPU maestro aloja al SO, y por esto puede convertirse en un cuello de botella.
3. **Multiprocesadores Simétricos**: hay una copia del SO en memoria y cualquier CPU puede ejecutarlo, eliminando la asimetría. Esto requiere sincronización.

### Planificación

- **Planificador de Tiempo Compartido**: los [[Hilos]] se ejecutan en orden de prioridad. Esto es útil para hilos que no están relacionados entre sí.
- **Planificador de Espacio Compartido**: cuando los hilos están entrerrelacionados de alguna manera, conviene asignarle $n$ CPUs a un conjunto de $n$ hilos relacionados.
